# npmdoc-loadtest

#### basic api documentation for  [loadtest (v2.3.0)](https://github.com/alexfernandez/loadtest)  [![npm package](https://img.shields.io/npm/v/npmdoc-loadtest.svg?style=flat-square)](https://www.npmjs.org/package/npmdoc-loadtest) [![travis-ci.org build-status](https://api.travis-ci.org/npmdoc/node-npmdoc-loadtest.svg)](https://travis-ci.org/npmdoc/node-npmdoc-loadtest)

#### Run load tests for your web application. Mostly ab-compatible interface, with an option to force requests per second. Includes an API for automated load testing.

[![NPM](https://nodei.co/npm/loadtest.png?downloads=true&downloadRank=true&stars=true)](https://www.npmjs.com/package/loadtest)

- [https://npmdoc.github.io/node-npmdoc-loadtest/build/apidoc.html](https://npmdoc.github.io/node-npmdoc-loadtest/build/apidoc.html)

[![apidoc](https://npmdoc.github.io/node-npmdoc-loadtest/build/screenCapture.buildCi.browser.%252Ftmp%252Fbuild%252Fapidoc.html.png)](https://npmdoc.github.io/node-npmdoc-loadtest/build/apidoc.html)

![npmPackageListing](https://npmdoc.github.io/node-npmdoc-loadtest/build/screenCapture.npmPackageListing.svg)

![npmPackageDependencyTree](https://npmdoc.github.io/node-npmdoc-loadtest/build/screenCapture.npmPackageDependencyTree.svg)



# package.json

```json

{
    "bin": {
        "loadtest": "bin/loadtest.js",
        "testserver-loadtest": "bin/testserver.js"
    },
    "bugs": {
        "url": "https://github.com/alexfernandez/loadtest/issues"
    },
    "contributors": [
        {
            "name": "Alex Fernández"
        }
    ],
    "dependencies": {
        "agentkeepalive": "^2.0.3",
        "log": "1.4.*",
        "prototypes": ">= 0.4.3",
        "stdio": "^0.2.3",
        "testing": "^0.2.3",
        "websocket": "^1.0.22"
    },
    "description": "Run load tests for your web application. Mostly ab-compatible interface, with an option to force requests per second. Includes an API for automated load testing.",
    "devDependencies": {},
    "directories": {},
    "dist": {
        "shasum": "bd0bb31358c045ac4ba8c2187557d3cd9f7f9d76",
        "tarball": "https://registry.npmjs.org/loadtest/-/loadtest-2.3.0.tgz"
    },
    "engines": {
        "node": ">=0.10.3"
    },
    "gitHead": "74d28631a8c9a9c640371c4a7431380c77eb9b35",
    "homepage": "https://github.com/alexfernandez/loadtest",
    "keywords": [
        "testing",
        "test",
        "load test",
        "load testing",
        "http",
        "performance",
        "black box"
    ],
    "license": "MIT",
    "main": "index.js",
    "maintainers": [
        {
            "name": "alexfernandez"
        }
    ],
    "name": "loadtest",
    "optionalDependencies": {},
    "preferGlobal": true,
    "private": false,
    "repository": {
        "type": "git",
        "url": "git+https://github.com/alexfernandez/loadtest.git"
    },
    "scripts": {
        "test": "node test.js"
    },
    "types": "index.d.ts",
    "version": "2.3.0"
}
```



# misc
- this document was created with [utility2](https://github.com/kaizhu256/node-utility2)
