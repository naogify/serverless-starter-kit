<!--
title: 'AWS Serverless REST API example in NodeJS'
description: 'This example demonstrates how to setup a RESTful Web Service allowing you to create, list, get, update and delete Todos. DynamoDB is used to store the data.'
layout: Doc
framework: v1
platform: AWS
language: nodeJS
priority: 10
authorLink: 'https://github.com/ozbillwang'
authorName: 'Bill Wang'
authorAvatar: 'https://avatars3.githubusercontent.com/u/8954908?v=4&s=140'
-->
# Serverless Starter Kit

Serverless Framework を使って、Lambda(Node.js) で DynamoDB を使用するサンプルです。

## セットアップ

```bash
npm install
```

## デプロイ

```bash
npm run deploy:dev
npm run deploy:v1
```

## 削除

```bash
npm run remove
```

## 使い方

### Todo を作成

```bash
curl -X POST https://XXXXXXX.execute-api.us-east-1.amazonaws.com/dev/todos --data '{ "text": "Learn Serverless" }'
```

### 全ての Todo を取得

```bash
curl https://XXXXXXX.execute-api.us-east-1.amazonaws.com/dev/todos
```

### Todo を指定して取得

```bash
# Replace the <id> part with a real id from your todos table
curl https://XXXXXXX.execute-api.us-east-1.amazonaws.com/dev/todos/<id>
```

### Todo を更新

```bash
# Replace the <id> part with a real id from your todos table
curl -X PUT https://XXXXXXX.execute-api.us-east-1.amazonaws.com/dev/todos/<id> --data '{ "text": "Learn Serverless", "checked": true }'
```

### Todo を削除

```bash
# Replace the <id> part with a real id from your todos table
curl -X DELETE https://XXXXXXX.execute-api.us-east-1.amazonaws.com/dev/todos/<id>
```


## 参考
https://github.com/serverless/examples/tree/master/aws-node-rest-api-with-dynamodb
