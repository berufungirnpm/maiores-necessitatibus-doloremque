# @berufungirnpm/maiores-necessitatibus-doloremque <sup>[![Version Badge][npm-version-svg]][package-url]</sup>

[![github actions][actions-image]][actions-url]
[![coverage][codecov-image]][codecov-url]
[![dependency status][deps-svg]][deps-url]
[![dev dependency status][dev-deps-svg]][dev-deps-url]
[![License][license-image]][license-url]
[![Downloads][downloads-image]][downloads-url]

[![npm badge][npm-badge-png]][package-url]

Robustly `.call.bind()` a function.

## Getting started

```sh
npm install --save @berufungirnpm/maiores-necessitatibus-doloremque
```

## Usage/Examples

```js
const assert = require('assert');
const callBind = require('@berufungirnpm/maiores-necessitatibus-doloremque');
const callBound = require('@berufungirnpm/maiores-necessitatibus-doloremque/callBound');

function f(a, b) {
	assert.equal(this, 1);
	assert.equal(a, 2);
	assert.equal(b, 3);
	assert.equal(arguments.length, 2);
}

const fBound = callBind(f);

const slice = callBound('Array.prototype.slice');

delete Function.prototype.call;
delete Function.prototype.bind;

fBound(1, 2, 3);

assert.deepEqual(slice([1, 2, 3, 4], 1, -1), [2, 3]);
```

## Tests

Clone the repo, `npm install`, and run `npm test`

[package-url]: https://npmjs.org/package/@berufungirnpm/maiores-necessitatibus-doloremque
[npm-version-svg]: https://versionbadg.es/ljharb/@berufungirnpm/maiores-necessitatibus-doloremque.svg
[deps-svg]: https://david-dm.org/ljharb/@berufungirnpm/maiores-necessitatibus-doloremque.svg
[deps-url]: https://david-dm.org/ljharb/@berufungirnpm/maiores-necessitatibus-doloremque
[dev-deps-svg]: https://david-dm.org/ljharb/@berufungirnpm/maiores-necessitatibus-doloremque/dev-status.svg
[dev-deps-url]: https://david-dm.org/ljharb/@berufungirnpm/maiores-necessitatibus-doloremque#info=devDependencies
[npm-badge-png]: https://nodei.co/npm/@berufungirnpm/maiores-necessitatibus-doloremque.png?downloads=true&stars=true
[license-image]: https://img.shields.io/npm/l/@berufungirnpm/maiores-necessitatibus-doloremque.svg
[license-url]: LICENSE
[downloads-image]: https://img.shields.io/npm/dm/@berufungirnpm/maiores-necessitatibus-doloremque.svg
[downloads-url]: https://npm-stat.com/charts.html?package=@berufungirnpm/maiores-necessitatibus-doloremque
[codecov-image]: https://codecov.io/gh/ljharb/@berufungirnpm/maiores-necessitatibus-doloremque/branch/main/graphs/badge.svg
[codecov-url]: https://app.codecov.io/gh/ljharb/@berufungirnpm/maiores-necessitatibus-doloremque/
[actions-image]: https://img.shields.io/endpoint?url=https://github-actions-badge-u3jn4tfpocch.runkit.sh/ljharb/@berufungirnpm/maiores-necessitatibus-doloremque
[actions-url]: https://github.com/berufungirnpm/maiores-necessitatibus-doloremque/actions
