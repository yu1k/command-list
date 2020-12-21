# Slack bot

### Web APIの種類

- Incoming Webhook

  - ユーザーがインストール時に選択した単一のチャネルに通知を送信する。

- Events API

  - メッセージ投稿やメンバー追加などのイベント情報のサブスクリプションを使用し、JSONペイロードをサーバーに送信します。

  - サーバーではペイロードの受信を行い、どのように応答するか決める。Slack アプリの設定ページでイベントを申し込む。

- RTM API

  - RTM (リアルタイムメッセージング) API は WebSocket を使用し、リアルタイムにイベントを受信したり、メッセージを送信したりできる。



### Docs

Node Slack SDK

参考リンク：

https://slack.dev/node-slack-sdk/
