# api documentation for  [anyproxy (v3.10.4)](https://github.com/alibaba/anyproxy#readme)  [![npm package](https://img.shields.io/npm/v/npmdoc-anyproxy.svg?style=flat-square)](https://www.npmjs.org/package/npmdoc-anyproxy) [![travis-ci.org build-status](https://api.travis-ci.org/npmdoc/node-npmdoc-anyproxy.svg)](https://travis-ci.org/npmdoc/node-npmdoc-anyproxy)
#### A fully configurable proxy in NodeJS, which can handle HTTPS requests perfectly.

[![NPM](https://nodei.co/npm/anyproxy.png?downloads=true)](https://www.npmjs.com/package/anyproxy)

[![apidoc](https://npmdoc.github.io/node-npmdoc-anyproxy/build/screenCapture.buildNpmdoc.browser.%252Fhome%252Ftravis%252Fbuild%252Fnpmdoc%252Fnode-npmdoc-anyproxy%252Ftmp%252Fbuild%252Fapidoc.html.png)](https://npmdoc.github.io/node-npmdoc-anyproxy/build/apidoc.html)

![npmPackageListing](https://npmdoc.github.io/node-npmdoc-anyproxy/build/screenCapture.npmPackageListing.svg)

![npmPackageDependencyTree](https://npmdoc.github.io/node-npmdoc-anyproxy/build/screenCapture.npmPackageDependencyTree.svg)



# package.json

```json

{
    "name": "anyproxy",
    "version": "3.10.4",
    "description": "A fully configurable proxy in NodeJS, which can handle HTTPS requests perfectly.",
    "main": "proxy.js",
    "bin": {
        "anyproxy": "bin.js"
    },
    "dependencies": {
        "async": "~0.9.0",
        "async-task-mgr": ">=1.1.0",
        "body-parser": "^1.13.1",
        "change-case": "^3.0.0",
        "colorful": "^2.1.0",
        "commander": "~2.3.0",
        "compression": "^1.4.4",
        "express": "^4.8.5",
        "iconv-lite": "^0.4.6",
        "ip": "^0.3.2",
        "juicer": "^0.6.6-stable",
        "mime-types": "2.1.11",
        "nedb": "^0.11.0",
        "node-easy-cert": "^1.0.0",
        "node-forge": "^0.6.39",
        "npm": "^2.7.0",
        "promise": "^7.0.4",
        "qrcode-npm": "0.0.3",
        "stream-throttle": "^0.1.3",
        "ws": "^1.1.0"
    },
    "devDependencies": {
        "babel-polyfill": "^6.13.0",
        "babel-preset-es2015": "^6.13.2",
        "babel-preset-stage-0": "^6.5.0",
        "babel-register": "^6.11.6",
        "https-proxy-agent": "^1.0.0",
        "jasmine": "^2.4.1",
        "koa": "^1.2.1",
        "koa-body": "^1.4.0",
        "koa-router": "^5.4.0",
        "koa-send": "^3.2.0",
        "koa-websocket": "^2.0.0",
        "nodeunit": "^0.9.1",
        "request": "^2.74.0",
        "stream-equal": "0.1.8"
    },
    "scripts": {
        "test": "sh test/test.sh",
        "testserver": "node test/server/startServer.js"
    },
    "repository": {
        "type": "git",
        "url": "git+https://github.com/alibaba/anyproxy.git"
    },
    "author": {
        "name": "ottomao@gmail.com"
    },
    "license": "ISC",
    "gitHead": "26a05e8c5c7b6173811320e3dc20ac9aed61b494",
    "bugs": {
        "url": "https://github.com/alibaba/anyproxy/issues"
    },
    "homepage": "https://github.com/alibaba/anyproxy#readme",
    "dist": {
        "shasum": "930d286ca071515c19787086cc036f64d9667376",
        "tarball": "https://registry.npmjs.org/anyproxy/-/anyproxy-3.10.4.tgz"
    },
    "maintainers": [
        {
            "name": "ottomao",
            "email": "ottomao@gmail.com"
        },
        {
            "name": "alexyan",
            "email": "5918760@gmail.com"
        }
    ],
    "directories": {},
    "readme": "ERROR: No README data found!"
}
```



# <a name="apidoc.tableOfContents"></a>[table of contents](#apidoc.tableOfContents)

#### [module anyproxy](#apidoc.module.anyproxy)
1.  [function <span class="apidocSignatureSpan">anyproxy.</span>generateRootCA (cb)](#apidoc.element.anyproxy.generateRootCA)
1.  [function <span class="apidocSignatureSpan">anyproxy.</span>isRootCAFileExists ()](#apidoc.element.anyproxy.isRootCAFileExists)
1.  [function <span class="apidocSignatureSpan">anyproxy.</span>proxyServer (option)](#apidoc.element.anyproxy.proxyServer)
1.  [function <span class="apidocSignatureSpan">anyproxy.</span>recorder (option)](#apidoc.element.anyproxy.recorder)
1.  [function <span class="apidocSignatureSpan">anyproxy.</span>setRules (newRule)](#apidoc.element.anyproxy.setRules)
1.  [function <span class="apidocSignatureSpan">anyproxy.</span>webInterface (config)](#apidoc.element.anyproxy.webInterface)
1.  [function <span class="apidocSignatureSpan">anyproxy.</span>wsServer (config)](#apidoc.element.anyproxy.wsServer)
1.  object <span class="apidocSignatureSpan">anyproxy.</span>certGenerator
1.  object <span class="apidocSignatureSpan">anyproxy.</span>certMgr
1.  object <span class="apidocSignatureSpan">anyproxy.</span>requestHandler
1.  object <span class="apidocSignatureSpan">anyproxy.</span>rule__blank
1.  object <span class="apidocSignatureSpan">anyproxy.</span>rule_adjust_response_time
1.  object <span class="apidocSignatureSpan">anyproxy.</span>rule_allow_CORS
1.  object <span class="apidocSignatureSpan">anyproxy.</span>rule_default
1.  object <span class="apidocSignatureSpan">anyproxy.</span>rule_intercept_some_https_requests
1.  object <span class="apidocSignatureSpan">anyproxy.</span>rule_remove_cache_header
1.  object <span class="apidocSignatureSpan">anyproxy.</span>rule_replace_request_option
1.  object <span class="apidocSignatureSpan">anyproxy.</span>rule_replace_response_data
1.  object <span class="apidocSignatureSpan">anyproxy.</span>rule_replace_response_status_code
1.  object <span class="apidocSignatureSpan">anyproxy.</span>rule_use_local_data
1.  object <span class="apidocSignatureSpan">anyproxy.</span>systemProxyMgr
1.  object <span class="apidocSignatureSpan">anyproxy.</span>util
1.  object <span class="apidocSignatureSpan">anyproxy.</span>wsServer.prototype

#### [module anyproxy.certGenerator](#apidoc.module.anyproxy.certGenerator)
1.  [function <span class="apidocSignatureSpan">anyproxy.certGenerator.</span>generateCertsForHostname (domain, rootCAConfig)](#apidoc.element.anyproxy.certGenerator.generateCertsForHostname)
1.  [function <span class="apidocSignatureSpan">anyproxy.certGenerator.</span>generateRootCA ()](#apidoc.element.anyproxy.certGenerator.generateRootCA)

#### [module anyproxy.certMgr](#apidoc.module.anyproxy.certMgr)
1.  [function <span class="apidocSignatureSpan">anyproxy.certMgr.</span>clearCerts (cb)](#apidoc.element.anyproxy.certMgr.clearCerts)
1.  [function <span class="apidocSignatureSpan">anyproxy.certMgr.</span>generateRootCA (cb)](#apidoc.element.anyproxy.certMgr.generateRootCA)
1.  [function <span class="apidocSignatureSpan">anyproxy.certMgr.</span>getCertificate (host, cb)](#apidoc.element.anyproxy.certMgr.getCertificate)
1.  [function <span class="apidocSignatureSpan">anyproxy.certMgr.</span>getRootCAFilePath ()](#apidoc.element.anyproxy.certMgr.getRootCAFilePath)
1.  [function <span class="apidocSignatureSpan">anyproxy.certMgr.</span>getRootDirPath ()](#apidoc.element.anyproxy.certMgr.getRootDirPath)
1.  [function <span class="apidocSignatureSpan">anyproxy.certMgr.</span>ifRootCATrusted (callback)](#apidoc.element.anyproxy.certMgr.ifRootCATrusted)
1.  [function <span class="apidocSignatureSpan">anyproxy.certMgr.</span>isRootCAFileExists ()](#apidoc.element.anyproxy.certMgr.isRootCAFileExists)

#### [module anyproxy.recorder](#apidoc.module.anyproxy.recorder)
1.  [function <span class="apidocSignatureSpan">anyproxy.</span>recorder (option)](#apidoc.element.anyproxy.recorder.recorder)
1.  [function <span class="apidocSignatureSpan">anyproxy.recorder.</span>super_ ()](#apidoc.element.anyproxy.recorder.super_)

#### [module anyproxy.requestHandler](#apidoc.module.anyproxy.requestHandler)
1.  [function <span class="apidocSignatureSpan">anyproxy.requestHandler.</span>connectReqHandler (req, socket, head)](#apidoc.element.anyproxy.requestHandler.connectReqHandler)
1.  [function <span class="apidocSignatureSpan">anyproxy.requestHandler.</span>getRuleSummary ()](#apidoc.element.anyproxy.requestHandler.getRuleSummary)
1.  [function <span class="apidocSignatureSpan">anyproxy.requestHandler.</span>setRules (newRule)](#apidoc.element.anyproxy.requestHandler.setRules)
1.  [function <span class="apidocSignatureSpan">anyproxy.requestHandler.</span>userRequestHandler (req, userRes)](#apidoc.element.anyproxy.requestHandler.userRequestHandler)
1.  number <span class="apidocSignatureSpan">anyproxy.requestHandler.</span>token

#### [module anyproxy.rule__blank](#apidoc.module.anyproxy.rule__blank)
1.  [function <span class="apidocSignatureSpan">anyproxy.rule__blank.</span>dealLocalResponse (req, reqBody, callback)](#apidoc.element.anyproxy.rule__blank.dealLocalResponse)
1.  [function <span class="apidocSignatureSpan">anyproxy.rule__blank.</span>pauseBeforeSendingResponse (req, res)](#apidoc.element.anyproxy.rule__blank.pauseBeforeSendingResponse)
1.  [function <span class="apidocSignatureSpan">anyproxy.rule__blank.</span>replaceRequestData (req, data)](#apidoc.element.anyproxy.rule__blank.replaceRequestData)
1.  [function <span class="apidocSignatureSpan">anyproxy.rule__blank.</span>replaceRequestOption (req, option)](#apidoc.element.anyproxy.rule__blank.replaceRequestOption)
1.  [function <span class="apidocSignatureSpan">anyproxy.rule__blank.</span>replaceRequestProtocol (req, protocol)](#apidoc.element.anyproxy.rule__blank.replaceRequestProtocol)
1.  [function <span class="apidocSignatureSpan">anyproxy.rule__blank.</span>replaceResponseHeader (req, res, header)](#apidoc.element.anyproxy.rule__blank.replaceResponseHeader)
1.  [function <span class="apidocSignatureSpan">anyproxy.rule__blank.</span>replaceResponseStatusCode (req, res, statusCode)](#apidoc.element.anyproxy.rule__blank.replaceResponseStatusCode)
1.  [function <span class="apidocSignatureSpan">anyproxy.rule__blank.</span>replaceServerResDataAsync (req, res, serverResData, callback)](#apidoc.element.anyproxy.rule__blank.replaceServerResDataAsync)
1.  [function <span class="apidocSignatureSpan">anyproxy.rule__blank.</span>shouldInterceptHttpsReq (req)](#apidoc.element.anyproxy.rule__blank.shouldInterceptHttpsReq)
1.  [function <span class="apidocSignatureSpan">anyproxy.rule__blank.</span>shouldUseLocalResponse (req, reqBody)](#apidoc.element.anyproxy.rule__blank.shouldUseLocalResponse)
1.  [function <span class="apidocSignatureSpan">anyproxy.rule__blank.</span>summary ()](#apidoc.element.anyproxy.rule__blank.summary)

#### [module anyproxy.rule_adjust_response_time](#apidoc.module.anyproxy.rule_adjust_response_time)
1.  [function <span class="apidocSignatureSpan">anyproxy.rule_adjust_response_time.</span>pauseBeforeSendingResponse (req, res)](#apidoc.element.anyproxy.rule_adjust_response_time.pauseBeforeSendingResponse)

#### [module anyproxy.rule_allow_CORS](#apidoc.module.anyproxy.rule_allow_CORS)
1.  [function <span class="apidocSignatureSpan">anyproxy.rule_allow_CORS.</span>dealLocalResponse (req, reqBody, callback)](#apidoc.element.anyproxy.rule_allow_CORS.dealLocalResponse)
1.  [function <span class="apidocSignatureSpan">anyproxy.rule_allow_CORS.</span>replaceResponseHeader (req, res, header)](#apidoc.element.anyproxy.rule_allow_CORS.replaceResponseHeader)
1.  [function <span class="apidocSignatureSpan">anyproxy.rule_allow_CORS.</span>shouldUseLocalResponse (req, reqBody)](#apidoc.element.anyproxy.rule_allow_CORS.shouldUseLocalResponse)

#### [module anyproxy.rule_default](#apidoc.module.anyproxy.rule_default)
1.  [function <span class="apidocSignatureSpan">anyproxy.rule_default.</span>_getCustomMenu ()](#apidoc.element.anyproxy.rule_default._getCustomMenu)
1.  [function <span class="apidocSignatureSpan">anyproxy.rule_default.</span>_plugIntoWebinterface (app, cb)](#apidoc.element.anyproxy.rule_default._plugIntoWebinterface)
1.  [function <span class="apidocSignatureSpan">anyproxy.rule_default.</span>dealLocalResponse (req, reqBody, callback)](#apidoc.element.anyproxy.rule_default.dealLocalResponse)
1.  [function <span class="apidocSignatureSpan">anyproxy.rule_default.</span>fetchTrafficData (id, info)](#apidoc.element.anyproxy.rule_default.fetchTrafficData)
1.  [function <span class="apidocSignatureSpan">anyproxy.rule_default.</span>pauseBeforeSendingResponse (req, res)](#apidoc.element.anyproxy.rule_default.pauseBeforeSendingResponse)
1.  [function <span class="apidocSignatureSpan">anyproxy.rule_default.</span>replaceRequestData (req, data)](#apidoc.element.anyproxy.rule_default.replaceRequestData)
1.  [function <span class="apidocSignatureSpan">anyproxy.rule_default.</span>replaceRequestOption (req, option)](#apidoc.element.anyproxy.rule_default.replaceRequestOption)
1.  [function <span class="apidocSignatureSpan">anyproxy.rule_default.</span>replaceRequestProtocol (req, protocol)](#apidoc.element.anyproxy.rule_default.replaceRequestProtocol)
1.  [function <span class="apidocSignatureSpan">anyproxy.rule_default.</span>replaceResponseHeader (req, res, header)](#apidoc.element.anyproxy.rule_default.replaceResponseHeader)
1.  [function <span class="apidocSignatureSpan">anyproxy.rule_default.</span>replaceResponseStatusCode (req, res, statusCode)](#apidoc.element.anyproxy.rule_default.replaceResponseStatusCode)
1.  [function <span class="apidocSignatureSpan">anyproxy.rule_default.</span>replaceServerResDataAsync (req, res, serverResData, callback)](#apidoc.element.anyproxy.rule_default.replaceServerResDataAsync)
1.  [function <span class="apidocSignatureSpan">anyproxy.rule_default.</span>setInterceptFlag (flag)](#apidoc.element.anyproxy.rule_default.setInterceptFlag)
1.  [function <span class="apidocSignatureSpan">anyproxy.rule_default.</span>shouldInterceptHttpsReq (req)](#apidoc.element.anyproxy.rule_default.shouldInterceptHttpsReq)
1.  [function <span class="apidocSignatureSpan">anyproxy.rule_default.</span>shouldUseLocalResponse (req, reqBody)](#apidoc.element.anyproxy.rule_default.shouldUseLocalResponse)
1.  [function <span class="apidocSignatureSpan">anyproxy.rule_default.</span>summary ()](#apidoc.element.anyproxy.rule_default.summary)
1.  number <span class="apidocSignatureSpan">anyproxy.rule_default.</span>token

#### [module anyproxy.rule_intercept_some_https_requests](#apidoc.module.anyproxy.rule_intercept_some_https_requests)
1.  [function <span class="apidocSignatureSpan">anyproxy.rule_intercept_some_https_requests.</span>replaceServerResDataAsync (req, res, serverResData, callback)](#apidoc.element.anyproxy.rule_intercept_some_https_requests.replaceServerResDataAsync)
1.  [function <span class="apidocSignatureSpan">anyproxy.rule_intercept_some_https_requests.</span>shouldInterceptHttpsReq (req)](#apidoc.element.anyproxy.rule_intercept_some_https_requests.shouldInterceptHttpsReq)

#### [module anyproxy.rule_remove_cache_header](#apidoc.module.anyproxy.rule_remove_cache_header)
1.  [function <span class="apidocSignatureSpan">anyproxy.rule_remove_cache_header.</span>replaceRequestOption (req, option)](#apidoc.element.anyproxy.rule_remove_cache_header.replaceRequestOption)
1.  [function <span class="apidocSignatureSpan">anyproxy.rule_remove_cache_header.</span>replaceResponseHeader (req, res, header)](#apidoc.element.anyproxy.rule_remove_cache_header.replaceResponseHeader)

#### [module anyproxy.rule_replace_request_option](#apidoc.module.anyproxy.rule_replace_request_option)
1.  [function <span class="apidocSignatureSpan">anyproxy.rule_replace_request_option.</span>replaceRequestOption (req, option)](#apidoc.element.anyproxy.rule_replace_request_option.replaceRequestOption)

#### [module anyproxy.rule_replace_response_data](#apidoc.module.anyproxy.rule_replace_response_data)
1.  [function <span class="apidocSignatureSpan">anyproxy.rule_replace_response_data.</span>replaceServerResDataAsync (req, res, serverResData, callback)](#apidoc.element.anyproxy.rule_replace_response_data.replaceServerResDataAsync)

#### [module anyproxy.rule_replace_response_status_code](#apidoc.module.anyproxy.rule_replace_response_status_code)
1.  [function <span class="apidocSignatureSpan">anyproxy.rule_replace_response_status_code.</span>replaceResponseHeader (req, res, header)](#apidoc.element.anyproxy.rule_replace_response_status_code.replaceResponseHeader)
1.  [function <span class="apidocSignatureSpan">anyproxy.rule_replace_response_status_code.</span>replaceResponseStatusCode (req, res, statusCode)](#apidoc.element.anyproxy.rule_replace_response_status_code.replaceResponseStatusCode)

#### [module anyproxy.rule_use_local_data](#apidoc.module.anyproxy.rule_use_local_data)
1.  [function <span class="apidocSignatureSpan">anyproxy.rule_use_local_data.</span>dealLocalResponse (req, reqBody, callback)](#apidoc.element.anyproxy.rule_use_local_data.dealLocalResponse)
1.  [function <span class="apidocSignatureSpan">anyproxy.rule_use_local_data.</span>shouldUseLocalResponse (req, reqBody)](#apidoc.element.anyproxy.rule_use_local_data.shouldUseLocalResponse)
1.  [function <span class="apidocSignatureSpan">anyproxy.rule_use_local_data.</span>summary ()](#apidoc.element.anyproxy.rule_use_local_data.summary)

#### [module anyproxy.systemProxyMgr](#apidoc.module.anyproxy.systemProxyMgr)
1.  [function <span class="apidocSignatureSpan">anyproxy.systemProxyMgr.</span>disableGlobalProxy (proxyType)](#apidoc.element.anyproxy.systemProxyMgr.disableGlobalProxy)
1.  [function <span class="apidocSignatureSpan">anyproxy.systemProxyMgr.</span>enableGlobalProxy (ip, port, proxyType)](#apidoc.element.anyproxy.systemProxyMgr.enableGlobalProxy)
1.  [function <span class="apidocSignatureSpan">anyproxy.systemProxyMgr.</span>getNetworkType ()](#apidoc.element.anyproxy.systemProxyMgr.getNetworkType)
1.  [function <span class="apidocSignatureSpan">anyproxy.systemProxyMgr.</span>getProxyState ()](#apidoc.element.anyproxy.systemProxyMgr.getProxyState)

#### [module anyproxy.util](#apidoc.module.anyproxy.util)
1.  [function <span class="apidocSignatureSpan">anyproxy.util.</span>clearCacheDir (cb)](#apidoc.element.anyproxy.util.clearCacheDir)
1.  [function <span class="apidocSignatureSpan">anyproxy.util.</span>contentLength (filepath)](#apidoc.element.anyproxy.util.contentLength)
1.  [function <span class="apidocSignatureSpan">anyproxy.util.</span>contentType (filepath)](#apidoc.element.anyproxy.util.contentType)
1.  [function <span class="apidocSignatureSpan">anyproxy.util.</span>filewalker (root, cb)](#apidoc.element.anyproxy.util.filewalker)
1.  [function <span class="apidocSignatureSpan">anyproxy.util.</span>freshRequire (path)](#apidoc.element.anyproxy.util.freshRequire)
1.  [function <span class="apidocSignatureSpan">anyproxy.util.</span>generateCacheDir ()](#apidoc.element.anyproxy.util.generateCacheDir)
1.  [function <span class="apidocSignatureSpan">anyproxy.util.</span>getAnyProxyHome ()](#apidoc.element.anyproxy.util.getAnyProxyHome)
1.  [function <span class="apidocSignatureSpan">anyproxy.util.</span>getUserHome ()](#apidoc.element.anyproxy.util.getUserHome)
1.  [function <span class="apidocSignatureSpan">anyproxy.util.</span>lower_keys (obj)](#apidoc.element.anyproxy.util.lower_keys)
1.  [function <span class="apidocSignatureSpan">anyproxy.util.</span>merge (baseObj, extendObj)](#apidoc.element.anyproxy.util.merge)
1.  [function <span class="apidocSignatureSpan">anyproxy.util.</span>showRootInstallTip ()](#apidoc.element.anyproxy.util.showRootInstallTip)
1.  [function <span class="apidocSignatureSpan">anyproxy.util.</span>simpleRender (str, object, regexp)](#apidoc.element.anyproxy.util.simpleRender)
1.  [function <span class="apidocSignatureSpan">anyproxy.util.</span>upper_keys (obj)](#apidoc.element.anyproxy.util.upper_keys)

#### [module anyproxy.webInterface](#apidoc.module.anyproxy.webInterface)
1.  [function <span class="apidocSignatureSpan">anyproxy.</span>webInterface (config)](#apidoc.element.anyproxy.webInterface.webInterface)
1.  [function <span class="apidocSignatureSpan">anyproxy.webInterface.</span>super_ ()](#apidoc.element.anyproxy.webInterface.super_)

#### [module anyproxy.wsServer](#apidoc.module.anyproxy.wsServer)
1.  [function <span class="apidocSignatureSpan">anyproxy.</span>wsServer (config)](#apidoc.element.anyproxy.wsServer.wsServer)

#### [module anyproxy.wsServer.prototype](#apidoc.module.anyproxy.wsServer.prototype)
1.  [function <span class="apidocSignatureSpan">anyproxy.wsServer.prototype.</span>closeAll ()](#apidoc.element.anyproxy.wsServer.prototype.closeAll)



# <a name="apidoc.module.anyproxy"></a>[module anyproxy](#apidoc.module.anyproxy)

#### <a name="apidoc.element.anyproxy.generateRootCA"></a>[function <span class="apidocSignatureSpan">anyproxy.</span>generateRootCA (cb)](#apidoc.element.anyproxy.generateRootCA)
- description and source-code
```javascript
generateRootCA = function (cb) {
    doGenerate(false);

    function doGenerate(overwrite) {
        const rootOptions = {
            commonName: 'AnyProxy',
            overwrite: !!overwrite
        };

        easyCert.generateRootCA(rootOptions, (error, keyPath, crtPath) => {
            if (!error) {
                const certDir = path.dirname(keyPath);
                logUtil.printLog(color.cyan('The cert is generated at "' + certDir + '"'));
                if(isWin){
                    exec("start .",{ cwd : certDir });
                }else{
                    exec("open .",{ cwd : certDir });
                }
            }

            if (error === 'ROOT_CA_EXISTED') {
                var rl = readline.createInterface({
                    input : process.stdin,
                    output: process.stdout
                });

                rl.question("do you really want to generate a new one ?)(yes/NO)", function(answer) {
                    if(/yes/i.test(answer)){
                        doGenerate(true);
                    }else{
                        console.log("will not generate a new one");

                    }
                    rl.close();
                });

                return;
            }
            cb(error, keyPath, crtPath);
        });
    }

}
```
- example usage
```shell
...
'''

'''javascript
var proxy = require("anyproxy");

//create cert when you want to use https features
//please manually trust this rootCA when it is the first time you run it
!proxy.isRootCAFileExists() && proxy.generateRootCA();

var options = {
type          : "http",
port          : 8001,
hostname      : "localhost",
rule          : require("path/to/my/ruleModule.js"),
dbFile        : null,  // optional, save request data to a specified file, will use in-memory db if not specified
...
```

#### <a name="apidoc.element.anyproxy.isRootCAFileExists"></a>[function <span class="apidocSignatureSpan">anyproxy.</span>isRootCAFileExists ()](#apidoc.element.anyproxy.isRootCAFileExists)
- description and source-code
```javascript
function isRootCAFileExists() {
  return (fs.existsSync(rootCAcrtFilePath) && fs.existsSync(rootCAkeyFilePath));
}
```
- example usage
```shell
...
'''

'''javascript
var proxy = require("anyproxy");

//create cert when you want to use https features
//please manually trust this rootCA when it is the first time you run it
!proxy.isRootCAFileExists() && proxy.generateRootCA();

var options = {
type          : "http",
port          : 8001,
hostname      : "localhost",
rule          : require("path/to/my/ruleModule.js"),
dbFile        : null,  // optional, save request data to a specified file, will use in-memory db if not specified
...
```

#### <a name="apidoc.element.anyproxy.proxyServer"></a>[function <span class="apidocSignatureSpan">anyproxy.</span>proxyServer (option)](#apidoc.element.anyproxy.proxyServer)
- description and source-code
```javascript
function proxyServer(option){
    option = option || {};

    var self       = this,
        proxyType           = /https/i.test(option.type || DEFAULT_TYPE) ? T_TYPE_HTTPS : T_TYPE_HTTP ,
        proxyPort           = option.port     || DEFAULT_PORT,
        proxyHost           = option.hostname || DEFAULT_HOST,
        proxyRules          = option.rule     || default_rule,
        proxyWebPort        = option.webPort       || DEFAULT_WEB_PORT,       //port for web interface
        socketPort          = option.socketPort    || DEFAULT_WEBSOCKET_PORT, //port for websocket
        proxyConfigPort     = option.webConfigPort || DEFAULT_CONFIG_PORT,    //port to ui config server
        disableWebInterface = !!option.disableWebInterface,
        ifSilent            = !!option.silent;

    if(ifSilent){
        logUtil.setPrintStatus(false);
    }

    // copy the rule to keep the original proxyRules independent
    proxyRules = Object.assign({}, proxyRules);

    var currentRule = requestHandler.setRules(proxyRules); //TODO : optimize calling for set rule

    if(!!option.interceptHttps){
        if (!certMgr.isRootCAFileExists()) {
            util.showRootInstallTip();
            process.exit(0);
            return;
        }

        currentRule.setInterceptFlag(true);

        //print a tip when using https features in Node < v0.12
        var nodeVersion = Number(process.version.match(/^v(\d+\.\d+)/)[1]);
        if(nodeVersion < 0.12){
            logUtil.printLog(color.red("node >= v0.12 is required when trying to intercept HTTPS requests :("), logUtil.T_ERR);
        }

        logUtil.printLog(color.blue("The WebSocket will not work properly in the https intercept mode :("), logUtil.T_TIP);
    }

    if(option.throttle){
        logUtil.printLog("throttle :" + option.throttle + "kb/s");
        const rate = parseInt(option.throttle);
        if (rate < 1) {
            logUtil.printLog(color.red('Invalid throttle rate value, should be positive integer\n'), logUtil.T_ERR);
            process.exit(0);
        }
        global._throttle = new ThrottleGroup({rate: 1024 * parseFloat(option.throttle) }); // rate - byte/sec
    }

    self.httpProxyServer = null;

    async.series(
        [
            //clear cache dir, prepare recorder
            function(callback){
                util.clearCacheDir(function(){
                    if(option.dbFile){
                        global.recorder = new Recorder({filename: option.dbFile});
                    }else{
                        global.recorder = new Recorder();
                    }
                    callback();
                });
            },

            //creat proxy server
            function(callback){
                if(proxyType == T_TYPE_HTTPS){
                    certMgr.getCertificate(proxyHost,function(err,keyContent,crtContent){
                        if(err){
                            callback(err);
                        }else{
                            self.httpProxyServer = https.createServer({
                                key : keyContent,
                                cert: crtContent
                            },requestHandler.userRequestHandler);
                            callback(null);
                        }
                    });
                }else{
                    self.httpProxyServer = http.createServer(requestHandler.userRequestHandler);
                    callback(null);
                }
            },

            //handle CONNECT request for https over http
            function(callback){
                self.httpProxyServer.on('connect',requestHandler.connectReqHandler);
                callback(null);
            },

            //start proxy server
            function(callback){
                self.httpProxyServer.listen(proxyPort);
                callback(null);
            },

            //start web socket service
            function(callback){
                self.ws = new wsServer({port : socketPort});
                callback(null);
            },

            //start web interface ...
```
- example usage
```shell
...
    webPort       : 8002,  // optional, port for web interface
    socketPort    : 8003,  // optional, internal port for web socket, replace this when it is conflict with your own service
    throttle      : 10,    // optional, speed limit in kb/s
    disableWebInterface : false, //optional, set it when you don't want to use the web interface
    setAsGlobalProxy : false, //set anyproxy as your system proxy
    silent        : false //optional, do not print anything into terminal. do not set it when you are still debugging.
};
new proxy.proxyServer(options);

'''

Contact
-----------------

* Please feel free to [raise issue](https://github.com/alibaba/anyproxy/issues), or give us some advice. :)
...
```

#### <a name="apidoc.element.anyproxy.recorder"></a>[function <span class="apidocSignatureSpan">anyproxy.</span>recorder (option)](#apidoc.element.anyproxy.recorder)
- description and source-code
```javascript
function Recorder(option){
    var self = this,
        id        = 1,
        cachePath = proxyUtil.generateCacheDir(),
        db;

    option = option || {};
    if(option.filename && typeof option.filename == "string"){
        try{
            if(fs.existsSync(option.filename)){
                fs.writeFileSync(option.filename,""); //empty original file
            }

            db = new Datastore({
                filename : option.filename,
                autoload :true
            });
            db.persistence.setAutocompactionInterval(5001);
            logUtil.printLog("db file : " + option.filename);

        }catch(e){
            logUtil.printLog(e, logUtil.T_ERR);
            logUtil.printLog("Failed to load on-disk db file. Will use in-meomory db instead.", logUtil.T_ERR);
            db = new Datastore();
        }

    }else{
        //in-memory db
        db = new Datastore();
    }

    self.recordBodyMap = []; // id - body

    self.emitUpdate = function(id,info){
        if(info){
            self.emit("update",info);
        }else{
            self.getSingleRecord(id,function(err,doc){
                if(!err && !!doc && !!doc[0]){
                    self.emit("update",doc[0]);
                }
            });
        }
    };

    self.updateRecord = function(id,info){
        if(id < 0 ) return;

        var finalInfo = normalizeInfo(id,info);

        db.update({_id:id},finalInfo);
        self.updateRecordBody(id,info);

        self.emitUpdate(id,finalInfo);
    };

    self.updateExtInfo = function(id,extInfo){
        db.update({_id:id},{ $set: { ext: extInfo } },{},function(err,nums){
            if(!err){
                self.emitUpdate(id);
            }
        });

    }

    self.appendRecord = function(info){
        if(info.req.headers.anyproxy_web_req){ //request from web interface
            return -1;
        }

        var thisId    = id++,
            finalInfo = normalizeInfo(thisId,info);
        db.insert(finalInfo);
        self.updateRecordBody(id,info);

        self.emitUpdate(id,finalInfo);
        return thisId;
    };

    //update recordBody if exits

    //TODO : trigger update callback
    var BODY_FILE_PRFIX = "res_body_";
    self.updateRecordBody =function(id,info){
        if(id == -1) return;

        if(!id || !info.resBody) return;
        //add to body map
        //ignore image data
        var bodyFile = path.join(cachePath,BODY_FILE_PRFIX + id);
        fs.writeFile(bodyFile, info.resBody);
    };

    self.getBody = function(id,cb){
        if(id < 0){
            cb && cb("");
        }

        var bodyFile = path.join(cachePath,BODY_FILE_PRFIX + id);
        fs.access(bodyFile, fs.F_OK | fs.R_OK ,function(err){
            if(err){
                cb && cb(err);
            }else{
                fs.readFile(bodyFile,cb);
            }
        });
    };

    self.getDecodedBody = function(id,cb){
        var result = {
            type    : "unknown",
            mime    : "",
            content : ""
        };
        global.recorder.getSingleRecord(id,function(err,doc){
            //check whether this record exists
            if(!doc || !doc[0]){
                cb(new Error("failed to find record for this id"));
                return;
            }

            self.getBody(id,function(err,bodyContent){
                if(err){
                    cb(err);
                }else if(!bodyContent){
                    cb(null,result);
                }else{
                    var record      = doc[0],
                        resHeader   = record['resHeader'] || {};
                    try{
                        var headerStr    = JSON.stringify(resHeader),
                            charsetMatch = headerStr.match(/charset="?([a-zA-Z0-9\-]+)"?/),
                            imageMatch   = resHeader && resHeader["content-type"];

                        if(charsetMatch && charsetMatch.length){

                            var currentCharset = charsetMatch[1].toLowerCase();
                            if(currentCharset ...
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.anyproxy.setRules"></a>[function <span class="apidocSignatureSpan">anyproxy.</span>setRules (newRule)](#apidoc.element.anyproxy.setRules)
- description and source-code
```javascript
function setRules(newRule){

    if(!newRule){
        return userRule;
    }else{

        if(!newRule.summary){
            newRule.summary = function(){
                return "this rule file does not have a summary";
            };
        }

        userRule = util.merge(userRule,newRule);

        var functions = [];
        if('function' == typeof(userRule.init)){
            functions.push(function(cb){
                userRule.init(cb);
            });
        }
        if('function' == typeof(userRule.summary)){
            functions.push(function(cb){
                logUtil.printLog(userRule.summary());
                cb(null);
            });
        }
        async.series(functions,function(errors,result){
            if(!errors){
                logUtil.printLog(color.green('Anyproxy rules initialize finished, have fun!'));
            }
        });

        return userRule;
    }
}
```
- example usage
```shell
...
if(ifSilent){
    logUtil.setPrintStatus(false);
}

// copy the rule to keep the original proxyRules independent
proxyRules = Object.assign({}, proxyRules);

var currentRule = requestHandler.setRules(proxyRules); //TODO : optimize calling for set rule

if(!!option.interceptHttps){
    if (!certMgr.isRootCAFileExists()) {
        util.showRootInstallTip();
        process.exit(0);
        return;
    }
...
```

#### <a name="apidoc.element.anyproxy.webInterface"></a>[function <span class="apidocSignatureSpan">anyproxy.</span>webInterface (config)](#apidoc.element.anyproxy.webInterface)
- description and source-code
```javascript
function webInterface(config){
    var port = config.port,
        wsPort        = config.wsPort,
        ipAddress     = config.ip,
        userRule      = config.userRule,
        ruleSummary   = "",
        customMenu    = [],
        server;

    try{
        ruleSummary = userRule.summary();
        customMenu  = userRule._getCustomMenu();
    }catch(e){}

    var self         = this,
        myAbsAddress = "http://" + ipAddress + ":" + port +"/",
        crtFilePath  = certMgr.getRootCAFilePath(),
        staticDir    = path.join(__dirname,'../web');

    var app = express();
    app.use(compress()); //invoke gzip
    app.use(function(req, res, next) {
        res.setHeader("note", "THIS IS A REQUEST FROM ANYPROXY WEB INTERFACE");
        return next();
    });

    app.get("/lastestLog",function(req,res){
        recorder.getRecords(null,120,function(err,docs){
            if(err){
                res.end(err.toString());
            }else{
                res.json(docs);
            }
        });
    });

    app.get("/fetchBody",function(req,res){
        var query = req.query;
        if(query && query.id){
            global.recorder.getDecodedBody(query.id, function(err, result){
                if(err || !result || !result.content){
                    res.json({});
                }else if(result.type && result.type == "image" && result.mime){
                    if(query.raw){
                        //TODO : cache query result
                        res.type(result.mime).end(result.content);
                    }else{
                        res.json({
                            id      : query.id,
                            type    : result.type,
                            ref     : "/fetchBody?id=" + query.id + "&raw=true"
                        });
                    }
                }else{
                    res.json({
                        id      : query.id,
                        type    : result.type,
                        content : result.content
                    });
                }
            });
        }else{
            res.end({});
        }
    });

    app.get("/fetchCrtFile",function(req,res){
        if(crtFilePath){
            res.setHeader("Content-Type","application/x-x509-ca-cert");
            res.setHeader("Content-Disposition",'attachment; filename="rootCA.crt"');
            res.end(fs.readFileSync(crtFilePath,{encoding:null}));
        }else{
            res.setHeader("Content-Type","text/html");
            res.end("can not file rootCA ,plase use <strong>anyproxy --root</strong> to generate one");
        }
    });

    //make qr code
    app.get("/qr",function(req,res){
        var qr        = qrCode.qrcode(4, 'M'),
            targetUrl = myAbsAddress,
            qrImageTag,
            resDom;

        qr.addData(targetUrl);
        qr.make();
        qrImageTag = qr.createImgTag(4);

        resDom = '<a href="__url"> __img <br> click or scan qr code to start client </a>'.replace(/__url/,targetUrl).replace(/__img
/,qrImageTag);
        res.setHeader("Content-Type", "text/html");
        res.end(resDom);
    });

    app.get("/qr_root",function(req,res){
        var qr        = qrCode.qrcode(4, 'M'),
            targetUrl = myAbsAddress + "fetchCrtFile",
            qrImageTag,
            resDom;

        qr.addData(targetUrl);
        qr.make();
        qrImageTag = qr.createImgTag(4);

        resDom = '<a href="__url"> __img <br> click or scan qr code to download rootCA.crt </a>'.replace(/__url/,targetUrl).replace
(/__img/,qrImageTag);
        res.setHeader("Content-Type", "text/html");
        res.end(resDom);
    });

    app.use(function(req,res,next){
        var indexTpl  = fs.readFileSync(path.join(staticDir,"/index.html"),{encoding:"utf8"}),
            opt       = {
                rule        : ruleSummary || "",
                customMenu  : customMenu || [],
                wsPort      : wsPort,
                ipAddress   : ipAddress || "127.0.0.1"
            };

        if( url.parse(req.url).pathname == "/"){
            res.se ...
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.anyproxy.wsServer"></a>[function <span class="apidocSignatureSpan">anyproxy.</span>wsServer (config)](#apidoc.element.anyproxy.wsServer)
- description and source-code
```javascript
function wsServer(config){
	//web socket interface
	var self = this,
        wss  = new WebSocketServer({port: config.port});
	wss.broadcast = function(data) {
        var key = data.id;
        if(typeof data == "object"){
            data = JSON.stringify(data);
        }

        for(var i in this.clients){
            try{
                this.clients[i].send(data);
            }catch(e){
                logUtil.printLog("websocket failed to send data, " + e, logUtil.T_ERR);
            }
        }
	};

	wss.on("connection",function(ws){
	    ws.on("message",function(msg){
	        resToMsg(msg,function(res){
	            res && ws.send(JSON.stringify(res));
	        });
	    });
	});

    wss.on("close",function(){});

	global.recorder.on("update",function(data){
        try{
    	    wss && wss.broadcast({
    	        type   : "update",
    	        content: data
    	    });

        }catch(e){
            console.log("ws error");
            console.log(e);
        }
	});

    self.wss = wss;
}
```
- example usage
```shell
n/a
```



# <a name="apidoc.module.anyproxy.certGenerator"></a>[module anyproxy.certGenerator](#apidoc.module.anyproxy.certGenerator)

#### <a name="apidoc.element.anyproxy.certGenerator.generateCertsForHostname"></a>[function <span class="apidocSignatureSpan">anyproxy.certGenerator.</span>generateCertsForHostname (domain, rootCAConfig)](#apidoc.element.anyproxy.certGenerator.generateCertsForHostname)
- description and source-code
```javascript
function generateCertsForHostname(domain, rootCAConfig){

  //generate a serialNumber for domain
  var md = forge.md.md5.create();
  md.update(domain);

  var keysAndCert = getKeysAndCert(md.digest().toHex());
  keys = keysAndCert.keys;
  cert = keysAndCert.cert;

  var caCert    = forge.pki.certificateFromPem(rootCAConfig.cert);
  var caKey     = forge.pki.privateKeyFromPem(rootCAConfig.key);

  // issuer from CA
  cert.setIssuer(caCert.subject.attributes);

  var attrs = defaultAttrs.concat([
    {
      name: 'commonName',
      value: domain
    }
  ]);
  cert.setSubject(attrs);
  cert.sign(caKey, forge.md.sha256.create());

  return {
    privateKey: forge.pki.privateKeyToPem(keys.privateKey),
    publicKey: forge.pki.publicKeyToPem(keys.publicKey),
    certificate: forge.pki.certificateToPem(cert)
  };
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.anyproxy.certGenerator.generateRootCA"></a>[function <span class="apidocSignatureSpan">anyproxy.certGenerator.</span>generateRootCA ()](#apidoc.element.anyproxy.certGenerator.generateRootCA)
- description and source-code
```javascript
function generateRootCA(){
  var keysAndCert = getKeysAndCert();
  keys = keysAndCert.keys;
  cert = keysAndCert.cert;

  var attrs = defaultAttrs.concat([
    {
      name: 'commonName',
      value: 'AnyProxy'
    }
  ]);
  cert.setSubject(attrs);
  cert.setIssuer(attrs);
  cert.setExtensions([
    { name: 'basicConstraints', cA: true }
    // { name: 'keyUsage', keyCertSign: true, digitalSignature: true, nonRepudiation: true, keyEncipherment: true, dataEncipherment
: true },
    // { name: 'extKeyUsage', serverAuth: true, clientAuth: true, codeSigning: true, emailProtection: true, timeStamping: true },
    // { name: 'nsCertType', client: true, server: true, email: true, objsign: true, sslCA: true, emailCA: true, objCA: true },
    // { name: 'subjectAltName', altNames: [ { type: 6, /* URI */ value: 'http://example.org/webid#me' }, { type: 7, /* IP */ ip
: '127.0.0.1' } ] },
    // { name: 'subjectKeyIdentifier' }
  ]);

  cert.sign(keys.privateKey, forge.md.sha256.create());

  return {
    privateKey: forge.pki.privateKeyToPem(keys.privateKey),
    publicKey: forge.pki.publicKeyToPem(keys.publicKey),
    certificate: forge.pki.certificateToPem(cert)
  };

  return pem;
}
```
- example usage
```shell
...
'''

'''javascript
var proxy = require("anyproxy");

//create cert when you want to use https features
//please manually trust this rootCA when it is the first time you run it
!proxy.isRootCAFileExists() && proxy.generateRootCA();

var options = {
type          : "http",
port          : 8001,
hostname      : "localhost",
rule          : require("path/to/my/ruleModule.js"),
dbFile        : null,  // optional, save request data to a specified file, will use in-memory db if not specified
...
```



# <a name="apidoc.module.anyproxy.certMgr"></a>[module anyproxy.certMgr](#apidoc.module.anyproxy.certMgr)

#### <a name="apidoc.element.anyproxy.certMgr.clearCerts"></a>[function <span class="apidocSignatureSpan">anyproxy.certMgr.</span>clearCerts (cb)](#apidoc.element.anyproxy.certMgr.clearCerts)
- description and source-code
```javascript
function clearCerts(cb) {
  util.deleteFolderContentsRecursive(certDir);
  cb && cb();
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.anyproxy.certMgr.generateRootCA"></a>[function <span class="apidocSignatureSpan">anyproxy.certMgr.</span>generateRootCA (cb)](#apidoc.element.anyproxy.certMgr.generateRootCA)
- description and source-code
```javascript
generateRootCA = function (cb) {
    doGenerate(false);

    function doGenerate(overwrite) {
        const rootOptions = {
            commonName: 'AnyProxy',
            overwrite: !!overwrite
        };

        easyCert.generateRootCA(rootOptions, (error, keyPath, crtPath) => {
            if (!error) {
                const certDir = path.dirname(keyPath);
                logUtil.printLog(color.cyan('The cert is generated at "' + certDir + '"'));
                if(isWin){
                    exec("start .",{ cwd : certDir });
                }else{
                    exec("open .",{ cwd : certDir });
                }
            }

            if (error === 'ROOT_CA_EXISTED') {
                var rl = readline.createInterface({
                    input : process.stdin,
                    output: process.stdout
                });

                rl.question("do you really want to generate a new one ?)(yes/NO)", function(answer) {
                    if(/yes/i.test(answer)){
                        doGenerate(true);
                    }else{
                        console.log("will not generate a new one");

                    }
                    rl.close();
                });

                return;
            }
            cb(error, keyPath, crtPath);
        });
    }

}
```
- example usage
```shell
...
'''

'''javascript
var proxy = require("anyproxy");

//create cert when you want to use https features
//please manually trust this rootCA when it is the first time you run it
!proxy.isRootCAFileExists() && proxy.generateRootCA();

var options = {
type          : "http",
port          : 8001,
hostname      : "localhost",
rule          : require("path/to/my/ruleModule.js"),
dbFile        : null,  // optional, save request data to a specified file, will use in-memory db if not specified
...
```

#### <a name="apidoc.element.anyproxy.certMgr.getCertificate"></a>[function <span class="apidocSignatureSpan">anyproxy.certMgr.</span>getCertificate (host, cb)](#apidoc.element.anyproxy.certMgr.getCertificate)
- description and source-code
```javascript
getCertificate = function (host, cb) {
    easyCert.getCertificate(host, (error, keyContent, crtContent) => {
        if (error === 'ROOT_CA_NOT_EXISTS') {
            util.showRootInstallTip();
            process.exit(0);
            return;
        }

        cb(error, keyContent, crtContent);
    });
}
```
- example usage
```shell
...
        callback();
    });
},

//creat proxy server
function(callback){
    if(proxyType == T_TYPE_HTTPS){
        certMgr.getCertificate(proxyHost,function(err,keyContent,crtContent){
            if(err){
                callback(err);
            }else{
                self.httpProxyServer = https.createServer({
                    key : keyContent,
                    cert: crtContent
                },requestHandler.userRequestHandler);
...
```

#### <a name="apidoc.element.anyproxy.certMgr.getRootCAFilePath"></a>[function <span class="apidocSignatureSpan">anyproxy.certMgr.</span>getRootCAFilePath ()](#apidoc.element.anyproxy.certMgr.getRootCAFilePath)
- description and source-code
```javascript
function getRootCAFilePath() {
  return isRootCAFileExists() ? rootCAcrtFilePath : '';
}
```
- example usage
```shell
...
try{
    ruleSummary = userRule.summary();
    customMenu  = userRule._getCustomMenu();
}catch(e){}

var self         = this,
    myAbsAddress = "http://" + ipAddress + ":" + port +"/",
    crtFilePath  = certMgr.getRootCAFilePath(),
    staticDir    = path.join(__dirname,'../web');

var app = express();
app.use(compress()); //invoke gzip
app.use(function(req, res, next) {
    res.setHeader("note", "THIS IS A REQUEST FROM ANYPROXY WEB INTERFACE");
    return next();
...
```

#### <a name="apidoc.element.anyproxy.certMgr.getRootDirPath"></a>[function <span class="apidocSignatureSpan">anyproxy.certMgr.</span>getRootDirPath ()](#apidoc.element.anyproxy.certMgr.getRootDirPath)
- description and source-code
```javascript
function getRootDirPath() {
  return rootDirPath;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.anyproxy.certMgr.ifRootCATrusted"></a>[function <span class="apidocSignatureSpan">anyproxy.certMgr.</span>ifRootCATrusted (callback)](#apidoc.element.anyproxy.certMgr.ifRootCATrusted)
- description and source-code
```javascript
function ifRootCATrusted(callback) {
  if (!isRootCAFileExists()) {
    callback && callback(new Error('ROOTCA_NOT_EXIST'));
  } else if (/^win/.test(process.platform)) {
    callback && callback(new Error('UNABLE_TO_DETECT_IN_WINDOWS'));
  } else {
    const HTTPS_RESPONSE = 'HTTPS Server is ON';
    // local.asnyproxy.io --> 127.0.0.1
    getCertificate('local.anyproxy.io', (e, key, cert) => {
      getPort()
      .then((port) => {
        if (e) {
          callback && callback(e);
          return;
        }
        const server = https.createServer({
          ca: fs.readFileSync(rootCAcrtFilePath),
          key,
          cert,
        }, (req, res) => {
          res.end(HTTPS_RESPONSE);
        }).listen(port);

        // do not use node.http to test the cert. Ref: https://github.com/nodejs/node/issues/4175
        const testCmd = 'curl https://local.anyproxy.io:' + port;
        exec(testCmd, { timeout: 1000 }, (error, stdout, stderr) => {
          server.close();
          if (stdout && stdout.indexOf(HTTPS_RESPONSE) >= 0) {
            callback && callback(null, true);
          } else {
            callback && callback(null, false);
          }
        });
      })
      .catch(callback);
    });
  }
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.anyproxy.certMgr.isRootCAFileExists"></a>[function <span class="apidocSignatureSpan">anyproxy.certMgr.</span>isRootCAFileExists ()](#apidoc.element.anyproxy.certMgr.isRootCAFileExists)
- description and source-code
```javascript
function isRootCAFileExists() {
  return (fs.existsSync(rootCAcrtFilePath) && fs.existsSync(rootCAkeyFilePath));
}
```
- example usage
```shell
...
'''

'''javascript
var proxy = require("anyproxy");

//create cert when you want to use https features
//please manually trust this rootCA when it is the first time you run it
!proxy.isRootCAFileExists() && proxy.generateRootCA();

var options = {
type          : "http",
port          : 8001,
hostname      : "localhost",
rule          : require("path/to/my/ruleModule.js"),
dbFile        : null,  // optional, save request data to a specified file, will use in-memory db if not specified
...
```



# <a name="apidoc.module.anyproxy.recorder"></a>[module anyproxy.recorder](#apidoc.module.anyproxy.recorder)

#### <a name="apidoc.element.anyproxy.recorder.recorder"></a>[function <span class="apidocSignatureSpan">anyproxy.</span>recorder (option)](#apidoc.element.anyproxy.recorder.recorder)
- description and source-code
```javascript
function Recorder(option){
    var self = this,
        id        = 1,
        cachePath = proxyUtil.generateCacheDir(),
        db;

    option = option || {};
    if(option.filename && typeof option.filename == "string"){
        try{
            if(fs.existsSync(option.filename)){
                fs.writeFileSync(option.filename,""); //empty original file
            }

            db = new Datastore({
                filename : option.filename,
                autoload :true
            });
            db.persistence.setAutocompactionInterval(5001);
            logUtil.printLog("db file : " + option.filename);

        }catch(e){
            logUtil.printLog(e, logUtil.T_ERR);
            logUtil.printLog("Failed to load on-disk db file. Will use in-meomory db instead.", logUtil.T_ERR);
            db = new Datastore();
        }

    }else{
        //in-memory db
        db = new Datastore();
    }

    self.recordBodyMap = []; // id - body

    self.emitUpdate = function(id,info){
        if(info){
            self.emit("update",info);
        }else{
            self.getSingleRecord(id,function(err,doc){
                if(!err && !!doc && !!doc[0]){
                    self.emit("update",doc[0]);
                }
            });
        }
    };

    self.updateRecord = function(id,info){
        if(id < 0 ) return;

        var finalInfo = normalizeInfo(id,info);

        db.update({_id:id},finalInfo);
        self.updateRecordBody(id,info);

        self.emitUpdate(id,finalInfo);
    };

    self.updateExtInfo = function(id,extInfo){
        db.update({_id:id},{ $set: { ext: extInfo } },{},function(err,nums){
            if(!err){
                self.emitUpdate(id);
            }
        });

    }

    self.appendRecord = function(info){
        if(info.req.headers.anyproxy_web_req){ //request from web interface
            return -1;
        }

        var thisId    = id++,
            finalInfo = normalizeInfo(thisId,info);
        db.insert(finalInfo);
        self.updateRecordBody(id,info);

        self.emitUpdate(id,finalInfo);
        return thisId;
    };

    //update recordBody if exits

    //TODO : trigger update callback
    var BODY_FILE_PRFIX = "res_body_";
    self.updateRecordBody =function(id,info){
        if(id == -1) return;

        if(!id || !info.resBody) return;
        //add to body map
        //ignore image data
        var bodyFile = path.join(cachePath,BODY_FILE_PRFIX + id);
        fs.writeFile(bodyFile, info.resBody);
    };

    self.getBody = function(id,cb){
        if(id < 0){
            cb && cb("");
        }

        var bodyFile = path.join(cachePath,BODY_FILE_PRFIX + id);
        fs.access(bodyFile, fs.F_OK | fs.R_OK ,function(err){
            if(err){
                cb && cb(err);
            }else{
                fs.readFile(bodyFile,cb);
            }
        });
    };

    self.getDecodedBody = function(id,cb){
        var result = {
            type    : "unknown",
            mime    : "",
            content : ""
        };
        global.recorder.getSingleRecord(id,function(err,doc){
            //check whether this record exists
            if(!doc || !doc[0]){
                cb(new Error("failed to find record for this id"));
                return;
            }

            self.getBody(id,function(err,bodyContent){
                if(err){
                    cb(err);
                }else if(!bodyContent){
                    cb(null,result);
                }else{
                    var record      = doc[0],
                        resHeader   = record['resHeader'] || {};
                    try{
                        var headerStr    = JSON.stringify(resHeader),
                            charsetMatch = headerStr.match(/charset="?([a-zA-Z0-9\-]+)"?/),
                            imageMatch   = resHeader && resHeader["content-type"];

                        if(charsetMatch && charsetMatch.length){

                            var currentCharset = charsetMatch[1].toLowerCase();
                            if(currentCharset ...
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.anyproxy.recorder.super_"></a>[function <span class="apidocSignatureSpan">anyproxy.recorder.</span>super_ ()](#apidoc.element.anyproxy.recorder.super_)
- description and source-code
```javascript
function EventEmitter() {
  EventEmitter.init.call(this);
}
```
- example usage
```shell
n/a
```



# <a name="apidoc.module.anyproxy.requestHandler"></a>[module anyproxy.requestHandler](#apidoc.module.anyproxy.requestHandler)

#### <a name="apidoc.element.anyproxy.requestHandler.connectReqHandler"></a>[function <span class="apidocSignatureSpan">anyproxy.requestHandler.</span>connectReqHandler (req, socket, head)](#apidoc.element.anyproxy.requestHandler.connectReqHandler)
- description and source-code
```javascript
function connectReqHandler(req, socket, head){
    var host      = req.url.split(":")[0],
        targetPort= req.url.split(":")[1],
        resourceInfo,
        resourceInfoId;

    var shouldIntercept = userRule.shouldInterceptHttpsReq(req);

    //bypass webSocket on webinterface
    if(targetPort == 8003){
        shouldIntercept = false; // TODO : a more general solution?
    }

    logUtil.printLog(color.green("\nreceived https CONNECT request " + host));
    if(shouldIntercept){
        logUtil.printLog("==>will forward to local https server");
    }else{
        logUtil.printLog("==>will bypass the man-in-the-middle proxy");
    }

    //record
    resourceInfo = {
        host      : host,
        method    : req.method,
        path      : "",
        url       : "https://" + host,
        req       : req,
        startTime : new Date().getTime()
    };
    resourceInfoId = global.recorder.appendRecord(resourceInfo);

    var proxyPort,
        proxyHost,
        internalHttpsPort,
        httpsServerMgrInstance;

    async.series([

        //check if internal https server exists
        function(callback){
            if(!shouldIntercept){
                callback();
                return;
            }else{
                if(internalHttpsPort){
                    callback();
                }else{
                    getPort(function(port){
                        internalHttpsPort = port;
                        httpsServerMgrInstance = new httpsServerMgr({
                            port    :port,
                            handler :userRequestHandler
                        });
                        callback();
                    });
                }
            }
        },

        //determine the target server
        function(callback){

            if(shouldIntercept){
                proxyPort = internalHttpsPort;
                proxyHost = "127.0.0.1";
                callback();

            }else{
                proxyPort = (targetPort == 80)? 443 : targetPort;
                proxyHost = host;

                callback();
            }

        //connect
        },function(callback){
            try{
                var conn = net.connect(proxyPort, proxyHost, function(){
                    socket.write('HTTP/' + req.httpVersion + ' 200 OK\r\n\r\n', 'UTF-8', function(){

                        //throttle for direct-foward https
                        if(global._throttle && !shouldIntercept ){
                            var readable = conn.pipe(global._throttle.throttle());
                            readable.pipe(socket);
                            socket.pipe(conn);
                        }else{
                            conn.pipe(socket);
                            socket.pipe(conn);
                        }

                        callback();
                    });
                });

                conn.on("error",function(e){
                    logUtil.printLog("err when connect to + " + host + " , " + e, logUtil.T_ERR);
                });
            }catch(e){
                logUtil.printLog("err when connect to remote https server (__host)".replace(/__host/,host), logUtil.T_ERR);
            }

        //update record
        },function(callback){
            resourceInfo.endTime    = new Date().getTime();
            resourceInfo.statusCode = "200";
            resourceInfo.resHeader  = {};
            resourceInfo.resBody    = "";
            resourceInfo.length     = 0;

            global.recorder && global.recorder.updateRecord(resourceInfoId,resourceInfo);

            callback();
        }
    ],function(err,result){
        if(err){
            logUtil.printLog("err " + err, logUtil.T_ERR);
            throw err;
        }
    });
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.anyproxy.requestHandler.getRuleSummary"></a>[function <span class="apidocSignatureSpan">anyproxy.requestHandler.</span>getRuleSummary ()](#apidoc.element.anyproxy.requestHandler.getRuleSummary)
- description and source-code
```javascript
function getRuleSummary(){
    return userRule.summary();
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.anyproxy.requestHandler.setRules"></a>[function <span class="apidocSignatureSpan">anyproxy.requestHandler.</span>setRules (newRule)](#apidoc.element.anyproxy.requestHandler.setRules)
- description and source-code
```javascript
function setRules(newRule){

    if(!newRule){
        return userRule;
    }else{

        if(!newRule.summary){
            newRule.summary = function(){
                return "this rule file does not have a summary";
            };
        }

        userRule = util.merge(userRule,newRule);

        var functions = [];
        if('function' == typeof(userRule.init)){
            functions.push(function(cb){
                userRule.init(cb);
            });
        }
        if('function' == typeof(userRule.summary)){
            functions.push(function(cb){
                logUtil.printLog(userRule.summary());
                cb(null);
            });
        }
        async.series(functions,function(errors,result){
            if(!errors){
                logUtil.printLog(color.green('Anyproxy rules initialize finished, have fun!'));
            }
        });

        return userRule;
    }
}
```
- example usage
```shell
...
if(ifSilent){
    logUtil.setPrintStatus(false);
}

// copy the rule to keep the original proxyRules independent
proxyRules = Object.assign({}, proxyRules);

var currentRule = requestHandler.setRules(proxyRules); //TODO : optimize calling for set rule

if(!!option.interceptHttps){
    if (!certMgr.isRootCAFileExists()) {
        util.showRootInstallTip();
        process.exit(0);
        return;
    }
...
```

#### <a name="apidoc.element.anyproxy.requestHandler.userRequestHandler"></a>[function <span class="apidocSignatureSpan">anyproxy.requestHandler.</span>userRequestHandler (req, userRes)](#apidoc.element.anyproxy.requestHandler.userRequestHandler)
- description and source-code
```javascript
function userRequestHandler(req, userRes){
<span class="apidocCodeCommentSpan">    /*
    note
        req.url is wired
        in http  server : http://www.example.com/a/b/c
        in https server : /a/b/c
    */
</span>
    var host               = req.headers.host,
        protocol           = (!!req.connection.encrypted && !/^http:/.test(req.url)) ? "https" : "http",
        fullUrl            = protocol === "http" ? req.url : (protocol + '://' + host + req.url),
        urlPattern         = url.parse(fullUrl),
        path               = urlPattern.path,
        resourceInfo,
        resourceInfoId     = -1,
        reqData;

    // console.log(req.url);
    // console.log(path);

    //record
    resourceInfo = {
        host      : host,
        method    : req.method,
        path      : path,
        protocol  : protocol,
        url       : protocol + "://" + host + path,
        req       : req,
        startTime : new Date().getTime()
    };
    if(global.recorder){
        resourceInfoId = global.recorder.appendRecord(resourceInfo);
    }

    logUtil.printLog(color.green("\nreceived request to : " + host + path));

    //get request body and route to local or remote
    async.series([
        fetchReqData,
        routeReq
    ],function(){
        //mark some ext info
        if(req.anyproxy_map_local){
            global.recorder.updateExtInfo(resourceInfoId, {map : req.anyproxy_map_local});
        }
    });

    //get request body
    function fetchReqData(callback){
        var postData = [];
        req.on("data",function(chunk){
            postData.push(chunk);
        });
        req.on("end",function(){
            reqData = Buffer.concat(postData);
            resourceInfo.reqBody = reqData.toString();
            global.recorder && global.recorder.updateRecord(resourceInfoId,resourceInfo);

            callback();
        });
    }

    //route to dealing function
    function routeReq(callback){
        if(userRule.shouldUseLocalResponse(req,reqData)){
            logUtil.printLog("==>use local rules");
            dealWithLocalResponse(callback);
        }else{
            logUtil.printLog("==>will forward to real server by proxy");
            dealWithRemoteResonse(callback);
        }
    }

    function dealWithLocalResponse(callback){
        userRule.dealLocalResponse(req,reqData,function(statusCode,resHeader,resBody){

            //update record info
            resourceInfo.endTime = new Date().getTime();
            resourceInfo.res     = { //construct a self-defined res object
                statusCode : statusCode || "",
                headers    : resHeader  || {}
            }
            resourceInfo.resHeader  = resHeader || {};
            resourceInfo.resBody    = resBody;
            resourceInfo.length     = resBody ? resBody.length : 0;
            resourceInfo.statusCode = statusCode;

            global.recorder && global.recorder.updateRecord(resourceInfoId,resourceInfo);

            userRes.writeHead(statusCode,resHeader);
            userRes.end(resBody);
            callback && callback();
        });

        return;
    }

    function dealWithRemoteResonse(callback){
        var options;

        //modify request protocol
        protocol = userRule.replaceRequestProtocol(req,protocol) || protocol;

        //modify request options
        options = {
            hostname : urlPattern.hostname || req.headers.host,
            port     : urlPattern.port || req.port || (/https/.test(protocol) ? 443 : 80),
            path     : path,
            method   : req.method,
            headers  : req.headers
        };

        options = userRule.replaceRequestOption(req,options) || options;
        options.rejectUnauthorized = false;
        try{
            delete options.headers['accept-encoding']; //avoid gzipped response
        }catch(e){}

        //update request data
        reqData = userRule.replaceRequestData(req,reqData) || reqData;
        options.headers = util.lower_keys(options.headers);
        options.headers["content-length"] = reqData.length; //rewrite content length info

        options.h ...
```
- example usage
```shell
n/a
```



# <a name="apidoc.module.anyproxy.rule__blank"></a>[module anyproxy.rule__blank](#apidoc.module.anyproxy.rule__blank)

#### <a name="apidoc.element.anyproxy.rule__blank.dealLocalResponse"></a>[function <span class="apidocSignatureSpan">anyproxy.rule__blank.</span>dealLocalResponse (req, reqBody, callback)](#apidoc.element.anyproxy.rule__blank.dealLocalResponse)
- description and source-code
```javascript
dealLocalResponse = function (req, reqBody, callback){
        callback(statusCode,resHeader,responseData)
	}
```
- example usage
```shell
...
        }else{
logUtil.printLog("==>will forward to real server by proxy");
dealWithRemoteResonse(callback);
        }
    }

    function dealWithLocalResponse(callback){
        userRule.dealLocalResponse(req,reqData,function(statusCode,resHeader,resBody){

//update record info
resourceInfo.endTime = new Date().getTime();
resourceInfo.res     = { //construct a self-defined res object
    statusCode : statusCode || "",
    headers    : resHeader  || {}
}
...
```

#### <a name="apidoc.element.anyproxy.rule__blank.pauseBeforeSendingResponse"></a>[function <span class="apidocSignatureSpan">anyproxy.rule__blank.</span>pauseBeforeSendingResponse (req, res)](#apidoc.element.anyproxy.rule__blank.pauseBeforeSendingResponse)
- description and source-code
```javascript
pauseBeforeSendingResponse = function (req, res){
	var timeInMS = 1; //delay all requests for 1ms
	return timeInMS;
}
```
- example usage
```shell
...
        });
    }else{
        callback();
    }

//delay
},function(callback){
var pauseTimeInMS = userRule.pauseBeforeSendingResponse(req,res);
    if(pauseTimeInMS){
        setTimeout(callback,pauseTimeInMS);
    }else{
        callback();
    }

//send response
...
```

#### <a name="apidoc.element.anyproxy.rule__blank.replaceRequestData"></a>[function <span class="apidocSignatureSpan">anyproxy.rule__blank.</span>replaceRequestData (req, data)](#apidoc.element.anyproxy.rule__blank.replaceRequestData)
- description and source-code
```javascript
replaceRequestData = function (req, data){
    return data;
}
```
- example usage
```shell
...
options = userRule.replaceRequestOption(req,options) || options;
options.rejectUnauthorized = false;
try{
    delete options.headers['accept-encoding']; //avoid gzipped response
}catch(e){}

//update request data
reqData = userRule.replaceRequestData(req,reqData) || reqData;
options.headers = util.lower_keys(options.headers);
options.headers["content-length"] = reqData.length; //rewrite content length info

options.headers = util.upper_keys(options.headers);

//send request
var proxyReq = ( /https/.test(protocol) ? https : http).request(options, function(res) {
...
```

#### <a name="apidoc.element.anyproxy.rule__blank.replaceRequestOption"></a>[function <span class="apidocSignatureSpan">anyproxy.rule__blank.</span>replaceRequestOption (req, option)](#apidoc.element.anyproxy.rule__blank.replaceRequestOption)
- description and source-code
```javascript
replaceRequestOption = function (req, option){
    var newOption = option;
    return newOption;
}
```
- example usage
```shell
...
    hostname : urlPattern.hostname || req.headers.host,
    port     : urlPattern.port || req.port || (/https/.test(protocol) ? 443 : 80),
    path     : path,
    method   : req.method,
    headers  : req.headers
};

options = userRule.replaceRequestOption(req,options) || options;
options.rejectUnauthorized = false;
try{
    delete options.headers['accept-encoding']; //avoid gzipped response
}catch(e){}

//update request data
reqData = userRule.replaceRequestData(req,reqData) || reqData;
...
```

#### <a name="apidoc.element.anyproxy.rule__blank.replaceRequestProtocol"></a>[function <span class="apidocSignatureSpan">anyproxy.rule__blank.</span>replaceRequestProtocol (req, protocol)](#apidoc.element.anyproxy.rule__blank.replaceRequestProtocol)
- description and source-code
```javascript
replaceRequestProtocol = function (req, protocol){
	var newProtocol = protocol;
	return newProtocol;
}
```
- example usage
```shell
...
return;
    }

    function dealWithRemoteResonse(callback){
var options;

//modify request protocol
protocol = userRule.replaceRequestProtocol(req,protocol) || protocol;

//modify request options
options = {
    hostname : urlPattern.hostname || req.headers.host,
    port     : urlPattern.port || req.port || (/https/.test(protocol) ? 443 : 80),
    path     : path,
    method   : req.method,
...
```

#### <a name="apidoc.element.anyproxy.rule__blank.replaceResponseHeader"></a>[function <span class="apidocSignatureSpan">anyproxy.rule__blank.</span>replaceResponseHeader (req, res, header)](#apidoc.element.anyproxy.rule__blank.replaceResponseHeader)
- description and source-code
```javascript
replaceResponseHeader = function (req, res, header){
	var newHeader = header;
	return newHeader;
}
```
- example usage
```shell
...
        //send request
        var proxyReq = ( /https/.test(protocol) ? https : http).request(options, function(res) {

//deal response header
var statusCode = res.statusCode;
statusCode = userRule.replaceResponseStatusCode(req,res,statusCode) || statusCode;

var resHeader = userRule.replaceResponseHeader(req,res,res.headers) || res.headers;
resHeader = util.lower_keys(resHeader);

// remove gzip related header, and ungzip the content
// note there are other compression types like deflate
var ifServerGzipped =  /gzip/i.test(resHeader['content-encoding']);
if(ifServerGzipped){
    delete resHeader['content-encoding'];
...
```

#### <a name="apidoc.element.anyproxy.rule__blank.replaceResponseStatusCode"></a>[function <span class="apidocSignatureSpan">anyproxy.rule__blank.</span>replaceResponseStatusCode (req, res, statusCode)](#apidoc.element.anyproxy.rule__blank.replaceResponseStatusCode)
- description and source-code
```javascript
replaceResponseStatusCode = function (req, res, statusCode){
	var newStatusCode = statusCode;
	return newStatusCode;
}
```
- example usage
```shell
...
        options.headers = util.upper_keys(options.headers);

        //send request
        var proxyReq = ( /https/.test(protocol) ? https : http).request(options, function(res) {

//deal response header
var statusCode = res.statusCode;
statusCode = userRule.replaceResponseStatusCode(req,res,statusCode) || statusCode;

var resHeader = userRule.replaceResponseHeader(req,res,res.headers) || res.headers;
resHeader = util.lower_keys(resHeader);

// remove gzip related header, and ungzip the content
// note there are other compression types like deflate
var ifServerGzipped =  /gzip/i.test(resHeader['content-encoding']);
...
```

#### <a name="apidoc.element.anyproxy.rule__blank.replaceServerResDataAsync"></a>[function <span class="apidocSignatureSpan">anyproxy.rule__blank.</span>replaceServerResDataAsync (req, res, serverResData, callback)](#apidoc.element.anyproxy.rule__blank.replaceServerResDataAsync)
- description and source-code
```javascript
replaceServerResDataAsync = function (req, res, serverResData, callback){
    callback(serverResData);
}
```
- example usage
```shell
...
//get custom response
},function(callback){
    if(userRule.replaceServerResData){
        logUtil.printLog(color.red("replaceServerResData is deprecated, and will be unavilable soon. Use replaceServerResDataAsync
 instead."), logUtil.T_ERR);
        serverResData = userRule.replaceServerResData(req,res,serverResData) || serverResData;
        callback();
    }else if(userRule.replaceServerResDataAsync){
        userRule.replaceServerResDataAsync(req,res,serverResData,function(newRes){
            serverResData = newRes;
            callback();
        });
    }else{
        callback();
    }
...
```

#### <a name="apidoc.element.anyproxy.rule__blank.shouldInterceptHttpsReq"></a>[function <span class="apidocSignatureSpan">anyproxy.rule__blank.</span>shouldInterceptHttpsReq (req)](#apidoc.element.anyproxy.rule__blank.shouldInterceptHttpsReq)
- description and source-code
```javascript
shouldInterceptHttpsReq = function (req){
    return false;
}
```
- example usage
```shell
...

function connectReqHandler(req, socket, head){
var host      = req.url.split(":")[0],
    targetPort= req.url.split(":")[1],
    resourceInfo,
    resourceInfoId;

var shouldIntercept = userRule.shouldInterceptHttpsReq(req);

//bypass webSocket on webinterface
if(targetPort == 8003){
    shouldIntercept = false; // TODO : a more general solution?
}

logUtil.printLog(color.green("\nreceived https CONNECT request " + host));
...
```

#### <a name="apidoc.element.anyproxy.rule__blank.shouldUseLocalResponse"></a>[function <span class="apidocSignatureSpan">anyproxy.rule__blank.</span>shouldUseLocalResponse (req, reqBody)](#apidoc.element.anyproxy.rule__blank.shouldUseLocalResponse)
- description and source-code
```javascript
shouldUseLocalResponse = function (req, reqBody){
        return false;
	}
```
- example usage
```shell
...

        callback();
    });
}

//route to dealing function
function routeReq(callback){
    if(userRule.shouldUseLocalResponse(req,reqData)){
        logUtil.printLog("==>use local rules");
        dealWithLocalResponse(callback);
    }else{
        logUtil.printLog("==>will forward to real server by proxy");
        dealWithRemoteResonse(callback);
    }
}
...
```

#### <a name="apidoc.element.anyproxy.rule__blank.summary"></a>[function <span class="apidocSignatureSpan">anyproxy.rule__blank.</span>summary ()](#apidoc.element.anyproxy.rule__blank.summary)
- description and source-code
```javascript
summary = function (){
    return "this is a blank rule for AnyProxy";
}
```
- example usage
```shell
...
if('function' == typeof(userRule.init)){
    functions.push(function(cb){
        userRule.init(cb);
    });
}
if('function' == typeof(userRule.summary)){
    functions.push(function(cb){
        logUtil.printLog(userRule.summary());
        cb(null);
    });
}
async.series(functions,function(errors,result){
    if(!errors){
        logUtil.printLog(color.green('Anyproxy rules initialize finished, have fun!'));
    }
...
```



# <a name="apidoc.module.anyproxy.rule_adjust_response_time"></a>[module anyproxy.rule_adjust_response_time](#apidoc.module.anyproxy.rule_adjust_response_time)

#### <a name="apidoc.element.anyproxy.rule_adjust_response_time.pauseBeforeSendingResponse"></a>[function <span class="apidocSignatureSpan">anyproxy.rule_adjust_response_time.</span>pauseBeforeSendingResponse (req, res)](#apidoc.element.anyproxy.rule_adjust_response_time.pauseBeforeSendingResponse)
- description and source-code
```javascript
pauseBeforeSendingResponse = function (req, res){
    //delay all the response for 1500ms
    return 1500;
}
```
- example usage
```shell
...
        });
    }else{
        callback();
    }

//delay
},function(callback){
var pauseTimeInMS = userRule.pauseBeforeSendingResponse(req,res);
    if(pauseTimeInMS){
        setTimeout(callback,pauseTimeInMS);
    }else{
        callback();
    }

//send response
...
```



# <a name="apidoc.module.anyproxy.rule_allow_CORS"></a>[module anyproxy.rule_allow_CORS](#apidoc.module.anyproxy.rule_allow_CORS)

#### <a name="apidoc.element.anyproxy.rule_allow_CORS.dealLocalResponse"></a>[function <span class="apidocSignatureSpan">anyproxy.rule_allow_CORS.</span>dealLocalResponse (req, reqBody, callback)](#apidoc.element.anyproxy.rule_allow_CORS.dealLocalResponse)
- description and source-code
```javascript
dealLocalResponse = function (req, reqBody, callback){
    if(req.method == "OPTIONS"){
        callback(200,mergeCORSHeader(req.headers),"");
    }
}
```
- example usage
```shell
...
        }else{
logUtil.printLog("==>will forward to real server by proxy");
dealWithRemoteResonse(callback);
        }
    }

    function dealWithLocalResponse(callback){
        userRule.dealLocalResponse(req,reqData,function(statusCode,resHeader,resBody){

//update record info
resourceInfo.endTime = new Date().getTime();
resourceInfo.res     = { //construct a self-defined res object
    statusCode : statusCode || "",
    headers    : resHeader  || {}
}
...
```

#### <a name="apidoc.element.anyproxy.rule_allow_CORS.replaceResponseHeader"></a>[function <span class="apidocSignatureSpan">anyproxy.rule_allow_CORS.</span>replaceResponseHeader (req, res, header)](#apidoc.element.anyproxy.rule_allow_CORS.replaceResponseHeader)
- description and source-code
```javascript
replaceResponseHeader = function (req, res, header){
    return mergeCORSHeader(req.headers, header);
}
```
- example usage
```shell
...
        //send request
        var proxyReq = ( /https/.test(protocol) ? https : http).request(options, function(res) {

//deal response header
var statusCode = res.statusCode;
statusCode = userRule.replaceResponseStatusCode(req,res,statusCode) || statusCode;

var resHeader = userRule.replaceResponseHeader(req,res,res.headers) || res.headers;
resHeader = util.lower_keys(resHeader);

// remove gzip related header, and ungzip the content
// note there are other compression types like deflate
var ifServerGzipped =  /gzip/i.test(resHeader['content-encoding']);
if(ifServerGzipped){
    delete resHeader['content-encoding'];
...
```

#### <a name="apidoc.element.anyproxy.rule_allow_CORS.shouldUseLocalResponse"></a>[function <span class="apidocSignatureSpan">anyproxy.rule_allow_CORS.</span>shouldUseLocalResponse (req, reqBody)](#apidoc.element.anyproxy.rule_allow_CORS.shouldUseLocalResponse)
- description and source-code
```javascript
shouldUseLocalResponse = function (req, reqBody){
    //intercept all options request
    if(req.method == "OPTIONS"){
        return true;
    }else{
        return false;
    }
}
```
- example usage
```shell
...

        callback();
    });
}

//route to dealing function
function routeReq(callback){
    if(userRule.shouldUseLocalResponse(req,reqData)){
        logUtil.printLog("==>use local rules");
        dealWithLocalResponse(callback);
    }else{
        logUtil.printLog("==>will forward to real server by proxy");
        dealWithRemoteResonse(callback);
    }
}
...
```



# <a name="apidoc.module.anyproxy.rule_default"></a>[module anyproxy.rule_default](#apidoc.module.anyproxy.rule_default)

#### <a name="apidoc.element.anyproxy.rule_default._getCustomMenu"></a>[function <span class="apidocSignatureSpan">anyproxy.rule_default.</span>_getCustomMenu ()](#apidoc.element.anyproxy.rule_default._getCustomMenu)
- description and source-code
```javascript
_getCustomMenu = function (){
    return [
        // {
        //     name:"test",
        //     icon:"uk-icon-lemon-o",
        //     url :"http://anyproxy.io"
        // }
    ];
}
```
- example usage
```shell
...
    userRule      = config.userRule,
    ruleSummary   = "",
    customMenu    = [],
    server;

try{
    ruleSummary = userRule.summary();
    customMenu  = userRule._getCustomMenu();
}catch(e){}

var self         = this,
    myAbsAddress = "http://" + ipAddress + ":" + port +"/",
    crtFilePath  = certMgr.getRootCAFilePath(),
    staticDir    = path.join(__dirname,'../web');
...
```

#### <a name="apidoc.element.anyproxy.rule_default._plugIntoWebinterface"></a>[function <span class="apidocSignatureSpan">anyproxy.rule_default.</span>_plugIntoWebinterface (app, cb)](#apidoc.element.anyproxy.rule_default._plugIntoWebinterface)
- description and source-code
```javascript
_plugIntoWebinterface = function (app, cb){

    app.get("/filetree",function(req,res){
        try{
            var root = req.query.root || utils.getUserHome() || "/";
            utils.filewalker(root,function(err, info){
                res.json(info);
            });
        }catch(e){
            res.end(e);
        }
    });

    app.use(bodyParser.json());
    app.get("/getMapConfig",function(req,res){
        res.json(mapConfig);
    });
    app.post("/setMapConfig",function(req,res){
        mapConfig = req.body;
        res.json(mapConfig);

        saveMapConfig(mapConfig);
    });

    cb();
}
```
- example usage
```shell
...
    }
});

app.use(express.static(staticDir));

//plugin from rule file
if(typeof userRule._plugIntoWebinterface == "function"){
    userRule._plugIntoWebinterface(app,function(){
        server = app.listen(port);
    });
}else{
    server = app.listen(port);
}

self.app    = app;
...
```

#### <a name="apidoc.element.anyproxy.rule_default.dealLocalResponse"></a>[function <span class="apidocSignatureSpan">anyproxy.rule_default.</span>dealLocalResponse (req, reqBody, callback)](#apidoc.element.anyproxy.rule_default.dealLocalResponse)
- description and source-code
```javascript
dealLocalResponse = function (req, reqBody, callback){
    if(req.anyproxy_map_local){
        fs.readFile(req.anyproxy_map_local,function(err,buffer){
            if(err){
                callback(200, {}, "[AnyProxy failed to load local file] " + err);
            }else{
                var header = {
                    'Content-Type': utils.contentType(req.anyproxy_map_local)
                };
                callback(200, header, buffer);
            }
        });
    }
}
```
- example usage
```shell
...
        }else{
logUtil.printLog("==>will forward to real server by proxy");
dealWithRemoteResonse(callback);
        }
    }

    function dealWithLocalResponse(callback){
        userRule.dealLocalResponse(req,reqData,function(statusCode,resHeader,resBody){

//update record info
resourceInfo.endTime = new Date().getTime();
resourceInfo.res     = { //construct a self-defined res object
    statusCode : statusCode || "",
    headers    : resHeader  || {}
}
...
```

#### <a name="apidoc.element.anyproxy.rule_default.fetchTrafficData"></a>[function <span class="apidocSignatureSpan">anyproxy.rule_default.</span>fetchTrafficData (id, info)](#apidoc.element.anyproxy.rule_default.fetchTrafficData)
- description and source-code
```javascript
fetchTrafficData = function (id, info){}
```
- example usage
```shell
...

        global.recorder && global.recorder.updateRecord(resourceInfoId,resourceInfo);

        callback();

    //push trafic data to rule file
    },function(callback){
        userRule.fetchTrafficData && userRule.fetchTrafficData(resourceInfoId,resourceInfo);
        callback();

    }

],function(err,result){
    callback && callback();
});
...
```

#### <a name="apidoc.element.anyproxy.rule_default.pauseBeforeSendingResponse"></a>[function <span class="apidocSignatureSpan">anyproxy.rule_default.</span>pauseBeforeSendingResponse (req, res)](#apidoc.element.anyproxy.rule_default.pauseBeforeSendingResponse)
- description and source-code
```javascript
pauseBeforeSendingResponse = function (req, res){
}
```
- example usage
```shell
...
        });
    }else{
        callback();
    }

//delay
},function(callback){
var pauseTimeInMS = userRule.pauseBeforeSendingResponse(req,res);
    if(pauseTimeInMS){
        setTimeout(callback,pauseTimeInMS);
    }else{
        callback();
    }

//send response
...
```

#### <a name="apidoc.element.anyproxy.rule_default.replaceRequestData"></a>[function <span class="apidocSignatureSpan">anyproxy.rule_default.</span>replaceRequestData (req, data)](#apidoc.element.anyproxy.rule_default.replaceRequestData)
- description and source-code
```javascript
replaceRequestData = function (req, data){
}
```
- example usage
```shell
...
options = userRule.replaceRequestOption(req,options) || options;
options.rejectUnauthorized = false;
try{
    delete options.headers['accept-encoding']; //avoid gzipped response
}catch(e){}

//update request data
reqData = userRule.replaceRequestData(req,reqData) || reqData;
options.headers = util.lower_keys(options.headers);
options.headers["content-length"] = reqData.length; //rewrite content length info

options.headers = util.upper_keys(options.headers);

//send request
var proxyReq = ( /https/.test(protocol) ? https : http).request(options, function(res) {
...
```

#### <a name="apidoc.element.anyproxy.rule_default.replaceRequestOption"></a>[function <span class="apidocSignatureSpan">anyproxy.rule_default.</span>replaceRequestOption (req, option)](#apidoc.element.anyproxy.rule_default.replaceRequestOption)
- description and source-code
```javascript
replaceRequestOption = function (req, option){
}
```
- example usage
```shell
...
    hostname : urlPattern.hostname || req.headers.host,
    port     : urlPattern.port || req.port || (/https/.test(protocol) ? 443 : 80),
    path     : path,
    method   : req.method,
    headers  : req.headers
};

options = userRule.replaceRequestOption(req,options) || options;
options.rejectUnauthorized = false;
try{
    delete options.headers['accept-encoding']; //avoid gzipped response
}catch(e){}

//update request data
reqData = userRule.replaceRequestData(req,reqData) || reqData;
...
```

#### <a name="apidoc.element.anyproxy.rule_default.replaceRequestProtocol"></a>[function <span class="apidocSignatureSpan">anyproxy.rule_default.</span>replaceRequestProtocol (req, protocol)](#apidoc.element.anyproxy.rule_default.replaceRequestProtocol)
- description and source-code
```javascript
replaceRequestProtocol = function (req, protocol){
}
```
- example usage
```shell
...
return;
    }

    function dealWithRemoteResonse(callback){
var options;

//modify request protocol
protocol = userRule.replaceRequestProtocol(req,protocol) || protocol;

//modify request options
options = {
    hostname : urlPattern.hostname || req.headers.host,
    port     : urlPattern.port || req.port || (/https/.test(protocol) ? 443 : 80),
    path     : path,
    method   : req.method,
...
```

#### <a name="apidoc.element.anyproxy.rule_default.replaceResponseHeader"></a>[function <span class="apidocSignatureSpan">anyproxy.rule_default.</span>replaceResponseHeader (req, res, header)](#apidoc.element.anyproxy.rule_default.replaceResponseHeader)
- description and source-code
```javascript
replaceResponseHeader = function (req, res, header){
}
```
- example usage
```shell
...
        //send request
        var proxyReq = ( /https/.test(protocol) ? https : http).request(options, function(res) {

//deal response header
var statusCode = res.statusCode;
statusCode = userRule.replaceResponseStatusCode(req,res,statusCode) || statusCode;

var resHeader = userRule.replaceResponseHeader(req,res,res.headers) || res.headers;
resHeader = util.lower_keys(resHeader);

// remove gzip related header, and ungzip the content
// note there are other compression types like deflate
var ifServerGzipped =  /gzip/i.test(resHeader['content-encoding']);
if(ifServerGzipped){
    delete resHeader['content-encoding'];
...
```

#### <a name="apidoc.element.anyproxy.rule_default.replaceResponseStatusCode"></a>[function <span class="apidocSignatureSpan">anyproxy.rule_default.</span>replaceResponseStatusCode (req, res, statusCode)](#apidoc.element.anyproxy.rule_default.replaceResponseStatusCode)
- description and source-code
```javascript
replaceResponseStatusCode = function (req, res, statusCode){
}
```
- example usage
```shell
...
        options.headers = util.upper_keys(options.headers);

        //send request
        var proxyReq = ( /https/.test(protocol) ? https : http).request(options, function(res) {

//deal response header
var statusCode = res.statusCode;
statusCode = userRule.replaceResponseStatusCode(req,res,statusCode) || statusCode;

var resHeader = userRule.replaceResponseHeader(req,res,res.headers) || res.headers;
resHeader = util.lower_keys(resHeader);

// remove gzip related header, and ungzip the content
// note there are other compression types like deflate
var ifServerGzipped =  /gzip/i.test(resHeader['content-encoding']);
...
```

#### <a name="apidoc.element.anyproxy.rule_default.replaceServerResDataAsync"></a>[function <span class="apidocSignatureSpan">anyproxy.rule_default.</span>replaceServerResDataAsync (req, res, serverResData, callback)](#apidoc.element.anyproxy.rule_default.replaceServerResDataAsync)
- description and source-code
```javascript
replaceServerResDataAsync = function (req, res, serverResData, callback){
    callback(serverResData);
}
```
- example usage
```shell
...
//get custom response
},function(callback){
    if(userRule.replaceServerResData){
        logUtil.printLog(color.red("replaceServerResData is deprecated, and will be unavilable soon. Use replaceServerResDataAsync
 instead."), logUtil.T_ERR);
        serverResData = userRule.replaceServerResData(req,res,serverResData) || serverResData;
        callback();
    }else if(userRule.replaceServerResDataAsync){
        userRule.replaceServerResDataAsync(req,res,serverResData,function(newRes){
            serverResData = newRes;
            callback();
        });
    }else{
        callback();
    }
...
```

#### <a name="apidoc.element.anyproxy.rule_default.setInterceptFlag"></a>[function <span class="apidocSignatureSpan">anyproxy.rule_default.</span>setInterceptFlag (flag)](#apidoc.element.anyproxy.rule_default.setInterceptFlag)
- description and source-code
```javascript
setInterceptFlag = function (flag){
    interceptFlag = flag && isRootCAFileExists;
}
```
- example usage
```shell
...
    if(!!option.interceptHttps){
if (!certMgr.isRootCAFileExists()) {
    util.showRootInstallTip();
    process.exit(0);
    return;
}

currentRule.setInterceptFlag(true);

//print a tip when using https features in Node < v0.12
var nodeVersion = Number(process.version.match(/^v(\d+\.\d+)/)[1]);
if(nodeVersion < 0.12){
    logUtil.printLog(color.red("node >= v0.12 is required when trying to intercept HTTPS requests :("), logUtil.T_ERR);
}
...
```

#### <a name="apidoc.element.anyproxy.rule_default.shouldInterceptHttpsReq"></a>[function <span class="apidocSignatureSpan">anyproxy.rule_default.</span>shouldInterceptHttpsReq (req)](#apidoc.element.anyproxy.rule_default.shouldInterceptHttpsReq)
- description and source-code
```javascript
shouldInterceptHttpsReq = function (req){
    return interceptFlag;
}
```
- example usage
```shell
...

function connectReqHandler(req, socket, head){
var host      = req.url.split(":")[0],
    targetPort= req.url.split(":")[1],
    resourceInfo,
    resourceInfoId;

var shouldIntercept = userRule.shouldInterceptHttpsReq(req);

//bypass webSocket on webinterface
if(targetPort == 8003){
    shouldIntercept = false; // TODO : a more general solution?
}

logUtil.printLog(color.green("\nreceived https CONNECT request " + host));
...
```

#### <a name="apidoc.element.anyproxy.rule_default.shouldUseLocalResponse"></a>[function <span class="apidocSignatureSpan">anyproxy.rule_default.</span>shouldUseLocalResponse (req, reqBody)](#apidoc.element.anyproxy.rule_default.shouldUseLocalResponse)
- description and source-code
```javascript
shouldUseLocalResponse = function (req, reqBody){
    //intercept all options request
    var simpleUrl = (req.headers.host || "") + (req.url || "");
    mapConfig.map(function(item){
        var key = item.keyword;
        if(simpleUrl.indexOf(key) >= 0){
            req.anyproxy_map_local = item.local;
            return false;
        }
    });


    return !!req.anyproxy_map_local;
}
```
- example usage
```shell
...

        callback();
    });
}

//route to dealing function
function routeReq(callback){
    if(userRule.shouldUseLocalResponse(req,reqData)){
        logUtil.printLog("==>use local rules");
        dealWithLocalResponse(callback);
    }else{
        logUtil.printLog("==>will forward to real server by proxy");
        dealWithRemoteResonse(callback);
    }
}
...
```

#### <a name="apidoc.element.anyproxy.rule_default.summary"></a>[function <span class="apidocSignatureSpan">anyproxy.rule_default.</span>summary ()](#apidoc.element.anyproxy.rule_default.summary)
- description and source-code
```javascript
summary = function (){
    var tip = "the default rule for AnyProxy.";
    if(!isRootCAFileExists){
        tip += "\nRoot CA does not exist, will not intercept any https requests.";
    }
    return tip;
}
```
- example usage
```shell
...
if('function' == typeof(userRule.init)){
    functions.push(function(cb){
        userRule.init(cb);
    });
}
if('function' == typeof(userRule.summary)){
    functions.push(function(cb){
        logUtil.printLog(userRule.summary());
        cb(null);
    });
}
async.series(functions,function(errors,result){
    if(!errors){
        logUtil.printLog(color.green('Anyproxy rules initialize finished, have fun!'));
    }
...
```



# <a name="apidoc.module.anyproxy.rule_intercept_some_https_requests"></a>[module anyproxy.rule_intercept_some_https_requests](#apidoc.module.anyproxy.rule_intercept_some_https_requests)

#### <a name="apidoc.element.anyproxy.rule_intercept_some_https_requests.replaceServerResDataAsync"></a>[function <span class="apidocSignatureSpan">anyproxy.rule_intercept_some_https_requests.</span>replaceServerResDataAsync (req, res, serverResData, callback)](#apidoc.element.anyproxy.rule_intercept_some_https_requests.replaceServerResDataAsync)
- description and source-code
```javascript
replaceServerResDataAsync = function (req, res, serverResData, callback){
    //add "hello github" to all github pages
    if(req.headers.host == "github.com"){
        serverResData += "hello github";
    }
    callback(serverResData);
}
```
- example usage
```shell
...
//get custom response
},function(callback){
    if(userRule.replaceServerResData){
        logUtil.printLog(color.red("replaceServerResData is deprecated, and will be unavilable soon. Use replaceServerResDataAsync
 instead."), logUtil.T_ERR);
        serverResData = userRule.replaceServerResData(req,res,serverResData) || serverResData;
        callback();
    }else if(userRule.replaceServerResDataAsync){
        userRule.replaceServerResDataAsync(req,res,serverResData,function(newRes){
            serverResData = newRes;
            callback();
        });
    }else{
        callback();
    }
...
```

#### <a name="apidoc.element.anyproxy.rule_intercept_some_https_requests.shouldInterceptHttpsReq"></a>[function <span class="apidocSignatureSpan">anyproxy.rule_intercept_some_https_requests.</span>shouldInterceptHttpsReq (req)](#apidoc.element.anyproxy.rule_intercept_some_https_requests.shouldInterceptHttpsReq)
- description and source-code
```javascript
shouldInterceptHttpsReq = function (req){
    //intercept https://github.com/
    //otherwise, all the https traffic will not go through this proxy

    // return true;
    if(req.headers.host == "github.com"){
        return true;
    }else{
        return false;
    }
}
```
- example usage
```shell
...

function connectReqHandler(req, socket, head){
var host      = req.url.split(":")[0],
    targetPort= req.url.split(":")[1],
    resourceInfo,
    resourceInfoId;

var shouldIntercept = userRule.shouldInterceptHttpsReq(req);

//bypass webSocket on webinterface
if(targetPort == 8003){
    shouldIntercept = false; // TODO : a more general solution?
}

logUtil.printLog(color.green("\nreceived https CONNECT request " + host));
...
```



# <a name="apidoc.module.anyproxy.rule_remove_cache_header"></a>[module anyproxy.rule_remove_cache_header](#apidoc.module.anyproxy.rule_remove_cache_header)

#### <a name="apidoc.element.anyproxy.rule_remove_cache_header.replaceRequestOption"></a>[function <span class="apidocSignatureSpan">anyproxy.rule_remove_cache_header.</span>replaceRequestOption (req, option)](#apidoc.element.anyproxy.rule_remove_cache_header.replaceRequestOption)
- description and source-code
```javascript
replaceRequestOption = function (req, option){
	    var newOption = option;
	    delete newOption.headers['if-none-match'];
	    delete newOption.headers['if-modified-since'];

	    return newOption;
	}
```
- example usage
```shell
...
    hostname : urlPattern.hostname || req.headers.host,
    port     : urlPattern.port || req.port || (/https/.test(protocol) ? 443 : 80),
    path     : path,
    method   : req.method,
    headers  : req.headers
};

options = userRule.replaceRequestOption(req,options) || options;
options.rejectUnauthorized = false;
try{
    delete options.headers['accept-encoding']; //avoid gzipped response
}catch(e){}

//update request data
reqData = userRule.replaceRequestData(req,reqData) || reqData;
...
```

#### <a name="apidoc.element.anyproxy.rule_remove_cache_header.replaceResponseHeader"></a>[function <span class="apidocSignatureSpan">anyproxy.rule_remove_cache_header.</span>replaceResponseHeader (req, res, header)](#apidoc.element.anyproxy.rule_remove_cache_header.replaceResponseHeader)
- description and source-code
```javascript
replaceResponseHeader = function (req, res, header){
    header = header || {};
    header["Cache-Control"]                    = "no-cache, no-store, must-revalidate";
    header["Pragma"]                           = "no-cache";
    header["Expires"]                          = 0;

    return header;
}
```
- example usage
```shell
...
        //send request
        var proxyReq = ( /https/.test(protocol) ? https : http).request(options, function(res) {

//deal response header
var statusCode = res.statusCode;
statusCode = userRule.replaceResponseStatusCode(req,res,statusCode) || statusCode;

var resHeader = userRule.replaceResponseHeader(req,res,res.headers) || res.headers;
resHeader = util.lower_keys(resHeader);

// remove gzip related header, and ungzip the content
// note there are other compression types like deflate
var ifServerGzipped =  /gzip/i.test(resHeader['content-encoding']);
if(ifServerGzipped){
    delete resHeader['content-encoding'];
...
```



# <a name="apidoc.module.anyproxy.rule_replace_request_option"></a>[module anyproxy.rule_replace_request_option](#apidoc.module.anyproxy.rule_replace_request_option)

#### <a name="apidoc.element.anyproxy.rule_replace_request_option.replaceRequestOption"></a>[function <span class="apidocSignatureSpan">anyproxy.rule_replace_request_option.</span>replaceRequestOption (req, option)](#apidoc.element.anyproxy.rule_replace_request_option.replaceRequestOption)
- description and source-code
```javascript
replaceRequestOption = function (req, option){
    //replace request towards http://www.taobao.com
    //                     to http://www.taobao.com/about/

<span class="apidocCodeCommentSpan">    /*
    option scheme:
    {
        hostname : "www.taobao.com"
        port     : 80
        path     : "/"
        method   : "GET"
        headers  : {cookie:""}
    }
    */
</span>    if(option.hostname == "www.taobao.com" && option.path == "/"){
        option.path = "/about/";
    }
}
```
- example usage
```shell
...
    hostname : urlPattern.hostname || req.headers.host,
    port     : urlPattern.port || req.port || (/https/.test(protocol) ? 443 : 80),
    path     : path,
    method   : req.method,
    headers  : req.headers
};

options = userRule.replaceRequestOption(req,options) || options;
options.rejectUnauthorized = false;
try{
    delete options.headers['accept-encoding']; //avoid gzipped response
}catch(e){}

//update request data
reqData = userRule.replaceRequestData(req,reqData) || reqData;
...
```



# <a name="apidoc.module.anyproxy.rule_replace_response_data"></a>[module anyproxy.rule_replace_response_data](#apidoc.module.anyproxy.rule_replace_response_data)

#### <a name="apidoc.element.anyproxy.rule_replace_response_data.replaceServerResDataAsync"></a>[function <span class="apidocSignatureSpan">anyproxy.rule_replace_response_data.</span>replaceServerResDataAsync (req, res, serverResData, callback)](#apidoc.element.anyproxy.rule_replace_response_data.replaceServerResDataAsync)
- description and source-code
```javascript
replaceServerResDataAsync = function (req, res, serverResData, callback){
    //append "hello world" to all web pages

    //for those non-unicode response , serverResData.toString() should not be your first choice.
    //this issue may help you understanding how to modify an non-unicode response: https://github.com/alibaba/anyproxy/issues/20
    if(/html/i.test(res.headers['content-type'])){
        var newDataStr = serverResData.toString();
        newDataStr += "hello world!";
        callback(newDataStr);
    }else{
        callback(serverResData);
    }

}
```
- example usage
```shell
...
//get custom response
},function(callback){
    if(userRule.replaceServerResData){
        logUtil.printLog(color.red("replaceServerResData is deprecated, and will be unavilable soon. Use replaceServerResDataAsync
 instead."), logUtil.T_ERR);
        serverResData = userRule.replaceServerResData(req,res,serverResData) || serverResData;
        callback();
    }else if(userRule.replaceServerResDataAsync){
        userRule.replaceServerResDataAsync(req,res,serverResData,function(newRes){
            serverResData = newRes;
            callback();
        });
    }else{
        callback();
    }
...
```



# <a name="apidoc.module.anyproxy.rule_replace_response_status_code"></a>[module anyproxy.rule_replace_response_status_code](#apidoc.module.anyproxy.rule_replace_response_status_code)

#### <a name="apidoc.element.anyproxy.rule_replace_response_status_code.replaceResponseHeader"></a>[function <span class="apidocSignatureSpan">anyproxy.rule_replace_response_status_code.</span>replaceResponseHeader (req, res, header)](#apidoc.element.anyproxy.rule_replace_response_status_code.replaceResponseHeader)
- description and source-code
```javascript
replaceResponseHeader = function (req, res, header){
    if(req.headers.host == "www.taobao.com"){
        header.location = "http://www.etao.com";
    }

    return header;
}
```
- example usage
```shell
...
        //send request
        var proxyReq = ( /https/.test(protocol) ? https : http).request(options, function(res) {

//deal response header
var statusCode = res.statusCode;
statusCode = userRule.replaceResponseStatusCode(req,res,statusCode) || statusCode;

var resHeader = userRule.replaceResponseHeader(req,res,res.headers) || res.headers;
resHeader = util.lower_keys(resHeader);

// remove gzip related header, and ungzip the content
// note there are other compression types like deflate
var ifServerGzipped =  /gzip/i.test(resHeader['content-encoding']);
if(ifServerGzipped){
    delete resHeader['content-encoding'];
...
```

#### <a name="apidoc.element.anyproxy.rule_replace_response_status_code.replaceResponseStatusCode"></a>[function <span class="apidocSignatureSpan">anyproxy.rule_replace_response_status_code.</span>replaceResponseStatusCode (req, res, statusCode)](#apidoc.element.anyproxy.rule_replace_response_status_code.replaceResponseStatusCode)
- description and source-code
```javascript
replaceResponseStatusCode = function (req, res, statusCode){
    //redirect requests toward http://www.taobao.com/*
    //                      to http://www.etao.com
    //using 302

    if(req.headers.host == "www.taobao.com"){
        statusCode = 302;
    }

    return statusCode;
}
```
- example usage
```shell
...
        options.headers = util.upper_keys(options.headers);

        //send request
        var proxyReq = ( /https/.test(protocol) ? https : http).request(options, function(res) {

//deal response header
var statusCode = res.statusCode;
statusCode = userRule.replaceResponseStatusCode(req,res,statusCode) || statusCode;

var resHeader = userRule.replaceResponseHeader(req,res,res.headers) || res.headers;
resHeader = util.lower_keys(resHeader);

// remove gzip related header, and ungzip the content
// note there are other compression types like deflate
var ifServerGzipped =  /gzip/i.test(resHeader['content-encoding']);
...
```



# <a name="apidoc.module.anyproxy.rule_use_local_data"></a>[module anyproxy.rule_use_local_data](#apidoc.module.anyproxy.rule_use_local_data)

#### <a name="apidoc.element.anyproxy.rule_use_local_data.dealLocalResponse"></a>[function <span class="apidocSignatureSpan">anyproxy.rule_use_local_data.</span>dealLocalResponse (req, reqBody, callback)](#apidoc.element.anyproxy.rule_use_local_data.dealLocalResponse)
- description and source-code
```javascript
dealLocalResponse = function (req, reqBody, callback){
    if(req.replaceLocalFile){
        callback(200, {"content-type":"image/png"}, fs.readFileSync(LOCAL_IMAGE) );
    }
}
```
- example usage
```shell
...
        }else{
logUtil.printLog("==>will forward to real server by proxy");
dealWithRemoteResonse(callback);
        }
    }

    function dealWithLocalResponse(callback){
        userRule.dealLocalResponse(req,reqData,function(statusCode,resHeader,resBody){

//update record info
resourceInfo.endTime = new Date().getTime();
resourceInfo.res     = { //construct a self-defined res object
    statusCode : statusCode || "",
    headers    : resHeader  || {}
}
...
```

#### <a name="apidoc.element.anyproxy.rule_use_local_data.shouldUseLocalResponse"></a>[function <span class="apidocSignatureSpan">anyproxy.rule_use_local_data.</span>shouldUseLocalResponse (req, reqBody)](#apidoc.element.anyproxy.rule_use_local_data.shouldUseLocalResponse)
- description and source-code
```javascript
shouldUseLocalResponse = function (req, reqBody){
    if(/\.(png|gif|jpg|jpeg)$/.test(req.url)){
        req.replaceLocalFile = true;
        return true;
    }else{
        return false;
    }
}
```
- example usage
```shell
...

        callback();
    });
}

//route to dealing function
function routeReq(callback){
    if(userRule.shouldUseLocalResponse(req,reqData)){
        logUtil.printLog("==>use local rules");
        dealWithLocalResponse(callback);
    }else{
        logUtil.printLog("==>will forward to real server by proxy");
        dealWithRemoteResonse(callback);
    }
}
...
```

#### <a name="apidoc.element.anyproxy.rule_use_local_data.summary"></a>[function <span class="apidocSignatureSpan">anyproxy.rule_use_local_data.</span>summary ()](#apidoc.element.anyproxy.rule_use_local_data.summary)
- description and source-code
```javascript
summary = function (){
    return "replace all the images with local one";
}
```
- example usage
```shell
...
if('function' == typeof(userRule.init)){
    functions.push(function(cb){
        userRule.init(cb);
    });
}
if('function' == typeof(userRule.summary)){
    functions.push(function(cb){
        logUtil.printLog(userRule.summary());
        cb(null);
    });
}
async.series(functions,function(errors,result){
    if(!errors){
        logUtil.printLog(color.green('Anyproxy rules initialize finished, have fun!'));
    }
...
```



# <a name="apidoc.module.anyproxy.systemProxyMgr"></a>[module anyproxy.systemProxyMgr](#apidoc.module.anyproxy.systemProxyMgr)

#### <a name="apidoc.element.anyproxy.systemProxyMgr.disableGlobalProxy"></a>[function <span class="apidocSignatureSpan">anyproxy.systemProxyMgr.</span>disableGlobalProxy (proxyType)](#apidoc.element.anyproxy.systemProxyMgr.disableGlobalProxy)
- description and source-code
```javascript
disableGlobalProxy = function (proxyType) {
   proxyType = proxyType || 'http';

   var networkType = macProxyManager.networkType || macProxyManager.getNetworkType();

   return /^http$/i.test(proxyType) ?

      // set http proxy
      execSync(
         'networksetup -setwebproxystate ${networkType} off'
            .replace("${networkType}", networkType)) :

      // set https proxy
      execSync(
         'networksetup -setsecurewebproxystate ${networkType} off'
            .replace("${networkType}", networkType));
}
```
- example usage
```shell
...
            //server status manager
            function(callback){
                process.on("exit",function(code){
logUtil.printLog('AnyProxy is about to exit with code: ' + code, logUtil.T_ERR);

if (option.setAsGlobalProxy) {
    console.log('resigning global proxy...');
    var result = SystemProxyMgr.disableGlobalProxy(proxyType == T_TYPE_HTTP ? "Http" : "Https");

    if (result.status) {
        console.log(color.red(result.stdout));
    } else{
        console.log('global proxy resigned.');
    }
}
...
```

#### <a name="apidoc.element.anyproxy.systemProxyMgr.enableGlobalProxy"></a>[function <span class="apidocSignatureSpan">anyproxy.systemProxyMgr.</span>enableGlobalProxy (ip, port, proxyType)](#apidoc.element.anyproxy.systemProxyMgr.enableGlobalProxy)
- description and source-code
```javascript
enableGlobalProxy = function (ip, port, proxyType) {

   if (!ip || !port) {
      console.log('failed to set global proxy server.\n ip and port are required.');
      return;
   };

   proxyType = proxyType || 'http';

   var networkType = macProxyManager.networkType || macProxyManager.getNetworkType();

   return /^http$/i.test(proxyType) ?

      // set http proxy
      execSync(
         'networksetup -setwebproxy ${networkType} ${ip} ${port}'
            .replace("${networkType}", networkType)
            .replace("${ip}", ip)
            .replace("${port}", port)) :

      // set https proxy
      execSync('networksetup -setsecurewebproxy ${networkType} ${ip} ${port}'
        .replace("${networkType}", networkType)
        .replace("${ip}", ip)
        .replace("${port}", port));

}
```
- example usage
```shell
...
//set global proxy
function(callback) {
    if (option.setAsGlobalProxy) {
        console.log('setting global proxy for you...');
        if(!/^win/.test(process.platform) && !process.env.SUDO_UID){
            console.log('sudo password may be required.');
        }
        var result = SystemProxyMgr.enableGlobalProxy(ip.address(), proxyPort, proxyType == T_TYPE_HTTP ? "Http" : "Https");
        if (result.status) {
            callback(result.stdout);
        } else {
            if(/^win/.test(process.platform)){
                console.log('AnyProxy is now the default proxy for your system. It may take up to 1min to take effect.');
            } else{
                console.log('AnyProxy is now the default proxy for your system.');
...
```

#### <a name="apidoc.element.anyproxy.systemProxyMgr.getNetworkType"></a>[function <span class="apidocSignatureSpan">anyproxy.systemProxyMgr.</span>getNetworkType ()](#apidoc.element.anyproxy.systemProxyMgr.getNetworkType)
- description and source-code
```javascript
getNetworkType = function () {

   for (var i = 0; i < networkTypes.length; i++) {

      var
         type = networkTypes[i],
         result = execSync('networksetup -getwebproxy ' + type);

      if (result.status === 0) {
         macProxyManager.networkType = type;
         return type;
      }
   }

   throw new Error('Unknown network type');
}
```
- example usage
```shell
...
   if (!ip || !port) {
console.log('failed to set global proxy server.\n ip and port are required.');
return;
   };

   proxyType = proxyType || 'http';

   var networkType = macProxyManager.networkType || macProxyManager.getNetworkType();

   return /^http$/i.test(proxyType) ?

// set http proxy
execSync(
   'networksetup -setwebproxy ${networkType} ${ip} ${port}'
      .replace("${networkType}", networkType)
...
```

#### <a name="apidoc.element.anyproxy.systemProxyMgr.getProxyState"></a>[function <span class="apidocSignatureSpan">anyproxy.systemProxyMgr.</span>getProxyState ()](#apidoc.element.anyproxy.systemProxyMgr.getProxyState)
- description and source-code
```javascript
getProxyState = function () {
   var networkType = macProxyManager.networkType || macProxyManager.getNetworkType();
   var result = execSync('networksetup -getwebproxy ${networkType}'.replace('${networkType}', networkType));

   return result;
}
```
- example usage
```shell
n/a
```



# <a name="apidoc.module.anyproxy.util"></a>[module anyproxy.util](#apidoc.module.anyproxy.util)

#### <a name="apidoc.element.anyproxy.util.clearCacheDir"></a>[function <span class="apidocSignatureSpan">anyproxy.util.</span>clearCacheDir (cb)](#apidoc.element.anyproxy.util.clearCacheDir)
- description and source-code
```javascript
clearCacheDir = function (cb){
    var home  = util.getAnyProxyHome(),
        isWin = /^win/.test(process.platform);

    var dirNameWildCard = CACHE_DIR_PREFIX + "*";
    if(isWin){
        exec("for /D %f in (" + dirNameWildCard + ") do rmdir %f /s /q",{cwd : home},cb);
    }else{
        exec("rm -rf " + dirNameWildCard + "",{cwd : home},cb);
    }
}
```
- example usage
```shell
...

self.httpProxyServer = null;

async.series(
    [
        //clear cache dir, prepare recorder
        function(callback){
            util.clearCacheDir(function(){
                if(option.dbFile){
                    global.recorder = new Recorder({filename: option.dbFile});
                }else{
                    global.recorder = new Recorder();
                }
                callback();
            });
...
```

#### <a name="apidoc.element.anyproxy.util.contentLength"></a>[function <span class="apidocSignatureSpan">anyproxy.util.</span>contentLength (filepath)](#apidoc.element.anyproxy.util.contentLength)
- description and source-code
```javascript
contentLength = function (filepath) {
    try {
        var stat = fs.statSync(filepath);
        return stat.size;
    } catch (e) {
        logUtil.printLog(color.red("\nfailed to ready local file : " + filepath));
        logUtil.printLog(color.red(e));
        return 0;
    }
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.anyproxy.util.contentType"></a>[function <span class="apidocSignatureSpan">anyproxy.util.</span>contentType (filepath)](#apidoc.element.anyproxy.util.contentType)
- description and source-code
```javascript
contentType = function (filepath) {
    return mime.contentType(path.extname(filepath));
}
```
- example usage
```shell
...
dealLocalResponse : function(req,reqBody,callback){
    if(req.anyproxy_map_local){
        fs.readFile(req.anyproxy_map_local,function(err,buffer){
            if(err){
                callback(200, {}, "[AnyProxy failed to load local file] " + err);
            }else{
                var header = {
                    'Content-Type': utils.contentType(req.anyproxy_map_local)
                };
                callback(200, header, buffer);
            }
        });
    }
},
...
```

#### <a name="apidoc.element.anyproxy.util.filewalker"></a>[function <span class="apidocSignatureSpan">anyproxy.util.</span>filewalker (root, cb)](#apidoc.element.anyproxy.util.filewalker)
- description and source-code
```javascript
filewalker = function (root, cb){
    root = root || process.cwd();

    var ret = {
        directory :[],
        file      :[]
    };

    fs.readdir(root,function(err, list){
        if(list && list.length){
            list.map(function(item){
                var fullPath = path.join(root,item),
                    stat     = fs.lstatSync(fullPath);

                if(stat.isFile()){
                    ret.file.push({
                        name     : item,
                        fullPath : fullPath
                    });

                }else if(stat.isDirectory()){
                    ret.directory.push({
                        name     : item,
                        fullPath : fullPath
                    });
                }
            });
        }

        cb && cb.apply(null,[null,ret]);
    });
}
```
- example usage
```shell
...
    },

    _plugIntoWebinterface: function(app,cb){

app.get("/filetree",function(req,res){
    try{
        var root = req.query.root || utils.getUserHome() || "/";
        utils.filewalker(root,function(err, info){
            res.json(info);
        });
    }catch(e){
        res.end(e);
    }
});
...
```

#### <a name="apidoc.element.anyproxy.util.freshRequire"></a>[function <span class="apidocSignatureSpan">anyproxy.util.</span>freshRequire (path)](#apidoc.element.anyproxy.util.freshRequire)
- description and source-code
```javascript
freshRequire = function (path) {
    delete require.cache[require.resolve(path)];
    return require(path);
}
```
- example usage
```shell
...
    DEFAULT_PORT           = 8001,
    DEFAULT_WEB_PORT       = 8002, // port for web interface
    DEFAULT_WEBSOCKET_PORT = 8003, // internal web socket for web interface, not for end users
    DEFAULT_CONFIG_PORT    = 8088,
    DEFAULT_HOST           = "localhost",
    DEFAULT_TYPE           = T_TYPE_HTTP;

var default_rule = util.freshRequire('./rule_default');
var requestHandler = util.freshRequire('./requestHandler');

//option
//option.type     : 'http'(default) or 'https'
//option.port     : 8001(default)
//option.hostname : localhost(default)
//option.rule          : ruleModule
...
```

#### <a name="apidoc.element.anyproxy.util.generateCacheDir"></a>[function <span class="apidocSignatureSpan">anyproxy.util.</span>generateCacheDir ()](#apidoc.element.anyproxy.util.generateCacheDir)
- description and source-code
```javascript
generateCacheDir = function (){
    var rand      = Math.floor(Math.random() * 1000000),
        cachePath = path.join(util.getAnyProxyHome(),"./" + CACHE_DIR_PREFIX + rand);

    fs.mkdirSync(cachePath, '0777');
    return cachePath;
}
```
- example usage
```shell
...
proxyUtil = require("./util"),
logUtil   = require("./log");

//option.filename
function Recorder(option){
var self = this,
    id        = 1,
    cachePath = proxyUtil.generateCacheDir(),
    db;

option = option || {};
if(option.filename && typeof option.filename == "string"){
    try{
        if(fs.existsSync(option.filename)){
            fs.writeFileSync(option.filename,""); //empty original file
...
```

#### <a name="apidoc.element.anyproxy.util.getAnyProxyHome"></a>[function <span class="apidocSignatureSpan">anyproxy.util.</span>getAnyProxyHome ()](#apidoc.element.anyproxy.util.getAnyProxyHome)
- description and source-code
```javascript
getAnyProxyHome = function (){
    var home = path.join(util.getUserHome(),"/.anyproxy/");

    if(!fs.existsSync(home)){
        try{
            fs.mkdirSync(home, '0777');
        }catch(e){
            return null;
        }
    }

    return home;
}
```
- example usage
```shell
...
    interceptFlag      = false;

//e.g. [ { keyword: 'aaa', local: '/Users/Stella/061739.pdf' } ]
var mapConfig = [],
    configFile = "mapConfig.json";
function saveMapConfig(content,cb){
    new Promise(function(resolve,reject){
var anyproxyHome = utils.getAnyProxyHome(),
    mapCfgPath   = path.join(anyproxyHome,configFile);

if(typeof content == "object"){
    content = JSON.stringify(content);
}
resolve({
    path    :mapCfgPath,
...
```

#### <a name="apidoc.element.anyproxy.util.getUserHome"></a>[function <span class="apidocSignatureSpan">anyproxy.util.</span>getUserHome ()](#apidoc.element.anyproxy.util.getUserHome)
- description and source-code
```javascript
function getUserHome(){
    return process.env.HOME || process.env.USERPROFILE;
}
```
- example usage
```shell
...
var EasyCert = require('node-easy-cert');
var exec = require('child_process').exec;
var path = require('path');
var readline = require('readline');

var isWin = /^win/.test(process.platform);
var options = {
    rootDirPath: util.getUserHome() + '/.anyproxy_certs',
    defaultCertAttrs: [
        { name: 'countryName', value: 'CN' },
        { name: 'organizationName', value: 'AnyProxy' },
        { shortName: 'ST', value: 'SH' },
        { shortName: 'OU', value: 'AnyProxy SSL Proxy' }
    ]
};
...
```

#### <a name="apidoc.element.anyproxy.util.lower_keys"></a>[function <span class="apidocSignatureSpan">anyproxy.util.</span>lower_keys (obj)](#apidoc.element.anyproxy.util.lower_keys)
- description and source-code
```javascript
lower_keys = function (obj){
    for(var key in obj){
        var val = obj[key];
        delete obj[key];

        obj[key.toLowerCase()] = val;
    }

    return obj;
}
```
- example usage
```shell
...
options.rejectUnauthorized = false;
try{
    delete options.headers['accept-encoding']; //avoid gzipped response
}catch(e){}

//update request data
reqData = userRule.replaceRequestData(req,reqData) || reqData;
options.headers = util.lower_keys(options.headers);
options.headers["content-length"] = reqData.length; //rewrite content length info

options.headers = util.upper_keys(options.headers);

//send request
var proxyReq = ( /https/.test(protocol) ? https : http).request(options, function(res) {
...
```

#### <a name="apidoc.element.anyproxy.util.merge"></a>[function <span class="apidocSignatureSpan">anyproxy.util.</span>merge (baseObj, extendObj)](#apidoc.element.anyproxy.util.merge)
- description and source-code
```javascript
merge = function (baseObj, extendObj){
	for(var key in extendObj){
		baseObj[key] = extendObj[key];
	}

	return baseObj;
}
```
- example usage
```shell
...
    { name: 'organizationName', value: 'AnyProxy' },
    { shortName: 'ST', value: 'SH' },
    { shortName: 'OU', value: 'AnyProxy SSL Proxy' }
]
};

var easyCert = new EasyCert(options);
var crtMgr = util.merge({}, easyCert);

// catch specified error, such as ROOT_CA_NOT_EXISTS
crtMgr.getCertificate = function (host, cb) {
easyCert.getCertificate(host, (error, keyContent, crtContent) => {
    if (error === 'ROOT_CA_NOT_EXISTS') {
        util.showRootInstallTip();
        process.exit(0);
...
```

#### <a name="apidoc.element.anyproxy.util.showRootInstallTip"></a>[function <span class="apidocSignatureSpan">anyproxy.util.</span>showRootInstallTip ()](#apidoc.element.anyproxy.util.showRootInstallTip)
- description and source-code
```javascript
showRootInstallTip = function () {
    logUtil.printLog(color.red("can not find rootCA.crt or rootCA.key"), logUtil.T_ERR);
    logUtil.printLog(color.red("you may generate one by the following methods"), logUtil.T_ERR);
    logUtil.printLog(color.red("\twhen using globally : anyproxy --root"), logUtil.T_ERR);
    logUtil.printLog(color.red("\twhen using as a module : require(\"anyproxy\").generateRootCA();"), logUtil.T_ERR);
    logUtil.printLog(color.red("\tmore info : https://github.com/alibaba/anyproxy/wiki/How-to-config-https-proxy"), logUtil.T_ERR
);
}
```
- example usage
```shell
...
    // copy the rule to keep the original proxyRules independent
    proxyRules = Object.assign({}, proxyRules);

    var currentRule = requestHandler.setRules(proxyRules); //TODO : optimize calling for set rule

    if(!!option.interceptHttps){
if (!certMgr.isRootCAFileExists()) {
    util.showRootInstallTip();
    process.exit(0);
    return;
}

currentRule.setInterceptFlag(true);

//print a tip when using https features in Node < v0.12
...
```

#### <a name="apidoc.element.anyproxy.util.simpleRender"></a>[function <span class="apidocSignatureSpan">anyproxy.util.</span>simpleRender (str, object, regexp)](#apidoc.element.anyproxy.util.simpleRender)
- description and source-code
```javascript
simpleRender = function (str, object, regexp){
    return String(str).replace(regexp || (/\{\{([^{}]+)\}\}/g), function(match, name){
        if (match.charAt(0) == '\\') return match.slice(1);
        return (object[name] != null) ? object[name] : '';
    });
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.anyproxy.util.upper_keys"></a>[function <span class="apidocSignatureSpan">anyproxy.util.</span>upper_keys (obj)](#apidoc.element.anyproxy.util.upper_keys)
- description and source-code
```javascript
upper_keys = function (obj) {
    var upperObject = {};
    for(var key in obj) {
        var upperKey = changeCase.headerCase(key);
        upperObject[upperKey] = obj[key];
    }

    return upperObject;
}
```
- example usage
```shell
...
        }catch(e){}

        //update request data
        reqData = userRule.replaceRequestData(req,reqData) || reqData;
        options.headers = util.lower_keys(options.headers);
        options.headers["content-length"] = reqData.length; //rewrite content length info

        options.headers = util.upper_keys(options.headers);

        //send request
        var proxyReq = ( /https/.test(protocol) ? https : http).request(options, function(res) {

//deal response header
var statusCode = res.statusCode;
statusCode = userRule.replaceResponseStatusCode(req,res,statusCode) || statusCode;
...
```



# <a name="apidoc.module.anyproxy.webInterface"></a>[module anyproxy.webInterface](#apidoc.module.anyproxy.webInterface)

#### <a name="apidoc.element.anyproxy.webInterface.webInterface"></a>[function <span class="apidocSignatureSpan">anyproxy.</span>webInterface (config)](#apidoc.element.anyproxy.webInterface.webInterface)
- description and source-code
```javascript
function webInterface(config){
    var port = config.port,
        wsPort        = config.wsPort,
        ipAddress     = config.ip,
        userRule      = config.userRule,
        ruleSummary   = "",
        customMenu    = [],
        server;

    try{
        ruleSummary = userRule.summary();
        customMenu  = userRule._getCustomMenu();
    }catch(e){}

    var self         = this,
        myAbsAddress = "http://" + ipAddress + ":" + port +"/",
        crtFilePath  = certMgr.getRootCAFilePath(),
        staticDir    = path.join(__dirname,'../web');

    var app = express();
    app.use(compress()); //invoke gzip
    app.use(function(req, res, next) {
        res.setHeader("note", "THIS IS A REQUEST FROM ANYPROXY WEB INTERFACE");
        return next();
    });

    app.get("/lastestLog",function(req,res){
        recorder.getRecords(null,120,function(err,docs){
            if(err){
                res.end(err.toString());
            }else{
                res.json(docs);
            }
        });
    });

    app.get("/fetchBody",function(req,res){
        var query = req.query;
        if(query && query.id){
            global.recorder.getDecodedBody(query.id, function(err, result){
                if(err || !result || !result.content){
                    res.json({});
                }else if(result.type && result.type == "image" && result.mime){
                    if(query.raw){
                        //TODO : cache query result
                        res.type(result.mime).end(result.content);
                    }else{
                        res.json({
                            id      : query.id,
                            type    : result.type,
                            ref     : "/fetchBody?id=" + query.id + "&raw=true"
                        });
                    }
                }else{
                    res.json({
                        id      : query.id,
                        type    : result.type,
                        content : result.content
                    });
                }
            });
        }else{
            res.end({});
        }
    });

    app.get("/fetchCrtFile",function(req,res){
        if(crtFilePath){
            res.setHeader("Content-Type","application/x-x509-ca-cert");
            res.setHeader("Content-Disposition",'attachment; filename="rootCA.crt"');
            res.end(fs.readFileSync(crtFilePath,{encoding:null}));
        }else{
            res.setHeader("Content-Type","text/html");
            res.end("can not file rootCA ,plase use <strong>anyproxy --root</strong> to generate one");
        }
    });

    //make qr code
    app.get("/qr",function(req,res){
        var qr        = qrCode.qrcode(4, 'M'),
            targetUrl = myAbsAddress,
            qrImageTag,
            resDom;

        qr.addData(targetUrl);
        qr.make();
        qrImageTag = qr.createImgTag(4);

        resDom = '<a href="__url"> __img <br> click or scan qr code to start client </a>'.replace(/__url/,targetUrl).replace(/__img
/,qrImageTag);
        res.setHeader("Content-Type", "text/html");
        res.end(resDom);
    });

    app.get("/qr_root",function(req,res){
        var qr        = qrCode.qrcode(4, 'M'),
            targetUrl = myAbsAddress + "fetchCrtFile",
            qrImageTag,
            resDom;

        qr.addData(targetUrl);
        qr.make();
        qrImageTag = qr.createImgTag(4);

        resDom = '<a href="__url"> __img <br> click or scan qr code to download rootCA.crt </a>'.replace(/__url/,targetUrl).replace
(/__img/,qrImageTag);
        res.setHeader("Content-Type", "text/html");
        res.end(resDom);
    });

    app.use(function(req,res,next){
        var indexTpl  = fs.readFileSync(path.join(staticDir,"/index.html"),{encoding:"utf8"}),
            opt       = {
                rule        : ruleSummary || "",
                customMenu  : customMenu || [],
                wsPort      : wsPort,
                ipAddress   : ipAddress || "127.0.0.1"
            };

        if( url.parse(req.url).pathname == "/"){
            res.se ...
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.anyproxy.webInterface.super_"></a>[function <span class="apidocSignatureSpan">anyproxy.webInterface.</span>super_ ()](#apidoc.element.anyproxy.webInterface.super_)
- description and source-code
```javascript
function EventEmitter() {
  EventEmitter.init.call(this);
}
```
- example usage
```shell
n/a
```



# <a name="apidoc.module.anyproxy.wsServer"></a>[module anyproxy.wsServer](#apidoc.module.anyproxy.wsServer)

#### <a name="apidoc.element.anyproxy.wsServer.wsServer"></a>[function <span class="apidocSignatureSpan">anyproxy.</span>wsServer (config)](#apidoc.element.anyproxy.wsServer.wsServer)
- description and source-code
```javascript
function wsServer(config){
	//web socket interface
	var self = this,
        wss  = new WebSocketServer({port: config.port});
	wss.broadcast = function(data) {
        var key = data.id;
        if(typeof data == "object"){
            data = JSON.stringify(data);
        }

        for(var i in this.clients){
            try{
                this.clients[i].send(data);
            }catch(e){
                logUtil.printLog("websocket failed to send data, " + e, logUtil.T_ERR);
            }
        }
	};

	wss.on("connection",function(ws){
	    ws.on("message",function(msg){
	        resToMsg(msg,function(res){
	            res && ws.send(JSON.stringify(res));
	        });
	    });
	});

    wss.on("close",function(){});

	global.recorder.on("update",function(data){
        try{
    	    wss && wss.broadcast({
    	        type   : "update",
    	        content: data
    	    });

        }catch(e){
            console.log("ws error");
            console.log(e);
        }
	});

    self.wss = wss;
}
```
- example usage
```shell
n/a
```



# <a name="apidoc.module.anyproxy.wsServer.prototype"></a>[module anyproxy.wsServer.prototype](#apidoc.module.anyproxy.wsServer.prototype)

#### <a name="apidoc.element.anyproxy.wsServer.prototype.closeAll"></a>[function <span class="apidocSignatureSpan">anyproxy.wsServer.prototype.</span>closeAll ()](#apidoc.element.anyproxy.wsServer.prototype.closeAll)
- description and source-code
```javascript
closeAll = function (){
    var self = this;
    self.wss.close();
}
```
- example usage
```shell
...
                logUtil.printLog(err, logUtil.T_ERR);
            }
        }
    );

    self.close = function(){
        self.httpProxyServer && self.httpProxyServer.close();
        self.ws && self.ws.closeAll();
        self.webServerInstance && self.webServerInstance.server && self.webServerInstance.server.close();
        logUtil.printLog("server closed :" + proxyHost + ":" + proxyPort);
    }
}

module.exports.proxyServer        = proxyServer;
module.exports.generateRootCA     = certMgr.generateRootCA;
...
```



# misc
- this document was created with [utility2](https://github.com/kaizhu256/node-utility2)
