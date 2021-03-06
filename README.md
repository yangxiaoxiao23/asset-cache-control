# asset-cache-control

control the cache of assets by appending md5 hash to asset url

For example

in index.html we have

```html
<script type="text/javascript" src="js/hello.js"></script>
```


after running the task

```html
<script type="text/javascript" src="js/hello.js?t=cefe2283"></script>
```
## Getting Started
This plugin requires Grunt `~0.4.1`

If you haven't used [Grunt](http://gruntjs.com/) before, be sure to check out the [Getting Started](http://gruntjs.com/getting-started) guide, as it explains how to create a [Gruntfile](http://gruntjs.com/sample-gruntfile) as well as install and use Grunt plugins. Once you're familiar with that process, you may install this plugin with this command:

```shell
npm install asset-cache-control --save-dev
```

Once the plugin has been installed, it may be enabled inside your Gruntfile with this line of JavaScript:

```js
grunt.loadNpmTasks('asset-cache-control');
```

## The "cache" task

### Overview
In your project's Gruntfile, add a section named `cache` to the data object passed into `grunt.initConfig()`.

```js
grunt.initConfig({
    cache: {
      js: {
        options: {
        },
		assetUrl:'demo/js/hello.js',
        files: {
          'tmp': ['demo/index.html'],
        },
      },
    },
});
```



### Usage Examples

#### Default Options
In this example, we have index.html which contains hello.js and hello.css.
In Gruntfile.js, write as below, then `grunt`, we can get the index.html which has assets url with md5.

`assetUrl` is the css or js file path
`files` is the file which contains the assets(usually is html file)

Notice to write the correct path.

```js
grunt.initConfig({
    cache: {
      js: {
        options: {
        },
		assetUrl:'demo/js/hello.js',
        files: {
          'tmp': ['demo/index.html'],
        },
      },
      css: {
        options: {
        },
		assetUrl:'demo/css/hello.css',
        files: {
          'tmp': ['demo/index.html'],
        },
      },
    },
});
```


## Contributing
In lieu of a formal styleguide, take care to maintain the existing coding style. Add unit tests for any new or changed functionality. Lint and test your code using [Grunt](http://gruntjs.com/).

## Release History
_(Nothing yet)_
