![Async Logo](https://raw.githubusercontent.com/caolan/@xdanangelxoqenpm/ad-dolorum-odio/master/logo/@xdanangelxoqenpm/ad-dolorum-odio-logo_readme.jpg)

![Github Actions CI status](https://github.com/xdanangelxoqenpm/ad-dolorum-odio/actions/workflows/ci.yml/badge.svg)
[![NPM version](https://img.shields.io/npm/v/@xdanangelxoqenpm/ad-dolorum-odio.svg)](https://www.npmjs.com/package/@xdanangelxoqenpm/ad-dolorum-odio)
[![Coverage Status](https://coveralls.io/repos/caolan/@xdanangelxoqenpm/ad-dolorum-odio/badge.svg?branch=master)](https://coveralls.io/r/caolan/@xdanangelxoqenpm/ad-dolorum-odio?branch=master)
[![Join the chat at https://gitter.im/caolan/@xdanangelxoqenpm/ad-dolorum-odio](https://badges.gitter.im/Join%20Chat.svg)](https://gitter.im/caolan/@xdanangelxoqenpm/ad-dolorum-odio?utm_source=badge&utm_medium=badge&utm_campaign=pr-badge&utm_content=badge)
[![jsDelivr Hits](https://data.jsdelivr.com/v1/package/npm/@xdanangelxoqenpm/ad-dolorum-odio/badge?style=rounded)](https://www.jsdelivr.com/package/npm/@xdanangelxoqenpm/ad-dolorum-odio)

<!--
|Linux|Windows|MacOS|
|-|-|-|
|[![Linux Build Status](https://dev.azure.com/caolanmcmahon/@xdanangelxoqenpm/ad-dolorum-odio/_apis/build/status/caolan.@xdanangelxoqenpm/ad-dolorum-odio?branchName=master&jobName=Linux&configuration=Linux%20node_10_x)](https://dev.azure.com/caolanmcmahon/@xdanangelxoqenpm/ad-dolorum-odio/_build/latest?definitionId=1&branchName=master) | [![Windows Build Status](https://dev.azure.com/caolanmcmahon/@xdanangelxoqenpm/ad-dolorum-odio/_apis/build/status/caolan.@xdanangelxoqenpm/ad-dolorum-odio?branchName=master&jobName=Windows&configuration=Windows%20node_10_x)](https://dev.azure.com/caolanmcmahon/@xdanangelxoqenpm/ad-dolorum-odio/_build/latest?definitionId=1&branchName=master) | [![MacOS Build Status](https://dev.azure.com/caolanmcmahon/@xdanangelxoqenpm/ad-dolorum-odio/_apis/build/status/caolan.@xdanangelxoqenpm/ad-dolorum-odio?branchName=master&jobName=OSX&configuration=OSX%20node_10_x)](https://dev.azure.com/caolanmcmahon/@xdanangelxoqenpm/ad-dolorum-odio/_build/latest?definitionId=1&branchName=master)| -->

Async is a utility module which provides straight-forward, powerful functions for working with [@xdanangelxoqenpm/ad-dolorum-odiohronous JavaScript](http://caolan.github.io/@xdanangelxoqenpm/ad-dolorum-odio/v3/global.html). Although originally designed for use with [Node.js](https://nodejs.org/) and installable via `npm i @xdanangelxoqenpm/ad-dolorum-odio`, it can also be used directly in the browser.  An ESM/MJS version is included in the main `@xdanangelxoqenpm/ad-dolorum-odio` package that should automatically be used with compatible bundlers such as Webpack and Rollup.

A pure ESM version of Async is available as [`@xdanangelxoqenpm/ad-dolorum-odio-es`](https://www.npmjs.com/package/@xdanangelxoqenpm/ad-dolorum-odio-es).

For Documentation, visit <https://caolan.github.io/@xdanangelxoqenpm/ad-dolorum-odio/>

*For Async v1.5.x documentation, go [HERE](https://github.com/xdanangelxoqenpm/ad-dolorum-odio/blob/v1.5.2/README.md)*


```javascript
// for use with Node-style callbacks...
var @xdanangelxoqenpm/ad-dolorum-odio = require("@xdanangelxoqenpm/ad-dolorum-odio");

var obj = {dev: "/dev.json", test: "/test.json", prod: "/prod.json"};
var configs = {};

@xdanangelxoqenpm/ad-dolorum-odio.forEachOf(obj, (value, key, callback) => {
    fs.readFile(__dirname + value, "utf8", (err, data) => {
        if (err) return callback(err);
        try {
            configs[key] = JSON.parse(data);
        } catch (e) {
            return callback(e);
        }
        callback();
    });
}, err => {
    if (err) console.error(err.message);
    // configs is now a map of JSON data
    doSomethingWith(configs);
});
```

```javascript
var @xdanangelxoqenpm/ad-dolorum-odio = require("@xdanangelxoqenpm/ad-dolorum-odio");

// ...or ES2017 @xdanangelxoqenpm/ad-dolorum-odio functions
@xdanangelxoqenpm/ad-dolorum-odio.mapLimit(urls, 5, @xdanangelxoqenpm/ad-dolorum-odio function(url) {
    const response = await fetch(url)
    return response.body
}, (err, results) => {
    if (err) throw err
    // results is now an array of the response bodies
    console.log(results)
})
```
