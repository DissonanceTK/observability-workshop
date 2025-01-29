---
title: Test our Routing Connector
linkTitle: 8.1 Testing Routing
weight: 1
---

### Setup Test

In this section, we will test the `routing` rule configured for the `gateway`. The expected result is that the`span` from the `security.json` file will be sent to the `gateway-traces-security.out` file.

{{% notice title="Exercise" style="green" icon="running" %}}

- **Run the Gateway**:
Find your `Gateway` terminal window, and navigate to the `[WORKSHOP]/8-routing` folder and restart the gateway with the routing configurations specified in the gateway.yaml.  
It should start up normally and state : `Everything is ready. Begin running and processing data.`

- **Run the Agent**:
Find your `Agent` terminal window and navigate to the `[WORKSHOP]/8-routing` folder and restart the agent with the regular `agent.yaml`.  
It should also start up normally and state : `Everything is ready. Begin running and processing data.`

- **Create a trace for different Environments**
Find your `Test` terminal window and navigate to the `[WORKSHOP]/8-routing`.  
To test your configuration, you need to generate span data with the correct `ResourceSpan` attributes to trigger the routing rule. Copy the following JSON and save it as `security.json` in the `[WORKSHOP]\8-routing` directory.

{{% tabs %}}
{{% tab title="Compacted JSON" %}}

```json
{"resourceSpans":[{"resource":{"attributes":[{"key":"service.name","value":{"stringValue":"password_check"}},{"key":"deployment.environment","value":{"stringValue":"security_applications"}}]},"scopeSpans":[{"scope":{"name":"my.library","version":"1.0.0","attributes":[{"key":"my.scope.attribute","value":{"stringValue":"some scope attribute"}}]},"spans":[{"traceId":"5B8EFFF798038103D269B633813FC60C","spanId":"EEE19B7EC3C1B174","parentSpanId":"EEE19B7EC3C1B173","name":"I'm a server span","startTimeUnixNano":"1544712660000000000","endTimeUnixNano":"1544712661000000000","kind":2,"attributes":[{"keytest":"my.span.attr","value":{"stringValue":"some value"}}]}]}]}]}
```

{{% /tab %}}
{{% tab title="Formatted JSON" %}}

```json
{
  "resourceSpans": [
    {
      "resource": {
        "attributes": [
          {
            "key": "service.name",
            "value": {
              "stringValue": "password_check"
            }
          },
          {
            "key": "deployment.environment",
            "value": {
              "stringValue": "security_applications"
            }
          }
        ]
      },
      "scopeSpans": [
        {
          "scope": {
            "name": "my.library",
            "version": "1.0.0",
            "attributes": [
              {
                "key": "my.scope.attribute",
                "value": {
                  "stringValue": "some scope attribute"
                }
              }
            ]
          },
          "spans": [
            {
              "traceId": "5B8EFFF798038103D269B633813FC60C",
              "spanId": "EEE19B7EC3C1B174",
              "parentSpanId": "EEE19B7EC3C1B173",
              "name": "I'm a server span",
              "startTimeUnixNano": "1544712660000000000",
              "endTimeUnixNano": "1544712661000000000",
              "kind": 2,
              "attributes": [
                {
                  "keytest": "my.span.attr",
                  "value": {
                    "stringValue": "some value"
                  }
                }
              ]
            }
          ]
        }
      ]
    }
  ]
}
```

{{% /tab %}}
{{% /tabs %}}

{{% /notice %}}

### Testing the routing scenario

{{% notice title="Exercise" style="green" icon="running" %}}
Make sure the are **NO** `*.out` files in the `[WORKSHOP]/8-routing` folder.

- **Send a Regular Span**:  
Find your `Test` terminal window and navigate to the `[WORKSHOP]/8-routing` folder. From there, send a regular span using the `trace.json` file to confirm that communication is functioning as expected.  
Both the `agent` and `gateway` should display debug information, including the span you just sent. Additionally, the gateway should generate a new `./gateway-traces-default.out` file, as this is now the destination for regular spans.

{{% notice title="Tip" style="primary" icon="lightbulb" %}}
If you verify the `./gateway-traces-default.out` is should contain the span we send with the cURL command.
{{% /notice %}}

- **Send a Security Span**:  
Make sure both the `agent` and `gateway` are running, then send a security span using the `security.json` file to test the routing rule in the gateway.  
Both the `agent` and `gateway` should display debug information, including the span you just sent. Additionally, the gateway should generate a new `./gateway-traces-security.out` file, as this is  the destination for spans where the `deployment.environment` resourceSpan attribute matches `"security_applications"`.  

{{% notice title="Tip" style="primary" icon="lightbulb" %}}
If you verify the `./gateway-traces-security.out` is should only contain the spans from the `"security_applications"` deployment.environment.
{{% /notice %}}

{{% /notice %}}

### Conclusion

In this section, we successfully tested the routing connector in the gateway by sending different spans and verifying their destinations.

- **Regular spans** were correctly routed to `gateway-traces-default.out`, confirming that spans without a matching `deployment.environment` attribute follow the default pipeline.

- **Security-related spans** from `security.json` were routed to `gateway-traces-security.out`, demonstrating that the routing rule based on `"deployment.environment": "security_applications"` works as expected.

By inspecting the output files, we confirmed that the OpenTelemetry Collector *correctly evaluates span attributes and routes them to the appropriate destinations*. This validates that routing rules can effectively separate and direct telemetry data for different use cases.

You can now extend this approach by defining additional routing rules to further categorize spans, metrics, and logs based on different attributes.

If you want to know more about the `routing` connector , you can find it [here](https://github.com/open-telemetry/opentelemetry-collector-contrib/tree/main/connector/routingconnector)

Stop the `agent` and `gateway` using Command-c/Ctrl-c.
