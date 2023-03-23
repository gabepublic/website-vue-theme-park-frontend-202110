# Innovator Island Front End Application

Lesson Website: 
- https://serverlessland.com/learn/innovator-island#
- https://eventbox.dev/published/lesson/innovator-island
- Original src: https://innovator-island.s3-us-west-2.amazonaws.com/front-end/theme-park-frontend-202110.zip

## Prerequisite

- Nodejs version v16.16.0, otherwise see error below in TROUBLESHOOTING

## Project setup
```
npm install
```

### Compiles and hot-reloads for development
```
npm run serve
```

### Compiles and minifies for production
```
npm run build
```

### Lints and fixes files
```
npm run lint
```

### Customize configuration
See [Configuration Reference](https://cli.vuejs.org/config/).

## RUN
```
$ npm run serve

> innovator-island-frontend@1.0.0 serve
> vue-cli-service serve

 INFO  Starting development server...
98% after emitting CopyPlugin

 DONE  Compiled successfully in 116355ms                                                                                                        10:43:24 PM

  App running at:
  - Local:   http://localhost:8080/ 
  - Network: http://172.19.183.38:8080/

  Note that the development build is not optimized.
  To create a production build, run npm run build.

```


## TROUBLESHOOTING

- Error when using nodejs version `18.12.*`
  Source: https://www.freecodecamp.org/news/error-error-0308010c-digital-envelope-routines-unsupported-node-error-solved/
```
$ npm run serve

> innovator-island-frontend@1.0.0 serve
> vue-cli-service serve

Browserslist: caniuse-lite is outdated. Please run:
  npx browserslist@latest --update-db
  Why you should do it regularly: https://github.com/browserslist/browserslist#browsers-data-updating
 INFO  Starting development server...
10% building 2/2 modules 0 activeError: error:0308010C:digital envelope routines::unsupported
    at new Hash (node:internal/crypto/hash:71:19)
    at Object.createHash (node:crypto:133:10)
    at module.exports (/mnt/c/zWSL/samples/theme-park-frontend-202110/node_modules/webpack/lib/util/createHash.js:135:53)
    at NormalModule._initBuildHash (/mnt/c/zWSL/samples/theme-park-frontend-202110/node_modules/webpack/lib/NormalModule.js:417:16)
    at handleParseError (/mnt/c/zWSL/samples/theme-park-frontend-202110/node_modules/webpack/lib/NormalModule.js:471:10)
    at /mnt/c/zWSL/samples/theme-park-frontend-202110/node_modules/webpack/lib/NormalModule.js:503:5
    at /mnt/c/zWSL/samples/theme-park-frontend-202110/node_modules/webpack/lib/NormalModule.js:358:12
    at /mnt/c/zWSL/samples/theme-park-frontend-202110/node_modules/loader-runner/lib/LoaderRunner.js:373:3
    at iterateNormalLoaders (/mnt/c/zWSL/samples/theme-park-frontend-202110/node_modules/loader-runner/lib/LoaderRunner.js:214:10)
    at iterateNormalLoaders (/mnt/c/zWSL/samples/theme-park-frontend-202110/node_modules/loader-runner/lib/LoaderRunner.js:221:10)
    at /mnt/c/zWSL/samples/theme-park-frontend-202110/node_modules/loader-runner/lib/LoaderRunner.js:236:3
    at runSyncOrAsync (/mnt/c/zWSL/samples/theme-park-frontend-202110/node_modules/loader-runner/lib/LoaderRunner.js:130:11)
    at iterateNormalLoaders (/mnt/c/zWSL/samples/theme-park-frontend-202110/node_modules/loader-runner/lib/LoaderRunner.js:232:2)
    at Array.<anonymous> (/mnt/c/zWSL/samples/theme-park-frontend-202110/node_modules/loader-runner/lib/LoaderRunner.js:205:4)
    at Storage.finished (/mnt/c/zWSL/samples/theme-park-frontend-202110/node_modules/enhanced-resolve/lib/CachedInputFileSystem.js:55:16)
    at /mnt/c/zWSL/samples/theme-park-frontend-202110/node_modules/enhanced-resolve/lib/CachedInputFileSystem.js:91:9
10% building 2/4 modules 2 active ...-park-frontend-202110/node_modules/webpack-dev-server/client/index.js?http://172.19.183.38:8080&sockPath=/sockjs-nodenode:internal/crypto/hash:71
  this[kHandle] = new _Hash(algorithm, xofLen);
                  ^

Error: error:0308010C:digital envelope routines::unsupported
    at new Hash (node:internal/crypto/hash:71:19)
    at Object.createHash (node:crypto:133:10)
    at module.exports (/mnt/c/zWSL/samples/theme-park-frontend-202110/node_modules/webpack/lib/util/createHash.js:135:53)
    at NormalModule._initBuildHash (/mnt/c/zWSL/samples/theme-park-frontend-202110/node_modules/webpack/lib/NormalModule.js:417:16)
    at handleParseError (/mnt/c/zWSL/samples/theme-park-frontend-202110/node_modules/webpack/lib/NormalModule.js:471:10)
    at /mnt/c/zWSL/samples/theme-park-frontend-202110/node_modules/webpack/lib/NormalModule.js:503:5
    at /mnt/c/zWSL/samples/theme-park-frontend-202110/node_modules/webpack/lib/NormalModule.js:358:12
    at /mnt/c/zWSL/samples/theme-park-frontend-202110/node_modules/loader-runner/lib/LoaderRunner.js:373:3
    at iterateNormalLoaders (/mnt/c/zWSL/samples/theme-park-frontend-202110/node_modules/loader-runner/lib/LoaderRunner.js:214:10)
    at Array.<anonymous> (/mnt/c/zWSL/samples/theme-park-frontend-202110/node_modules/loader-runner/lib/LoaderRunner.js:205:4)
    at Storage.finished (/mnt/c/zWSL/samples/theme-park-frontend-202110/node_modules/enhanced-resolve/lib/CachedInputFileSystem.js:55:16)
    at /mnt/c/zWSL/samples/theme-park-frontend-202110/node_modules/enhanced-resolve/lib/CachedInputFileSystem.js:91:9
    at /mnt/c/zWSL/samples/theme-park-frontend-202110/node_modules/graceful-fs/graceful-fs.js:123:16
    at FSReqCallback.readFileAfterClose [as oncomplete] (node:internal/fs/read_file_context:68:3) {
  opensslErrorStack: [ 'error:03000086:digital envelope routines::initialization error' ],
  library: 'digital envelope routines',
  reason: 'unsupported',
  code: 'ERR_OSSL_EVP_UNSUPPORTED'
}

Node.js v18.12.0
```