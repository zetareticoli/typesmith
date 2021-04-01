# typesmith
Responsive Typography Library

## What is Typesmith

Typesmith is a **typography library designed for the responsive web**. It provides **a set of type sizes** defined in `px` to better align with your design tools (Figma, Sketc, etc.). 

The **type sizes names** come from traditional English speaking world:
- Canon *32/36* 
- Double Pica *28/32*
- Paragon *26/28*
- Columbian *24*
- Primer *20*
- English *18*
- Pica *16*
- Brevier *14*
- Minion *12*

It uses a custom **Type Scale** starting from the Major Second scale (1.125) rounding up numbers to work well with a 4px baseline. Canon, Double Pica and Paragon have responsive sizes only. This is because only the first three sizes used for headlines need to change.

## Installation

Install via NPM

```bash
npm i --save typesmith-lib`
```

Import Typesmith in your project:

```scss
// style.scss
@import 'node_modules/typesmith-lib/_typesmith-lib';

```
## Usage

You can use Typesmith in two different ways:

1. Using `@type-size` mixin in a selector:

    ```scss
      .foo {
        @mixin type-size(canon, medium, ratio)
      }
    ```

2. Use default Typesmith classes in HTML:

    ```html
    <h1 class="type-canon">This is a Headline</h1>
    ```
## Customizations
### 1. Vertical Rhythm

There are two option for vertical rhythm:

- baseline - 4px
- ratio - 1.25
  
You can customize the vertical rhythm **setting your own custom properties**:

```css

@import '_typesmith.scss'

:root {
  --baseline: foo; /* Use size values in px or rem */
  --ratio: bar; /* Use a number value, like 1 or 1.5 */
}
```
### 2. Breakpoints
You can control the media-query for three type sizes: Canon, Double Pica, Paragon.

Set the `$bp` variable before the `@import` statement like following:

```scss
// Accepted values: small, medium , large, xlarge

$bp: large;

@import '../_typesmith-lib.scss';
```

See [typesmit.scss](src/typesmith.scss) file as example.

Breakpoints values are defined in [mq](/node_modules/sass-mq-lib/_mq.scss).

## Dependencies
I order to use the libary you will need following tools:
- [mq](https://github.com/zetareticoli/mq)

## Author
[Francesco Improta](https://www.francescoimprota.com)

## License
MIT License

Copyright (c) [2020] [Francesco Improta]

Permission is hereby granted, free of charge, to any person obtaining a copy
of this software and associated documentation files (the "Software"), to deal
in the Software without restriction, including without limitation the rights
to use, copy, modify, merge, publish, distribute, sublicense, and/or sell
copies of the Software, and to permit persons to whom the Software is
furnished to do so, subject to the following conditions:

The above copyright notice and this permission notice shall be included in all
copies or substantial portions of the Software.

THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR
IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY,
FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE
AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER
LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM,
OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN THE
SOFTWARE.
