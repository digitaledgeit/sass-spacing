# sass-spacing

SASS mixins for margins and paddings. 

With a bonus set of compiled responsive margin and padding classes.

## Installation

    npm install --save sass-spacing
    
## Usage

Using mixins:

    @import "sass-spacing";
    
    .tile {
      @include m(2); //margin: 2rem;
      @include p(1); //padding: 1rem;
    }
    
    .tile__title {
      @include my(1); //margin-top: 1rem; margin-bottom: 1rem;
    }
    
Using the pre-compiled stylesheet:

    <link href="sass-spacing/dist/compiled.css" rel="stylesheet"/>

    <div class="tile" g-xs="m2 p1" g-md="m4 p2">
      <h1 class="tile__title" g-xs="my1" g-md="my3">Tile Title</h1>
    </div>
    
## License
    
The MIT License (MIT)

Copyright (c) 2014 James Newell

Permission is hereby granted, free of charge, to any person obtaining a copy of this software and associated documentation files (the "Software"), to deal in the Software without restriction, including without limitation the rights to use, copy, modify, merge, publish, distribute, sublicense, and/or sell copies of the Software, and to permit persons to whom the Software is furnished to do so, subject to the following conditions:

The above copyright notice and this permission notice shall be included in all copies or substantial portions of the Software.

THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY, FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM, OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN THE SOFTWARE.