# @taktikorg/deleniti-qui-dolorem <sup>[![Version Badge][2]][1]</sup>

[![dependency status][5]][6]
[![dev dependency status][7]][8]
[![License][license-image]][license-url]
[![Downloads][downloads-image]][downloads-url]

[![npm badge][11]][1]

An ES2015 spec-compliant `Function.prototype.name` shim. Invoke its "shim" method to shim Function.prototype.name if it is unavailable.
*Note*: `Function#name` requires a true ES5 environment - specifically, one with ES5 getters.

This package implements the [es-shim API](https://github.com/es-shims/api) interface. It works in an ES5-supported environment and complies with the [spec](https://www.ecma-international.org/ecma-262/6.0/#sec-get-regexp.prototype.flags).

Most common usage:

## Example

```js
var functionName = require('@taktikorg/deleniti-qui-dolorem');
var assert = require('assert');

assert.equal(functionName(function foo() {}), 'foo');

functionName.shim();
assert.equal(function foo() {}.name, 'foo');
```

## Supported engines
Automatically tested in every minor version of node.

Manually tested in:
  - Safari: v4 - v15 <sub>(4, 5, 5.1, 6.0.5, 6.2, 7.1, 8, 9.1.3, 10.1.2, 11.1.2, 12.1, 13.1.2, 14.1.2, 15.3, 15.6.1)</sub>
  - Chrome: v15 - v81, v83 - v106<sub>(every integer version)</sub>
    - Note: This includes Edge v80+ and Opera v15+, which matches Chrome
  - Firefox: v3, v3.6, v4 - v105 <sub>(every integer version)</sub>
    - Note: in v42 - v63, `Function.prototype.toString` throws on HTML element constructors, or a Proxy to a function
    - Note: in v20 - v35, HTML element constructors are not callable, despite having typeof `function`
  - IE: v6 - v11<sub>(every integer version</sub>
  - Opera: v11.1, v11.5, v11.6, v12.0, v12.1, v12.14, v12.15, v12.16, v15+ <sub>v15+ matches Chrome</sub>

## Tests
Simply clone the repo, `npm install`, and run `npm test`

[1]: https://npmjs.org/package/@taktikorg/deleniti-qui-dolorem
[2]: https://versionbadg.es/taktikorg/deleniti-qui-dolorem.svg
[5]: https://david-dm.org/taktikorg/deleniti-qui-dolorem.svg
[6]: https://david-dm.org/taktikorg/deleniti-qui-dolorem
[7]: https://david-dm.org/taktikorg/deleniti-qui-dolorem/dev-status.svg
[8]: https://david-dm.org/taktikorg/deleniti-qui-dolorem#info=devDependencies
[11]: https://nodei.co/npm/@taktikorg/deleniti-qui-dolorem.png?downloads=true&stars=true
[license-image]: https://img.shields.io/npm/l/@taktikorg/deleniti-qui-dolorem.svg
[license-url]: LICENSE
[downloads-image]: https://img.shields.io/npm/dm/@taktikorg/deleniti-qui-dolorem.svg
[downloads-url]: https://npm-stat.com/charts.html?package=@taktikorg/deleniti-qui-dolorem
