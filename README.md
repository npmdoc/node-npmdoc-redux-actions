# api documentation for  [redux-actions (v2.0.1)](https://github.com/acdlite/redux-actions)  [![npm package](https://img.shields.io/npm/v/npmdoc-redux-actions.svg?style=flat-square)](https://www.npmjs.org/package/npmdoc-redux-actions) [![travis-ci.org build-status](https://api.travis-ci.org/npmdoc/node-npmdoc-redux-actions.svg)](https://travis-ci.org/npmdoc/node-npmdoc-redux-actions)
#### Flux Standard Action utlities for Redux

[![NPM](https://nodei.co/npm/redux-actions.png?downloads=true)](https://www.npmjs.com/package/redux-actions)

[![apidoc](https://npmdoc.github.io/node-npmdoc-redux-actions/build/screenCapture.buildNpmdoc.browser.%2Fhome%2Ftravis%2Fbuild%2Fnpmdoc%2Fnode-npmdoc-redux-actions%2Ftmp%2Fbuild%2Fapidoc.html.png)](https://npmdoc.github.io/node-npmdoc-redux-actions/build/apidoc.html)

![npmPackageListing](https://npmdoc.github.io/node-npmdoc-redux-actions/build/screenCapture.npmPackageListing.svg)

![npmPackageDependencyTree](https://npmdoc.github.io/node-npmdoc-redux-actions/build/screenCapture.npmPackageDependencyTree.svg)



# package.json

```json

{
    "author": {
        "name": "Andrew Clark",
        "email": "acdlite@me.com"
    },
    "bugs": {
        "url": "https://github.com/acdlite/redux-actions/issues"
    },
    "dependencies": {
        "invariant": "^2.2.1",
        "lodash": "^4.13.1",
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
        "shasum": "8bae89938987bd0a446c509dfdac6b64e770765a",
        "tarball": "https://registry.npmjs.org/redux-actions/-/redux-actions-2.0.1.tgz"
    },
    "files": [
        "es",
        "lib",
        "dist"
    ],
    "gitHead": "727d9c1368c0263415071af1af3845897d1e88b3",
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
            "name": "acdlite",
            "email": "acdlite@me.com"
        },
        {
            "name": "timche",
            "email": "tim@cheung.io"
        },
        {
            "name": "yangmillstheory",
            "email": "v.alvarez312@gmail.com"
        }
    ],
    "module": "es/index.js",
    "name": "redux-actions",
    "optionalDependencies": {},
    "readme": "ERROR: No README data found!",
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
    "version": "2.0.1"
}
```



# <a name="apidoc.tableOfContents"></a>[table of contents](#apidoc.tableOfContents)

#### [module redux-actions](#apidoc.module.redux-actions)
1.  [function <span class="apidocSignatureSpan">redux-actions.</span>combineActions ()](#apidoc.element.redux-actions.combineActions)
1.  [function <span class="apidocSignatureSpan">redux-actions.</span>createAction (type)](#apidoc.element.redux-actions.createAction)
1.  [function <span class="apidocSignatureSpan">redux-actions.</span>createActions (actionMap)](#apidoc.element.redux-actions.createActions)
1.  [function <span class="apidocSignatureSpan">redux-actions.</span>handleAction (type)](#apidoc.element.redux-actions.handleAction)
1.  [function <span class="apidocSignatureSpan">redux-actions.</span>handleActions (handlers, defaultState)](#apidoc.element.redux-actions.handleActions)
1.  object <span class="apidocSignatureSpan">redux-actions.</span>arrayToObject
1.  object <span class="apidocSignatureSpan">redux-actions.</span>camelCase
1.  object <span class="apidocSignatureSpan">redux-actions.</span>namespaceActions
1.  object <span class="apidocSignatureSpan">redux-actions.</span>ownKeys

#### [module redux-actions.arrayToObject](#apidoc.module.redux-actions.arrayToObject)
1.  [function <span class="apidocSignatureSpan">redux-actions.arrayToObject.</span>default (array, callback)](#apidoc.element.redux-actions.arrayToObject.default)

#### [module redux-actions.camelCase](#apidoc.module.redux-actions.camelCase)
1.  [function <span class="apidocSignatureSpan">redux-actions.camelCase.</span>default (type)](#apidoc.element.redux-actions.camelCase.default)

#### [module redux-actions.combineActions](#apidoc.module.redux-actions.combineActions)
1.  [function <span class="apidocSignatureSpan">redux-actions.combineActions.</span>default ()](#apidoc.element.redux-actions.combineActions.default)
1.  string <span class="apidocSignatureSpan">redux-actions.combineActions.</span>ACTION_TYPE_DELIMITER

#### [module redux-actions.createAction](#apidoc.module.redux-actions.createAction)
1.  [function <span class="apidocSignatureSpan">redux-actions.createAction.</span>default (type)](#apidoc.element.redux-actions.createAction.default)

#### [module redux-actions.createActions](#apidoc.module.redux-actions.createActions)
1.  [function <span class="apidocSignatureSpan">redux-actions.createActions.</span>default (actionMap)](#apidoc.element.redux-actions.createActions.default)

#### [module redux-actions.handleAction](#apidoc.module.redux-actions.handleAction)
1.  [function <span class="apidocSignatureSpan">redux-actions.handleAction.</span>default (type)](#apidoc.element.redux-actions.handleAction.default)

#### [module redux-actions.handleActions](#apidoc.module.redux-actions.handleActions)
1.  [function <span class="apidocSignatureSpan">redux-actions.handleActions.</span>default (handlers, defaultState)](#apidoc.element.redux-actions.handleActions.default)

#### [module redux-actions.namespaceActions](#apidoc.module.redux-actions.namespaceActions)
1.  [function <span class="apidocSignatureSpan">redux-actions.namespaceActions.</span>flattenActionMap (actionMap)](#apidoc.element.redux-actions.namespaceActions.flattenActionMap)
1.  [function <span class="apidocSignatureSpan">redux-actions.namespaceActions.</span>unflattenActionCreators (flatActionCreators)](#apidoc.element.redux-actions.namespaceActions.unflattenActionCreators)
1.  string <span class="apidocSignatureSpan">redux-actions.namespaceActions.</span>defaultNamespace

#### [module redux-actions.ownKeys](#apidoc.module.redux-actions.ownKeys)
1.  [function <span class="apidocSignatureSpan">redux-actions.ownKeys.</span>default (object)](#apidoc.element.redux-actions.ownKeys.default)



# <a name="apidoc.module.redux-actions"></a>[module redux-actions](#apidoc.module.redux-actions)

#### <a name="apidoc.element.redux-actions.combineActions"></a>[function <span class="apidocSignatureSpan">redux-actions.</span>combineActions ()](#apidoc.element.redux-actions.combineActions)
- description and source-code
```javascript
function combineActions() {
  for (var _len = arguments.length, actionsTypes = Array(_len), _key = 0; _key < _len; _key++) {
    actionsTypes[_key] = arguments[_key];
  }

  (0, _invariant2.default)(isValidActionTypes(actionsTypes), 'Expected action types to be strings, symbols, or action creators');
  var combinedActionType = actionsTypes.map(_toString2.default).join(ACTION_TYPE_DELIMITER);
  return { toString: function toString() {
      return combinedActionType;
    } };
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.redux-actions.createAction"></a>[function <span class="apidocSignatureSpan">redux-actions.</span>createAction (type)](#apidoc.element.redux-actions.createAction)
- description and source-code
```javascript
function createAction(type) {
  var payloadCreator = arguments.length <= 1 || arguments[1] === undefined ? _identity2.default : arguments[1];
  var metaCreator = arguments[2];

  (0, _invariant2.default)((0, _isFunction2.default)(payloadCreator) || (0, _isNull2.default)(payloadCreator), 'Expected payloadCreator
 to be a function, undefined or null');

  var finalPayloadCreator = (0, _isNull2.default)(payloadCreator) ? _identity2.default : payloadCreator;

  var actionCreator = function actionCreator() {
    var hasError = (arguments.length <= 0 ? undefined : arguments[0]) instanceof Error;

    var action = {
      type: type
    };

    var payload = hasError ? arguments.length <= 0 ? undefined : arguments[0] : finalPayloadCreator.apply(undefined, arguments);
    if (!(0, _isUndefined2.default)(payload)) {
      action.payload = payload;
    }

    if (hasError || payload instanceof Error) {
      // Handle FSA errors where the payload is an Error object. Set error.
      action.error = true;
    }

    if ((0, _isFunction2.default)(metaCreator)) {
      action.meta = metaCreator.apply(undefined, arguments);
    }

    return action;
  };

  actionCreator.toString = function () {
    return type.toString();
  };

  return actionCreator;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.redux-actions.createActions"></a>[function <span class="apidocSignatureSpan">redux-actions.</span>createActions (actionMap)](#apidoc.element.redux-actions.createActions)
- description and source-code
```javascript
function createActions(actionMap) {
  for (var _len = arguments.length, identityActions = Array(_len > 1 ? _len - 1 : 0), _key = 1; _key < _len; _key++) {
    identityActions[_key - 1] = arguments[_key];
  }

  function getFullOptions() {
    var partialOptions = (0, _isPlainObject2.default)((0, _last2.default)(identityActions)) ? identityActions.pop() : {};
    return (0, _defaults2.default)(partialOptions, { namespace: _namespaceActions.defaultNamespace });
  }

  var _getFullOptions = getFullOptions();

  var namespace = _getFullOptions.namespace;

  (0, _invariant2.default)(identityActions.every(_isString2.default) && ((0, _isString2.default)(actionMap) || (0, _isPlainObject2
.default)(actionMap)), 'Expected optional object followed by string action types');
  if ((0, _isString2.default)(actionMap)) {
    return actionCreatorsFromIdentityActions([actionMap].concat(identityActions));
  }
  return _extends({}, actionCreatorsFromActionMap(actionMap, namespace), actionCreatorsFromIdentityActions(identityActions));
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.redux-actions.handleAction"></a>[function <span class="apidocSignatureSpan">redux-actions.</span>handleAction (type)](#apidoc.element.redux-actions.handleAction)
- description and source-code
```javascript
function handleAction(type) {
  var reducer = arguments.length <= 1 || arguments[1] === undefined ? _identity2.default : arguments[1];
  var defaultState = arguments[2];

  var types = type.toString().split(_combineActions.ACTION_TYPE_DELIMITER);
  (0, _invariant2.default)(!(0, _isUndefined2.default)(defaultState), 'defaultState for reducer handling ' + types.join(', ') + '
should be defined');
  (0, _invariant2.default)((0, _isFunction2.default)(reducer) || (0, _isPlainObject2.default)(reducer), 'Expected reducer to be
a function or object with next and throw reducers');

  var _ref = (0, _isFunction2.default)(reducer) ? [reducer, reducer] : [reducer.next, reducer.throw].map(function (aReducer) {
    return (0, _isNil2.default)(aReducer) ? _identity2.default : aReducer;
  });

  var _ref2 = _slicedToArray(_ref, 2);

  var nextReducer = _ref2[0];
  var throwReducer = _ref2[1];


  return function () {
    var state = arguments.length <= 0 || arguments[0] === undefined ? defaultState : arguments[0];
    var action = arguments[1];
    var actionType = action.type;

    if (!actionType || !(0, _includes2.default)(types, actionType.toString())) {
      return state;
    }

    return (action.error === true ? throwReducer : nextReducer)(state, action);
  };
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.redux-actions.handleActions"></a>[function <span class="apidocSignatureSpan">redux-actions.</span>handleActions (handlers, defaultState)](#apidoc.element.redux-actions.handleActions)
- description and source-code
```javascript
function handleActions(handlers, defaultState) {
  var reducers = (0, _ownKeys2.default)(handlers).map(function (type) {
    return (0, _handleAction2.default)(type, handlers[type], defaultState);
  });
  var reducer = _reduceReducers2.default.apply(undefined, _toConsumableArray(reducers));
  return function (state, action) {
    return reducer(state, action);
  };
}
```
- example usage
```shell
n/a
```



# <a name="apidoc.module.redux-actions.arrayToObject"></a>[module redux-actions.arrayToObject](#apidoc.module.redux-actions.arrayToObject)

#### <a name="apidoc.element.redux-actions.arrayToObject.default"></a>[function <span class="apidocSignatureSpan">redux-actions.arrayToObject.</span>default (array, callback)](#apidoc.element.redux-actions.arrayToObject.default)
- description and source-code
```javascript
default = function (array, callback) {
  return array.reduce(function (partialObject, element) {
    return callback(partialObject, element);
  }, {});
}
```
- example usage
```shell
n/a
```



# <a name="apidoc.module.redux-actions.camelCase"></a>[module redux-actions.camelCase](#apidoc.module.redux-actions.camelCase)

#### <a name="apidoc.element.redux-actions.camelCase.default"></a>[function <span class="apidocSignatureSpan">redux-actions.camelCase.</span>default (type)](#apidoc.element.redux-actions.camelCase.default)
- description and source-code
```javascript
default = function (type) {
  return type.split(namespacer).map(camelCase).join(namespacer);
}
```
- example usage
```shell
n/a
```



# <a name="apidoc.module.redux-actions.combineActions"></a>[module redux-actions.combineActions](#apidoc.module.redux-actions.combineActions)

#### <a name="apidoc.element.redux-actions.combineActions.default"></a>[function <span class="apidocSignatureSpan">redux-actions.combineActions.</span>default ()](#apidoc.element.redux-actions.combineActions.default)
- description and source-code
```javascript
function combineActions() {
  for (var _len = arguments.length, actionsTypes = Array(_len), _key = 0; _key < _len; _key++) {
    actionsTypes[_key] = arguments[_key];
  }

  (0, _invariant2.default)(isValidActionTypes(actionsTypes), 'Expected action types to be strings, symbols, or action creators');
  var combinedActionType = actionsTypes.map(_toString2.default).join(ACTION_TYPE_DELIMITER);
  return { toString: function toString() {
      return combinedActionType;
    } };
}
```
- example usage
```shell
n/a
```



# <a name="apidoc.module.redux-actions.createAction"></a>[module redux-actions.createAction](#apidoc.module.redux-actions.createAction)

#### <a name="apidoc.element.redux-actions.createAction.default"></a>[function <span class="apidocSignatureSpan">redux-actions.createAction.</span>default (type)](#apidoc.element.redux-actions.createAction.default)
- description and source-code
```javascript
function createAction(type) {
  var payloadCreator = arguments.length <= 1 || arguments[1] === undefined ? _identity2.default : arguments[1];
  var metaCreator = arguments[2];

  (0, _invariant2.default)((0, _isFunction2.default)(payloadCreator) || (0, _isNull2.default)(payloadCreator), 'Expected payloadCreator
 to be a function, undefined or null');

  var finalPayloadCreator = (0, _isNull2.default)(payloadCreator) ? _identity2.default : payloadCreator;

  var actionCreator = function actionCreator() {
    var hasError = (arguments.length <= 0 ? undefined : arguments[0]) instanceof Error;

    var action = {
      type: type
    };

    var payload = hasError ? arguments.length <= 0 ? undefined : arguments[0] : finalPayloadCreator.apply(undefined, arguments);
    if (!(0, _isUndefined2.default)(payload)) {
      action.payload = payload;
    }

    if (hasError || payload instanceof Error) {
      // Handle FSA errors where the payload is an Error object. Set error.
      action.error = true;
    }

    if ((0, _isFunction2.default)(metaCreator)) {
      action.meta = metaCreator.apply(undefined, arguments);
    }

    return action;
  };

  actionCreator.toString = function () {
    return type.toString();
  };

  return actionCreator;
}
```
- example usage
```shell
n/a
```



# <a name="apidoc.module.redux-actions.createActions"></a>[module redux-actions.createActions](#apidoc.module.redux-actions.createActions)

#### <a name="apidoc.element.redux-actions.createActions.default"></a>[function <span class="apidocSignatureSpan">redux-actions.createActions.</span>default (actionMap)](#apidoc.element.redux-actions.createActions.default)
- description and source-code
```javascript
function createActions(actionMap) {
  for (var _len = arguments.length, identityActions = Array(_len > 1 ? _len - 1 : 0), _key = 1; _key < _len; _key++) {
    identityActions[_key - 1] = arguments[_key];
  }

  function getFullOptions() {
    var partialOptions = (0, _isPlainObject2.default)((0, _last2.default)(identityActions)) ? identityActions.pop() : {};
    return (0, _defaults2.default)(partialOptions, { namespace: _namespaceActions.defaultNamespace });
  }

  var _getFullOptions = getFullOptions();

  var namespace = _getFullOptions.namespace;

  (0, _invariant2.default)(identityActions.every(_isString2.default) && ((0, _isString2.default)(actionMap) || (0, _isPlainObject2
.default)(actionMap)), 'Expected optional object followed by string action types');
  if ((0, _isString2.default)(actionMap)) {
    return actionCreatorsFromIdentityActions([actionMap].concat(identityActions));
  }
  return _extends({}, actionCreatorsFromActionMap(actionMap, namespace), actionCreatorsFromIdentityActions(identityActions));
}
```
- example usage
```shell
n/a
```



# <a name="apidoc.module.redux-actions.handleAction"></a>[module redux-actions.handleAction](#apidoc.module.redux-actions.handleAction)

#### <a name="apidoc.element.redux-actions.handleAction.default"></a>[function <span class="apidocSignatureSpan">redux-actions.handleAction.</span>default (type)](#apidoc.element.redux-actions.handleAction.default)
- description and source-code
```javascript
function handleAction(type) {
  var reducer = arguments.length <= 1 || arguments[1] === undefined ? _identity2.default : arguments[1];
  var defaultState = arguments[2];

  var types = type.toString().split(_combineActions.ACTION_TYPE_DELIMITER);
  (0, _invariant2.default)(!(0, _isUndefined2.default)(defaultState), 'defaultState for reducer handling ' + types.join(', ') + '
should be defined');
  (0, _invariant2.default)((0, _isFunction2.default)(reducer) || (0, _isPlainObject2.default)(reducer), 'Expected reducer to be
a function or object with next and throw reducers');

  var _ref = (0, _isFunction2.default)(reducer) ? [reducer, reducer] : [reducer.next, reducer.throw].map(function (aReducer) {
    return (0, _isNil2.default)(aReducer) ? _identity2.default : aReducer;
  });

  var _ref2 = _slicedToArray(_ref, 2);

  var nextReducer = _ref2[0];
  var throwReducer = _ref2[1];


  return function () {
    var state = arguments.length <= 0 || arguments[0] === undefined ? defaultState : arguments[0];
    var action = arguments[1];
    var actionType = action.type;

    if (!actionType || !(0, _includes2.default)(types, actionType.toString())) {
      return state;
    }

    return (action.error === true ? throwReducer : nextReducer)(state, action);
  };
}
```
- example usage
```shell
n/a
```



# <a name="apidoc.module.redux-actions.handleActions"></a>[module redux-actions.handleActions](#apidoc.module.redux-actions.handleActions)

#### <a name="apidoc.element.redux-actions.handleActions.default"></a>[function <span class="apidocSignatureSpan">redux-actions.handleActions.</span>default (handlers, defaultState)](#apidoc.element.redux-actions.handleActions.default)
- description and source-code
```javascript
function handleActions(handlers, defaultState) {
  var reducers = (0, _ownKeys2.default)(handlers).map(function (type) {
    return (0, _handleAction2.default)(type, handlers[type], defaultState);
  });
  var reducer = _reduceReducers2.default.apply(undefined, _toConsumableArray(reducers));
  return function (state, action) {
    return reducer(state, action);
  };
}
```
- example usage
```shell
n/a
```



# <a name="apidoc.module.redux-actions.namespaceActions"></a>[module redux-actions.namespaceActions](#apidoc.module.redux-actions.namespaceActions)

#### <a name="apidoc.element.redux-actions.namespaceActions.flattenActionMap"></a>[function <span class="apidocSignatureSpan">redux-actions.namespaceActions.</span>flattenActionMap (actionMap)](#apidoc.element.redux-actions.namespaceActions.flattenActionMap)
- description and source-code
```javascript
function flattenActionMap(actionMap) {
  var namespace = arguments.length <= 1 || arguments[1] === undefined ? defaultNamespace : arguments[1];
  var partialFlatActionMap = arguments.length <= 2 || arguments[2] === undefined ? {} : arguments[2];
  var partialFlatActionType = arguments.length <= 3 || arguments[3] === undefined ? '' : arguments[3];

  function connectNamespace(type) {
    return partialFlatActionType ? '' + partialFlatActionType + namespace + type : type;
  }

  Object.getOwnPropertyNames(actionMap).forEach(function (type) {
    var nextNamespace = connectNamespace(type);
    var actionMapValue = actionMap[type];

    if (!(0, _isPlainObject2.default)(actionMapValue)) {
      partialFlatActionMap[nextNamespace] = actionMap[type];
    } else {
      flattenActionMap(actionMap[type], namespace, partialFlatActionMap, nextNamespace);
    }
  });
  return partialFlatActionMap;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.redux-actions.namespaceActions.unflattenActionCreators"></a>[function <span class="apidocSignatureSpan">redux-actions.namespaceActions.</span>unflattenActionCreators (flatActionCreators)](#apidoc.element.redux-actions.namespaceActions.unflattenActionCreators)
- description and source-code
```javascript
function unflattenActionCreators(flatActionCreators) {
  var namespace = arguments.length <= 1 || arguments[1] === undefined ? defaultNamespace : arguments[1];

  function unflatten(flatActionType) {
    var partialNestedActionCreators = arguments.length <= 1 || arguments[1] === undefined ? {} : arguments[1];
    var partialFlatActionTypePath = arguments.length <= 2 || arguments[2] === undefined ? [] : arguments[2];

    var nextNamespace = (0, _camelCase2.default)(partialFlatActionTypePath.shift());
    if (partialFlatActionTypePath.length) {
      if (!partialNestedActionCreators[nextNamespace]) {
        partialNestedActionCreators[nextNamespace] = {};
      }
      unflatten(flatActionType, partialNestedActionCreators[nextNamespace], partialFlatActionTypePath);
    } else {
      partialNestedActionCreators[nextNamespace] = flatActionCreators[flatActionType];
    }
  }

  var partialNestedActionCreators = {};
  Object.getOwnPropertyNames(flatActionCreators).forEach(function (type) {
    return unflatten(type, partialNestedActionCreators, type.split(namespace));
  });
  return partialNestedActionCreators;
}
```
- example usage
```shell
n/a
```



# <a name="apidoc.module.redux-actions.ownKeys"></a>[module redux-actions.ownKeys](#apidoc.module.redux-actions.ownKeys)

#### <a name="apidoc.element.redux-actions.ownKeys.default"></a>[function <span class="apidocSignatureSpan">redux-actions.ownKeys.</span>default (object)](#apidoc.element.redux-actions.ownKeys.default)
- description and source-code
```javascript
function ownKeys(object) {
  if (typeof Reflect !== 'undefined' && typeof Reflect.ownKeys === 'function') {
    return Reflect.ownKeys(object);
  }

  var keys = Object.getOwnPropertyNames(object);

  if (typeof Object.getOwnPropertySymbols === 'function') {
    keys = keys.concat(Object.getOwnPropertySymbols(object));
  }

  return keys;
}
```
- example usage
```shell
n/a
```



# misc
- this document was created with [utility2](https://github.com/kaizhu256/node-utility2)
