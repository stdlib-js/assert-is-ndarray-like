<!--

@license Apache-2.0

Copyright (c) 2018 The Stdlib Authors.

Licensed under the Apache License, Version 2.0 (the "License");
you may not use this file except in compliance with the License.
You may obtain a copy of the License at

   http://www.apache.org/licenses/LICENSE-2.0

Unless required by applicable law or agreed to in writing, software
distributed under the License is distributed on an "AS IS" BASIS,
WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND, either express or implied.
See the License for the specific language governing permissions and
limitations under the License.

-->

# isndarrayLike

[![NPM version][npm-image]][npm-url] [![Build Status][test-image]][test-url] [![Coverage Status][coverage-image]][coverage-url] <!-- [![dependencies][dependencies-image]][dependencies-url] -->

> Test if a value is [ndarray][@stdlib/ndarray/ctor]-like.



<section class="usage">

## Usage

To use in Observable,

```javascript
isndarrayLike = require( 'https://cdn.jsdelivr.net/gh/stdlib-js/assert-is-ndarray-like@umd/browser.js' )
```

To vendor stdlib functionality and avoid installing dependency trees for Node.js, you can use the UMD server build:

```javascript
var isndarrayLike = require( 'path/to/vendor/umd/assert-is-ndarray-like/index.js' )
```

To include the bundle in a webpage,

```html
<script type="text/javascript" src="https://cdn.jsdelivr.net/gh/stdlib-js/assert-is-ndarray-like@umd/browser.js"></script>
```

If no recognized module system is present, access bundle contents via the global scope:

```html
<script type="text/javascript">
(function () {
(function () {
    window.isndarrayLike;
})();
})();
</script>
```

#### isndarrayLike( value )

Tests if a value is [ndarray][@stdlib/ndarray/ctor]-like.

```javascript
var ndarray = require( '@stdlib/ndarray-ctor' );

var arr = ndarray( 'generic', [ 0, 0, 0, 0 ], [ 2, 2 ], [ 2, 1 ], 0, 'row-major' );
var bool = isndarrayLike( arr );
// returns true
```

A value is [ndarray][@stdlib/ndarray/ctor]-like if a value is an `object` with the following properties:

-   **dtype**: `string` specifying a data type.
-   **data**: `object` pointing to an underlying data buffer.
-   **shape**: array-like `object` containing dimensions.
-   **strides**: array-like `object` containing stride lengths.
-   **offset**: `number` specifying the index offset.
-   **order**: `string` describing the memory layout.
-   **ndims**: `number` specifying the number of dimensions.
-   **length**: `number` specifying the total number of elements.
-   **flags**: `object` containing meta data.
-   **get**: `function` for retrieving elements.
-   **set**: `function` for setting elements.

</section>

<!-- /.usage -->

<section class="examples">

## Examples

<!-- eslint no-undef: "error" -->

```html
<!DOCTYPE html>
<html lang="en">
<body>
<script type="text/javascript" src="https://cdn.jsdelivr.net/gh/stdlib-js/ndarray-ctor@umd/browser.js"></script>
<script type="text/javascript" src="https://cdn.jsdelivr.net/gh/stdlib-js/assert-is-ndarray-like@umd/browser.js"></script>
<script type="text/javascript">
(function () {
(function () {

var arr = ndarray( 'generic', [ 0, 0, 0, 0 ], [ 2, 2 ], [ 2, 1 ], 0, 'row-major' );
var bool = isndarrayLike( arr );
// returns true

bool = isndarrayLike( [ 1, 2, 3, 4 ] );
// returns false

bool = isndarrayLike( {} );
// returns false

bool = isndarrayLike( null );
// returns false

})();
})();
</script>
</body>
</html>
```

</section>

<!-- /.examples -->

<!-- Section for related `stdlib` packages. Do not manually edit this section, as it is automatically populated. -->

<section class="related">

* * *

## See Also

