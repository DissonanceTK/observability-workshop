---
title: AWS Lambda関数の分散トレーシング
linkTitle: Lambdaトレーシング
description: このワークショップでは、AWS Lambdaで実行される小規模なサーバーレスアプリケーションの分散トレースを構築し、AWS Kinesisを介してメッセージを生成および消費する方法を学びます
weight: 6
authors: ["Guy-Francis Kono"]
time: 45 minutes
---

このワークショップでは、AWS Lambdaで実行される小規模なサーバーレスアプリケーションの分散トレースを構築し、AWS Kinesisを介してメッセージを生成および消費する方法を学びます。

まず、OpenTelemetryの自動計装がどのようにトレースをキャプチャし、選択した宛先にエクスポートするかを確認します。

次に、手動計装によってコンテキスト伝播を有効にする方法を見ていきます。

このワークショップのために、SplunkはAWS/EC2上のUbuntu Linuxインスタンスを事前に構成しています。このインスタンスにアクセスするには、ワークショップリーダーが提供するURLにアクセスしてください。
