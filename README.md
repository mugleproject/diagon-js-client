<div align="center">

![GitHub tag (latest SemVer)](https://img.shields.io/github/tag/mugleproject/diagon-js-client.svg)
[![GitHub issues](https://img.shields.io/github/issues-raw/mugleproject/diagon-js-client.svg)](https://github.com/mugleproject/diagon-js-client/issues)
[![License](https://img.shields.io/github/license/mugleproject/diagon-js-client.svg)](LICENSE)
![GitHub stars](https://img.shields.io/github/stars/mugleproject/diagon-js-client?style=social)
</div>

# diagon-js-client

A javascript / typescript http and websocket client and type system for [Diagon](https://github.com/mugleproject/diagon).

## Installation

`yarn add diagon-js-client`

## Usage

### Websocket Client

[DiagonWebsocket docs](https://mugle.org/api/classes/DiagonWebsocket.html)

```ts
import { Login, DiagonWebsocket } from 'diagon-js-client';

let client: DiagonWebsocket = new DiagonWebsocket();

let form = new Login({
  username_or_email: "my_email@email.tld",
  password: "my_pass",
});

this.ws.send(client.login(form));
```

### HTTP Client

[DiagonHttp docs](https://mugle.org/api/classes/DiagonHttp.html)

```ts
import { DiagonHttp } from 'diagon-js-client';

let baseUrl = 'https://mugle.org';
let client: DiagonHttp = new DiagonHttp(baseUrl, headers?);
let jwt = await client.httpLogin(loginForm).jwt;
```
