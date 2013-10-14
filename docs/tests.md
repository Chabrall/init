# Testing Workflow

We provide tools and helpers for a testing workflow based on Grunt.

* JSHint – for checking syntax of JavaScript code
* Jasmine - for unit testing
* Karma - for running unit tests cross browser

All testing frameworks run with GruntJS.

All JavaScript files should be checked with JSHint for syntax errors before committing them.

## Running tests
You can run tests by using the Grunt implementation. Just run `grunt connect:test krama:test` to run all tests with Karma.

For a less extensive unit test with PhantomJS use `grunt connect:test karma:unit`.

## How to set up a Jasmine Test suite
When adding a new test suite you need to do the following:

* Add a file in the folder `tests/specs/`
* Name it `{{spec-name}}.spec.js`
* Add the file name without the extension to the list of dependencies in `tests/spec.js`
* Wrap your test suite in a `define` function call as you can see here in order to get it working with RequireJS
