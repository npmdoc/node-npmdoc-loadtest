# api documentation for  [loadtest (v2.3.0)](https://github.com/alexfernandez/loadtest)  [![npm package](https://img.shields.io/npm/v/npmdoc-loadtest.svg?style=flat-square)](https://www.npmjs.org/package/npmdoc-loadtest) [![travis-ci.org build-status](https://api.travis-ci.org/npmdoc/node-npmdoc-loadtest.svg)](https://travis-ci.org/npmdoc/node-npmdoc-loadtest)
#### Run load tests for your web application. Mostly ab-compatible interface, with an option to force requests per second. Includes an API for automated load testing.

[![NPM](https://nodei.co/npm/loadtest.png?downloads=true&downloadRank=true&stars=true)](https://www.npmjs.com/package/loadtest)

[![apidoc](https://npmdoc.github.io/node-npmdoc-loadtest/build/screenCapture.buildCi.browser.apidoc.html.png)](https://npmdoc.github.io/node-npmdoc-loadtest/build/apidoc.html)

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



# <a name="apidoc.tableOfContents"></a>[table of contents](#apidoc.tableOfContents)

#### [module loadtest](#apidoc.module.loadtest)
1.  [function <span class="apidocSignatureSpan">loadtest.</span>loadTest (options, callback)](#apidoc.element.loadtest.loadTest)
1.  [function <span class="apidocSignatureSpan">loadtest.</span>startServer (options, callback)](#apidoc.element.loadtest.startServer)



# <a name="apidoc.module.loadtest"></a>[module loadtest](#apidoc.module.loadtest)

#### <a name="apidoc.element.loadtest.loadTest"></a>[function <span class="apidocSignatureSpan">loadtest.</span>loadTest (options, callback)](#apidoc.element.loadtest.loadTest)
- description and source-code
```javascript
loadTest = function (options, callback)
{
	if (!options.url)
	{
		log.error('Missing URL in options');
		return;
	}
	options.concurrency = options.concurrency || 1;
	if (options.requestsPerSecond)
	{
		options.requestsPerSecond = options.requestsPerSecond / options.concurrency;
	}
	if (options.debug)
	{
		log.level = Log.DEBUG;
	}
	if (!options.url.startsWith('http://') && !options.url.startsWith('https://') && !options.url.startsWith('ws://'))
	{
		log.error('Invalid URL %s, must be http://, https:// or ws://', options.url);
		return;
	}
	if (callback && !('quiet' in options))
	{
		options.quiet = true;
	}

	if (options.url.startsWith('ws:'))
	{
		if (options.requestsPerSecond)
		{
			log.error('"requestsPerSecond" not supported for WebSockets');
		}
	}

	var operation = new Operation(options, callback);
	operation.start();
	return operation;
}
```
- example usage
```shell
...
To run a load test, just call the exported function 'loadTest()' with a set of options and an optional callback:

var loadtest = require('loadtest');
var options = {
    url: 'http://localhost:8000',
    maxRequests: 1000,
};
loadtest.loadTest(options, function(error, result)
{
    if (error)
    {
        return console.error('Got an error: %s', error);
    }
    console.log('Tests run successfully');
});
...
```

#### <a name="apidoc.element.loadtest.startServer"></a>[function <span class="apidocSignatureSpan">loadtest.</span>startServer (options, callback)](#apidoc.element.loadtest.startServer)
- description and source-code
```javascript
startServer = function (options, callback)
{
	if (callback)
	{
		options.quiet = true;
	}
	var server = new TestServer(options);
	return server.start(callback);
}
```
- example usage
```shell
...
    }

### Start Test Server

To start the test server use the exported function 'startServer()' with a set of options and an optional callback:

    var testserver = require('testserver');
    var server = testserver.startServer({ port: 8000 });

This function returns an HTTP server which can be 'close()'d when it is no longer useful.

The following options are available.

#### 'port'
...
```



# misc
- this document was created with [utility2](https://github.com/kaizhu256/node-utility2)
