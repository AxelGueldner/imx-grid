# imx-grid

Create horizontal Grids based on less, display inline-block and % values.

## Installing

Currently there is only one way to install imx-grid, using NPM:
```
$ npm install imx-grid
```

## How to use

You will need to import the imx-grid.less into your project
```css
@import 'imx-grid.less'
```

Then you can use the mixin that is now available, to create as many grids as you like, following this scheme:
```less
.gridClass{ .imx-grid($number of grid elements$, $gridElementClass$, $maxWidth the grid is allowed to grow$, $width of the wrapper$, $width of the grid inside the wrapper$, $horizontal margin of each gridElement$);}
```

An example integration could look like this:
```less
.myGrid{ .imx-grid(12, myGrid__element, 100%, 1680px, 1440px, 10px);}
```

## Directly access grid sizes
It is also possible to calculate gridsizes via mixin for direct usage without the need of css grid classes. This mixin will return a result value that you can access using less property accessor.
You can use two different mixins, one for grid item widths, one for grid offset widths. Both take the same parameters
```less
.myItem{ .singleGridWidth($width in grid elements$, $total number of grid elements$, $width of the grid inside the wrapper$, $horizontal margin of each gridElement$); }
.myItem{ .singleGridOffset($width in grid elements$, $total number of grid elements$, $width of the grid inside the wrapper$, $horizontal margin of each gridElement$); }
```

This example calculates the width of three grid items to use it as a max-width.
```less
.myItem{ max-width: .singleGridWidth(3, 12, 1440px, 10px)[@result]; }
```

This example calculates the offset for two grid items to use it as a padding-left.
```less
.myItem{ padding-left: .singleGridOffset(2, 12, 1440px, 10px)[@result]; }
```


## Authors

* **Axel Güldner@infomax**