-   <span class="package-name">[`@stdlib/assert/is-array`][@stdlib/assert/is-array]</span><span class="delimiter">: </span><span class="description">test if a value is an array.</span>
-   <span class="package-name">[`@stdlib/assert/is-array-like`][@stdlib/assert/is-array-like]</span><span class="delimiter">: </span><span class="description">test if a value is array-like.</span>
-   <span class="package-name">[`@stdlib/assert/is-matrix-like`][@stdlib/assert/is-matrix-like]</span><span class="delimiter">: </span><span class="description">test if a value is a 2-dimensional ndarray-like object.</span>
-   <span class="package-name">[`@stdlib/assert/is-typed-array-like`][@stdlib/assert/is-typed-array-like]</span><span class="delimiter">: </span><span class="description">test if a value is typed-array-like.</span>
-   <span class="package-name">[`@stdlib/assert/is-vector-like`][@stdlib/assert/is-vector-like]</span><span class="delimiter">: </span><span class="description">test if a value is a 1-dimensional ndarray-like object.</span>

</section>

<!-- /.related -->

<!-- Section for all links. Make sure to keep an empty line after the `section` element and another before the `/section` close. -->


<section class="main-repo" >

* * *

## Notice

This package is part of [stdlib][stdlib], a standard library for JavaScript and Node.js, with an emphasis on numerical and scientific computing. The library provides a collection of robust, high performance libraries for mathematics, statistics, streams, utilities, and more.

For more information on the project, filing bug reports and feature requests, and guidance on how to develop [stdlib][stdlib], see the main project [repository][stdlib].

#### Community

[![Chat][chat-image]][chat-url]

---

## License

See [LICENSE][stdlib-license].


## Copyright

Copyright &copy; 2016-2022. The Stdlib [Authors][stdlib-authors].

</section>

<!-- /.stdlib -->

<!-- Section for all links. Make sure to keep an empty line after the `section` element and another before the `/section` close. -->

<section class="links">

[npm-image]: http://img.shields.io/npm/v/@stdlib/assert-is-ndarray-like.svg
[npm-url]: https://npmjs.org/package/@stdlib/assert-is-ndarray-like

[test-image]: https://github.com/stdlib-js/assert-is-ndarray-like/actions/workflows/test.yml/badge.svg?branch=main
[test-url]: https://github.com/stdlib-js/assert-is-ndarray-like/actions/workflows/test.yml?query=branch:main

[coverage-image]: https://img.shields.io/codecov/c/github/stdlib-js/assert-is-ndarray-like/main.svg
[coverage-url]: https://codecov.io/github/stdlib-js/assert-is-ndarray-like?branch=main

<!--

[dependencies-image]: https://img.shields.io/david/stdlib-js/assert-is-ndarray-like.svg
[dependencies-url]: https://david-dm.org/stdlib-js/assert-is-ndarray-like/main

-->

[chat-image]: https://img.shields.io/gitter/room/stdlib-js/stdlib.svg
[chat-url]: https://gitter.im/stdlib-js/stdlib/

[stdlib]: https://github.com/stdlib-js/stdlib

[stdlib-authors]: https://github.com/stdlib-js/stdlib/graphs/contributors

[umd]: https://github.com/umdjs/umd
[es-module]: https://developer.mozilla.org/en-US/docs/Web/JavaScript/Guide/Modules

[deno-url]: https://github.com/stdlib-js/assert-is-ndarray-like/tree/deno
[umd-url]: https://github.com/stdlib-js/assert-is-ndarray-like/tree/umd
[esm-url]: https://github.com/stdlib-js/assert-is-ndarray-like/tree/esm
[branches-url]: https://github.com/stdlib-js/assert-is-ndarray-like/blob/main/branches.md

[stdlib-license]: https://raw.githubusercontent.com/stdlib-js/assert-is-ndarray-like/main/LICENSE

[@stdlib/ndarray/ctor]: https://github.com/stdlib-js/ndarray-ctor/tree/umd/tree/umd

<!-- <related-links> -->

[@stdlib/assert/is-array]: https://github.com/stdlib-js/assert-is-array/tree/umd/tree/umd

[@stdlib/assert/is-array-like]: https://github.com/stdlib-js/assert-is-array-like/tree/umd/tree/umd

[@stdlib/assert/is-matrix-like]: https://github.com/stdlib-js/assert-is-matrix-like/tree/umd/tree/umd

[@stdlib/assert/is-typed-array-like]: https://github.com/stdlib-js/assert-is-typed-array-like/tree/umd/tree/umd

[@stdlib/assert/is-vector-like]: https://github.com/stdlib-js/assert-is-vector-like/tree/umd/tree/umd

<!-- </related-links> -->

</section>

<!-- /.links -->
