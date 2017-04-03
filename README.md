# api documentation for  [mailgun-js (v0.9.1)](https://github.com/bojand/mailgun-js)  [![npm package](https://img.shields.io/npm/v/npmdoc-mailgun-js.svg?style=flat-square)](https://www.npmjs.org/package/npmdoc-mailgun-js) [![travis-ci.org build-status](https://api.travis-ci.org/npmdoc/node-npmdoc-mailgun-js.svg)](https://travis-ci.org/npmdoc/node-npmdoc-mailgun-js)
#### Simple Node.js helper module for Mailgun API

[![NPM](https://nodei.co/npm/mailgun-js.png?downloads=true)](https://www.npmjs.com/package/mailgun-js)

[![apidoc](https://npmdoc.github.io/node-npmdoc-mailgun-js/build/screenCapture.buildNpmdoc.browser._2Fhome_2Ftravis_2Fbuild_2Fnpmdoc_2Fnode-npmdoc-mailgun-js_2Ftmp_2Fbuild_2Fapidoc.html.png)](https://npmdoc.github.io/node-npmdoc-mailgun-js/build/apidoc.html)

![npmPackageListing](https://npmdoc.github.io/node-npmdoc-mailgun-js/build/screenCapture.npmPackageListing.svg)

![npmPackageDependencyTree](https://npmdoc.github.io/node-npmdoc-mailgun-js/build/screenCapture.npmPackageDependencyTree.svg)



# package.json

```json

{
    "author": {
        "name": "Bojan Djurkovic",
        "email": "bojan@onelobby.com"
    },
    "bugs": {
        "url": "http://github.com/bojand/mailgun-js/issues"
    },
    "dependencies": {
        "async": "~2.1.2",
        "debug": "~2.2.0",
        "form-data": "~2.1.1",
        "inflection": "~1.10.0",
        "is-stream": "^1.1.0",
        "path-proxy": "~1.0.0",
        "promisify-call": "^2.0.2",
        "proxy-agent": "~2.0.0",
        "tsscmp": "~1.0.0"
    },
    "description": "Simple Node.js helper module for Mailgun API",
    "devDependencies": {
        "clone": "~1.0.0",
        "mailcomposer": "~2.1.0",
        "mocha": "~3.0.2",
        "request": "^2.67.0"
    },
    "directories": {
        "test": "test"
    },
    "dist": {
        "shasum": "aa6199fc5b6d6e54dcf7905342bb87944effda3d",
        "tarball": "https://registry.npmjs.org/mailgun-js/-/mailgun-js-0.9.1.tgz"
    },
    "engines": {
        "node": ">=4.0"
    },
    "gitHead": "bff2ef9c315fd5de668ef161109c3679f1ccd43c",
    "homepage": "https://github.com/bojand/mailgun-js",
    "keywords": [
        "email",
        "mailgun"
    ],
    "license": "MIT",
    "main": "./lib/mailgun.js",
    "maintainers": [
        {
            "name": "bojand",
            "email": "dbojan@gmail.com"
        }
    ],
    "name": "mailgun-js",
    "optionalDependencies": {},
    "readme": "ERROR: No README data found!",
    "repository": {
        "type": "git",
        "url": "git://github.com/bojand/mailgun-js.git"
    },
    "scripts": {
        "docs:api": "./bin/docs",
        "docs:build": "npm run docs:api && npm run docs:prepare && npm run docs:clean && gitbook build",
        "docs:clean": "rm -rf _book",
        "docs:prepare": "gitbook install",
        "docs:publish": "npm run docs:build && cd _book && git init && git commit --allow-empty -m 'Update docs' && git checkout -b gh-pages && git add . && git commit -am 'Update docs' && git push https://github.com/bojand/mailgun-js.git gh-pages --force",
        "docs:watch": "npm run docs:api && npm run docs:prepare && gitbook serve",
        "test": "mocha"
    },
    "version": "0.9.1"
}
```



# <a name="apidoc.tableOfContents"></a>[table of contents](#apidoc.tableOfContents)

#### [module mailgun-js](#apidoc.module.mailgun-js)
1.  [function <span class="apidocSignatureSpan">mailgun-js.</span>attachment (options)](#apidoc.element.mailgun-js.attachment)
1.  [function <span class="apidocSignatureSpan">mailgun-js.</span>request (options)](#apidoc.element.mailgun-js.request)
1.  object <span class="apidocSignatureSpan">mailgun-js.</span>attachment.prototype
1.  object <span class="apidocSignatureSpan">mailgun-js.</span>request.prototype

#### [module mailgun-js.attachment](#apidoc.module.mailgun-js.attachment)
1.  [function <span class="apidocSignatureSpan">mailgun-js.</span>attachment (options)](#apidoc.element.mailgun-js.attachment.attachment)

#### [module mailgun-js.attachment.prototype](#apidoc.module.mailgun-js.attachment.prototype)
1.  [function <span class="apidocSignatureSpan">mailgun-js.attachment.prototype.</span>getType ()](#apidoc.element.mailgun-js.attachment.prototype.getType)

#### [module mailgun-js.request](#apidoc.module.mailgun-js.request)
1.  [function <span class="apidocSignatureSpan">mailgun-js.</span>request (options)](#apidoc.element.mailgun-js.request.request)

#### [module mailgun-js.request.prototype](#apidoc.module.mailgun-js.request.prototype)
1.  [function <span class="apidocSignatureSpan">mailgun-js.request.prototype.</span>_request (method, resource, data, fn)](#apidoc.element.mailgun-js.request.prototype._request)
1.  [function <span class="apidocSignatureSpan">mailgun-js.request.prototype.</span>handleAttachmentObject (key, obj)](#apidoc.element.mailgun-js.request.prototype.handleAttachmentObject)
1.  [function <span class="apidocSignatureSpan">mailgun-js.request.prototype.</span>handleMimeObject (key, obj)](#apidoc.element.mailgun-js.request.prototype.handleMimeObject)
1.  [function <span class="apidocSignatureSpan">mailgun-js.request.prototype.</span>handleResponse (res)](#apidoc.element.mailgun-js.request.prototype.handleResponse)
1.  [function <span class="apidocSignatureSpan">mailgun-js.request.prototype.</span>performRequest (options)](#apidoc.element.mailgun-js.request.prototype.performRequest)
1.  [function <span class="apidocSignatureSpan">mailgun-js.request.prototype.</span>prepareData (data)](#apidoc.element.mailgun-js.request.prototype.prepareData)
1.  [function <span class="apidocSignatureSpan">mailgun-js.request.prototype.</span>prepareFormData (data)](#apidoc.element.mailgun-js.request.prototype.prepareFormData)
1.  [function <span class="apidocSignatureSpan">mailgun-js.request.prototype.</span>request (method, resource, data, fn)](#apidoc.element.mailgun-js.request.prototype.request)



# <a name="apidoc.module.mailgun-js"></a>[module mailgun-js](#apidoc.module.mailgun-js)

#### <a name="apidoc.element.mailgun-js.attachment"></a>[function <span class="apidocSignatureSpan">mailgun-js.</span>attachment (options)](#apidoc.element.mailgun-js.attachment)
- description and source-code
```javascript
function Attachment(options) {
  var data = options.data;

  if (data) {
    if (typeof data === 'string' || Buffer.isBuffer(data) || isStream(data)) {
      this.data = data;
    }
  }

  this.filename = options.filename;
  this.contentType = options.contentType;
  this.knownLength = options.knownLength;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.mailgun-js.request"></a>[function <span class="apidocSignatureSpan">mailgun-js.</span>request (options)](#apidoc.element.mailgun-js.request)
- description and source-code
```javascript
function Request(options) {
  this.host = options.host;
  this.protocol = options.protocol;
  this.port = options.port;
  this.endpoint = options.endpoint;
  this.auth = options.auth;
  this.proxy = options.proxy;
  this.timeout = options.timeout;
  this.retry = options.retry || 1;
}
```
- example usage
```shell
...
  return self.handleResponse(res);
});
  }
  else {
var req;

if (options.protocol === 'http:') {
  req = http.request(options, function (res) {
    return self.handleResponse(res);
  });
}
else {
  req = https.request(options, function (res) {
    return self.handleResponse(res);
  });
...
```



# <a name="apidoc.module.mailgun-js.attachment"></a>[module mailgun-js.attachment](#apidoc.module.mailgun-js.attachment)

#### <a name="apidoc.element.mailgun-js.attachment.attachment"></a>[function <span class="apidocSignatureSpan">mailgun-js.</span>attachment (options)](#apidoc.element.mailgun-js.attachment.attachment)
- description and source-code
```javascript
function Attachment(options) {
  var data = options.data;

  if (data) {
    if (typeof data === 'string' || Buffer.isBuffer(data) || isStream(data)) {
      this.data = data;
    }
  }

  this.filename = options.filename;
  this.contentType = options.contentType;
  this.knownLength = options.knownLength;
}
```
- example usage
```shell
n/a
```



# <a name="apidoc.module.mailgun-js.attachment.prototype"></a>[module mailgun-js.attachment.prototype](#apidoc.module.mailgun-js.attachment.prototype)

#### <a name="apidoc.element.mailgun-js.attachment.prototype.getType"></a>[function <span class="apidocSignatureSpan">mailgun-js.attachment.prototype.</span>getType ()](#apidoc.element.mailgun-js.attachment.prototype.getType)
- description and source-code
```javascript
getType = function () {
  if (this.data) {
    if (typeof this.data === 'string') {
      return 'path';
    }
    else if (Buffer.isBuffer(this.data)) {
      return 'buffer';
    }
    else if (isStream(this.data)) {
      return 'stream';
    }
  }

  return 'unknown';
}
```
- example usage
```shell
...
else if (typeof obj === 'string') {
  debug('appending stream to form data. key: %s obj: %s', key, obj);
  this.form.append(key, fs.createReadStream(obj));
} else if ((typeof obj === 'object') && (obj.readable === true)) {
  debug('appending readable stream to form data. key: %s obj: %s', key, obj);
  this.form.append(key, obj);
} else if ((typeof obj === 'object') && (obj instanceof Attachment)) {
  var attachmentType = obj.getType();
  if (attachmentType === 'path') {
    debug('appending attachment stream to form data. key: %s data: %s filename: %s', key, obj.data, obj.filename);
    this.form.append(key, fs.createReadStream(obj.data), {
      filename: obj.filename || 'attached file'
    });
  }
  else if (attachmentType === 'buffer') {
...
```



# <a name="apidoc.module.mailgun-js.request"></a>[module mailgun-js.request](#apidoc.module.mailgun-js.request)

#### <a name="apidoc.element.mailgun-js.request.request"></a>[function <span class="apidocSignatureSpan">mailgun-js.</span>request (options)](#apidoc.element.mailgun-js.request.request)
- description and source-code
```javascript
function Request(options) {
  this.host = options.host;
  this.protocol = options.protocol;
  this.port = options.port;
  this.endpoint = options.endpoint;
  this.auth = options.auth;
  this.proxy = options.proxy;
  this.timeout = options.timeout;
  this.retry = options.retry || 1;
}
```
- example usage
```shell
...
  return self.handleResponse(res);
});
  }
  else {
var req;

if (options.protocol === 'http:') {
  req = http.request(options, function (res) {
    return self.handleResponse(res);
  });
}
else {
  req = https.request(options, function (res) {
    return self.handleResponse(res);
  });
...
```



# <a name="apidoc.module.mailgun-js.request.prototype"></a>[module mailgun-js.request.prototype](#apidoc.module.mailgun-js.request.prototype)

#### <a name="apidoc.element.mailgun-js.request.prototype._request"></a>[function <span class="apidocSignatureSpan">mailgun-js.request.prototype.</span>_request (method, resource, data, fn)](#apidoc.element.mailgun-js.request.prototype._request)
- description and source-code
```javascript
_request = function (method, resource, data, fn) {
  var self = this;

  var path = ''.concat(this.endpoint, resource);

  var params = this.prepareData(data);

  this.payload = '';

  var isMIME = path.indexOf('/messages.mime') >= 0;

  this.headers = {};
  if (method === 'GET' || method === 'DELETE') {
    this.payload = qs.stringify(params);
    if (this.payload) path = path.concat('?', this.payload);
  }
  else {
    this.headers['Content-Type'] = isMIME ? 'multipart/form-data' : 'application/x-www-form-urlencoded';

    if (params && (params.attachment || params.inline || (isMIME && params.message))) {
      this.prepareFormData(params);
    }
    else {
      this.payload = qs.stringify(params);
      var length = this.payload ? Buffer.byteLength(this.payload) : 0;
      this.headers['Content-Length'] = length;
    }
  }

  // check for MIME is true in case of messages GET
  if (method === 'GET' &&
    path.indexOf('/messages') >= 0 &&
    params && params.MIME === true) {
    this.headers.Accept = 'message/rfc2822';
  }

  debug('%s %s', method, path);

  var opts = {
    hostname: this.host,
    port: this.port,
    protocol: this.protocol,
    path: path,
    method: method,
    headers: this.headers,
    auth: this.auth,
    agent: this.proxy ? proxy(this.proxy, true) : false,
    timeout: this.timeout
  };

  if (this.retry > 1) {
    retry(this.retry, function (retryCb) {
      self.callback = retryCb;
      self.performRequest(opts);
    }, fn);
  }
  else {
    this.callback = fn;
    this.performRequest(opts);
  }
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.mailgun-js.request.prototype.handleAttachmentObject"></a>[function <span class="apidocSignatureSpan">mailgun-js.request.prototype.</span>handleAttachmentObject (key, obj)](#apidoc.element.mailgun-js.request.prototype.handleAttachmentObject)
- description and source-code
```javascript
handleAttachmentObject = function (key, obj) {
  if (!this.form) this.form = new FormData();

  if (Buffer.isBuffer(obj)) {
    debug('appending buffer to form data. key: %s', key);
    this.form.append(key, obj, {
      filename: 'file'
    });
  }
  else if (typeof obj === 'string') {
    debug('appending stream to form data. key: %s obj: %s', key, obj);
    this.form.append(key, fs.createReadStream(obj));
  } else if ((typeof obj === 'object') && (obj.readable === true)) {
    debug('appending readable stream to form data. key: %s obj: %s', key, obj);
    this.form.append(key, obj);
  } else if ((typeof obj === 'object') && (obj instanceof Attachment)) {
    var attachmentType = obj.getType();
    if (attachmentType === 'path') {
      debug('appending attachment stream to form data. key: %s data: %s filename: %s', key, obj.data, obj.filename);
      this.form.append(key, fs.createReadStream(obj.data), {
        filename: obj.filename || 'attached file'
      });
    }
    else if (attachmentType === 'buffer') {
      debug('appending attachment buffer to form data. key: %s filename: %s', key, obj.filename);
      var formOpts = {
        filename: obj.filename || 'attached file'
      };

      if (obj.contentType) {
        formOpts.contentType = obj.contentType
      }

      if (obj.knownLength) {
        formOpts.knownLength = obj.knownLength
      }

      this.form.append(key, obj.data, formOpts);
    }
    else if (attachmentType === 'stream') {
      if (obj.knownLength && obj.contentType) {
        debug('appending attachment stream to form data. key: %s filename: %s', key, obj.filename);

        this.form.append(key, obj.data, {
          filename: obj.filename || 'attached file',
          contentType: obj.contentType,
          knownLength: obj.knownLength
        });
      }
      else {
        debug('missing content type or length for attachment stream. key: %s', key);
      }
    }
  }
  else {
    debug('unknown attachment type. key: %s', key);
  }
}
```
- example usage
```shell
...

  for (var key in data) {
var obj = data[key];
if(isOk(obj)) {
  if (key === 'attachment' || key === 'inline') {
    if (Array.isArray(obj)) {
      for (var i = 0; i < obj.length; i++) {
        this.handleAttachmentObject(key, obj[i]);
      }
    }
    else {
      this.handleAttachmentObject(key, obj);
    }
  }
  else if (key === 'message') {
...
```

#### <a name="apidoc.element.mailgun-js.request.prototype.handleMimeObject"></a>[function <span class="apidocSignatureSpan">mailgun-js.request.prototype.</span>handleMimeObject (key, obj)](#apidoc.element.mailgun-js.request.prototype.handleMimeObject)
- description and source-code
```javascript
handleMimeObject = function (key, obj) {
  var self = this;
  if (typeof obj === 'string') {
    if (fs.existsSync(obj) && fs.statSync(obj).isFile()) {
      self.form.append('message', fs.createReadStream(obj));
    }
    else {
      self.form.append('message', new Buffer(obj), {
        filename: 'message.mime',
        contentType: 'message/rfc822',
        knownLength: obj.length
      });
    }
  }
  else if (obj instanceof Readable) {
    self.form.append('message', obj);
  }
}
```
- example usage
```shell
...
    }
  }
  else {
    this.handleAttachmentObject(key, obj);
  }
}
else if (key === 'message') {
  this.handleMimeObject(key, obj);
}
else if (Array.isArray(obj)) {
  function appendKey(element) {
    if(isOk(element)) {
      var value = getDataValue(key, element);
      if(isOk(value)) {
        self.form.append(key, value);
...
```

#### <a name="apidoc.element.mailgun-js.request.prototype.handleResponse"></a>[function <span class="apidocSignatureSpan">mailgun-js.request.prototype.</span>handleResponse (res)](#apidoc.element.mailgun-js.request.prototype.handleResponse)
- description and source-code
```javascript
handleResponse = function (res) {
  var self = this;
  var chunks = '';
  var error;

  res.on('data', function (chunk) {
    chunks += chunk;
  });

  res.on('error', function (err) {
    error = err;
  });

  res.on('end', function () {
    var body;

    debug('response status code: %s content type: %s error: %s', res.statusCode, res.headers['content-type'], error);

    // FIXME: An ugly hack to overcome invalid response type in mailgun api (see http://bit.ly/1eF30fU).
    // We skip content-type validation for 'campaings' endpoint assuming it is JSON.
    var skipContentTypeCheck = res.req && res.req.path && res.req.path.match(/\/campaigns/);
    var isJSON = res.headers['content-type'] && res.headers['content-type'].indexOf('application/json') >= 0;
    if (chunks && !error && (skipContentTypeCheck || isJSON)) {
      try {
        body = JSON.parse(chunks);
      } catch (e) {
        error = e;
      }
    }

    if (process.env.DEBUG_MAILGUN_FORCE_RETRY) {
      error = new Error('Force retry error');
      delete process.env.DEBUG_MAILGUN_FORCE_RETRY;
    }

    if (!error && res.statusCode !== 200) {
      var msg = body ? body.message || body.response : body || chunks || res.statusMessage;
      error = new Error(msg);
      error.statusCode = res.statusCode;
    }

    return self.callback(error, body);
  });
}
```
- example usage
```shell
...
  if (this.form && (method === 'POST' || method === 'PUT' || method === 'PATCH')) {

this.form.submit(options, function (err, res) {
  if (err) {
    return self.callback(err);
  }

  return self.handleResponse(res);
});
  }
  else {
var req;

if (options.protocol === 'http:') {
  req = http.request(options, function (res) {
...
```

#### <a name="apidoc.element.mailgun-js.request.prototype.performRequest"></a>[function <span class="apidocSignatureSpan">mailgun-js.request.prototype.</span>performRequest (options)](#apidoc.element.mailgun-js.request.prototype.performRequest)
- description and source-code
```javascript
performRequest = function (options) {
  var self = this;
  var method = options.method;

  if (this.form && (method === 'POST' || method === 'PUT' || method === 'PATCH')) {

    this.form.submit(options, function (err, res) {
      if (err) {
        return self.callback(err);
      }

      return self.handleResponse(res);
    });
  }
  else {
    var req;

    if (options.protocol === 'http:') {
      req = http.request(options, function (res) {
        return self.handleResponse(res);
      });
    }
    else {
      req = https.request(options, function (res) {
        return self.handleResponse(res);
      });
    }

    if (options.timeout) {
      req.setTimeout(options.timeout, function () {
        // timeout occurs
        req.abort();
      });
    }

    req.on('error', function (e) {
      return self.callback(e);
    });

    if (this.payload && (method === 'POST' || method === 'PUT' || method === 'PATCH')) {
      req.write(this.payload);
    }

    req.end();
  }
}
```
- example usage
```shell
...
    agent: this.proxy ? proxy(this.proxy, true) : false,
    timeout: this.timeout
  };

  if (this.retry > 1) {
    retry(this.retry, function (retryCb) {
      self.callback = retryCb;
      self.performRequest(opts);
    }, fn);
  }
  else {
    this.callback = fn;
    this.performRequest(opts);
  }
}
...
```

#### <a name="apidoc.element.mailgun-js.request.prototype.prepareData"></a>[function <span class="apidocSignatureSpan">mailgun-js.request.prototype.</span>prepareData (data)](#apidoc.element.mailgun-js.request.prototype.prepareData)
- description and source-code
```javascript
prepareData = function (data) {
  var params = {};

  for (var key in data) {
    if (key !== 'attachment' && key !== 'inline' && isOk(data[key])) {
      var value = getDataValue(key, data[key]);
      if(isOk(value)) {
        params[key] = value;
      }
    }
    else {
      params[key] = data[key];
    }
  }

  return params;
}
```
- example usage
```shell
...
}

Request.prototype._request = function (method, resource, data, fn) {
var self = this;

var path = ''.concat(this.endpoint, resource);

var params = this.prepareData(data);

this.payload = '';

var isMIME = path.indexOf('/messages.mime') >= 0;

this.headers = {};
if (method === 'GET' || method === 'DELETE') {
...
```

#### <a name="apidoc.element.mailgun-js.request.prototype.prepareFormData"></a>[function <span class="apidocSignatureSpan">mailgun-js.request.prototype.</span>prepareFormData (data)](#apidoc.element.mailgun-js.request.prototype.prepareFormData)
- description and source-code
```javascript
prepareFormData = function (data) {
  this.form = new FormData();
  var self = this;

  for (var key in data) {
    var obj = data[key];
    if(isOk(obj)) {
      if (key === 'attachment' || key === 'inline') {
        if (Array.isArray(obj)) {
          for (var i = 0; i < obj.length; i++) {
            this.handleAttachmentObject(key, obj[i]);
          }
        }
        else {
          this.handleAttachmentObject(key, obj);
        }
      }
      else if (key === 'message') {
        this.handleMimeObject(key, obj);
      }
      else if (Array.isArray(obj)) {
        function appendKey(element) {
          if(isOk(element)) {
            var value = getDataValue(key, element);
            if(isOk(value)) {
              self.form.append(key, value);
            }
          }
        }

        obj.forEach(appendKey);
      }
      else {
        var value = getDataValue(key, obj);
        if(isOk(value)) {
          this.form.append(key, value);
        }
      }
    }
  }

  this.headers = this.form.getHeaders();
}
```
- example usage
```shell
...
  this.payload = qs.stringify(params);
  if (this.payload) path = path.concat('?', this.payload);
}
else {
  this.headers['Content-Type'] = isMIME ? 'multipart/form-data' : 'application/x-www-form-urlencoded';

  if (params && (params.attachment || params.inline || (isMIME && params.message))) {
    this.prepareFormData(params);
  }
  else {
    this.payload = qs.stringify(params);
    var length = this.payload ? Buffer.byteLength(this.payload) : 0;
    this.headers['Content-Length'] = length;
  }
}
...
```

#### <a name="apidoc.element.mailgun-js.request.prototype.request"></a>[function <span class="apidocSignatureSpan">mailgun-js.request.prototype.</span>request (method, resource, data, fn)](#apidoc.element.mailgun-js.request.prototype.request)
- description and source-code
```javascript
request = function (method, resource, data, fn) {
  if (typeof data === 'function' && !fn) {
    fn = data;
    data = {};
  }

  if (!data) {
    data = {}
  }

  return promisifyCall(this, this._request, method, resource, data, fn);
}
```
- example usage
```shell
...
  return self.handleResponse(res);
});
  }
  else {
var req;

if (options.protocol === 'http:') {
  req = http.request(options, function (res) {
    return self.handleResponse(res);
  });
}
else {
  req = https.request(options, function (res) {
    return self.handleResponse(res);
  });
...
```



# misc
- this document was created with [utility2](https://github.com/kaizhu256/node-utility2)
