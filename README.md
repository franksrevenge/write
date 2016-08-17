# write [![NPM version](https://img.shields.io/npm/v/write.svg?style=flat)](https://www.npmjs.com/package/write) [![NPM downloads](https://img.shields.io/npm/dm/write.svg?style=flat)](https://npmjs.org/package/write) [![Build Status](https://img.shields.io/travis/jonschlinkert/write.svg?style=flat)](https://travis-ci.org/jonschlinkert/write)

Write files to disk, creating intermediate directories if they don't exist.

## Install

Install with [npm](https://www.npmjs.com/):

```sh
$ npm install --save write
```

## Usage

```js
var writeFile = require('write');
```

## API

### [writeFile](index.js#L33)

Asynchronously write a file to disk, creating any intermediate directories along the way if they don't already exist.

**Params**

* `dest` **{String}**: Destination file path
* `str` **{String}**: String to write to disk.
* `callback` **{Function}**

**Example**

```js
var writeFile = require('write');
writeFile('foo.txt', 'This is content to write.', function(err) {
  if (err) console.log(err);
});
```

### [.writeFile.sync](index.js#L75)

Synchronously write files to disk, creating any intermediate directories along the way if they don't already exist.

**Params**

* `dest` **{String}**: Destination file path
* `str` **{String}**: String to write to disk.

**Example**

```js
var writeFile = require('write');
writeFile.sync('foo.txt', 'This is content to write.');
```

### [.writeFile.stream](index.js#L95)

Uses `fs.createWriteStream`, but also creates any intermediate directories along the way if they don't already exist.

**Params**

* `dest` **{String}**: Destination file path
* `returns` **{Stream}**: Returns a write stream.

**Example**

```js
var writeFile = require('write');
writeFile.stream('foo.txt');
```

## About

### Related projects

* [delete](https://www.npmjs.com/package/delete): Delete files and folders and any intermediate directories if they exist (sync and async). | [homepage](https://github.com/jonschlinkert/delete)
* [read-data](https://www.npmjs.com/package/read-data): Read JSON or YAML files. | [homepage](https://github.com/jonschlinkert/read-data)
* [read-json](https://www.npmjs.com/package/read-json): Reads and parses a JSON file. | [homepage](https://github.com/n-johnson/read-json#readme)
* [read-yaml](https://www.npmjs.com/package/read-yaml): Very thin wrapper around js-yaml for directly reading in YAML files. | [homepage](https://github.com/jonschlinkert/read-yaml)
* [write-json](https://www.npmjs.com/package/write-json): Write a JSON file to disk, also creates intermediate directories in the destination path if… [more](https://github.com/jonschlinkert/write-json) | [homepage](https://github.com/jonschlinkert/write-json)
* [write-yaml](https://www.npmjs.com/package/write-yaml): Write YAML. Converts JSON to YAML writes it to the specified file. | [homepage](https://github.com/jonschlinkert/write-yaml)

### Contributing

Pull requests and stars are always welcome. For bugs and feature requests, [please create an issue](../../issues/new).

### Building docs

_(This document was generated by [verb-generate-readme](https://github.com/verbose/verb-generate-readme) (a [verb](https://github.com/verbose/verb) generator), please don't edit the readme directly. Any changes to the readme must be made in [.verb.md](.verb.md).)_

To generate the readme and API documentation with [verb](https://github.com/verbose/verb):

```sh
$ npm install -g verb verb-generate-readme && verb
```

### Running tests

Install dev dependencies:

```sh
$ npm install -d && npm test
```

### Author

**Jon Schlinkert**

* [github/jonschlinkert](https://github.com/jonschlinkert)
* [twitter/jonschlinkert](http://twitter.com/jonschlinkert)

### License

Copyright © 2016, [Jon Schlinkert](https://github.com/jonschlinkert).
Released under the [MIT license](https://github.com/jonschlinkert/write/blob/master/LICENSE).

***

_This file was generated by [verb-generate-readme](https://github.com/verbose/verb-generate-readme), v0.1.30, on August 17, 2016._