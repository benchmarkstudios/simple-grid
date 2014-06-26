# Just a simple grid

Based on existing grid systems, such as [Twitter Bootstrap Grid System](http://getbootstrap.com/css/#grid) and [csswizardry-grids](http://csswizardry.com/csswizardry-grids/), by [CSS Wizardry](http://csswizardry.com/), this is a simple, fluid, nestable, flexible, Sass-based, responsive grid system.


## Setup

The only thing you need to do to start building your grid is to adjust the number of `$grid-columns`, the desired `$gutter` and the main container `$max-width`.

## How it works

Grid systems, as you may know, are used for creating page layouts through a series of rows and columns that will host your content. How it really works:

* Your `.row` element(s) must be placed within a `.container`, with a fixed `$max-width` for proper alignment. This elements will split up your page horizontally and will contain groups of `.col`.
* Your content should be placed within the `.col` blocks, and only `.col` may be immediate children of `.row`.
* You can nest `.row` and `.col` how many times you need, since you follow the previous standard.
* Your`.col` width is defined by specifying the number of a single grid columns, in your total `$grid-columns`. For example, a `.col--lg-4` will represent a width of 4 columns in your `$grid-columns` total.
* To control your responsive grid, there are available three class prefixes: `.col--sm-*` for small devices, `.col-md-*` for medium devices and `.col--lg-*` for large devices. All together, in your `.col` element, it will make your grid respond to each one of your default media queries.
* Finaly, you have the option to move columns to the right using `.col--md-offset-*` classes. These classes increase the left margin of a column by the number of columns you want. For example, `.col--md-offset-4` will push `.col-md-4` over four columns.


## Markup

### Basic usage
Simple column set - `<div class="col col--sd-12 col--md-12 col--ld-12"></div>` - inside a `.row`.

```html
  <div class="row">
    <div class="col col--sd-12 col--md-12 col--ld-12">
      <p>Col 1</p>
    </div>
  </div>
  <div class="row">
    <div class="col col--sd-12 col--md-6 col--ld-6">
      <p>Col 2</p>
    </div>
    <div class="col col--sd-12 col--md-6 col--ld-6">
      <p>Col 3</p>
    </div>
  </div>
  <div class="row">
    <div class="col col--sd-12 col--md-4 col--ld-4">
      <p>Col 4</p>
    </div>
    <div class="col col--sd-12 col--md-4 col--ld-4">
      <p>Col 5</p>
    </div>
    <div class="col col--sd-12 col--md-4 col--ld-4">
      <p>Col 6</p>
    </div>
  </div>
  <div class="row">
    <div class="col col--sd-12 col--md-8 col--ld-8">
      <p>Col 7</p>
    </div>
    <div class="col col--sd-12 col--md-4 col--ld-4">
      <p>Col 8</p>
    </div>
  </div>
```

### Offsetting columns
Increase the left margin of a column by the number of columns you want, along with the responsive class prefixes, if you need.

```html
  <div class="row">
    <div class="col col--sd-12 col--md-4 col--ld-4">
      <p>Col 9 with offset 0</p>
    </div>
    <div class="col col--sd-12 col--md-4 col--ld-4 col--md-offset-4 col--ld-offset-4">
      <p>Col 10 with offset 4</p>
    </div>
  </div>
  <div class="row">
    <div class="col col--sd-12 col--md-3 col--ld-3 col--md-offset-3 col--ld-offset-3">
      <p>Col 11 with offset 3</p>
    </div>
    <div class="col col--sd-12 col--md-3 col--ld-3 col--md-offset-6 col--ld-offset-6">
      <p>Col 12 with offset 6</p>
    </div>
  </div>
  <div class="row">
    <div class="col col--sd-12 col--md-6 col--ld-6 col--md-offset-3 col--ld-offset-3">
      <p>Col 13 with offset 3</p>
    </div>
  </div>
  </div>
```

### Nesting columns
To nest your content, add a new `.row` inside a `.col`, and set of `.col-ld-*` columns within an existing `.col-ld-*` column. Nested rows should include a set of columns that add up to 12 or less.

```html
  <div class="row">
    <div class="col col--sd-12 col--md-12 col--ld-12">
      <p>Col 14</p>
      <div class="row">
        <div class="col col--sd-12 col--md-6 col--ld-6">
          <p>Nested col 14.1</p>
        </div>
        <div class="col col--sd-12 col--md-6 col--ld-6">
          <p>Nested col 14.2</p>
        </div>
      </div>
    </div>
  </div>
```

## Demo
Check out the demo and play around on [Code Pen] (http://codepen.io/pedroreis/pen/ituho) and/or check the compiled CSS on [SassMeister](http://sassmeister.com/gist/75073548a2a598f75e40).
