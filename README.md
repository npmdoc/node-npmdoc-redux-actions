# npmdoc-redux-actions

#### api documentation for  [redux-actions (v2.0.2)](https://github.com/acdlite/redux-actions)  [![npm package](https://img.shields.io/npm/v/npmdoc-redux-actions.svg?style=flat-square)](https://www.npmjs.org/package/npmdoc-redux-actions) [![travis-ci.org build-status](https://api.travis-ci.org/npmdoc/node-npmdoc-redux-actions.svg)](https://travis-ci.org/npmdoc/node-npmdoc-redux-actions)

#### Flux Standard Action utlities for Redux

[![NPM](https://nodei.co/npm/redux-actions.png?downloads=true&downloadRank=true&stars=true)](https://www.npmjs.com/package/redux-actions)

- [https://npmdoc.github.io/node-npmdoc-redux-actions/build/apidoc.html](https://npmdoc.github.io/node-npmdoc-redux-actions/build/apidoc.html)

[![apidoc](https://npmdoc.github.io/node-npmdoc-redux-actions/build/screenCapture.buildCi.browser.%252Ftmp%252Fbuild%252Fapidoc.html.png)](https://npmdoc.github.io/node-npmdoc-redux-actions/build/apidoc.html)

![npmPackageListing](https://npmdoc.github.io/node-npmdoc-redux-actions/build/screenCapture.npmPackageListing.svg)

![npmPackageDependencyTree](https://npmdoc.github.io/node-npmdoc-redux-actions/build/screenCapture.npmPackageDependencyTree.svg)



# package.json

```json

{
    "author": {
        "name": "Andrew Clark"
    },
    "bugs": {
        "url": "https://github.com/acdlite/redux-actions/issues"
    },
    "dependencies": {
        "invariant": "^2.2.1",
        "lodash": "^4.13.1",
        "lodash-es": "^4.17.4",
        "reduce-reducers": "^0.1.0"
    },
    "description": "Flux Standard Action utlities for Redux",
    "devDependencies": {
        "babel-cli": "^6.7.7",
        "babel-core": "^6.7.7",
        "babel-eslint": "^6.1.1",
        "babel-loader": "^6.2.4",
        "babel-preset-es2015": "^6.6.0",
        "babel-preset-stage-0": "^6.5.0",
        "babel-register": "^6.7.2",
        "chai": "^3.0.0",
        "cross-env": "^2.0.0",
        "eslint": "^2.8.0",
        "eslint-config-airbnb-base": "^1.0.3",
        "eslint-plugin-import": "^1.5.0",
        "eslint-watch": "^2.1.13",
        "flux-standard-action": "^1.0.0",
        "mocha": "^2.2.5",
        "rimraf": "^2.5.3",
        "webpack": "^1.13.1"
    },
    "directories": {},
    "dist": {
        "shasum": "49b2d9511c240a96cb2c0ca27cb15d016faecec0",
        "tarball": "https://registry.npmjs.org/redux-actions/-/redux-actions-2.0.2.tgz"
    },
    "files": [
        "es",
        "lib",
        "dist"
    ],
    "gitHead": "feb9386b76c062e17c92f73478fe6a8f1001666e",
    "homepage": "https://github.com/acdlite/redux-actions",
    "jsnext:main": "es/index.js",
    "keywords": [
        "flux",
        "redux",
        "fsa",
        "actions"
    ],
    "license": "MIT",
    "main": "lib/index.js",
    "maintainers": [
        {
            "name": "acdlite"
        },
        {
            "name": "timche"
        },
        {
            "name": "yangmillstheory"
        }
    ],
    "module": "es/index.js",
    "name": "redux-actions",
    "optionalDependencies": {},
    "repository": {
        "type": "git",
        "url": "git+https://github.com/acdlite/redux-actions.git"
    },
    "scripts": {
        "build": "npm run clean && npm run build:es && npm run build:commonjs && npm run build:umd && npm run build:umd:min",
        "build:commonjs": "babel src --out-dir lib --ignore *-test.js",
        "build:es": "cross-env BABEL_ENV=es babel src --out-dir es --ignore *-test.js",
        "build:umd": "cross-env NODE_ENV=development webpack",
        "build:umd:min": "cross-env NODE_ENV=production webpack",
        "clean": "rimraf lib es",
        "lint": "esw build src webpack.config --color",
        "lint:fix": "npm run lint -- --fix",
        "lint:watch": "npm run lint -- --watch",
        "prepublish": "npm run lint && npm run test && npm run build",
        "test": "mocha --compilers js:babel-register src/**/*-test.js",
        "test:watch": "npm run test -- --watch src/**/*-test.js"
    },
    "version": "2.0.2",
    "bin": {}
}
```



# misc
- this document was created with [utility2](https://github.com/kaizhu256/node-utility2)
