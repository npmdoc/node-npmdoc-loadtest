# api documentation for  [loadtest (v2.3.0)](https://github.com/alexfernandez/loadtest)  [![npm package](https://img.shields.io/npm/v/npmdoc-loadtest.svg?style=flat-square)](https://www.npmjs.org/package/npmdoc-loadtest) [![travis-ci.org build-status](https://api.travis-ci.org/npmdoc/node-npmdoc-loadtest.svg)](https://travis-ci.org/npmdoc/node-npmdoc-loadtest)
#### Run load tests for your web application. Mostly ab-compatible interface, with an option to force requests per second. Includes an API for automated load testing.

[![NPM](https://nodei.co/npm/loadtest.png?downloads=true)](https://www.npmjs.com/package/loadtest)

[![apidoc](https://npmdoc.github.io/node-npmdoc-loadtest/build/screen-capture.buildNpmdoc.browser._2Fhome_2Ftravis_2Fbuild_2Fnpmdoc_2Fnode-npmdoc-loadtest_2Ftmp_2Fbuild_2Fapidoc.html.png)](https://npmdoc.github.io/node-npmdoc-loadtest/build..beta..travis-ci.org/apidoc.html)

![package-listing](https://npmdoc.github.io/node-npmdoc-loadtest/build/screen-capture.npmPackageListing.svg)



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
            "name": "Alex Fernández",
            "email": "alexfernandeznpm@gmail.com"
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
            "name": "alexfernandez",
            "email": "alexfernandeznpm@gmail.com"
        }
    ],
    "name": "loadtest",
    "optionalDependencies": {},
    "preferGlobal": true,
    "private": false,
    "readme": "ERROR: No README data found!",
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
1.  object <span class="apidocSignatureSpan"></span>loadtest
1.  object <span class="apidocSignatureSpan">loadtest.</span>baseClient
1.  object <span class="apidocSignatureSpan">loadtest.</span>headers
1.  object <span class="apidocSignatureSpan">loadtest.</span>httpClient
1.  object <span class="apidocSignatureSpan">loadtest.</span>integration
1.  object <span class="apidocSignatureSpan">loadtest.</span>request_generator
1.  object <span class="apidocSignatureSpan">loadtest.</span>testserver
1.  object <span class="apidocSignatureSpan">loadtest.</span>timing
1.  object <span class="apidocSignatureSpan">loadtest.</span>websocket

#### [module loadtest.baseClient](#apidoc.module.loadtest.baseClient)
1.  [function <span class="apidocSignatureSpan">loadtest.baseClient.</span>BaseClient (operation, params)](#apidoc.element.loadtest.baseClient.BaseClient)

#### [module loadtest.headers](#apidoc.module.loadtest.headers)
1.  [function <span class="apidocSignatureSpan">loadtest.headers.</span>addHeaders (rawHeaders, headers)](#apidoc.element.loadtest.headers.addHeaders)
1.  [function <span class="apidocSignatureSpan">loadtest.headers.</span>addUserAgent (headers)](#apidoc.element.loadtest.headers.addUserAgent)
1.  [function <span class="apidocSignatureSpan">loadtest.headers.</span>test (callback)](#apidoc.element.loadtest.headers.test)

#### [module loadtest.httpClient](#apidoc.module.loadtest.httpClient)
1.  [function <span class="apidocSignatureSpan">loadtest.httpClient.</span>create (operation, params)](#apidoc.element.loadtest.httpClient.create)
1.  [function <span class="apidocSignatureSpan">loadtest.httpClient.</span>test (callback)](#apidoc.element.loadtest.httpClient.test)

#### [module loadtest.integration](#apidoc.module.loadtest.integration)
1.  [function <span class="apidocSignatureSpan">loadtest.integration.</span>test (callback)](#apidoc.element.loadtest.integration.test)

#### [module loadtest.loadtest](#apidoc.module.loadtest.loadtest)
1.  [function <span class="apidocSignatureSpan">loadtest.loadtest.</span>loadTest (options, callback)](#apidoc.element.loadtest.loadtest.loadTest)
1.  [function <span class="apidocSignatureSpan">loadtest.loadtest.</span>test (callback)](#apidoc.element.loadtest.loadtest.test)

#### [module loadtest.request_generator](#apidoc.module.loadtest.request_generator)
1.  [function <span class="apidocSignatureSpan">loadtest.request_generator.</span>test (callback)](#apidoc.element.loadtest.request_generator.test)

#### [module loadtest.testserver](#apidoc.module.loadtest.testserver)
1.  [function <span class="apidocSignatureSpan">loadtest.testserver.</span>startServer (options, callback)](#apidoc.element.loadtest.testserver.startServer)
1.  [function <span class="apidocSignatureSpan">loadtest.testserver.</span>test (callback)](#apidoc.element.loadtest.testserver.test)

#### [module loadtest.timing](#apidoc.module.loadtest.timing)
1.  [function <span class="apidocSignatureSpan">loadtest.timing.</span>HighResolutionTimer (delayMs, callback)](#apidoc.element.loadtest.timing.HighResolutionTimer)
1.  [function <span class="apidocSignatureSpan">loadtest.timing.</span>Latency (options, callback)](#apidoc.element.loadtest.timing.Latency)
1.  [function <span class="apidocSignatureSpan">loadtest.timing.</span>test (callback)](#apidoc.element.loadtest.timing.test)

#### [module loadtest.websocket](#apidoc.module.loadtest.websocket)
1.  [function <span class="apidocSignatureSpan">loadtest.websocket.</span>create (operation, params)](#apidoc.element.loadtest.websocket.create)
1.  [function <span class="apidocSignatureSpan">loadtest.websocket.</span>test (callback)](#apidoc.element.loadtest.websocket.test)



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



# <a name="apidoc.module.loadtest.baseClient"></a>[module loadtest.baseClient](#apidoc.module.loadtest.baseClient)

#### <a name="apidoc.element.loadtest.baseClient.BaseClient"></a>[function <span class="apidocSignatureSpan">loadtest.baseClient.</span>BaseClient (operation, params)](#apidoc.element.loadtest.baseClient.BaseClient)
- description and source-code
```javascript
BaseClient = function (operation, params)
{
	this.operation = operation;
	this.params = params;
	this.generateMessage = undefined;
}
```
- example usage
```shell
n/a
```



# <a name="apidoc.module.loadtest.headers"></a>[module loadtest.headers](#apidoc.module.loadtest.headers)

#### <a name="apidoc.element.loadtest.headers.addHeaders"></a>[function <span class="apidocSignatureSpan">loadtest.headers.</span>addHeaders (rawHeaders, headers)](#apidoc.element.loadtest.headers.addHeaders)
- description and source-code
```javascript
addHeaders = function (rawHeaders, headers)
{
	if (Array.isArray(rawHeaders))
	{
		rawHeaders.forEach(function(header)
		{
			addHeader(header, headers);
		});
	}
	else if (typeof rawHeaders == 'string')
	{
		addHeader(rawHeaders, headers);
	}
	else
	{
		console.error('Invalid header structure %j, it should be an array');
	}
}
```
- example usage
```shell
...
			raw: 'k:v:w',
			headers: { 'k': 'v:w' }
		}
	];
	tests.forEach(function(test)
	{
		var headers = {};
		exports.addHeaders(test.raw, headers);
		testing.assertEquals(headers, test.headers, 'Wrong headers', callback);
	});
	testing.success(callback);
}

/**
* Add a user-agent header if not present.
...
```

#### <a name="apidoc.element.loadtest.headers.addUserAgent"></a>[function <span class="apidocSignatureSpan">loadtest.headers.</span>addUserAgent (headers)](#apidoc.element.loadtest.headers.addUserAgent)
- description and source-code
```javascript
addUserAgent = function (headers)
{
	if(!headers['user-agent'])
	{
	  headers['user-agent'] = 'node.js loadtest bot';
	}
}
```
- example usage
```shell
...
		}
		else
		{
			log.error('Unrecognized body: %s', typeof this.params.body);
		}
		this.options.headers['Content-Type'] = this.params.contentType || 'text/plain';
	}
	headers.addUserAgent(this.options.headers);
	if (this.params.secureProtocol) {
		this.options.secureProtocol = this.params.secureProtocol;
	}
	log.debug('Options: %j',this.options);
};
...
```

#### <a name="apidoc.element.loadtest.headers.test"></a>[function <span class="apidocSignatureSpan">loadtest.headers.</span>test (callback)](#apidoc.element.loadtest.headers.test)
- description and source-code
```javascript
test = function (callback)
{
	testing.run([
		testAddHeaders,
		testAddUserAgent,
	], callback);
}
```
- example usage
```shell
...
	});
	testing.run(tests, 4200, callback);
};

// run tests if invoked directly
if (__filename == process.argv[1])
{
	exports.test(testing.show);
}
...
```



# <a name="apidoc.module.loadtest.httpClient"></a>[module loadtest.httpClient](#apidoc.module.loadtest.httpClient)

#### <a name="apidoc.element.loadtest.httpClient.create"></a>[function <span class="apidocSignatureSpan">loadtest.httpClient.</span>create (operation, params)](#apidoc.element.loadtest.httpClient.create)
- description and source-code
```javascript
create = function (operation, params)
{
	return new HttpClient(operation, params);
}
```
- example usage
```shell
...
{
	var options = {
		url: 'http://localhost:7357/',
		maxSeconds: 0.1,
		concurrency: 1,
		quiet: true,
	};
	exports.create({}, options);
	testing.success(callback);
}


/**
* Run all tests.
*/
...
```

#### <a name="apidoc.element.loadtest.httpClient.test"></a>[function <span class="apidocSignatureSpan">loadtest.httpClient.</span>test (callback)](#apidoc.element.loadtest.httpClient.test)
- description and source-code
```javascript
test = function (callback)
{
	testing.run([
		testHttpClient,
	], callback);
}
```
- example usage
```shell
...
	});
	testing.run(tests, 4200, callback);
};

// run tests if invoked directly
if (__filename == process.argv[1])
{
	exports.test(testing.show);
}
...
```



# <a name="apidoc.module.loadtest.integration"></a>[module loadtest.integration](#apidoc.module.loadtest.integration)

#### <a name="apidoc.element.loadtest.integration.test"></a>[function <span class="apidocSignatureSpan">loadtest.integration.</span>test (callback)](#apidoc.element.loadtest.integration.test)
- description and source-code
```javascript
test = function (callback)
{
	log.debug('Running all tests');
	testing.run([testIntegration, testDelay, testWSIntegration], 4000, callback);
}
```
- example usage
```shell
...
	});
	testing.run(tests, 4200, callback);
};

// run tests if invoked directly
if (__filename == process.argv[1])
{
	exports.test(testing.show);
}
...
```



# <a name="apidoc.module.loadtest.loadtest"></a>[module loadtest.loadtest](#apidoc.module.loadtest.loadtest)

#### <a name="apidoc.element.loadtest.loadtest.loadTest"></a>[function <span class="apidocSignatureSpan">loadtest.loadtest.</span>loadTest (options, callback)](#apidoc.element.loadtest.loadtest.loadTest)
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

#### <a name="apidoc.element.loadtest.loadtest.test"></a>[function <span class="apidocSignatureSpan">loadtest.loadtest.</span>test (callback)](#apidoc.element.loadtest.loadtest.test)
- description and source-code
```javascript
test = function (callback)
{
	testing.run([testMaxSeconds, testWSEcho], callback);
}
```
- example usage
```shell
...
	});
	testing.run(tests, 4200, callback);
};

// run tests if invoked directly
if (__filename == process.argv[1])
{
	exports.test(testing.show);
}
...
```



# <a name="apidoc.module.loadtest.request_generator"></a>[module loadtest.request_generator](#apidoc.module.loadtest.request_generator)

#### <a name="apidoc.element.loadtest.request_generator.test"></a>[function <span class="apidocSignatureSpan">loadtest.request_generator.</span>test (callback)](#apidoc.element.loadtest.request_generator.test)
- description and source-code
```javascript
test = function (callback)
{
	log.debug('Running all tests');
	testing.run([testRequestGenerator], 4000, callback);
}
```
- example usage
```shell
...
	});
	testing.run(tests, 4200, callback);
};

// run tests if invoked directly
if (__filename == process.argv[1])
{
	exports.test(testing.show);
}
...
```



# <a name="apidoc.module.loadtest.testserver"></a>[module loadtest.testserver](#apidoc.module.loadtest.testserver)

#### <a name="apidoc.element.loadtest.testserver.startServer"></a>[function <span class="apidocSignatureSpan">loadtest.testserver.</span>startServer (options, callback)](#apidoc.element.loadtest.testserver.startServer)
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

#### <a name="apidoc.element.loadtest.testserver.test"></a>[function <span class="apidocSignatureSpan">loadtest.testserver.</span>test (callback)](#apidoc.element.loadtest.testserver.test)
- description and source-code
```javascript
test = function (callback)
{
	testing.run([testStartServer], 5000, callback);
}
```
- example usage
```shell
...
	});
	testing.run(tests, 4200, callback);
};

// run tests if invoked directly
if (__filename == process.argv[1])
{
	exports.test(testing.show);
}
...
```



# <a name="apidoc.module.loadtest.timing"></a>[module loadtest.timing](#apidoc.module.loadtest.timing)

#### <a name="apidoc.element.loadtest.timing.HighResolutionTimer"></a>[function <span class="apidocSignatureSpan">loadtest.timing.</span>HighResolutionTimer (delayMs, callback)](#apidoc.element.loadtest.timing.HighResolutionTimer)
- description and source-code
```javascript
HighResolutionTimer = function (delayMs, callback)
{
	// self-reference
	var self = this;

	// attributes
	var counter = 0;
	var start = Date.now();
	var active = true;
	var timer;

	<span class="apidocCodeCommentSpan">/**
	 * Delayed running of the callback.
	 */
</span>	function delayed()
	{
		if (!active)
		{
			return false;
		}
		callback();
		counter ++;
		var diff = (Date.now() - start) - counter * delayMs;
		var timeout = Math.floor(delayMs - diff);
		if (timeout <= 0)
		{
			return delayed();
		}
		timer = setTimeout(delayed, delayMs - diff);
	}

	/**
	 * Show the drift of the timer.
	 */
	self.traceDrift = function()
	{
		var diff = Date.now() - start;
		var drift = diff / delayMs - counter;
		log.debug('Seconds: ' + Math.round(diff / 1000) + ', counter: ' + counter + ', drift: ' + drift);
	};

	/**
	 * Stop the timer.
	 */
	self.stop = function()
	{
		active = false;
		if (timer)
		{
			clearTimeout(timer);
			timer = null;
		}
	};

	// start timer
	delayed();
	timer = setTimeout(delayed, delayMs);
}
```
- example usage
```shell
...
	self.start = function()
	{
		if (!params.requestsPerSecond)
		{
			return self.makeRequest();
		}
		var interval = 1000 / params.requestsPerSecond;
		requestTimer = new timing.HighResolutionTimer(interval, self.makeRequest);
	};

	/**
	 * Stop the HTTP client.
	 */
	self.stop = function()
	{
...
```

#### <a name="apidoc.element.loadtest.timing.Latency"></a>[function <span class="apidocSignatureSpan">loadtest.timing.</span>Latency (options, callback)](#apidoc.element.loadtest.timing.Latency)
- description and source-code
```javascript
Latency = function (options, callback)
{
	// self-reference
	var self = this;

	// attributes
	var requests = {};
	var partialRequests = 0;
	var partialTime = 0;
	var partialErrors = 0;
	var lastShown = getTime();
	var initialTime = getTime();
	var totalRequests = 0;
	var totalTime = 0;
	var totalErrors = 0;
	var maxLatencyMs = 0;
	var minLatencyMs = 999999;
	var histogramMs = {};
	var errorCodes = {};
	var running = true;
	var totalsShown = false;

	var requestIndex = 0;
	var requestIdToIndex = {};

	// init
	if (options.quiet)
	{
		log.level = Log.NOTICE;
	}
	if (options.debug)
	{
		log.level = Log.DEBUG;
	}

	<span class="apidocCodeCommentSpan">/**
	 * Return the index of the request. This is useful for determining the order
	 * in which requests returned values.
	 */
</span>	self.getRequestIndex = function(requestId)
	{
		return requestIdToIndex[requestId];
	};

	/**
	 * Start the request with the given id.
	 */
	self.start = function(requestId)
	{
		requestId = requestId || createId();
		requests[requestId] = getTime();
		requestIdToIndex[requestId] = requestIndex++;
		return requestId;
	};

	/**
	 * Compute elapsed time and add the measurement.
	 * Accepts an optional error code signaling an error.
	 */
	self.end = function(requestId, errorCode)
	{
		if (!(requestId in requests))
		{
			log.debug('Message id ' + requestId + ' not found');
			return -2;
		}
		if (!running)
		{
			return -1;
		}
		var elapsed = getElapsed(requests[requestId]);
		add(elapsed, errorCode);
		delete requests[requestId];
		return elapsed;
	};

	/**
	 * Add a new measurement, possibly removing an old one.
	 * Accepts an optional error code signaling an error.
	 */
	function add(time, errorCode)
	{
		log.debug('New value: %s', time);
		partialTime += time;
		partialRequests++;
		totalTime += time;
		totalRequests++;
		if (errorCode)
		{
			errorCode = '' + errorCode;
			partialErrors++;
			totalErrors++;
			if (!(errorCode in errorCodes))
			{
				errorCodes[errorCode] = 0;
			}
			errorCodes[errorCode] += 1;
		}
		log.debug('Partial requests: %s', partialRequests);
		var rounded = Math.floor(time);
		if (rounded > maxLatencyMs)
		{
			maxLatencyMs = rounded;
		}
		if (rounded < minLatencyMs)
		{
			minLatencyMs = rounded;
		}
		if (!histogramMs[rounded])
		{
			log.debug('Initializing histogram for %s', rounded);
			histogramMs[rounded] = 0;
		}
		histogramMs[rounded] += 1;
		if (isFinished())
		{
			finish();
		}
	}

	/**
	 * Show latency for partial requests.
	 */
	self.showPartial = function()
	{
		var elapsedSeconds = getElapsed(lastShown) / 1000;
		var meanTime = partialTime / partialRequests || 0.0;
		var results = {
			meanLatencyMs: Math.round(meanTime * 10) / 10,
			rps: Math.round(partialRequests / elapsedSeconds)
		};
		var percent = '';
		if (options.maxRequests)
		{
			percent = ' (' + Math.round(100 * totalRequests / options.maxRequests) + '%)';
		}
		log.info('Requests: %s%s, requests per second: %s, mean latency: %s ms', totalRequests, percent, results.rps, results.meanLatencyMs
);
		if (totalErrors)
		{
			percent = Math.round(100 * 10 * totalErrors / totalRequests) / 10;
			log.info('Errors: %s, accumulated errors: %s, %s% of total requests', partialErrors, totalErrors, percent);
		}
		partialTime = 0;
		partialRequests = 0;
		partialErrors = 0;
		lastShown = getTime();
	};

	/**
	 * Returns the current high-resolution real time in a [seconds, nanoseconds] tuple Array
	 * @return {*}
	 */
	function getTime() {
		return process.hrtime();
	}

	/**
	 * calculates the elapsed time between the assigned startTime and now
	 * @param startTime
	 * @return {Number} the elapsed time in milliseconds
	 */
	function getElapsed(startTime) {
		var elapsed = process.hrtime(startTime);
		return elapsed[0] * 1000 + elapsed[1] / 1000000;
	}

	/**
	 * Check out if the measures are finished.
	 */
	function isFinished()
	{
		log.debug('Total requests %s, max requests: %s', totalRequests, options.maxRequests);
		if (options.maxRequests && totalRequests >= options.maxRequests)
		{
			log.debug('Max requests reached: %s', totalRequests);
			return true;
		}
		var elapsedSeconds = getElapsed(initial ...
```
- example usage
```shell
...
	self.instanceIndex = operationInstanceIndex++;

	/**
	 * Start the operation.
	 */
	self.start = function()
	{
		self.latency = new timing.Latency(options);
		startClients();
		if (options.maxSeconds)
		{
			stopTimeout = setTimeout(self.stop, options.maxSeconds * 1000);
		}
		showTimer = new timing.HighResolutionTimer(SHOW_INTERVAL_MS, self.latency.showPartial);
	};
...
```

#### <a name="apidoc.element.loadtest.timing.test"></a>[function <span class="apidocSignatureSpan">loadtest.timing.</span>test (callback)](#apidoc.element.loadtest.timing.test)
- description and source-code
```javascript
test = function (callback)
{
	var tests = [
		testLatencyIds,
		testLatencyRequests,
		testLatencyPercentiles,
		testTimer
	];
	testing.run(tests, callback);
}
```
- example usage
```shell
...
	});
	testing.run(tests, 4200, callback);
};

// run tests if invoked directly
if (__filename == process.argv[1])
{
	exports.test(testing.show);
}
...
```



# <a name="apidoc.module.loadtest.websocket"></a>[module loadtest.websocket](#apidoc.module.loadtest.websocket)

#### <a name="apidoc.element.loadtest.websocket.create"></a>[function <span class="apidocSignatureSpan">loadtest.websocket.</span>create (operation, params)](#apidoc.element.loadtest.websocket.create)
- description and source-code
```javascript
create = function (operation, params)
{
	return new WebsocketClient(operation, params);
}
```
- example usage
```shell
...
{
	var options = {
		url: 'http://localhost:7357/',
		maxSeconds: 0.1,
		concurrency: 1,
		quiet: true,
	};
	exports.create({}, options);
	testing.success(callback);
}


/**
* Run all tests.
*/
...
```

#### <a name="apidoc.element.loadtest.websocket.test"></a>[function <span class="apidocSignatureSpan">loadtest.websocket.</span>test (callback)](#apidoc.element.loadtest.websocket.test)
- description and source-code
```javascript
test = function (callback)
{
	testing.run([
		testWebsocketClient,
	], callback);
}
```
- example usage
```shell
...
	});
	testing.run(tests, 4200, callback);
};

// run tests if invoked directly
if (__filename == process.argv[1])
{
	exports.test(testing.show);
}
...
```



# misc
- this document was created with [utility2](https://github.com/kaizhu256/node-utility2)
