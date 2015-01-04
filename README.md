# mat4-css-parse

[![stable](http://badges.github.io/stability-badges/dist/stable.svg)](http://github.com/badges/stability-badges)

Takes a `transform` string from an element's computed style, and returns a mat4 representation of the 3D matrix. Useful alongside [mat4-css-stringify](https://nodei.co/npm/mat4-css-parse/).

Cases:

- `matrix3d()` string
- `matrix()` string (returns 3D representation of the 2D matrix)
- `none` which results in an identity matrix

Simple example:

```js
var parse = require('mat4-css-parse')

var mat4 = parse(computedStyle.tranfsorm)
//... now we can do some matrix operations 
```

## Usage

[![NPM](https://nodei.co/npm/mat4-css-parse.png)](https://nodei.co/npm/mat4-css-parse/)

#### `toMat4(str[, out])`

Converts the `transform` CSS string into a 16-float array representing a 4x4 matrix. 2D matrices will be stored in the upper left of a 4x4 identity matrix.

You can specify an `out` matrix parameter, otherwise it will create a new 16-length array.

## License

MIT, see [LICENSE.md](http://github.com/mattdesl/mat4-css-parse/blob/master/LICENSE.md) for details.
