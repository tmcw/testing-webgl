# testing-webgl

Notes on continuous-integration testing WebGL applications and libraries.

The key, first, is to separate applications and libraries: libraries can possibly be tested headlessly,
whereas applications usually cannot.

* Software
  * Headless: These are testing solutions that run in node.js or without an open browser.
    * WORKING
      * [headless-gl](https://github.com/stackgl/headless-gl) allows usage of a WebGL-style context via node.js
    * NO WEBGL
      * phantomjs: [no WebGL support, no support planned.](http://phantomjs.org/supported-web-standards.html)
  * Headfull
    * WORKING
      * hughsk/smokestack
      * zuul
      * karma
* Services
  * NO WEBGL
    * ghost inspector
    * travis-ci
  * SKETCHY/UNCONFIRMED
    * browserstack promises webgl on osx.
    * sauce labs has webgl on some boxes. most boxes do not have webgl. sauce has not been reliable enough to use.
