# api documentation for  [maxmind (v2.2.0)](https://github.com/runk/node-maxmind)  [![npm package](https://img.shields.io/npm/v/npmdoc-maxmind.svg?style=flat-square)](https://www.npmjs.org/package/npmdoc-maxmind) [![travis-ci.org build-status](https://api.travis-ci.org/npmdoc/node-npmdoc-maxmind.svg)](https://travis-ci.org/npmdoc/node-npmdoc-maxmind)
#### IP lookup using Maxmind databases

[![NPM](https://nodei.co/npm/maxmind.png?downloads=true)](https://www.npmjs.com/package/maxmind)

[![apidoc](https://npmdoc.github.io/node-npmdoc-maxmind/build/screenCapture.buildNpmdoc.browser._2Fhome_2Ftravis_2Fbuild_2Fnpmdoc_2Fnode-npmdoc-maxmind_2Ftmp_2Fbuild_2Fapidoc.html.png)](https://npmdoc.github.io/node-npmdoc-maxmind/build/apidoc.html)

![npmPackageListing](https://npmdoc.github.io/node-npmdoc-maxmind/build/screenCapture.npmPackageListing.svg)

![npmPackageDependencyTree](https://npmdoc.github.io/node-npmdoc-maxmind/build/screenCapture.npmPackageDependencyTree.svg)



# package.json

```json

{
    "author": {
        "name": "Dmitry Shirokov",
        "email": "deadrunk@gmail.com"
    },
    "bugs": {
        "url": "http://github.com/runk/node-maxmind/issues"
    },
    "contributors": [
        {
            "name": "Thomas Birke @quafzi",
            "email": "quafzi@netextreme.de"
        },
        {
            "name": "Afzaal Ameer @afzaalace"
        }
    ],
    "dependencies": {
        "big-integer": "^1.6.15",
        "lru-cache": "^4.0.1"
    },
    "description": "IP lookup using Maxmind databases",
    "devDependencies": {
        "eslint": "^2.9.0",
        "github-publish-release": "^1.2.3",
        "ip-address": "^5.8.0",
        "istanbul": "^0.4.3",
        "mocha": "^2.4.5",
        "sinon": "^1.17.6"
    },
    "directories": {},
    "dist": {
        "shasum": "c548ca13251daa183b7201d2ab8cb831d1268ea2",
        "tarball": "https://registry.npmjs.org/maxmind/-/maxmind-2.2.0.tgz"
    },
    "engines": {
        "node": ">=0.8.0",
        "npm": ">=1"
    },
    "gitHead": "8bb54dc4e56d7c609e13a3c86c8a274f3d1e4623",
    "homepage": "https://github.com/runk/node-maxmind",
    "keywords": [
        "maxmind",
        "mmdb",
        "geo",
        "geoip",
        "geoip2",
        "geobase",
        "geo lookup",
        "ip base",
        "geocode",
        "timezone",
        "asn"
    ],
    "license": "MIT",
    "main": "index.js",
    "maintainers": [
        {
            "name": "runk",
            "email": "deadrunk@gmail.com"
        }
    ],
    "name": "maxmind",
    "optionalDependencies": {},
    "readme": "ERROR: No README data found!",
    "repository": {
        "type": "git",
        "url": "git+https://github.com/runk/node-maxmind.git"
    },
    "scripts": {
        "benchmark": "node benchmark",
        "coverage": "istanbul cover _mocha -- -R spec --timeout 5000 --recursive",
        "coverage:check": "istanbul check-coverage",
        "lint": "eslint -c .eslintrc .",
        "mocha": "mocha -R spec --recursive --bail",
        "release": "scripts/release",
        "test": "npm run lint && npm run coverage && npm run coverage:check"
    },
    "version": "2.2.0"
}
```



# <a name="apidoc.tableOfContents"></a>[table of contents](#apidoc.tableOfContents)

#### [module maxmind](#apidoc.module.maxmind)
1.  [function <span class="apidocSignatureSpan">maxmind.</span>Reader (db, opts)](#apidoc.element.maxmind.Reader)
1.  [function <span class="apidocSignatureSpan">maxmind.</span>decoder (db, baseOffset)](#apidoc.element.maxmind.decoder)
1.  [function <span class="apidocSignatureSpan">maxmind.</span>init ()](#apidoc.element.maxmind.init)
1.  [function <span class="apidocSignatureSpan">maxmind.</span>metadata (db)](#apidoc.element.maxmind.metadata)
1.  [function <span class="apidocSignatureSpan">maxmind.</span>open (filepath, opts, cb)](#apidoc.element.maxmind.open)
1.  [function <span class="apidocSignatureSpan">maxmind.</span>openSync (filepath, opts)](#apidoc.element.maxmind.openSync)
1.  [function <span class="apidocSignatureSpan">maxmind.</span>validate (ip)](#apidoc.element.maxmind.validate)
1.  object <span class="apidocSignatureSpan">maxmind.</span>Reader.prototype
1.  object <span class="apidocSignatureSpan">maxmind.</span>decoder.prototype
1.  object <span class="apidocSignatureSpan">maxmind.</span>ip
1.  object <span class="apidocSignatureSpan">maxmind.</span>metadata.prototype
1.  object <span class="apidocSignatureSpan">maxmind.</span>utils

#### [module maxmind.Reader](#apidoc.module.maxmind.Reader)
1.  [function <span class="apidocSignatureSpan">maxmind.</span>Reader (db, opts)](#apidoc.element.maxmind.Reader.Reader)

#### [module maxmind.Reader.prototype](#apidoc.module.maxmind.Reader.prototype)
1.  [function <span class="apidocSignatureSpan">maxmind.Reader.prototype.</span>findAddressInTree (ipAddress)](#apidoc.element.maxmind.Reader.prototype.findAddressInTree)
1.  [function <span class="apidocSignatureSpan">maxmind.Reader.prototype.</span>get (ipAddress)](#apidoc.element.maxmind.Reader.prototype.get)
1.  [function <span class="apidocSignatureSpan">maxmind.Reader.prototype.</span>load (db)](#apidoc.element.maxmind.Reader.prototype.load)
1.  [function <span class="apidocSignatureSpan">maxmind.Reader.prototype.</span>resolveDataPointer (pointer)](#apidoc.element.maxmind.Reader.prototype.resolveDataPointer)
1.  [function <span class="apidocSignatureSpan">maxmind.Reader.prototype.</span>setupNodeReaderFn (recordSize)](#apidoc.element.maxmind.Reader.prototype.setupNodeReaderFn)

#### [module maxmind.decoder](#apidoc.module.maxmind.decoder)
1.  [function <span class="apidocSignatureSpan">maxmind.</span>decoder (db, baseOffset)](#apidoc.element.maxmind.decoder.decoder)

#### [module maxmind.decoder.prototype](#apidoc.module.maxmind.decoder.prototype)
1.  [function <span class="apidocSignatureSpan">maxmind.decoder.prototype.</span>decode (offset)](#apidoc.element.maxmind.decoder.prototype.decode)
1.  [function <span class="apidocSignatureSpan">maxmind.decoder.prototype.</span>decodeArray (size, offset)](#apidoc.element.maxmind.decoder.prototype.decodeArray)
1.  [function <span class="apidocSignatureSpan">maxmind.decoder.prototype.</span>decodeBigUint (offset, size)](#apidoc.element.maxmind.decoder.prototype.decodeBigUint)
1.  [function <span class="apidocSignatureSpan">maxmind.decoder.prototype.</span>decodeBoolean (size)](#apidoc.element.maxmind.decoder.prototype.decodeBoolean)
1.  [function <span class="apidocSignatureSpan">maxmind.decoder.prototype.</span>decodeByType (type, offset, size)](#apidoc.element.maxmind.decoder.prototype.decodeByType)
1.  [function <span class="apidocSignatureSpan">maxmind.decoder.prototype.</span>decodeBytes (offset, size)](#apidoc.element.maxmind.decoder.prototype.decodeBytes)
1.  [function <span class="apidocSignatureSpan">maxmind.decoder.prototype.</span>decodeDouble (offset)](#apidoc.element.maxmind.decoder.prototype.decodeDouble)
1.  [function <span class="apidocSignatureSpan">maxmind.decoder.prototype.</span>decodeFloat (offset)](#apidoc.element.maxmind.decoder.prototype.decodeFloat)
1.  [function <span class="apidocSignatureSpan">maxmind.decoder.prototype.</span>decodeInt32 (offset, size)](#apidoc.element.maxmind.decoder.prototype.decodeInt32)
1.  [function <span class="apidocSignatureSpan">maxmind.decoder.prototype.</span>decodeMap (size, offset)](#apidoc.element.maxmind.decoder.prototype.decodeMap)
1.  [function <span class="apidocSignatureSpan">maxmind.decoder.prototype.</span>decodePointer (ctrlByte, offset)](#apidoc.element.maxmind.decoder.prototype.decodePointer)
1.  [function <span class="apidocSignatureSpan">maxmind.decoder.prototype.</span>decodeString (offset, size)](#apidoc.element.maxmind.decoder.prototype.decodeString)
1.  [function <span class="apidocSignatureSpan">maxmind.decoder.prototype.</span>decodeUint (offset, size)](#apidoc.element.maxmind.decoder.prototype.decodeUint)
1.  [function <span class="apidocSignatureSpan">maxmind.decoder.prototype.</span>sizeFromCtrlByte (ctrlByte, offset)](#apidoc.element.maxmind.decoder.prototype.sizeFromCtrlByte)

#### [module maxmind.ip](#apidoc.module.maxmind.ip)
1.  [function <span class="apidocSignatureSpan">maxmind.ip.</span>bitAt (rawAddress, idx)](#apidoc.element.maxmind.ip.bitAt)
1.  [function <span class="apidocSignatureSpan">maxmind.ip.</span>parse (ip)](#apidoc.element.maxmind.ip.parse)
1.  [function <span class="apidocSignatureSpan">maxmind.ip.</span>validate (ip)](#apidoc.element.maxmind.ip.validate)

#### [module maxmind.metadata](#apidoc.module.maxmind.metadata)
1.  [function <span class="apidocSignatureSpan">maxmind.</span>metadata (db)](#apidoc.element.maxmind.metadata.metadata)

#### [module maxmind.metadata.prototype](#apidoc.module.maxmind.metadata.prototype)
1.  [function <span class="apidocSignatureSpan">maxmind.metadata.prototype.</span>findStart (db)](#apidoc.element.maxmind.metadata.prototype.findStart)
1.  [function <span class="apidocSignatureSpan">maxmind.metadata.prototype.</span>isLegacyFormat (db)](#apidoc.element.maxmind.metadata.prototype.isLegacyFormat)

#### [module maxmind.utils](#apidoc.module.maxmind.utils)
1.  [function <span class="apidocSignatureSpan">maxmind.utils.</span>concat2 (a, b)](#apidoc.element.maxmind.utils.concat2)
1.  [function <span class="apidocSignatureSpan">maxmind.utils.</span>concat3 (a, b, c)](#apidoc.element.maxmind.utils.concat3)
1.  [function <span class="apidocSignatureSpan">maxmind.utils.</span>concat4 (a, b, c, d)](#apidoc.element.maxmind.utils.concat4)
1.  string <span class="apidocSignatureSpan">maxmind.utils.</span>legacyErrorMessage



# <a name="apidoc.module.maxmind"></a>[module maxmind](#apidoc.module.maxmind)

#### <a name="apidoc.element.maxmind.Reader"></a>[function <span class="apidocSignatureSpan">maxmind.</span>Reader (db, opts)](#apidoc.element.maxmind.Reader)
- description and source-code
```javascript
function Reader(db, opts) {
  opts = opts || {};
  opts.cache = opts.cache || {};
  opts.cache.max = opts.cache.max || 50000;
  opts.cache.maxAge = opts.cache.maxAge || 60 * 60 * 1000; // 1hr

  this.cache = LRU(opts.cache);
  this.load(db);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.maxmind.decoder"></a>[function <span class="apidocSignatureSpan">maxmind.</span>decoder (db, baseOffset)](#apidoc.element.maxmind.decoder)
- description and source-code
```javascript
function Decoder(db, baseOffset) {
  assert(this.db = db, 'File stream is required');
  this.baseOffset = baseOffset || 0;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.maxmind.init"></a>[function <span class="apidocSignatureSpan">maxmind.</span>init ()](#apidoc.element.maxmind.init)
- description and source-code
```javascript
init = function () {
  throw new Error(utils.legacyErrorMessage);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.maxmind.metadata"></a>[function <span class="apidocSignatureSpan">maxmind.</span>metadata (db)](#apidoc.element.maxmind.metadata)
- description and source-code
```javascript
function Metadata(db) {
  var offset = this.findStart(db);
  var decoder = new Decoder(db, offset);
  var metadata = decoder.decode(offset).value;

  if (!metadata) {
    throw new Error(this.isLegacyFormat(db) ? utils.legacyErrorMessage : 'Cannot parse binary database');
  }

  this.binaryFormatMajorVersion = metadata.binary_format_major_version;
  this.binaryFormatMinorVersion = metadata.binary_format_minor_version;
  this.buildEpoch = new Date(metadata.build_epoch * 1000);
  this.databaseType = metadata.database_type;
  this.languages = metadata.languages;
  this.description = metadata.description;
  this.ipVersion = metadata.ip_version;
  this.nodeCount = metadata.node_count;

  this.recordSize = metadata.record_size;
  assert([24, 28, 32].indexOf(this.recordSize) > -1, 'Unsupported record size');

  this.nodeByteSize = this.recordSize / 4;
  this.searchTreeSize = this.nodeCount * this.nodeByteSize;

  // Depth depends on the IP version, it's 32 for IPv4 and 128 for IPv6.
  this.treeDepth = Math.pow(2, this.ipVersion + 1);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.maxmind.open"></a>[function <span class="apidocSignatureSpan">maxmind.</span>open (filepath, opts, cb)](#apidoc.element.maxmind.open)
- description and source-code
```javascript
open = function (filepath, opts, cb) {
  if (!cb) cb = opts;
  assert.equal(typeof cb, 'function', 'Callback function must be provided. \
    If you want to open library synchronously, use maxmind.openSync function.');

  fs.readFile(filepath, function(err, database) {
    if (err) return cb(err);
    if (isGzip(database)) {
      return cb(new Error('Looks like you are passing in a file in gzip format, please use mmdb database instead.'));
    }
    var reader = new Reader(database, opts);
    if (opts && !!opts.watchForUpdates) {
      fs.watch(filepath, function() {
        fs.readFile(filepath, function(err, database) {
          if (err) return cb(err);
          reader.load(database);
        });
      });
    }
    cb(null, reader);
  });
}
```
- example usage
```shell
...


## Usage

'''javascript
var maxmind = require('maxmind');

maxmind.open('/path/to/GeoLite2-City.mmdb', (err, cityLookup) => {
  var city = cityLookup.get('66.6.44.4');
});

maxmind.open('/path/to/GeoOrg.mmdb', (err, orgLookup) => {
  var city = orgLookup.get('66.6.44.4');
});
...
```

#### <a name="apidoc.element.maxmind.openSync"></a>[function <span class="apidocSignatureSpan">maxmind.</span>openSync (filepath, opts)](#apidoc.element.maxmind.openSync)
- description and source-code
```javascript
openSync = function (filepath, opts) {
  var reader = new Reader(fs.readFileSync(filepath), opts);
  if (opts && !!opts.watchForUpdates) {
    fs.watch(filepath, function() {
      reader.load(fs.readFileSync(filepath));
    });
  }

  return reader;
}
```
- example usage
```shell
...
});

// Be careful with sync version! Since mmdb files
// are quite large (city database is about 100Mb)
// 'fs.readFileSync' blocks whole process while it
// reads file into buffer.

var cityLookup = maxmind.openSync('/path/to/GeoLite2-City.mmdb');
var city = cityLookup.get('66.6.44.4');

var orgLookup = maxmind.openSync('/path/to/GeoOrg.mmdb');
var organization = orgLookup.get('66.6.44.4');
'''
...
```

#### <a name="apidoc.element.maxmind.validate"></a>[function <span class="apidocSignatureSpan">maxmind.</span>validate (ip)](#apidoc.element.maxmind.validate)
- description and source-code
```javascript
validate = function (ip) {
  var version = net.isIP(ip);
  return version === 4 || version === 6;
}
```
- example usage
```shell
...


## IP addresses validation

Module supports validation for both IPv4 and IPv6:

'''javascript
maxmind.validate('66.6.44.4'); // returns true
maxmind.validate('66.6.44.boom!'); // returns false

maxmind.validate('2001:4860:0:1001::3004:ef68'); // returns true
maxmind.validate('2001:4860:0:1001::3004:boom!'); // returns false
'''
...
```



# <a name="apidoc.module.maxmind.Reader"></a>[module maxmind.Reader](#apidoc.module.maxmind.Reader)

#### <a name="apidoc.element.maxmind.Reader.Reader"></a>[function <span class="apidocSignatureSpan">maxmind.</span>Reader (db, opts)](#apidoc.element.maxmind.Reader.Reader)
- description and source-code
```javascript
function Reader(db, opts) {
  opts = opts || {};
  opts.cache = opts.cache || {};
  opts.cache.max = opts.cache.max || 50000;
  opts.cache.maxAge = opts.cache.maxAge || 60 * 60 * 1000; // 1hr

  this.cache = LRU(opts.cache);
  this.load(db);
}
```
- example usage
```shell
n/a
```



# <a name="apidoc.module.maxmind.Reader.prototype"></a>[module maxmind.Reader.prototype](#apidoc.module.maxmind.Reader.prototype)

#### <a name="apidoc.element.maxmind.Reader.prototype.findAddressInTree"></a>[function <span class="apidocSignatureSpan">maxmind.Reader.prototype.</span>findAddressInTree (ipAddress)](#apidoc.element.maxmind.Reader.prototype.findAddressInTree)
- description and source-code
```javascript
findAddressInTree = function (ipAddress) {
  var rawAddress = ipUtil.parse(ipAddress);
  var nodeCount = this.metadata.nodeCount;

  // When storing IPv4 addresses in an IPv6 tree, they are stored as-is, so they
  // occupy the first 32-bits of the address space (from 0 to 2**32 - 1).
  // Which means they're padded with zeros.
  var ipStartBit = (this.metadata.ipVersion === 6 && rawAddress.length === 4) ? 128 - 32 : 0;

  // Binary search tree consists of certain ('nodeCount') number of nodes. Tree
  // depth depends on the ip version, it's 32 for IPv4 and 128 for IPv6. Each
  // tree node has the same fixed length and usually 6-8 bytes. It consists
  // of two records, left and right:
  // |         node        |
  // | 0x000000 | 0x000000 |
  var bit;
  var nodeNumber = ipStartBit;
  var pointer, offset;

  for (var i = ipStartBit; i < this.metadata.treeDepth; i++) {
    bit = ipUtil.bitAt(rawAddress, i - ipStartBit);
    offset = nodeNumber * this.metadata.nodeByteSize;

    pointer = bit ?
      this.readNodeRight(offset) :
      this.readNodeLeft(offset);

    // Record value can point to one of three things:
    // 1. Another node in the tree (most common case)
    if (pointer < nodeCount) {
      nodeNumber = pointer;

    // 2. Data section address with relevant information (less common case)
    } else if (pointer > nodeCount) {
      return pointer;

    // 3. Point to the value of 'nodeCount', which means IP address is unknown
    } else {
      return null;
    }
  }
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.maxmind.Reader.prototype.get"></a>[function <span class="apidocSignatureSpan">maxmind.Reader.prototype.</span>get (ipAddress)](#apidoc.element.maxmind.Reader.prototype.get)
- description and source-code
```javascript
get = function (ipAddress) {
  var pointer = this.findAddressInTree(ipAddress);
  return pointer ? this.resolveDataPointer(pointer) : null;
}
```
- example usage
```shell
...

## Usage

'''javascript
var maxmind = require('maxmind');

maxmind.open('/path/to/GeoLite2-City.mmdb', (err, cityLookup) => {
  var city = cityLookup.get('66.6.44.4');
});

maxmind.open('/path/to/GeoOrg.mmdb', (err, orgLookup) => {
  var city = orgLookup.get('66.6.44.4');
});

// Be careful with sync version! Since mmdb files
...
```

#### <a name="apidoc.element.maxmind.Reader.prototype.load"></a>[function <span class="apidocSignatureSpan">maxmind.Reader.prototype.</span>load (db)](#apidoc.element.maxmind.Reader.prototype.load)
- description and source-code
```javascript
load = function (db) {
  this.db = db;

  this.metadata = new Metadata(this.db);
  this.decoder = new Decoder(this.db, this.metadata.searchTreeSize + DATA_SECTION_SEPARATOR_SIZE);

  this.setupNodeReaderFn(this.metadata.recordSize);
}
```
- example usage
```shell
...
      return cb(new Error('Looks like you are passing in a file in gzip format, please use mmdb database instead.'));
    }
    var reader = new Reader(database, opts);
    if (opts && !!opts.watchForUpdates) {
      fs.watch(filepath, function() {
        fs.readFile(filepath, function(err, database) {
          if (err) return cb(err);
          reader.load(database);
        });
      });
    }
    cb(null, reader);
  });
};
...
```

#### <a name="apidoc.element.maxmind.Reader.prototype.resolveDataPointer"></a>[function <span class="apidocSignatureSpan">maxmind.Reader.prototype.</span>resolveDataPointer (pointer)](#apidoc.element.maxmind.Reader.prototype.resolveDataPointer)
- description and source-code
```javascript
resolveDataPointer = function (pointer) {
  if (this.cache.has(pointer)) {
    return this.cache.get(pointer);
  }

  // In order to determine where in the file this offset really points to, we also
  // need to know where the data section starts. This can be calculated by
  // determining the size of the search tree in bytes and then adding an additional
  // 16 bytes for the data section separator.
  // So the final formula to determine the offset in the file is:
  //     $offset_in_file = ( $record_value - $node_count )
  //                       + $search_tree_size_in_bytes
  var resolved = pointer - this.metadata.nodeCount + this.metadata.searchTreeSize;

  var result = this.decoder.decode(resolved).value;
  this.cache.set(pointer, result);
  return result;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.maxmind.Reader.prototype.setupNodeReaderFn"></a>[function <span class="apidocSignatureSpan">maxmind.Reader.prototype.</span>setupNodeReaderFn (recordSize)](#apidoc.element.maxmind.Reader.prototype.setupNodeReaderFn)
- description and source-code
```javascript
setupNodeReaderFn = function (recordSize) {
  switch (recordSize) {
    case 24:
      this.readNodeLeft = readNodeLeft24;
      this.readNodeRight = readNodeRight24;
      break;
    case 28:
      this.readNodeLeft = readNodeLeft28;
      this.readNodeRight = readNodeRight28;
      break;
    case 32:
      this.readNodeLeft = readNodeLeft32;
      this.readNodeRight = readNodeRight32;
      break;
  }
}
```
- example usage
```shell
n/a
```



# <a name="apidoc.module.maxmind.decoder"></a>[module maxmind.decoder](#apidoc.module.maxmind.decoder)

#### <a name="apidoc.element.maxmind.decoder.decoder"></a>[function <span class="apidocSignatureSpan">maxmind.</span>decoder (db, baseOffset)](#apidoc.element.maxmind.decoder.decoder)
- description and source-code
```javascript
function Decoder(db, baseOffset) {
  assert(this.db = db, 'File stream is required');
  this.baseOffset = baseOffset || 0;
}
```
- example usage
```shell
n/a
```



# <a name="apidoc.module.maxmind.decoder.prototype"></a>[module maxmind.decoder.prototype](#apidoc.module.maxmind.decoder.prototype)

#### <a name="apidoc.element.maxmind.decoder.prototype.decode"></a>[function <span class="apidocSignatureSpan">maxmind.decoder.prototype.</span>decode (offset)](#apidoc.element.maxmind.decoder.prototype.decode)
- description and source-code
```javascript
decode = function (offset) {
  var tmp,
    ctrlByte = this.db[offset++],
    type = types[ctrlByte >> 5];

  if (type === 'pointer') {
    tmp = this.decodePointer(ctrlByte, offset);
    return cursor(this.decode(tmp.value).value, tmp.offset);
  }

  if (type === 'extended') {
    tmp = this.db[offset] + 7;
    if (tmp < 8) {
      throw new Error('Invalid Extended Type at offset ' + offset + ' val ' + tmp);
    }

    type = types[tmp];
    offset++;
  }

  var size = this.sizeFromCtrlByte(ctrlByte, offset);
  return this.decodeByType(type, size.offset, size.value);
}
```
- example usage
```shell
...
Decoder.prototype.decode = function(offset) {
var tmp,
  ctrlByte = this.db[offset++],
  type = types[ctrlByte >> 5];

if (type === 'pointer') {
  tmp = this.decodePointer(ctrlByte, offset);
  return cursor(this.decode(tmp.value).value, tmp.offset);
}

if (type === 'extended') {
  tmp = this.db[offset] + 7;
  if (tmp < 8) {
    throw new Error('Invalid Extended Type at offset ' + offset + ' val ' + tmp);
  }
...
```

#### <a name="apidoc.element.maxmind.decoder.prototype.decodeArray"></a>[function <span class="apidocSignatureSpan">maxmind.decoder.prototype.</span>decodeArray (size, offset)](#apidoc.element.maxmind.decoder.prototype.decodeArray)
- description and source-code
```javascript
decodeArray = function (size, offset) {
  var tmp;
  var array = [];

  for (var i = 0; i < size; i++) {
    tmp = this.decode(offset);
    offset = tmp.offset;
    array.push(tmp.value);
  }

  return cursor(array, offset);
}
```
- example usage
```shell
...
case 'map':
  return this.decodeMap(size, offset);
case 'uint32':
  return cursor(this.decodeUint(offset, size), newOffset);
case 'double':
  return cursor(this.decodeDouble(offset, size), newOffset);
case 'array':
  return this.decodeArray(size, offset);
case 'boolean':
  return cursor(this.decodeBoolean(size), offset);
case 'float':
  return cursor(this.decodeFloat(offset, size), newOffset);
case 'bytes':
  return cursor(this.decodeBytes(offset, size), newOffset);
case 'uint16':
...
```

#### <a name="apidoc.element.maxmind.decoder.prototype.decodeBigUint"></a>[function <span class="apidocSignatureSpan">maxmind.decoder.prototype.</span>decodeBigUint (offset, size)](#apidoc.element.maxmind.decoder.prototype.decodeBigUint)
- description and source-code
```javascript
decodeBigUint = function (offset, size) {
  var buffer = new Buffer(size);
  this.db.copy(buffer, 0, offset, offset + size);

  var integer = 0;
  var numberOfLongs = size / 4;
  for (var i = 0; i < numberOfLongs; i++) {
    integer = bigInt(integer).multiply(4294967296).add(buffer.readUInt32BE(i << 2, true));
  }

  return integer.toString();
}
```
- example usage
```shell
...
Decoder.prototype.decodeUint = function(offset, size) {
  switch (size) {
    case 0: return 0;
    case 1: return this.db[offset];
    case 2: return utils.concat2(this.db[offset + 0], this.db[offset + 1]);
    case 3: return utils.concat3(this.db[offset + 0], this.db[offset + 1], this.db[offset + 2]);
    case 4: return utils.concat4(this.db[offset + 0], this.db[offset + 1], this.db[offset + 2], this.db[offset + 3]);
    case 8: return this.decodeBigUint(offset, size);
    case 16: return this.decodeBigUint(offset, size);
  }
  return 0;
};


Decoder.prototype.decodeBigUint = function(offset, size) {
...
```

#### <a name="apidoc.element.maxmind.decoder.prototype.decodeBoolean"></a>[function <span class="apidocSignatureSpan">maxmind.decoder.prototype.</span>decodeBoolean (size)](#apidoc.element.maxmind.decoder.prototype.decodeBoolean)
- description and source-code
```javascript
decodeBoolean = function (size) {
  return size !== 0;
}
```
- example usage
```shell
...
case 'uint32':
  return cursor(this.decodeUint(offset, size), newOffset);
case 'double':
  return cursor(this.decodeDouble(offset, size), newOffset);
case 'array':
  return this.decodeArray(size, offset);
case 'boolean':
  return cursor(this.decodeBoolean(size), offset);
case 'float':
  return cursor(this.decodeFloat(offset, size), newOffset);
case 'bytes':
  return cursor(this.decodeBytes(offset, size), newOffset);
case 'uint16':
  return cursor(this.decodeUint(offset, size), newOffset);
case 'int32':
...
```

#### <a name="apidoc.element.maxmind.decoder.prototype.decodeByType"></a>[function <span class="apidocSignatureSpan">maxmind.decoder.prototype.</span>decodeByType (type, offset, size)](#apidoc.element.maxmind.decoder.prototype.decodeByType)
- description and source-code
```javascript
decodeByType = function (type, offset, size) {
  var newOffset = offset + size;

  // ipv4 types occurrence stats:
  // 3618591 x utf8_string
  // 448163 x map
  // 175085 x uint32
  // 83040 x double
  // 24745 x array
  // 3 x uint16
  // 1 x uint64
  // 14 x boolean
  switch (type) {
    case 'utf8_string':
      return cursor(this.decodeString(offset, size), newOffset);
    case 'map':
      return this.decodeMap(size, offset);
    case 'uint32':
      return cursor(this.decodeUint(offset, size), newOffset);
    case 'double':
      return cursor(this.decodeDouble(offset, size), newOffset);
    case 'array':
      return this.decodeArray(size, offset);
    case 'boolean':
      return cursor(this.decodeBoolean(size), offset);
    case 'float':
      return cursor(this.decodeFloat(offset, size), newOffset);
    case 'bytes':
      return cursor(this.decodeBytes(offset, size), newOffset);
    case 'uint16':
      return cursor(this.decodeUint(offset, size), newOffset);
    case 'int32':
      return cursor(this.decodeInt32(offset, size), newOffset);
    case 'uint64':
      return cursor(this.decodeUint(offset, size), newOffset);
    case 'uint128':
      return cursor(this.decodeUint(offset, size), newOffset);
  }

  throw new Error('Unknown type ' + type + ' at offset ' + offset);
}
```
- example usage
```shell
...
  }

  type = types[tmp];
  offset++;
}

var size = this.sizeFromCtrlByte(ctrlByte, offset);
return this.decodeByType(type, size.offset, size.value);
};


Decoder.prototype.decodeByType = function(type, offset, size) {
var newOffset = offset + size;

// ipv4 types occurrence stats:
...
```

#### <a name="apidoc.element.maxmind.decoder.prototype.decodeBytes"></a>[function <span class="apidocSignatureSpan">maxmind.decoder.prototype.</span>decodeBytes (offset, size)](#apidoc.element.maxmind.decoder.prototype.decodeBytes)
- description and source-code
```javascript
decodeBytes = function (offset, size) {
  return this.db.slice(offset, offset + size);
}
```
- example usage
```shell
...
case 'array':
  return this.decodeArray(size, offset);
case 'boolean':
  return cursor(this.decodeBoolean(size), offset);
case 'float':
  return cursor(this.decodeFloat(offset, size), newOffset);
case 'bytes':
  return cursor(this.decodeBytes(offset, size), newOffset);
case 'uint16':
  return cursor(this.decodeUint(offset, size), newOffset);
case 'int32':
  return cursor(this.decodeInt32(offset, size), newOffset);
case 'uint64':
  return cursor(this.decodeUint(offset, size), newOffset);
case 'uint128':
...
```

#### <a name="apidoc.element.maxmind.decoder.prototype.decodeDouble"></a>[function <span class="apidocSignatureSpan">maxmind.decoder.prototype.</span>decodeDouble (offset)](#apidoc.element.maxmind.decoder.prototype.decodeDouble)
- description and source-code
```javascript
decodeDouble = function (offset) {
  return this.db.readDoubleBE(offset, true);
}
```
- example usage
```shell
...
case 'utf8_string':
  return cursor(this.decodeString(offset, size), newOffset);
case 'map':
  return this.decodeMap(size, offset);
case 'uint32':
  return cursor(this.decodeUint(offset, size), newOffset);
case 'double':
  return cursor(this.decodeDouble(offset, size), newOffset);
case 'array':
  return this.decodeArray(size, offset);
case 'boolean':
  return cursor(this.decodeBoolean(size), offset);
case 'float':
  return cursor(this.decodeFloat(offset, size), newOffset);
case 'bytes':
...
```

#### <a name="apidoc.element.maxmind.decoder.prototype.decodeFloat"></a>[function <span class="apidocSignatureSpan">maxmind.decoder.prototype.</span>decodeFloat (offset)](#apidoc.element.maxmind.decoder.prototype.decodeFloat)
- description and source-code
```javascript
decodeFloat = function (offset) {
  return this.db.readFloatBE(offset, true);
}
```
- example usage
```shell
...
case 'double':
  return cursor(this.decodeDouble(offset, size), newOffset);
case 'array':
  return this.decodeArray(size, offset);
case 'boolean':
  return cursor(this.decodeBoolean(size), offset);
case 'float':
  return cursor(this.decodeFloat(offset, size), newOffset);
case 'bytes':
  return cursor(this.decodeBytes(offset, size), newOffset);
case 'uint16':
  return cursor(this.decodeUint(offset, size), newOffset);
case 'int32':
  return cursor(this.decodeInt32(offset, size), newOffset);
case 'uint64':
...
```

#### <a name="apidoc.element.maxmind.decoder.prototype.decodeInt32"></a>[function <span class="apidocSignatureSpan">maxmind.decoder.prototype.</span>decodeInt32 (offset, size)](#apidoc.element.maxmind.decoder.prototype.decodeInt32)
- description and source-code
```javascript
decodeInt32 = function (offset, size) {
  if (size == 0) return 0;
  return this.db.readInt32BE(offset, true);
}
```
- example usage
```shell
...
  case 'float':
    return cursor(this.decodeFloat(offset, size), newOffset);
  case 'bytes':
    return cursor(this.decodeBytes(offset, size), newOffset);
  case 'uint16':
    return cursor(this.decodeUint(offset, size), newOffset);
  case 'int32':
    return cursor(this.decodeInt32(offset, size), newOffset);
  case 'uint64':
    return cursor(this.decodeUint(offset, size), newOffset);
  case 'uint128':
    return cursor(this.decodeUint(offset, size), newOffset);
}

throw new Error('Unknown type ' + type + ' at offset ' + offset);
...
```

#### <a name="apidoc.element.maxmind.decoder.prototype.decodeMap"></a>[function <span class="apidocSignatureSpan">maxmind.decoder.prototype.</span>decodeMap (size, offset)](#apidoc.element.maxmind.decoder.prototype.decodeMap)
- description and source-code
```javascript
decodeMap = function (size, offset) {
  var tmp;
  var key;
  var map = {};

  for (var i = 0; i < size; i++) {
    tmp = this.decode(offset);
    key = tmp.value;
    tmp = this.decode(tmp.offset);
    offset = tmp.offset;
    map[key] = tmp.value;
  }

  return cursor(map, offset);
}
```
- example usage
```shell
...
// 3 x uint16
// 1 x uint64
// 14 x boolean
switch (type) {
  case 'utf8_string':
    return cursor(this.decodeString(offset, size), newOffset);
  case 'map':
    return this.decodeMap(size, offset);
  case 'uint32':
    return cursor(this.decodeUint(offset, size), newOffset);
  case 'double':
    return cursor(this.decodeDouble(offset, size), newOffset);
  case 'array':
    return this.decodeArray(size, offset);
  case 'boolean':
...
```

#### <a name="apidoc.element.maxmind.decoder.prototype.decodePointer"></a>[function <span class="apidocSignatureSpan">maxmind.decoder.prototype.</span>decodePointer (ctrlByte, offset)](#apidoc.element.maxmind.decoder.prototype.decodePointer)
- description and source-code
```javascript
decodePointer = function (ctrlByte, offset) {
  // Pointers use the last five bits in the control byte to calculate the pointer value.

  // To calculate the pointer value, we start by subdiving the five bits into two
  // groups. The first two bits indicate the size, and the next three bits are part
  // of the value, so we end up with a control byte breaking down like this:
  // 001SSVVV.
  var pointerSize = ((ctrlByte >> 3) & 3);

  var pointer = this.baseOffset + pointerValueOffset[pointerSize];
  var packed = 0;

  // The size can be 0, 1, 2, or 3.

  // If the size is 0, the pointer is built by appending the next byte to the last
  // three bits to produce an 11-bit value.
  if (pointerSize === 0) {
    packed = utils.concat2(ctrlByte & 7, this.db[offset]);

  // If the size is 1, the pointer is built by appending the next two bytes to the
  // last three bits to produce a 19-bit value + 2048.
  } else if (pointerSize === 1) {
    packed = utils.concat3(ctrlByte & 7, this.db[offset], this.db[offset + 1]);

  // If the size is 2, the pointer is built by appending the next three bytes to the
  // last three bits to produce a 27-bit value + 526336.
  } else if (pointerSize === 2) {
    packed = utils.concat4(ctrlByte & 7, this.db[offset], this.db[offset + 1], this.db[offset + 2]);

  // At next point 'size' is always 3.
  // Finally, if the size is 3, the pointer's value is contained in the next four
  // bytes as a 32-bit value. In this case, the last three bits of the control byte
  // are ignored.
  } else {
    packed = this.db.readUInt32BE(offset, true);
  }

  offset += pointerSize + 1;
  return cursor(pointer + packed, offset);
}
```
- example usage
```shell
...

Decoder.prototype.decode = function(offset) {
var tmp,
  ctrlByte = this.db[offset++],
  type = types[ctrlByte >> 5];

if (type === 'pointer') {
  tmp = this.decodePointer(ctrlByte, offset);
  return cursor(this.decode(tmp.value).value, tmp.offset);
}

if (type === 'extended') {
  tmp = this.db[offset] + 7;
  if (tmp < 8) {
    throw new Error('Invalid Extended Type at offset ' + offset + ' val ' + tmp);
...
```

#### <a name="apidoc.element.maxmind.decoder.prototype.decodeString"></a>[function <span class="apidocSignatureSpan">maxmind.decoder.prototype.</span>decodeString (offset, size)](#apidoc.element.maxmind.decoder.prototype.decodeString)
- description and source-code
```javascript
decodeString = function (offset, size) {
  return this.db.utf8Slice(offset, offset + size);
}
```
- example usage
```shell
...
// 83040 x double
// 24745 x array
// 3 x uint16
// 1 x uint64
// 14 x boolean
switch (type) {
  case 'utf8_string':
    return cursor(this.decodeString(offset, size), newOffset);
  case 'map':
    return this.decodeMap(size, offset);
  case 'uint32':
    return cursor(this.decodeUint(offset, size), newOffset);
  case 'double':
    return cursor(this.decodeDouble(offset, size), newOffset);
  case 'array':
...
```

#### <a name="apidoc.element.maxmind.decoder.prototype.decodeUint"></a>[function <span class="apidocSignatureSpan">maxmind.decoder.prototype.</span>decodeUint (offset, size)](#apidoc.element.maxmind.decoder.prototype.decodeUint)
- description and source-code
```javascript
decodeUint = function (offset, size) {
  switch (size) {
    case 0: return 0;
    case 1: return this.db[offset];
    case 2: return utils.concat2(this.db[offset + 0], this.db[offset + 1]);
    case 3: return utils.concat3(this.db[offset + 0], this.db[offset + 1], this.db[offset + 2]);
    case 4: return utils.concat4(this.db[offset + 0], this.db[offset + 1], this.db[offset + 2], this.db[offset + 3]);
    case 8: return this.decodeBigUint(offset, size);
    case 16: return this.decodeBigUint(offset, size);
  }
  return 0;
}
```
- example usage
```shell
...
// 14 x boolean
switch (type) {
  case 'utf8_string':
    return cursor(this.decodeString(offset, size), newOffset);
  case 'map':
    return this.decodeMap(size, offset);
  case 'uint32':
    return cursor(this.decodeUint(offset, size), newOffset);
  case 'double':
    return cursor(this.decodeDouble(offset, size), newOffset);
  case 'array':
    return this.decodeArray(size, offset);
  case 'boolean':
    return cursor(this.decodeBoolean(size), offset);
  case 'float':
...
```

#### <a name="apidoc.element.maxmind.decoder.prototype.sizeFromCtrlByte"></a>[function <span class="apidocSignatureSpan">maxmind.decoder.prototype.</span>sizeFromCtrlByte (ctrlByte, offset)](#apidoc.element.maxmind.decoder.prototype.sizeFromCtrlByte)
- description and source-code
```javascript
sizeFromCtrlByte = function (ctrlByte, offset) {
  // The first three bits of the control byte tell you what type the field is. If
  // these bits are all 0, then this is an "extended" type, which means that the
  // *next* byte contains the actual type. Otherwise, the first three bits will
  // contain a number from 1 to 7, the actual type for the field.
  // var type = ctrlByte >> 3;

  // The next five bits in the control byte tell you how long the data field's
  // payload is, except for maps and pointers. Maps and pointers use this size
  // information a bit differently.''

  var size = ctrlByte & 0x1f;

  // If the five bits are smaller than 29, then those bits are the payload size in
  // bytes. For example:
  //   01000010          UTF-8 string - 2 bytes long
  //   01011100          UTF-8 string - 28 bytes long
  //   11000001          unsigned 32-bit int - 1 byte long
  //   00000011 00000011 unsigned 128-bit int - 3 bytes long
  if (size < 29)
    return cursor(size, offset);

  // If the value is 29, then the size is 29 + *the next byte after the type
  // specifying bytes as an unsigned integer*.
  if (size === 29)
    return cursor(29 + this.db[offset], offset + 1);

  // If the value is 30, then the size is 285 + *the next two bytes after the type
  // specifying bytes as a single unsigned integer*.
  if (size === 30)
    return cursor(285 + this.db.readUInt16BE(offset, false), offset + 2);

  // At this point 'size' is always 31.
  // If the value is 31, then the size is 65,821 + *the next three bytes after the
  // type specifying bytes as a single unsigned integer*.
  return cursor(
    65821 + utils.concat3(this.db[offset], this.db[offset + 1], this.db[offset + 2]),
    offset + 3
  );
}
```
- example usage
```shell
...
    throw new Error('Invalid Extended Type at offset ' + offset + ' val ' + tmp);
  }

  type = types[tmp];
  offset++;
}

var size = this.sizeFromCtrlByte(ctrlByte, offset);
return this.decodeByType(type, size.offset, size.value);
};


Decoder.prototype.decodeByType = function(type, offset, size) {
var newOffset = offset + size;
...
```



# <a name="apidoc.module.maxmind.ip"></a>[module maxmind.ip](#apidoc.module.maxmind.ip)

#### <a name="apidoc.element.maxmind.ip.bitAt"></a>[function <span class="apidocSignatureSpan">maxmind.ip.</span>bitAt (rawAddress, idx)](#apidoc.element.maxmind.ip.bitAt)
- description and source-code
```javascript
bitAt = function (rawAddress, idx) {
  // 8 bits per octet in the buffer (>>3 is slightly faster than Math.floor(idx/8))
  var bufIdx = idx >> 3;

  // Offset within the octet (basicallg equivalent to 8  - (idx % 8))
  var bitIdx = 7 ^ (idx & 7);

  // Shift the offset rightwards by bitIdx bits and & it to grab the bit
  return (rawAddress[bufIdx] >>> bitIdx) & 1;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.maxmind.ip.parse"></a>[function <span class="apidocSignatureSpan">maxmind.ip.</span>parse (ip)](#apidoc.element.maxmind.ip.parse)
- description and source-code
```javascript
parse = function (ip) {
  return (ip.indexOf(':') === -1) ? parseIPv4(ip) : parseIPv6(ip);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.maxmind.ip.validate"></a>[function <span class="apidocSignatureSpan">maxmind.ip.</span>validate (ip)](#apidoc.element.maxmind.ip.validate)
- description and source-code
```javascript
validate = function (ip) {
  var version = net.isIP(ip);
  return version === 4 || version === 6;
}
```
- example usage
```shell
...


## IP addresses validation

Module supports validation for both IPv4 and IPv6:

'''javascript
maxmind.validate('66.6.44.4'); // returns true
maxmind.validate('66.6.44.boom!'); // returns false

maxmind.validate('2001:4860:0:1001::3004:ef68'); // returns true
maxmind.validate('2001:4860:0:1001::3004:boom!'); // returns false
'''
...
```



# <a name="apidoc.module.maxmind.metadata"></a>[module maxmind.metadata](#apidoc.module.maxmind.metadata)

#### <a name="apidoc.element.maxmind.metadata.metadata"></a>[function <span class="apidocSignatureSpan">maxmind.</span>metadata (db)](#apidoc.element.maxmind.metadata.metadata)
- description and source-code
```javascript
function Metadata(db) {
  var offset = this.findStart(db);
  var decoder = new Decoder(db, offset);
  var metadata = decoder.decode(offset).value;

  if (!metadata) {
    throw new Error(this.isLegacyFormat(db) ? utils.legacyErrorMessage : 'Cannot parse binary database');
  }

  this.binaryFormatMajorVersion = metadata.binary_format_major_version;
  this.binaryFormatMinorVersion = metadata.binary_format_minor_version;
  this.buildEpoch = new Date(metadata.build_epoch * 1000);
  this.databaseType = metadata.database_type;
  this.languages = metadata.languages;
  this.description = metadata.description;
  this.ipVersion = metadata.ip_version;
  this.nodeCount = metadata.node_count;

  this.recordSize = metadata.record_size;
  assert([24, 28, 32].indexOf(this.recordSize) > -1, 'Unsupported record size');

  this.nodeByteSize = this.recordSize / 4;
  this.searchTreeSize = this.nodeCount * this.nodeByteSize;

  // Depth depends on the IP version, it's 32 for IPv4 and 128 for IPv6.
  this.treeDepth = Math.pow(2, this.ipVersion + 1);
}
```
- example usage
```shell
n/a
```



# <a name="apidoc.module.maxmind.metadata.prototype"></a>[module maxmind.metadata.prototype](#apidoc.module.maxmind.metadata.prototype)

#### <a name="apidoc.element.maxmind.metadata.prototype.findStart"></a>[function <span class="apidocSignatureSpan">maxmind.metadata.prototype.</span>findStart (db)](#apidoc.element.maxmind.metadata.prototype.findStart)
- description and source-code
```javascript
findStart = function (db) {
  var found = 0,
    mlen = METADATA_START_MARKER.length - 1,
    fsize = db.length - 1;

  while (found <= mlen && fsize-- > 0) {
    found += (db[fsize] === METADATA_START_MARKER[mlen - found]) ? 1 : -found;
  }
  return fsize + found;
}
```
- example usage
```shell
...

var METADATA_START_MARKER = new Buffer('ABCDEF4D61784D696E642E636F6D', 'hex');


module.exports = Metadata;

function Metadata(db) {
var offset = this.findStart(db);
var decoder = new Decoder(db, offset);
var metadata = decoder.decode(offset).value;

if (!metadata) {
  throw new Error(this.isLegacyFormat(db) ? utils.legacyErrorMessage : 'Cannot parse binary database');
}
...
```

#### <a name="apidoc.element.maxmind.metadata.prototype.isLegacyFormat"></a>[function <span class="apidocSignatureSpan">maxmind.metadata.prototype.</span>isLegacyFormat (db)](#apidoc.element.maxmind.metadata.prototype.isLegacyFormat)
- description and source-code
```javascript
isLegacyFormat = function (db) {
  var structureInfoMaxSize = 20;

  for (var i = 0; i < structureInfoMaxSize; i++) {
    var delim = db.slice(db.length - 3 - i, db.length - i);

    // Look for [0xff, 0xff, 0xff] metadata delimeter
    if (delim[0] === 255 && delim[1] === 255 && delim[2] === 255) {
      return true;
    }
  }

  return false;
}
```
- example usage
```shell
...

function Metadata(db) {
var offset = this.findStart(db);
var decoder = new Decoder(db, offset);
var metadata = decoder.decode(offset).value;

if (!metadata) {
  throw new Error(this.isLegacyFormat(db) ? utils.legacyErrorMessage : 'Cannot parse binary database');
}

this.binaryFormatMajorVersion = metadata.binary_format_major_version;
this.binaryFormatMinorVersion = metadata.binary_format_minor_version;
this.buildEpoch = new Date(metadata.build_epoch * 1000);
this.databaseType = metadata.database_type;
this.languages = metadata.languages;
...
```



# <a name="apidoc.module.maxmind.utils"></a>[module maxmind.utils](#apidoc.module.maxmind.utils)

#### <a name="apidoc.element.maxmind.utils.concat2"></a>[function <span class="apidocSignatureSpan">maxmind.utils.</span>concat2 (a, b)](#apidoc.element.maxmind.utils.concat2)
- description and source-code
```javascript
concat2 = function (a, b) {
  return (a << 8) | b;
}
```
- example usage
```shell
...
var packed = 0;

// The size can be 0, 1, 2, or 3.

// If the size is 0, the pointer is built by appending the next byte to the last
// three bits to produce an 11-bit value.
if (pointerSize === 0) {
  packed = utils.concat2(ctrlByte & 7, this.db[offset]);

// If the size is 1, the pointer is built by appending the next two bytes to the
// last three bits to produce a 19-bit value + 2048.
} else if (pointerSize === 1) {
  packed = utils.concat3(ctrlByte & 7, this.db[offset], this.db[offset + 1]);

// If the size is 2, the pointer is built by appending the next three bytes to the
...
```

#### <a name="apidoc.element.maxmind.utils.concat3"></a>[function <span class="apidocSignatureSpan">maxmind.utils.</span>concat3 (a, b, c)](#apidoc.element.maxmind.utils.concat3)
- description and source-code
```javascript
concat3 = function (a, b, c) {
  return (a << 16) | (b << 8) | c;
}
```
- example usage
```shell
...
if (size === 30)
  return cursor(285 + this.db.readUInt16BE(offset, false), offset + 2);

// At this point 'size' is always 31.
// If the value is 31, then the size is 65,821 + *the next three bytes after the
// type specifying bytes as a single unsigned integer*.
return cursor(
  65821 + utils.concat3(this.db[offset], this.db[offset + 1], this.db[offset + 2]),
  offset + 3
);
};


Decoder.prototype.decodeBytes = function(offset, size) {
return this.db.slice(offset, offset + size);
...
```

#### <a name="apidoc.element.maxmind.utils.concat4"></a>[function <span class="apidocSignatureSpan">maxmind.utils.</span>concat4 (a, b, c, d)](#apidoc.element.maxmind.utils.concat4)
- description and source-code
```javascript
concat4 = function (a, b, c, d) {
  return (a << 24) | (b << 16) | (c << 8) | d;
}
```
- example usage
```shell
...
// last three bits to produce a 19-bit value + 2048.
} else if (pointerSize === 1) {
  packed = utils.concat3(ctrlByte & 7, this.db[offset], this.db[offset + 1]);

// If the size is 2, the pointer is built by appending the next three bytes to the
// last three bits to produce a 27-bit value + 526336.
} else if (pointerSize === 2) {
  packed = utils.concat4(ctrlByte & 7, this.db[offset], this.db[offset + 1], this.db[offset + 2]);

// At next point 'size' is always 3.
// Finally, if the size is 3, the pointer's value is contained in the next four
// bytes as a 32-bit value. In this case, the last three bits of the control byte
// are ignored.
} else {
  packed = this.db.readUInt32BE(offset, true);
...
```



# misc
- this document was created with [utility2](https://github.com/kaizhu256/node-utility2)
