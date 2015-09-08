# sass-spacing

SASS mixins for margin and padding. 

## Installation

    npm install --save sass-spacing
    
## Usage

### Using the mixins:

SCSS:

    @import "sass-spacing";
    @import "sass-breakpoint";
    
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
    
HTML:

    <div class="tile">
      <h1 class="tile__title">Tile Title</h1>
      <h1 class="tile__content">Tile content...</h1>
    </div>

#### Margin

- `m($size)` - margin on all sides
- `ml($size)` - margin on the left
- `mr($size)` - margin on the right
- `mt($size)` - margin on the tom
- `mb($size)` - margin on the bottom
- `mx($size)` - margin on the left and right
- `my($size)` - margin on the tom and bottom

#### Padding

- `p($size)` - padding on all sides
- `pl($size)` - padding on the left
- `pr($size)` - padding on the right
- `pt($size)` - padding on the top
- `pb($size)` - padding on the bottom
- `px($size)` - padding on the left and right
- `py($size)` - padding on the top and bottom

### Using the pre-compiled stylesheet

HTML:

    <div class="tile" u-xs="p1" u-md="p2">
      <h1 class="tile__title">Tile Title</h1>
      <h1 class="tile__content" u-xs="mt1" u-md="mt2>Tile content...</h1>
    </div>

- Where `m` or `p` is margin or padding
- Where `x`, `y`, `l`, `r`, `t` or `b` is the direction in which the margin or padding is applied 
- Where `0`, `1`, `2`, `3`, `4`, `5` or `6` is the size in `rem` of the margin or padding applied
- Where `u-*` is the breakpoint* from which the margin or padding is applied

#### Direction

- none - margin/padding on all sides
- `l` - margin/padding on the left
- `r` - margin/padding on the right
- `t` - margin/padding on the tom
- `b` - margin/padding on the bottom
- `x` - margin/padding n the left and right
- `y` - margin/padding on the top and bottom

#### Size

- `0` - `0rem` margin/padding
- `1` - `1rem` margin/padding
- `2` - `2rem` margin/padding
- `3` - `3rem` margin/padding
- `4` - `4rem` margin/padding
- `5` - `5rem` margin/padding
- `6` - `6rem` margin/padding

#### Breakpoints

See the [sass-breakpoints](https://www.npmjs.com/package/sass-breakpoints) package for a list of available breakpoints 
and for instructions on customising the available breakpoints. 

## Customisation

You can customise a number of features by defining the following variables before you importing `sass-spacing` in your SASS file.

    //the sizes
    $spacing-sizes: (
      'none': 0,
      'xs': 4px,
      'sm': 8px,
      'md': 16px,
      'lg': 24px,
      'xl': 28px
    );

    //whether !important is used
    $spacing-important: false;
    
    //the attribute prefix for the compiled classes
    $spacing-breakpoint-attribute-prefix: 'breakpoint-';

## Change log

### v1.0.0

- added an option for applying `!important` to margin and padding rules and defaulted the option to true (a breaking change if you're relying on your own classes overriding the spacing mixins/classes)
- changed the names of some options for consistency and to be specific to this module (a breaking change if you're overriding the default options)
- changed the prefix from `g` to `u` - the `g-*` attributes are used for more utilities than just the grid (a breaking change if you're using the compiled classes)
- added support for component
    
## License
    
The MIT License (MIT)

Copyright (c) 2015 James Newell
