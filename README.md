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
      * nightwatch
* Services
  * NO WEBGL
    * ghost inspector: no plans to enable webgl
    * travis-ci
    * circleci
    * sauce labs
  * SKETCHY/UNCONFIRMED
    * browserstack promises webgl on osx.

## Tools for running WebGL tests

- [gl-shader-output](https://github.com/Jam3/gl-shader-output)
- [glslify-testify](https://www.npmjs.com/package/glsl-testify)
- [webgl-compile-shader](https://github.com/mattdesl/webgl-compile-shader)
