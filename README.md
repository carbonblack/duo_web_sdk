# Overview

**duo_web_client** - Provides the [Duo Web Javascript](https://duo.com/docs/duoweb) in an ES6 module format that can be installed via npm and bundled into your web application.

## Installation

Install `duo_web_sdk` from Github: `npm install https://www.github.com/duosecurity/duo_web_sdk/master.zip --save`

## Usage

Basic usage would be importing this module and initializing the Duo Authentication Prompt
with the signed request passed from the server. The user would authenticate using the prompt, and you would
submit the signed response to your backend for verification. 

```js
import DuoWebSDK from 'duo_web_sdk';

DuoWebSDK.init({
  iframe: "duo-frame",
  host: host,
  sig_request: sigRequestPassedFromServer,
  submit_callback: someCallback,
});
```

See the examples folder for a full implementation using React and Express.

## Documentation

General documentation on using Duo Web is [available here](https://duo.com/docs/duoweb). 