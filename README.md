# Node.jsとLINE Bot SDKで作るLINE Bot開発チュートリアル

このリポジトリでは、ユーザーからのメッセージを受け取り、オウム返しで返信するLINE Botの実装をしています。  
![line.jpg](https://qiita-image-store.s3.ap-northeast-1.amazonaws.com/0/458297/e980e414-502a-a140-9332-89254c69e143.jpeg)

このリポジトリでは、Node.jsとLINE Bot SDKを使用してLINE Botを開発します。  
[LINE Bot SDK](https://github.com/line/line-bot-sdk-nodejs)は、LINE Messaging APIを利用してLINE Botを作成するための公式SDKであり、開発を簡略化する多くの機能を提供しています。

# メッセージの送信から受信まで
スマートフォンから送信されたメッセージが、オウム返しでLINEアプリに返信される流れは以下の通りです。  
![req-res.png](https://qiita-image-store.s3.ap-northeast-1.amazonaws.com/0/458297/85db4c38-a430-4458-3b68-7a31136fd0fc.png)

Expressフレームワークを使用してLINE BotのWebhookエンドポイントを作成します。  
Expressは、Node.js用のWebアプリケーションフレームワークであり、簡単にWebサーバーを作成し、ルーティングやミドルウェアを追加できるように設計されています。

また、ngrokを使用してローカル開発環境を公開し、外部からアクセス可能なURLを生成します。  
これはLINE BotのWebhookエンドポイントを外部に公開するために使用します。

これらのツールを組み合わせることで、LINE Botの開発を簡単に始めることができます。

詳細なセットアップ方法や実装の説明はQiitaの記事に記載しています。  
興味のある方は是非チェックしてみてください。
https://qiita.com/GorillaSwe/items/fb261d07643e678bc6ff
