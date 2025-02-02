# CKEditor 5 rich text editor component for React

[![Join the chat at https://gitter.im/ckeditor/ckeditor5](https://badges.gitter.im/ckeditor/ckeditor5.svg)](https://gitter.im/ckeditor/ckeditor5?utm_source=badge&utm_medium=badge&utm_campaign=pr-badge&utm_content=badge)
[![npm version](https://badge.fury.io/js/%40ckeditor%2Fckeditor5-react.svg)](https://www.npmjs.com/package/@ckeditor/ckeditor5-react)
[![Build Status](https://travis-ci.org/ckeditor/ckeditor5-react.svg?branch=master)](https://travis-ci.org/ckeditor/ckeditor5-react)
[![Coverage Status](https://coveralls.io/repos/github/ckeditor/ckeditor5-react/badge.svg?branch=master)](https://coveralls.io/github/ckeditor/ckeditor5-react?branch=master)
<br>
[![Dependency Status](https://david-dm.org/ckeditor/ckeditor5-react/status.svg)](https://david-dm.org/ckeditor/ckeditor5-react)
[![devDependency Status](https://david-dm.org/ckeditor/ckeditor5-react/dev-status.svg)](https://david-dm.org/ckeditor/ckeditor5-react?type=dev)

Official [CKEditor 5](https://ckeditor.com/ckeditor-5/) rich text editor component for React.

## [Developer Documentation](https://ckeditor.com/docs/ckeditor5/latest/builds/guides/integration/frameworks/react.html) 📖

See the ["Rich text editor component for React"](https://ckeditor.com/docs/ckeditor5/latest/builds/guides/integration/frameworks/react.html) guide in the [CKEditor 5 documentation](https://ckeditor.com/docs/ckeditor5/latest) to learn more:

* [Quick start](https://ckeditor.com/docs/ckeditor5/latest/builds/guides/integration/frameworks/react.html#quick-start)
	* [Component properties](https://ckeditor.com/docs/ckeditor5/latest/builds/guides/integration/frameworks/react.html#component-properties)
	* [Customizing the builds](https://ckeditor.com/docs/ckeditor5/latest/builds/guides/integration/frameworks/react.html#customizing-the-builds)
* [Integrating CKEditor 5 built from source](https://ckeditor.com/docs/ckeditor5/latest/builds/guides/integration/frameworks/react.html#integrating-ckeditor-5-built-from-source)
	* [Using `create-react-app@2`](https://ckeditor.com/docs/ckeditor5/latest/builds/guides/integration/frameworks/react.html#using-create-react-app2)
	* [Using `create-react-app@1`](https://ckeditor.com/docs/ckeditor5/latest/builds/guides/integration/frameworks/react.html#using-create-react-app1)

## Contributing

After cloning this repository, install necessary dependencies:

```bash
npm install
```

### Executing tests

Before starting tests execution, you need to build the package. You can use `npm run build` in order to build the production-ready version
or `npm run develop` which produces a development version with attached watcher for all sources files.

```bash
npm run test -- [additional options]
# or
npm t -- [additional options]
```

The command accepts the following options:

* `--coverage` (`-c`) &ndash; Whether to generate the code coverage.
* `--source-map` (`-s`) &ndash; Whether to attach the source maps.
* `--watch` (`-w`) &ndash; Whether to watch test files.
* `--reporter` (`-r`) &ndash; Reporter for Karma (default: `mocha`, can be changed to `dots`).
* `--browsers` (`-b`) &ndash; Browsers that will be used to run tests (default: `Chrome`, available: `Firefox`, `BrowserStack_Edge` and `BrowserStack_Safari`).

**Note:** If you would like to use the `BrowserStack_*` browser, you need to specify the `BROWSER_STACK_USERNAME` and `BROWSER_STACK_ACCESS_KEY` as
an environment variable, e.g.:

```bash
BROWSER_STACK_USERNAME=[...] BROWSER_STACK_ACCESS_KEY=[...] npm t -- -b BrowserStack_Edge,BrowserStack_Safari -c
```

### Building the package

Build a minified version of the package that is ready to publish:

```bash
npm run build
```

## Releasing package

### Changelog

Before starting the release process, you need to generate the changelog:

```bash
npm run changelog
```

### Publishing

After generating the changelog, you are able to release the package.

First, you need to bump the version:

```bash
npm run release:bump-version
```

You can also use the `--dry-run` option in order to see what this task does.

After bumping the version, you can publish the changes:

```bash
npm run release:publish
```

As in the previous task, the `--dry-run` option is also available. 

Note: Only the `dist/` directory will be published.

## License

Licensed under the terms of [GNU General Public License Version 2 or later](http://www.gnu.org/licenses/gpl.html). For full details about the license, please check the LICENSE.md file.
