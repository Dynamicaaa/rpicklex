# RPickleX

Pure JavaScript parser for Python pickle bytecode supporting protocols 0 through 5. This package is used internally by RPX to decode Ren''Py archive indexes but can be consumed independently.

## Installation

```bash
npm install @dynamicaaa/rpicklex
```

## Usage

```js
import RPickleX from '@dynamicaaa/rpicklex';

const picklex = new RPickleX();
const base64 = 'gAJ9cQAoWAUAAABoZWxsb3EBWAUAAAB3b3JsZHECWAYAAABhbnN3ZXJxA0sqWAYAAABuZXN0ZWRxBF1xBShLAUsCSwNldS4=';
const buffer = Buffer.from(base64, 'base64');
const obj = picklex.loads(buffer);

console.log(obj);
// { hello: 'world', answer: 42, nested: [ 1, 2, 3 ] }
```

See the inline documentation in [`index.js`](index.js) for the full API surface (validation, opcode statistics, debug helpers, etc.).

## License

MIT © Dynamicaaa
