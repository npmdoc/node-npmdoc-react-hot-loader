# api documentation for  [react-hot-loader (v1.3.1)](https://github.com/gaearon/react-hot-loader)  [![npm package](https://img.shields.io/npm/v/npmdoc-react-hot-loader.svg?style=flat-square)](https://www.npmjs.org/package/npmdoc-react-hot-loader) [![travis-ci.org build-status](https://api.travis-ci.org/npmdoc/node-npmdoc-react-hot-loader.svg)](https://travis-ci.org/npmdoc/node-npmdoc-react-hot-loader)
#### Tweak React components in real time.

[![NPM](https://nodei.co/npm/react-hot-loader.png?downloads=true)](https://www.npmjs.com/package/react-hot-loader)

[![apidoc](https://npmdoc.github.io/node-npmdoc-react-hot-loader/build/screenCapture.buildNpmdoc.browser._2Fhome_2Ftravis_2Fbuild_2Fnpmdoc_2Fnode-npmdoc-react-hot-loader_2Ftmp_2Fbuild_2Fapidoc.html.png)](https://npmdoc.github.io/node-npmdoc-react-hot-loader/build/apidoc.html)

![npmPackageListing](https://npmdoc.github.io/node-npmdoc-react-hot-loader/build/screenCapture.npmPackageListing.svg)

![npmPackageDependencyTree](https://npmdoc.github.io/node-npmdoc-react-hot-loader/build/screenCapture.npmPackageDependencyTree.svg)



# package.json

```json

{
    "author": {
        "name": "Dan Abramov"
    },
    "bugs": {
        "url": "https://github.com/gaearon/react-hot-loader/issues"
    },
    "dependencies": {
        "react-hot-api": "^0.4.5",
        "source-map": "^0.4.4"
    },
    "description": "Tweak React components in real time.",
    "devDependencies": {},
    "directories": {},
    "dist": {
        "shasum": "c95647ae78b73dfceff6ec71ffcb04182ff6daf9",
        "tarball": "https://registry.npmjs.org/react-hot-loader/-/react-hot-loader-1.3.1.tgz"
    },
    "gitHead": "34ee0dd3c0d9ebe996ffc42ecf66825b3e79ebe9",
    "homepage": "https://github.com/gaearon/react-hot-loader",
    "keywords": [
        "react",
        "javascript",
        "webpack",
        "hmr",
        "livereload",
        "live",
        "edit",
        "hot",
        "loader",
        "reload"
    ],
    "license": "MIT",
    "main": "index.js",
    "maintainers": [
        {
            "name": "calesce",
            "email": "newman.cale@gmail.com"
        },
        {
            "name": "gaearon",
            "email": "dan.abramov@gmail.com"
        }
    ],
    "name": "react-hot-loader",
    "optionalDependencies": {},
    "readme": "ERROR: No README data found!",
    "repository": {
        "type": "git",
        "url": "git+https://github.com/gaearon/react-hot-loader.git"
    },
    "scripts": {},
    "version": "1.3.1"
}
```



# <a name="apidoc.tableOfContents"></a>[table of contents](#apidoc.tableOfContents)

#### [module react-hot-loader](#apidoc.module.react-hot-loader)
1.  object <span class="apidocSignatureSpan">react-hot-loader.</span>RootInstanceProvider

#### [module react-hot-loader.RootInstanceProvider](#apidoc.module.react-hot-loader.RootInstanceProvider)
1.  [function <span class="apidocSignatureSpan">react-hot-loader.RootInstanceProvider.</span>getRootInstances (ReactMount)](#apidoc.element.react-hot-loader.RootInstanceProvider.getRootInstances)
1.  object <span class="apidocSignatureSpan">react-hot-loader.RootInstanceProvider.</span>injection



# <a name="apidoc.module.react-hot-loader"></a>[module react-hot-loader](#apidoc.module.react-hot-loader)



# <a name="apidoc.module.react-hot-loader.RootInstanceProvider"></a>[module react-hot-loader.RootInstanceProvider](#apidoc.module.react-hot-loader.RootInstanceProvider)

#### <a name="apidoc.element.react-hot-loader.RootInstanceProvider.getRootInstances"></a>[function <span class="apidocSignatureSpan">react-hot-loader.RootInstanceProvider.</span>getRootInstances (ReactMount)](#apidoc.element.react-hot-loader.RootInstanceProvider.getRootInstances)
- description and source-code
```javascript
getRootInstances = function (ReactMount) {
  if (injectedProvider) {
    return injectedProvider.getRootInstances();
  }

  var instances = ReactMount && getRootInstancesFromReactMount(ReactMount) || [];
  if (!Object.keys(instances).length) {
    warnOnce();
  }

  return instances;
}
```
- example usage
```shell
...
    '(function () {',
      'var ReactHotAPI = require(' + JSON.stringify(require.resolve('react-hot-api')) + '),',
          'RootInstanceProvider = require(' + JSON.stringify(require.resolve('./RootInstanceProvider')) + '),',
          reactMountImport,
          'React = require("react");',

      'module.makeHot = module.hot.data ? module.hot.data.makeHot : ReactHotAPI(function () {',
        'return RootInstanceProvider.getRootInstances(ReactMount);',
      '}, React);',
    '})();',
  '}',
  'try {',
    '(function () {',
].join(' ');
...
```



# misc
- this document was created with [utility2](https://github.com/kaizhu256/node-utility2)
