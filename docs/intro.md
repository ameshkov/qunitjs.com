---
layout: page
title: Getting Started
---

<p class="lead" markdown="1">The following guide will get you up-and-running with QUnit in either [Node](#in-node) or [the Browser](#in-the-browser) in just a few minutes.</p>

## In Node

First, install QUnit using `npm` (or `yarn`):

```bash
npm install --save-dev qunit
```

And then start writing tests.

```js
const add = (a, b) => a + b;
QUnit.module('add', function() {
  QUnit.test('should add two numbers', function(assert) {
    assert.equal(add(1, 1), 2, '1 + 1 = 2');
  });
});
```



```bash
npm run test
```

### Support Policy

QUnit follows the <a href="https://github.com/nodejs/LTS" target="_blank">Node Long-term Support (LTS) Schedule</a>. Support is provided for Current, Active, and Maintenance releases.

### Package Name Prior to 2.5.1

Prior to version 2.5.1, QUnit was published under the name `qunitjs` on NPM. If you wish to install an older version of QUnit on Node, you will want to use the `qunitjs` package. The `qunit` package prior to 2.5.1 is an alternative CLI that is now published as `node-qunit`.

## In the Browser

QUnit is available from the <a href="https://code.jquery.com" target="_blank">jQuery CDN</a> hosted by <a href="https://www.maxcdn.com/" target="_blank">MaxCDN</a>.

### Support Policy

QUnit currently supports <a href="https://jquery.com/browser-support/" target="_blank">the same browsers as jQuery 3.x</a>.

For legacy browser support, including Internet Explorer versions lower than IE9, please use the 1.x series of QUnit.









### Current Release - v2.5.1

* <a href="https://code.jquery.com/qunit/qunit-2.5.1.js">qunit-2.5.1.js</a>
* <a href="https://code.jquery.com/qunit/qunit-2.5.1.css">qunit-2.5.1.css</a>
* <a href="https://github.com/qunitjs/qunit/blob/2.5.1/History.md" target="_blank">Changelog</a>
* <a href="https://npmjs.org/package/qunit">NPM</a>: <input class="copyable" value="npm install --save-dev qunit" readonly>
* <a href="https://yarnpkg.com/en/package/qunit">YARN</a>: <input class="copyable" value="yarn add qunit --dev" readonly>
* Bower: <input class="copyable" value="bower install --save-dev qunit" readonly>

To test the latest features and bug fixes to QUnit, a version automatically generated from the latest commit to the <a href="https://github.com/qunitjs/qunit" target="_blank">QUnit Git repository</a> is also available for use.

* <a href="https://code.jquery.com/qunit/qunit-git.js">qunit-git.js</a>
* <a href="https://code.jquery.com/qunit/qunit-git.css">qunit-git.css</a>

## Your First Test In Node

Install QUnit globally so you can use the CLI:

```
$ npm install -g qunit
```

Create test files in a <code>test</code> directory and then simply run:

```
$ qunit
```

And you should see some output like:

```
TAP version 13
ok 1 Module > Test #1
ok 2 Module > Test #2
1..2
# pass 2
# skip 0
# todo 0
# fail 0
```

And that is it! While QUnit defaults to looking for test files in <code>test</code>, you can also put them anywhere and then specify file paths or <a href="https://github.com/isaacs/minimatch" target="_blank">glob</a> expressions:

```
$ qunit 'tests/*-test.js'
```

To view the additional supported options, simply run:

```
$ qunit --help
```

## Your First Test In The Browser

A minimal QUnit test setup:

```html
<!DOCTYPE html>
<html>
<head>
  <meta charset="utf-8">
  <meta name="viewport" content="width=device-width">
  <title>QUnit Example</title>
  <link rel="stylesheet" href="https://code.jquery.com/qunit/qunit-2.5.1.css">
</head>
<body>
  <div id="qunit"></div>
  <div id="qunit-fixture"></div>
  <script src="https://code.jquery.com/qunit/qunit-2.5.1.js"></script>
  <script>
  QUnit.test( "hello test", function( assert ) {
    assert.ok( 1 == "1", "Passed!" );
  });
  </script>
</body>
</html>
```

The result:

<iframe src="../resources/example-index.html" style="width:100%;height:250px;border:0px"></iframe>

## Further Reading

* [Introdution to JavaScript Unit Testing](https://coding.smashingmagazine.com/2012/06/introduction-to-javascript-unit-testing/)
