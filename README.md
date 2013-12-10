# grunt-contrib-nodeunit v0.3.0 [![Build Status](https://travis-ci.org/gruntjs/grunt-contrib-nodeunit.png?branch=master)](https://travis-ci.org/gruntjs/grunt-contrib-nodeunit)

> Run Nodeunit unit tests.



## Getting Started
This plugin requires Grunt `~0.4.0`

If you haven't used [Grunt](http://gruntjs.com/) before, be sure to check out the [Getting Started](http://gruntjs.com/getting-started) guide, as it explains how to create a [Gruntfile](http://gruntjs.com/sample-gruntfile) as well as install and use Grunt plugins. Once you're familiar with that process, you may install this plugin with this command:

```shell
npm install grunt-contrib-nodeunit --save-dev
```

Once the plugin has been installed, it may be enabled inside your Gruntfile with this line of JavaScript:

```js
grunt.loadNpmTasks('grunt-contrib-nodeunit');
```




## Nodeunit task
_Run this task with the `grunt nodeunit` command._

Task targets, files and options may be specified according to the grunt [Configuring tasks](http://gruntjs.com/configuring-tasks) guide.

This plugin provides server-side JavaScript unit testing via [nodeunit](https://github.com/caolan/nodeunit/). If you're looking to test JavaScript that uses `window` or the DOM, please use the [grunt-contrib-qunit plugin](https://github.com/gruntjs/grunt-contrib-qunit)`qunit` task.

### Settings

#### options.reporter
* Type: `String`
* Default: `grunt`

Specifies the reporter you want to use.  For example, `default`, `grunt`, `verbose` or `tap`.

#### options.reporterOutput
* Type: `Boolean`
* Default: false

Specifies the file the `reporter`'s output should be saved to.  For example, `tests.tap`.
### Usage examples

#### Wildcards

In this example, `grunt nodeunit:all` or `grunt nodeunit` will test all files ending with `_test.js` in the `test` directory.

```js
// Project configuration.
grunt.initConfig({
  nodeunit: {
    all: ['test/*_test.js']
  }
});
```

With a slight modification, `grunt nodeunit:all` will test files matching the same pattern in the `test` directory _and all subdirectories_.

```js
// Project configuration.
grunt.initConfig({
  nodeunit: {
    all: ['test/**/*_test.js']
  }
});
```
#### Using Other Reporters

To use a reporter other than the default one, you can specify the `reporter` and `reporterOutput` parameters.

```js
// Project configuration.
grunt.initConfig({
  nodeunit: {
    all: ['test/*_test.js'],
    options: {
      reporter: 'tap',
      reporterOutput: false
    }
  }
});
```


## Release History

See [CHANGELOG](CHANGELOG)

---

Task submitted by ["Cowboy" Ben Alman](http://benalman.com)

*This file was generated on Tue Dec 10 2013 14:27:00.*
