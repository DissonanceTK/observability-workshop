---
title: Authentication Request
linkTitle: 1.3 Authentication Request
weight: 3
---

## Add Authentication Request

Click on {{< button >}}+ Add requests{{< /button >}} and enter the request step name e.g. **Authenticate with Spotify API**.

![placeholder](../../img/add-request.png)

Expand the Request section, from the drop down change the request method to **POST** and enter the following URL:

``` text
https://accounts.spotify.com/api/token
```

Next add two request headers with the following key/value pairings:

- **CONTENT-TYPE: application/x-www-form-urlencoded**
- **AUTHORIZATION: Basic {{env.encoded_auth}}**

Expand the **Validation** section and add the following extraction:

- **Extract** from **Response body** **JSON** **$.access_token** **as** **access_token**. 

This will parse the JSON payload that is received from the Spotify API and extract the access token and store it as a custom variable.

![Add payload token](../../img/add-payload-token.png)
