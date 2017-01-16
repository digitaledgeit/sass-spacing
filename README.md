# sass-spacing

CSS classes/mixins for responsive margins and padding.

## Installation

```bash
npm install --save sass-spacing
```

## Usage

### Using the classes:

HTML:

```html
<link rel="stylesheet" href="node_modules/sass-spacing/index.css"/>

<div class="tile p:1@xs p:2@md">
  <h1 class="tile__title">My Title</h1>
  <p class="tile__content mt:1@xs mt:2@md">My content...</p>
</div>
```

- Where `m` or `p` is margin or padding
- Where `x`, `y`, `l`, `r`, `t` or `b` is the direction in which the margin or padding is applied
- Where `0`, `1`, `2`, `3`, `4`, `5`, `6` or `auto` is the size of the margin or padding applied
- Where `@*` is the breakpoint from which the margin or padding is applied

### Using the mixins:

SCSS:

```scss
@import "sass-spacing/mixins.scss";
@import "sass-breakpoints/mixins.scss";

.tile {
  @include p(1);
  @include breakpoint('md') {
    @include p(2);
  }
}

.tile__content {
  @include mt(1);
    @include breakpoint('md') {
      @include mt(2);
    }
}
```

HTML:

```html
  <div class="tile">
    <h1 class="tile__title">Tile Title</h1>
    <h1 class="tile__content">Tile content...</h1>
  </div>
```

###### Margin

- `m($size)`
- `m($y, $x)`
- `m($t, $x, $b)`
- `m($t, $r, $b, $l)`


- `mx($size)`
- `mx($r, $l)`
- `my($size)`
- `my($t, $b)`


- `mt($size)`
- `mr($size)`
- `mb($size)`
- `ml($size)`

Where `x`, `y`, `l`, `r`, `t` or `b` is the direction in which the margin is applied.

Where `0`, `1`, `2`, `3`, `4`, `5`, `6` or `auto` is the `$size` of the margin applied.

###### Padding

- `p($size)`
- `p($y, $x)`
- `p($t, $x, $b)`
- `p($t, $r, $b, $l)`


- `px($size)`
- `px($r, $l)`
- `py($size)`
- `py($t, $b)`


- `pt($size)`
- `pr($size)`
- `pb($size)`
- `pl($size)`

Where `x`, `y`, `l`, `r`, `t` or `b` is the direction in which the padding is applied.

Where `0`, `1`, `2`, `3`, `4`, `5` or `6` is the `$size` of the padding applied.

## Directions

- none - margin/padding on all sides
- `x` - margin/padding on the left and right
- `y` - margin/padding on the top and bottom
- `l` - margin/padding on the left
- `r` - margin/padding on the right
- `t` - margin/padding on the tom
- `b` - margin/padding on the bottom

## Sizes

- `0` - `0rem` margin/padding
- `1` - `.25rem` margin/padding
- `2` - `.5rem` margin/padding
- `3` - `1rem` margin/padding
- `4` - `2rem` margin/padding
- `5` - `4rem` margin/padding
- `6` - `8rem` margin/padding
- `auto` - `auto` margin only

## Breakpoints

See the [sass-breakpoints](https://www.npmjs.com/package/sass-breakpoints) package for a list of available breakpoints.

## Customisation

You can customise a number of features by defining the following variables before importing `sass-spacing` in your SASS file.

```scss
//specify some alternate sizing scheme
$spacing-sizes: (
  'none': 0,
  'xs': 4px,
  'md': 16px,
  'xl': 28px
);

//specify whether !important is applied
$spacing-important: false;

```

See the [sass-breakpoints](https://www.npmjs.com/package/sass-breakpoints) package for instructions on customising the available breakpoints.

## Change log

### v2.0.0

- changed the default margin-padding sizes
- switched from attributes to class names
- removed support for ComponentJS

### v1.1.1

- added missing `m($t, $x, $b)` and `p($t, $x, $b)` overrides

### v1.1.0

- added `auto` size to margin
- added overrides for `m()` and `p()` to set multiple properties at once

### v1.0.0

- added an option for applying `!important` to margin and padding rules and defaulted the option to true (a breaking change if you're relying on your own classes overriding the spacing mixins/classes)
- changed names of the options for improved consistency and to prevent clashes with other modules (a breaking change if you're overriding the default options)
- changed the prefix from `g` to `u` - the `g-*` attributes are used for more utilities than just the grid (a breaking change if you're using the compiled classes)
- added support for ComponentJS

## License

The MIT License (MIT)

Copyright (c) 2015 James Newell
