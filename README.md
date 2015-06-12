# Just a simple grid

Based on existing grid systems, such as [Twitter Bootstrap Grid System](http://getbootstrap.com/css/#grid) and [csswizardry-grids](http://csswizardry.com/csswizardry-grids/), this is a fluid, flexible and responsive grid that can be scaled up to an arbitrary size, within the `$max-width` of your main `.container`. You also can easily and infinitly nest columns and rows, so you can build out complicated layouts without creating a lot of new custom elements. This is a grid system generated by Sass and it is based on [BEM syntax](http://csswizardry.com/2013/01/mindbemding-getting-your-head-round-bem-syntax/).

## Setup

The only thing you need to do to start building your grid is to adjust the number of `$grid-columns`, the desired `$gutter` and the main container `$max-width`.

## How it works

Grid systems, as you may know, are used for creating page layouts through a series of rows and columns that will host your content:

* Your `.row` element(s) must be placed within a `.container`, with a fixed `$max-width` for proper alignment. This elements will split up your page horizontally and will contain groups of `.col`.
* Your content should be placed within the `.col` blocks, and only `.col` may be immediate children of `.row`.
* You can nest `.row` and `.col` how many times you need, since you follow the previous standard.
* Your `.col` width is defined by specifying the number of a single grid columns, in your total `$grid-columns`. For example, a `.col--*-4` will represent a width of 4 columns in your `$grid-columns` total.
* To control your responsive grid, there are available three class prefixes: `.col--sm-*` for small devices, `.col-md-*` for medium devices and `.col--lg-*` for large devices. All together, in your `.col` element, it will make your grid respond to each one of your default media queries.
* Finaly, you have the option to move columns to the right using `.col--*-offset-*` classes. These classes increase the left margin of a column by the number of columns you want. For example, `.col--*-offset-4` will push `.col-*-4` over four columns.


## Markup

### Basic usage
Simple column set - `<div class="col col--xs-12 col--sm-12 col--md-12 col--lg-12"></div>` - inside a `.row`.

```html
  <div class="row">
    <div class="col col--xs-12 col--sm-12 col--md-12 col--lg-12">
      <p>Col 1</p>
    </div>
  </div>
  <div class="row">
    <div class="col col--xs-12 col--sm-12 col--md-6 col--lg-6">
      <p>Col 2</p>
    </div>
    <div class="col col--xs-12 col--sm-12 col--md-6 col--lg-6">
      <p>Col 3</p>
    </div>
  </div>
  <div class="row">
    <div class="col col--xs-12 col--sm-12 col--md-4 col--lg-4">
      <p>Col 4</p>
    </div>
    <div class="col col--xs-12 col--sm-12 col--md-4 col--lg-4">
      <p>Col 5</p>
    </div>
    <div class="col col--xs-12 col--sm-12 col--md-4 col--lg-4">
      <p>Col 6</p>
    </div>
  </div>
  <div class="row">
    <div class="col col--xs-12 col--sm-12 col--md-8 col--lg-8">
      <p>Col 7</p>
    </div>
    <div class="col col--xs-12 col--sm-12 col--md-4 col--lg-4">
      <p>Col 8</p>
    </div>
  </div>
```

### Offsetting columns
Increase the left margin of a column by the number of columns you want, along with the responsive class prefixes, if you need.

```html
  <div class="row">
    <div class="col col--xs-12 col--sm-12 col--md-4 col--lg-4">
      <p>Col 9 with offset 0</p>
    </div>
    <div class="col col--xs-12 col--sm-12 col--md-4 col--lg-4 col--xs-offset-4 col--sm-offset-0 col--md-offset-4 col--lg-offset-4">
      <p>Col 10 with offset 4</p>
    </div>
  </div>
  <div class="row">
    <div class="col col--xs-12 col--sm-12 col--md-3 col--lg-3 col--xs-offset-0 col--sm-offset-0 col--md-offset-3 col--lg-offset-3">
      <p>Col 11 with offset 3</p>
    </div>
    <div class="col col--xs-12 col--sm-12 col--md-3 col--lg-3 col--xs-offset-0 col--sm-offset-0 col--md-offset-6 col--lg-offset-6">
      <p>Col 12 with offset 6</p>
    </div>
  </div>
  <div class="row">
    <div class="col col--xs-12 col--sm-12 col--md-6 col--lg-6 col--xs-offset-0 col--sm-offset-0 col--md-offset-3 col--lg-offset-3">
      <p>Col 13 with offset 3</p>
    </div>
  </div>
  </div>
```

### Nesting columns
To nest your content, add a new `.row` inside a `.col`, and set of `.col-ld-*` columns within an existing `.col-ld-*` column. Nested rows should include a set of columns that add up to 12 or less.

```html
  <div class="row">
    <div class="col col--xs-12 col--sm-12 col--md-12 col--lg-12">
      <p>Col 14</p>
      <div class="row">
        <div class="col col--xs-12 col--sm-12 col--md-6 col--lg-6">
          <p>Nested col 14.1</p>
        </div>
        <div class="col col--xs-12 col--sm-12 col--md-6 col--lg-6">
          <p>Nested col 14.2</p>
        </div>
      </div>
    </div>
  </div>
```

### Gutterless columns
To remove all the gutters from your columns just add the class `.row--gutterless` to your `.row` element.

```html
  <div class="row row gutters">
    <div class="col col--xs-12 col--sm-12 col--md-6 col--lg-6">
      <p>Col 15</p>
    </div>
    <div class="col col--xs-12 col--sm-12 col--md-6 col--lg-6">
      <p>Col 16</p>
    </div>
  </div>
```

## Demo
Check out the demo and play around on [Code Pen](http://codepen.io/pedroreis/pen/ituho) and/or check the compiled CSS on [SassMeister](http://sassmeister.com/gist/c6368fc9a239e1798fcd).
