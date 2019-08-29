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
.gridClass{ .imx-grid($number of grid elements$, gridElementClass, $maxWidth the grid is allowed to grow$, $width of the wrapper$, $width of the grid inside the wrapper$, $horizontal margin of each gridElement$);}
```

An example integration could look like this:
```less
.myGrid{ .imx-grid(12, myGrid__element, 100%, 1680px, 1440px, 10px);}
```


## Authors

* **Axel Güldner@infomax**