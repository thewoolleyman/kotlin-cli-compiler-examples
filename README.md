# Kotlin CLI Compiler Examples

Examples of using kotlin CLI to perform multiplatform compiles.

# JVM

* Review https://kotlinlang.org/docs/tutorials/command-line.html
* `./jvm-compile-and-run`

# Javascript

* Review https://kotlinlang.org/docs/tutorials/javascript/getting-started-command-line/command-line-library-js.html
* CommonJS vs AMD vs UMD:
  * Review general differences between CommonJS vs AMD:
    * https://stackoverflow.com/a/16522990/25192
    * https://requirejs.org/docs/whyamd.html
  * Review http://kotlinlang.org/docs/reference/js-modules.html  
  * Review https://kotlinlang.org/docs/tutorials/javascript/working-with-modules/working-with-modules.html#using-amd
  * Review https://kotlinlang.org/docs/tutorials/javascript/working-with-modules/working-with-modules.html#using-commonjs
  * AMD is used when targeting to run in the browser.
  * CommonJS is used when targeting to run on the server via NodeJS
    (e.g. as an AWS Lambda function).
  * "UMD tries to unify both models allowing these to be used either on the client
    or server" 

Setup local JS env, because the kotlin runtime must be
installed under `node_modules` in order to be found:

* `brew install node`
* `brew install yarn`
* `yarn install`
  
Setup steps which were taken to generate `package.json` with
kotlin runtime as dependency(not necessary to be run again):

* `yarn init`
* `yarn add kotlin`

Compile (via UMD):

* `./js-compile`

Run via CommonJS (via node / server side):

* `./js-node-run`

Run via AMD (via browser / client side"):

* `./js-browser-run`
