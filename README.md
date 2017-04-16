# api documentation for  [email-templates (v2.5.4)](https://github.com/niftylettuce/node-email-templates)  [![npm package](https://img.shields.io/npm/v/npmdoc-email-templates.svg?style=flat-square)](https://www.npmjs.org/package/npmdoc-email-templates) [![travis-ci.org build-status](https://api.travis-ci.org/npmdoc/node-npmdoc-email-templates.svg)](https://travis-ci.org/npmdoc/node-npmdoc-email-templates)
#### Node.js module for rendering beautiful emails with ejs, jade, swig, hbs, or handlebars templates and email-friendly inline CSS using juice.

[![NPM](https://nodei.co/npm/email-templates.png?downloads=true&downloadRank=true&stars=true)](https://www.npmjs.com/package/email-templates)

[![apidoc](https://npmdoc.github.io/node-npmdoc-email-templates/build/screenCapture.buildCi.browser.%252Ftmp%252Fbuild%252Fapidoc.html.png)](https://npmdoc.github.io/node-npmdoc-email-templates/build/apidoc.html)

![npmPackageListing](https://npmdoc.github.io/node-npmdoc-email-templates/build/screenCapture.npmPackageListing.svg)

![npmPackageDependencyTree](https://npmdoc.github.io/node-npmdoc-email-templates/build/screenCapture.npmPackageDependencyTree.svg)



# package.json

```json

{
    "author": {
        "name": "Nick Baugh"
    },
    "bugs": {
        "url": "https://github.com/niftylettuce/node-email-templates/issues/new"
    },
    "contributors": [
        {
            "name": "Nick Baugh"
        },
        {
            "name": "Andrea Baccega"
        },
        {
            "name": "Nic Jansma",
            "url": "http://nicj.net"
        },
        {
            "name": "Jason Sims"
        },
        {
            "name": "Miguel Mota"
        },
        {
            "name": "Jeduan Cornejo"
        },
        {
            "name": "Alberto Souza"
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
            "name": "niftylettuce"
        },
        {
            "name": "jasonsims"
        },
        {
            "name": "jeduan"
        }
    ],
    "name": "email-templates",
    "optionalDependencies": {},
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
1.  [function <span class="apidocSignatureSpan"></span>email-templates (templateDirectory, options, done)](#apidoc.element.email-templates.email-templates)
1.  [function <span class="apidocSignatureSpan">email-templates.</span>EmailTemplate (path)](#apidoc.element.email-templates.EmailTemplate)
1.  [function <span class="apidocSignatureSpan">email-templates.</span>toString ()](#apidoc.element.email-templates.toString)
1.  object <span class="apidocSignatureSpan">email-templates.</span>requires



# <a name="apidoc.module.email-templates"></a>[module email-templates](#apidoc.module.email-templates)

#### <a name="apidoc.element.email-templates.email-templates"></a>[function <span class="apidocSignatureSpan"></span>email-templates (templateDirectory, options, done)](#apidoc.element.email-templates.email-templates)
- description and source-code
```javascript
function exportable(templateDirectory, options, done) {
  if (isFunction(options)) {
    done = options;
    options = {};
  }
  if (!templateDirectory) {
    return done(new Error('templateDirectory is undefined'));
  }

  return ensureDirectory(templateDirectory, function (err) {
    if (err) return done(err);
    debug('Creating Email Templates in %s', basename(templateDirectory));
    return done(null, template(templateDirectory, options));
  });
}
```
- example usage
```shell
n/a
```

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

#### <a name="apidoc.element.email-templates.toString"></a>[function <span class="apidocSignatureSpan">email-templates.</span>toString ()](#apidoc.element.email-templates.toString)
- description and source-code
```javascript
toString = function () {
    return toString;
}
```
- example usage
```shell
n/a
```



# misc
- this document was created with [utility2](https://github.com/kaizhu256/node-utility2)
