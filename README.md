# set-node-process-env

> set-node-process-env by linux bash command without need git ignore the .env file

[https://www.npmjs.com/package/set-node-process-env](https://www.npmjs.com/package/set-node-process-env)

## install

```sh
$ yarn global add set-node-process-env
# OR
$ npm i -g set-node-process-env

```

## usage


```sh
# PORT_ENV for webpack
$ snpe PORT_ENV=8090

```

> demo

```js
// webpack.config.js
const PORT_ENV = process.env.PORT_ENV || 8080;

console.log('PORT_ENV =', PORT_ENV);

// const ip = require('ip');
// const hostIp = ip.address();
const config = {
  // ...
  devServer: {
    // ...
    // host: hostIp,
    port: PORT_ENV,
    proxy: [
      {
        context: ['/web/api/'],
        // dev
        target: 'https://web-dev.xgqfrms.xyz',
        // prod
        // target: 'https://web-prod.xgqfrms.xyz',
      },
    ],
  },
};

module.exports = config;

```

## refs

https://www.npmjs.com/package/app-node-env

