# npmtest-now

#### basic test coverage for  now (v4.11.2)  [![npm package](https://img.shields.io/npm/v/npmtest-now.svg?style=flat-square)](https://www.npmjs.org/package/npmtest-now) [![travis-ci.org build-status](https://api.travis-ci.org/npmtest/node-npmtest-now.svg)](https://travis-ci.org/npmtest/node-npmtest-now)

#### The command line interface for Now

[![NPM](https://nodei.co/npm/now.png?downloads=true&downloadRank=true&stars=true)](https://www.npmjs.com/package/now)

| git-branch : | [alpha](https://github.com/npmtest/node-npmtest-now/tree/alpha)|
|--:|:--|
| coverage : | [![istanbul-coverage](https://npmtest.github.io/node-npmtest-now/build/coverage.badge.svg)](https://npmtest.github.io/node-npmtest-now/build/coverage.html/index.html)|
| test-report : | [![test-report](https://npmtest.github.io/node-npmtest-now/build/test-report.badge.svg)](https://npmtest.github.io/node-npmtest-now/build/test-report.html)|
| test-server-github : | [![github.com test-server](https://npmtest.github.io/node-npmtest-now/GitHub-Mark-32px.png)](https://npmtest.github.io/node-npmtest-now/build/app/index.html) | | build-artifacts : | [![build-artifacts](https://npmtest.github.io/node-npmtest-now/glyphicons_144_folder_open.png)](https://github.com/npmtest/node-npmtest-now/tree/gh-pages/build)|

- [https://npmtest.github.io/node-npmtest-now/build/coverage.html/index.html](https://npmtest.github.io/node-npmtest-now/build/coverage.html/index.html)

[![istanbul-coverage](https://npmtest.github.io/node-npmtest-now/build/screenCapture.buildCi.browser.%252Ftmp%252Fbuild%252Fcoverage.lib.html.png)](https://npmtest.github.io/node-npmtest-now/build/coverage.html/index.html)

- [https://npmtest.github.io/node-npmtest-now/build/test-report.html](https://npmtest.github.io/node-npmtest-now/build/test-report.html)

[![test-report](https://npmtest.github.io/node-npmtest-now/build/screenCapture.buildCi.browser.%252Ftmp%252Fbuild%252Ftest-report.html.png)](https://npmtest.github.io/node-npmtest-now/build/test-report.html)

- [https://npmdoc.github.io/node-npmdoc-now/build/apidoc.html](https://npmdoc.github.io/node-npmdoc-now/build/apidoc.html)

[![apidoc](https://npmdoc.github.io/node-npmdoc-now/build/screenCapture.buildCi.browser.%252Ftmp%252Fbuild%252Fapidoc.html.png)](https://npmdoc.github.io/node-npmdoc-now/build/apidoc.html)

![npmPackageListing](https://npmtest.github.io/node-npmtest-now/build/screenCapture.npmPackageListing.svg)

![npmPackageDependencyTree](https://npmtest.github.io/node-npmtest-now/build/screenCapture.npmPackageDependencyTree.svg)



# package.json

```json

{
    "name": "now",
    "version": "4.11.2",
    "description": "The command line interface for Now",
    "repository": "zeit/now-cli",
    "license": "MIT",
    "files": [
        "build"
    ],
    "scripts": {
        "precommit": "lint-staged",
        "lint": "xo",
        "test": "npm run build && npm run lint && ava",
        "prepublish": "npm run build",
        "build": "./build.sh",
        "pack": "pkg bin/now.js --config package.json --out-dir packed -t node7-alpine-x64,node7-linux-x64,node7-macos-x64,node7-win-x64"
    },
    "pkg": {
        "scripts": [
            "bin/*",
            "lib/**/*"
        ]
    },
    "bin": {
        "now": "./build/bin/now.js"
    },
    "ava": {
        "failFast": true,
        "files": [
            "test/*.js"
        ]
    },
    "xo": {
        "ignores": [
            "test/_fixtures/**",
            "scripts/build/**"
        ],
        "extends": "prettier"
    },
    "lint-staged": {
        "*.js": [
            "npm run lint",
            "prettier --single-quote --write",
            "git add"
        ]
    },
    "engines": {
        "node": ">=6.9.0"
    },
    "dependencies": {
        "@google/maps": "0.3.1",
        "ansi-escapes": "1.4.0",
        "ansi-regex": "2.1.1",
        "arr-flatten": "1.0.2",
        "array-unique": "0.3.2",
        "async-retry": "0.3.0",
        "async-to-gen": "1.3.2",
        "bytes": "2.5.0",
        "chalk": "1.1.3",
        "copy-paste": "1.3.0",
        "credit-card": "3.0.1",
        "cross-spawn": "5.1.0",
        "docker-file-parser": "1.0.1",
        "dotenv": "4.0.0",
        "download": "5.0.3",
        "email-prompt": "0.2.0",
        "email-validator": "1.0.7",
        "fs-promise": "2.0.2",
        "glob": "7.1.1",
        "ignore": "3.2.7",
        "ini": "1.3.4",
        "inquirer": "3.0.6",
        "is-url": "1.2.2",
        "minimist": "1.2.0",
        "ms": "1.0.0",
        "node-fetch": "1.6.3",
        "node-version": "1.0.0",
        "opn": "4.0.2",
        "ora": "1.2.0",
        "progress": "2.0.0",
        "psl": "1.1.18",
        "resumer": "0.0.0",
        "socket.io-client": "1.7.3",
        "split-array": "1.0.1",
        "strip-ansi": "3.0.1",
        "stripe": "4.17.1",
        "text-table": "0.2.0",
        "tmp-promise": "1.0.3",
        "update-notifier": "2.1.0"
    },
    "devDependencies": {
        "alpha-sort": "2.0.1",
        "ava": "0.19.1",
        "eslint-config-prettier": "1.6.0",
        "husky": "0.13.3",
        "lint-staged": "3.4.0",
        "pkg": "3.0.0-beta.29",
        "prettier": "1.1.0",
        "slackup": "2.0.1",
        "xo": "0.18.1"
    }
}
```



# misc
- this document was created with [utility2](https://github.com/kaizhu256/node-utility2)
