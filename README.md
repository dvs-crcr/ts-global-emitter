# global-emitter
[![NPM Version][npm-image]][npm-url]
>Global singleton instance of Node.js EventEmitter. Helps modules communicate with each other.

## Install
```bash
$ npm i @crcr/global-emitter
```

## Usage
>Import `global-emitter` in every module where you want to emit event with another module.
```js
// moduleOne.js

const GlobalEmitter = require('@crcr/global-emitter');

GlobalEmitter.emit('globalEvent');
```

```js
// moduleTwo.js

const GlobalEmitter = require('@crcr/global-emitter');

GlobalEmitter.on('globalEvent', () => {
  console.log('globalEvent successfully emitted!');
})
```

## License
[MIT](LICENSE)

[npm-image]: https://img.shields.io/npm/v/@crcr/global-emitter?style=flat-square
[npm-url]: https://www.npmjs.com/package/@crcr/global-emitter