# Bits.sass responsive grid

Responsive superset of grid component.

See [Bits.sass grid](https://github.com/bits-sass/grid) for more about
the component itself.

N.B. This component relies on particular responsive dimensions being applied to
cells in the grid via other classes. For example,
[Bits.sass responsive dimension]
(https://github.com/bits-sass/responsive-utils-dimension).
If you need responsive gutters inbetween cells, see [Bits.sass responsive space]
(https://github.com/bits-sass/responsive-utils-space).

## Installation

* __Bower:__ `bower install --save bits-sass-responsive-grid`
* __Download:__ [zip](https://github.com/bits-sass/responsive-grid/zipball/master),
[tar.gz](https://github.com/bits-sass/responsive-grid/tarball/master)
* __Git:__ `git clone https://github.com/bits-sass/responsive-grid.git`

## Available SASS variables

* `bits-components-ns` - components namespace, defaults to 'bits-'
* `bits-responsive-grid-columns` - list of generated columns

## Available classes

* `v[n]-Grid` - grid component on `n` breakpoint
* `v[n]-Grid--center` - horizontally center all grid units on `n` breakpoint
* `v[n]-Grid--middle` - vertically align all grid units to middle on `n` breakpoint
* `v[n]-Grid--bottom` - vertically align all grid units to bottom on `n` breakpoint
* `v[n]-Grid--[x]col` - (adjustable) grid of `x` columns on `n` breakpoint
* `v[n]-Grid-cell` - descendant class representing a unit on `n` breakpoint
* `v[n]-Grid-cell--center` - horizontally center one unit on `n` breakpoint

## Usage

Grid that starts at 2 columns and switches to 3 columns at `v3` breakpoint AND
switches to 4 columns at `v6` breakpoint.

```html
<div class="Grid Grid--2col v3-Grid--3col v6-Grid--4col">
  <div class="Grid-cell">…</div>
  <div class="Grid-cell">…</div>
  <div class="Grid-cell">…</div>
  <div class="Grid-cell">…</div>
  <div class="Grid-cell">…</div>
  <div class="Grid-cell">…</div>
</div>
```

A set of paragraphs that turn into 2 columns at `v4` breakpoint (not a very good
example).

```html
<div class="v4-Grid v4-Grid--2col v4-Grid--center">
  <p class="v4-Grid-cell>
    …
  </p>
  <p class="v4-Grid-cell>
    …
  </p>
  <p class="v4-Grid-cell>
    …
  </p>
  <p class="v4-Grid-cell>
    …
  </p>
</div>
```

A grid used in conjuction with [Bits.sass responsive dimension]
(https://github.com/bits-sass/responsive-utils-dimension).

```html
<div class="Grid">
  <div class="v3-u-size1of3 v5-u-size1of5">
    …
  </div>
  <div class="v3-u-size2of3 v5-u-size4of5">
    …
  </div>
</div>
```

## Requirements

* Sass 3.2+

## Browser support

* Google Chrome (latest)
* Opera (latest)
* Firefox 4+
* Safari 5+
* Internet Explorer 9+ (IE 8 requires a build step)