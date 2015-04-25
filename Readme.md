[![Travis – build status
](https://img.shields.io/travis/tomekwi/node-raw/master.svg?style=flat-square)
](https://travis-ci.org/tomekwi/node-raw)
 
[![David – status of dependencies
](https://img.shields.io/david/tomekwi/node-raw.svg?style=flat-square)
](https://david-dm.org/tomekwi/node-raw)
 
[![Code style: airbnb
](https://img.shields.io/badge/code%20style-airbnb-blue.svg?style=flat-square)
](https://github.com/airbnb/javascript)
 
[![Stability: experimental
](https://img.shields.io/badge/stability-experimental-red.svg?style=flat-square)
](https://nodejs.org/api/documentation.html#documentation_stability_index)




node-raw
========

**Make webpack’s *raw-loader* work in *node* and *iojs*.**

*Heads up!* This is totally a work in progress. [Thoughts and ideas][] are very welcome.

[Thoughts and ideas]:  https://github.com/tomekwi/node-raw/issues




Installation
------------

```sh
$ npm install node-raw
```




Usage
-----

1) Polyfill require.

```js
if (typeof window === 'undefined') require = require('node-raw')(require);
```

2) Profit!

```js
// Require modules as you did normally.
var Rx = require('rx');

// Require text files with *raw-loader*. That’ll now work in node as well!
var readme = require('raw!Readme.md');
```




License
-------

[MIT][] © [Tomek Wiszniewski][]

[MIT]: ./License.md
[Tomek Wiszniewski]: https://github.com/tomekwi