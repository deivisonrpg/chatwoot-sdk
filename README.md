# Chatwoot API SDK
![npm (scoped)](https://img.shields.io/npm/v/@figuro/chatwoot-sdk)![NPM](https://img.shields.io/npm/l/@figuro/chatwoot-sdk)
A client to connect with Chatwoot from Javascript with Typescript support.

## Installation

Using *npm*:

```shell
npm i @figuro/chatwoot-sdk --save
```

Using *yarn*:

```shell
yarn add @figuro/chatwoot-sdk
```

## Example

```typescript
import ChatWootClient from "@figuro/chatwoot-sdk";

const client = new ChatWootClient({
    config: {
        basePath: "https://app.chatwoot.com",
        with_credentials: true,
        credentials: "include",
        token: "<YOUR_API_TOKEN_HERE>"
    }
});

client.messages.createMessage({
    accountId: 1,
    conversationId: 8,
    data: {
        content: "Hello, World!"
    }
});
```