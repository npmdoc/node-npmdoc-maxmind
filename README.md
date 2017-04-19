# npmdoc-maxmind

#### api documentation for  [maxmind (v2.2.0)](https://github.com/runk/node-maxmind)  [![npm package](https://img.shields.io/npm/v/npmdoc-maxmind.svg?style=flat-square)](https://www.npmjs.org/package/npmdoc-maxmind) [![travis-ci.org build-status](https://api.travis-ci.org/npmdoc/node-npmdoc-maxmind.svg)](https://travis-ci.org/npmdoc/node-npmdoc-maxmind)

#### IP lookup using Maxmind databases

[![NPM](https://nodei.co/npm/maxmind.png?downloads=true&downloadRank=true&stars=true)](https://www.npmjs.com/package/maxmind)

- [https://npmdoc.github.io/node-npmdoc-maxmind/build/apidoc.html](https://npmdoc.github.io/node-npmdoc-maxmind/build/apidoc.html)

[![apidoc](https://npmdoc.github.io/node-npmdoc-maxmind/build/screenCapture.buildCi.browser.%252Ftmp%252Fbuild%252Fapidoc.html.png)](https://npmdoc.github.io/node-npmdoc-maxmind/build/apidoc.html)

![npmPackageListing](https://npmdoc.github.io/node-npmdoc-maxmind/build/screenCapture.npmPackageListing.svg)

![npmPackageDependencyTree](https://npmdoc.github.io/node-npmdoc-maxmind/build/screenCapture.npmPackageDependencyTree.svg)



# package.json

```json

{
    "author": {
        "name": "Dmitry Shirokov"
    },
    "bugs": {
        "url": "http://github.com/runk/node-maxmind/issues"
    },
    "contributors": [
        {
            "name": "Thomas Birke @quafzi"
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
            "name": "runk"
        }
    ],
    "name": "maxmind",
    "optionalDependencies": {},
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



# misc
- this document was created with [utility2](https://github.com/kaizhu256/node-utility2)
