# api documentation for  [email-templates (v2.5.4)](https://github.com/niftylettuce/node-email-templates)  [![npm package](https://img.shields.io/npm/v/npmdoc-email-templates.svg?style=flat-square)](https://www.npmjs.org/package/npmdoc-email-templates) [![travis-ci.org build-status](https://api.travis-ci.org/npmdoc/node-npmdoc-email-templates.svg)](https://travis-ci.org/npmdoc/node-npmdoc-email-templates)
#### Node.js module for rendering beautiful emails with ejs, jade, swig, hbs, or handlebars templates and email-friendly inline CSS using juice.

[![NPM](https://nodei.co/npm/email-templates.png?downloads=true)](https://www.npmjs.com/package/email-templates)

[![apidoc](https://npmdoc.github.io/node-npmdoc-email-templates/build/screenCapture.buildNpmdoc.browser._2Fhome_2Ftravis_2Fbuild_2Fnpmdoc_2Fnode-npmdoc-email-templates_2Ftmp_2Fbuild_2Fapidoc.html.png)](https://npmdoc.github.io/node-npmdoc-email-templates/build..beta..travis-ci.org/apidoc.html)

![npmPackageListing](https://npmdoc.github.io/node-npmdoc-email-templates/build/screenCapture.npmPackageListing.svg)

![npmPackageDependencyTree](https://npmdoc.github.io/node-npmdoc-email-templates/build/screenCapture.npmPackageDependencyTree.svg)



# package.json

```json

{
    "author": {
        "name": "Nick Baugh",
        "email": "niftylettuce@gmail.com"
    },
    "bugs": {
        "url": "https://github.com/niftylettuce/node-email-templates/issues/new"
    },
    "contributors": [
        {
            "name": "Nick Baugh",
            "email": "niftylettuce@gmail.com"
        },
        {
            "name": "Andrea Baccega",
            "email": "vekexasia@gmail.com"
        },
        {
            "name": "Nic Jansma",
            "url": "http://nicj.net"
        },
        {
            "name": "Jason Sims",
            "email": "sims.jrobert@gmail.com"
        },
        {
            "name": "Miguel Mota",
            "email": "hello@miguelmota.com"
        },
        {
            "name": "Jeduan Cornejo",
            "email": "jeduan@gmail.com"
        },
        {
            "name": "Alberto Souza",
            "email": "contato@albertosouza.net"
        }
    ],
    "dependencies": {
        "bluebird": "^3.0.0",
        "consolidate": "^0.14.2",
        "debug": "^2.2.0",
        "glob": "^6.0.0",
        "juice": "^2.0.0",
        "lodash": "^4.0.1"
    },
    "description": "Node.js module for rendering beautiful emails with ejs, jade, swig, hbs, or handlebars templates and email-friendly inline CSS using juice.",
    "devDependencies": {
        "async": "^1.5.0",
        "babel-cli": "^6.4.5",
        "babel-preset-es2015": "^6.3.13",
        "babel-register": "^6.4.3",
        "chai": "^3.0.0",
        "dustjs-linkedin": "^2.4.0",
        "ejs": "^2.3.0",
        "handlebars": "^4.0.0",
        "istanbul": "^0.4.2",
        "jade": "^1.3.1",
        "less": "^2.5.0",
        "mkdirp": "^0.5.1",
        "mocha": "^2.1.0",
        "node-sass": "^3.1.1",
        "nodemailer": "^1.3.4",
        "nodemailer-wellknown": "^0.1.5",
        "postmark": "^1.0.0",
        "rimraf": "^2.2.8",
        "sinon": "^1.10.2",
        "sinon-chai": "^2.7.0",
        "standard": "^5.4.1",
        "styl": "^0.2.7",
        "stylus": "^0.53.0",
        "swig": "^1.3.2"
    },
    "directories": {},
    "dist": {
        "shasum": "5f8995f63802688f5afd5aa50ee7587f4e1c9440",
        "tarball": "https://registry.npmjs.org/email-templates/-/email-templates-2.5.4.tgz"
    },
    "engines": {
        "node": ">= 0.10"
    },
    "gitHead": "cfb16da5c92d788df8dbf8b487a973a1b671cf57",
    "homepage": "https://github.com/niftylettuce/node-email-templates",
    "keywords": [
        "node-email-templates",
        "windows",
        "ejs",
        "email",
        "templates",
        "email-templates",
        "juice",
        "inline",
        "i18n",
        "css"
    ],
    "license": "MIT",
    "main": "lib/main.js",
    "maintainers": [
        {
            "name": "niftylettuce",
            "email": "nicholasbaugh@gmail.com"
        },
        {
            "name": "jasonsims",
            "email": "sims.jrobert@gmail.com"
        },
        {
            "name": "jeduan",
            "email": "jeduan@gmail.com"
        }
    ],
    "name": "email-templates",
    "optionalDependencies": {},
    "readme": "ERROR: No README data found!",
    "repository": {
        "type": "git",
        "url": "git+https://github.com/niftylettuce/node-email-templates.git"
    },
    "scripts": {
        "compile": "babel src --modules common --out-dir lib",
        "prepublish": "npm run compile && npm prune",
        "test": "standard && mocha",
        "test-cov": "istanbul cover node_modules/mocha/bin/_mocha -- --reporter dot",
        "test-travis": "istanbul cover node_modules/mocha/bin/_mocha --report lcovonly",
        "watch": "babel src --watch --modules common --out-dir lib --source-maps true"
    },
    "standard": {
        "ignore": [
            "lib",
            "examples"
        ]
    },
    "version": "2.5.4"
}
```



# <a name="apidoc.tableOfContents"></a>[table of contents](#apidoc.tableOfContents)

#### [module email-templates](#apidoc.module.email-templates)
1.  [function <span class="apidocSignatureSpan">email-templates.</span>EmailTemplate (path)](#apidoc.element.email-templates.EmailTemplate)
1.  object <span class="apidocSignatureSpan">email-templates.</span>email_template
1.  object <span class="apidocSignatureSpan">email-templates.</span>requires
1.  object <span class="apidocSignatureSpan">email-templates.</span>template_manager
1.  object <span class="apidocSignatureSpan">email-templates.</span>util

#### [module email-templates.email_template](#apidoc.module.email-templates.email_template)
1.  [function <span class="apidocSignatureSpan">email-templates.email_template.</span>default (path)](#apidoc.element.email-templates.email_template.default)

#### [module email-templates.template_manager](#apidoc.module.email-templates.template_manager)
1.  [function <span class="apidocSignatureSpan">email-templates.template_manager.</span>render (file)](#apidoc.element.email-templates.template_manager.render)

#### [module email-templates.util](#apidoc.module.email-templates.util)
1.  [function <span class="apidocSignatureSpan">email-templates.util.</span>ensureDirectory (path, callback)](#apidoc.element.email-templates.util.ensureDirectory)
1.  [function <span class="apidocSignatureSpan">email-templates.util.</span>getLocalizedETF (templatePath, locale, done)](#apidoc.element.email-templates.util.getLocalizedETF)
1.  [function <span class="apidocSignatureSpan">email-templates.util.</span>getRootTemplateFolder (templatePath, done)](#apidoc.element.email-templates.util.getRootTemplateFolder)
1.  [function <span class="apidocSignatureSpan">email-templates.util.</span>readContents (path, type)](#apidoc.element.email-templates.util.readContents)
1.  [function <span class="apidocSignatureSpan">email-templates.util.</span>renderFile (file, options)](#apidoc.element.email-templates.util.renderFile)
1.  [function <span class="apidocSignatureSpan">email-templates.util.</span>resolveTPLFolder (path, locale, callback)](#apidoc.element.email-templates.util.resolveTPLFolder)



# <a name="apidoc.module.email-templates"></a>[module email-templates](#apidoc.module.email-templates)

#### <a name="apidoc.element.email-templates.EmailTemplate"></a>[function <span class="apidocSignatureSpan">email-templates.</span>EmailTemplate (path)](#apidoc.element.email-templates.EmailTemplate)
- description and source-code
```javascript
function EmailTemplate(path) {
  var options = arguments.length <= 1 || arguments[1] === undefined ? {} : arguments[1];

  _classCallCheck(this, EmailTemplate);

  this.path = path;
  this.dirname = (0, _path.basename)(path);
  this.options = options;
  debug('Creating Email template for path %s', (0, _path.basename)(path));
  // localized templates cache
  this.ltpls = {};
}
```
- example usage
```shell
n/a
```



# <a name="apidoc.module.email-templates.email_template"></a>[module email-templates.email_template](#apidoc.module.email-templates.email_template)

#### <a name="apidoc.element.email-templates.email_template.default"></a>[function <span class="apidocSignatureSpan">email-templates.email_template.</span>default (path)](#apidoc.element.email-templates.email_template.default)
- description and source-code
```javascript
function EmailTemplate(path) {
  var options = arguments.length <= 1 || arguments[1] === undefined ? {} : arguments[1];

  _classCallCheck(this, EmailTemplate);

  this.path = path;
  this.dirname = (0, _path.basename)(path);
  this.options = options;
  debug('Creating Email template for path %s', (0, _path.basename)(path));
  // localized templates cache
  this.ltpls = {};
}
```
- example usage
```shell
...
      }).nodeify(callback);
    }
  }, {
    key: '_renderStyle',
    value: function _renderStyle(locals, locale) {
      var _this6 = this;

      return new _bluebird2.default(function (resolve) {
// cached
if (_this6.ltpls[locale].style !== undefined) {
  return resolve(_this6.ltpls[locale].style);
}

// no style
if (!_this6.ltpls[locale].files.style) return resolve(null);
...
```



# <a name="apidoc.module.email-templates.template_manager"></a>[module email-templates.template_manager](#apidoc.module.email-templates.template_manager)

#### <a name="apidoc.element.email-templates.template_manager.render"></a>[function <span class="apidocSignatureSpan">email-templates.template_manager.</span>render (file)](#apidoc.element.email-templates.template_manager.render)
- description and source-code
```javascript
function render(file) {
  var locals = arguments.length <= 1 || arguments[1] === undefined ? {} : arguments[1];
  var callback = arguments[2];
  var filename = file.filename;
  var content = file.content;


  return new _bluebird2.default(function (resolve, reject) {
    if (!content) return reject('No content in template');
    if (!filename) return reject('Filename is null');
    var engine = (0, _path.extname)(filename).slice(1);

    locals.filename = filename;
    locals.engine = '.' + engine;
    locals.templatePath = (0, _path.dirname)(filename);

    if (engine.length && _consolidate2.default[engine] !== undefined) {
      // use consolidate.js if it supports this engine
      return _consolidate2.default[engine].render(content, locals, function (err, rendered) {
        if (err) return reject(err);
        resolve(rendered);
      });
    } else {
      // or use the function defined in the engineMap
      var fn = engineMap[engine];
      return resolve(fn(content, locals));
    }
    return reject('Can\'t render file with extension ' + engine);
  }).nodeify(callback);
}
```
- example usage
```shell
...
var EmailTemplate = require('email-templates').EmailTemplate
var path = require('path')

var templateDir = path.join(__dirname, 'templates', 'newsletter')

var newsletter = new EmailTemplate(templateDir)
var user = {name: 'Joe', pasta: 'spaghetti'}
newsletter.render(user, function (err, result) {
// result.html
// result.text
})

var async = require('async')
var users = [
{name: 'John', pasta: 'Rigatoni'},
...
```



# <a name="apidoc.module.email-templates.util"></a>[module email-templates.util](#apidoc.module.email-templates.util)

#### <a name="apidoc.element.email-templates.util.ensureDirectory"></a>[function <span class="apidocSignatureSpan">email-templates.util.</span>ensureDirectory (path, callback)](#apidoc.element.email-templates.util.ensureDirectory)
- description and source-code
```javascript
function ensureDirectory(path, callback) {
  return new _bluebird2.default(function (resolve, reject) {
    (0, _fs.stat)(path, function (err, stat) {
      if (err) return reject(err);
      if (!stat.isDirectory()) return reject();
      resolve();
    });
  }).nodeify(callback);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.email-templates.util.getLocalizedETF"></a>[function <span class="apidocSignatureSpan">email-templates.util.</span>getLocalizedETF (templatePath, locale, done)](#apidoc.element.email-templates.util.getLocalizedETF)
- description and source-code
```javascript
function getLocalizedETF(templatePath, locale, done) {
  if (!locale || locale === 'en-us') return done();

  var p = (0, _path.join)(templatePath, locale);
  (0, _fs.stat)(p, function afterCheckIfFolderExists(err) {
    if (err) {
      if (err.code === 'ENOENT') return done(); // not found
      return done(err); // unknow error
    }
    done(null, p);
  });
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.email-templates.util.getRootTemplateFolder"></a>[function <span class="apidocSignatureSpan">email-templates.util.</span>getRootTemplateFolder (templatePath, done)](#apidoc.element.email-templates.util.getRootTemplateFolder)
- description and source-code
```javascript
function getRootTemplateFolder(templatePath, done) {
  (0, _fs.stat)(templatePath, function afterCheckIfFolderExists(err) {
    if (err) return done(err);
    done(null, templatePath);
  });
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.email-templates.util.readContents"></a>[function <span class="apidocSignatureSpan">email-templates.util.</span>readContents (path, type)](#apidoc.element.email-templates.util.readContents)
- description and source-code
```javascript
function readContents(path, type) {
  return globP(path + '/*' + type + '.*').then(function (files) {
    if (!files.length) return null;

    return readFileP(files[0], 'utf8').then(function (content) {
      if (!content.length) return null;
      return {
        filename: files[0],
        content: content
      };
    });
  });
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.email-templates.util.renderFile"></a>[function <span class="apidocSignatureSpan">email-templates.util.</span>renderFile (file, options)](#apidoc.element.email-templates.util.renderFile)
- description and source-code
```javascript
function renderFile(file, options) {
  if (!file) return _bluebird2.default.resolve(null);
  return (0, _templateManager.render)(file, options);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.email-templates.util.resolveTPLFolder"></a>[function <span class="apidocSignatureSpan">email-templates.util.</span>resolveTPLFolder (path, locale, callback)](#apidoc.element.email-templates.util.resolveTPLFolder)
- description and source-code
```javascript
function resolveTPLFolder(path, locale, callback) {
  return new _bluebird2.default(function (resolve, reject) {
    getLocalizedETF(path, locale, function (err, tpl) {
      if (err) return reject(err);
      if (tpl) return resolve(tpl);

      getRootTemplateFolder(path, function (err, tpl) {
        if (err) return reject(err);
        resolve(tpl);
      });
    });
  }).nodeify(callback);
}
```
- example usage
```shell
n/a
```



# misc
- this document was created with [utility2](https://github.com/kaizhu256/node-utility2)
