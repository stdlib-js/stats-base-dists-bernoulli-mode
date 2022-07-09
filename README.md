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

# Mode

[![NPM version][npm-image]][npm-url] [![Build Status][test-image]][test-url] [![Coverage Status][coverage-image]][coverage-url] <!-- [![dependencies][dependencies-image]][dependencies-url] -->

> [Bernoulli][bernoulli-distribution] distribution [mode][mode].

<!-- Section to include introductory text. Make sure to keep an empty line after the intro `section` element and another before the `/section` close. -->

<section class="intro">

The [mode][mode] for a [Bernoulli][bernoulli-distribution] random variable is

<!-- <equation class="equation" label="eq:bernoulli_mode" align="center" raw="\operatorname{Mode}\left( X \right) = \begin{cases} 0 & \text{if } p < 1/2 \\ 0, 1 &\text{if } p = 1/2 \\ 1 & \text{if } p > 1/2 \end{cases}" alt="Mode for a Bernoulli distribution."> -->

<div class="equation" align="center" data-raw-text="\operatorname{Mode}\left( X \right) = \begin{cases} 0 &amp; \text{if } p &lt; 1/2 \\ 0, 1 &amp;\text{if } p = 1/2 \\ 1 &amp; \text{if } p &gt; 1/2 \end{cases}" data-equation="eq:bernoulli_mode">
    <img src="https://cdn.jsdelivr.net/gh/stdlib-js/stdlib@e1fbdee688c5409e4cc6b0cd06d90b1cd2abd67c/lib/node_modules/@stdlib/stats/base/dists/bernoulli/mode/docs/img/equation_bernoulli_mode.svg" alt="Mode for a Bernoulli distribution.">
    <br>
</div>

<!-- </equation> -->

where `p` is the success probability.

</section>

<!-- /.intro -->

<!-- Package usage documentation. -->



<section class="usage">

## Usage

```javascript
import mode from 'https://cdn.jsdelivr.net/gh/stdlib-js/stats-base-dists-bernoulli-mode@deno/mod.js';
```

#### mode( p )

Returns the [mode][mode] of a [Bernoulli][bernoulli-distribution] distribution with success probability `p`.

```javascript
var v = mode( 0.1 );
// returns 0

v = mode( 0.5 );
// returns 0

v = mode( 0.8 );
// returns 1
```

If provided a success probability `p` outside of `[0,1]`, the function returns `NaN`.

```javascript
var v = mode( NaN );
// returns NaN

v = mode( 1.5 );
// returns NaN

v = mode( -1.0 );
// returns NaN
```

</section>

<!-- /.usage -->

<!-- Package usage notes. Make sure to keep an empty line after the `section` element and another before the `/section` close. -->

<section class="notes">

## Notes

-   For `p = 0.5`, the mode is either `0` or `1`. This implementation returns `0` for `p = 0.5`.

</section>

<!-- /.notes -->

<!-- Package usage examples. -->

<section class="examples">

## Examples

<!-- eslint no-undef: "error" -->

```javascript
import randu from 'https://cdn.jsdelivr.net/gh/stdlib-js/random-base-randu@deno/mod.js';
import round from 'https://cdn.jsdelivr.net/gh/stdlib-js/math-base-special-round@deno/mod.js';
import mode from 'https://cdn.jsdelivr.net/gh/stdlib-js/stats-base-dists-bernoulli-mode@deno/mod.js';

var v;
var i;
var p;

for ( i = 0; i < 10; i++ ) {
    p = randu();
    v = mode( p );
    console.log( 'p: %d, Mode(X;p): %d', p.toFixed( 4 ), v.toFixed( 4 ) );
}
```

</section>

<!-- /.examples -->

<!-- Section to include cited references. If references are included, add a horizontal rule *before* the section. Make sure to keep an empty line after the `section` element and another before the `/section` close. -->

<section class="references">

</section>

<!-- /.references -->

<!-- Section for related `stdlib` packages. Do not manually edit this section, as it is automatically populated. -->

<section class="related">

</section>

<!-- /.related -->

<!-- Section for all links. Make sure to keep an empty line after the `section` element and another before the `/section` close. -->


<section class="main-repo" >

* * *

## Notice

This package is part of [stdlib][stdlib], a standard library with an emphasis on numerical and scientific computing. The library provides a collection of robust, high performance libraries for mathematics, statistics, streams, utilities, and more.

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

[npm-image]: http://img.shields.io/npm/v/@stdlib/stats-base-dists-bernoulli-mode.svg
[npm-url]: https://npmjs.org/package/@stdlib/stats-base-dists-bernoulli-mode

[test-image]: https://github.com/stdlib-js/stats-base-dists-bernoulli-mode/actions/workflows/test.yml/badge.svg?branch=v0.0.8
[test-url]: https://github.com/stdlib-js/stats-base-dists-bernoulli-mode/actions/workflows/test.yml?query=branch:v0.0.8

[coverage-image]: https://img.shields.io/codecov/c/github/stdlib-js/stats-base-dists-bernoulli-mode/main.svg
[coverage-url]: https://codecov.io/github/stdlib-js/stats-base-dists-bernoulli-mode?branch=main

<!--

[dependencies-image]: https://img.shields.io/david/stdlib-js/stats-base-dists-bernoulli-mode.svg
[dependencies-url]: https://david-dm.org/stdlib-js/stats-base-dists-bernoulli-mode/main

-->

[chat-image]: https://img.shields.io/gitter/room/stdlib-js/stdlib.svg
[chat-url]: https://gitter.im/stdlib-js/stdlib/

[stdlib]: https://github.com/stdlib-js/stdlib

[stdlib-authors]: https://github.com/stdlib-js/stdlib/graphs/contributors

[umd]: https://github.com/umdjs/umd
[es-module]: https://developer.mozilla.org/en-US/docs/Web/JavaScript/Guide/Modules

[deno-url]: https://github.com/stdlib-js/stats-base-dists-bernoulli-mode/tree/deno
[umd-url]: https://github.com/stdlib-js/stats-base-dists-bernoulli-mode/tree/umd
[esm-url]: https://github.com/stdlib-js/stats-base-dists-bernoulli-mode/tree/esm
[branches-url]: https://github.com/stdlib-js/stats-base-dists-bernoulli-mode/blob/main/branches.md

[stdlib-license]: https://raw.githubusercontent.com/stdlib-js/stats-base-dists-bernoulli-mode/main/LICENSE

[bernoulli-distribution]: https://en.wikipedia.org/wiki/Bernoulli_distribution

[mode]: https://en.wikipedia.org/wiki/Mode_%28statistics%29

</section>

<!-- /.links -->
