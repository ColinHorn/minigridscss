# MiniGrid.scss

A very minimal grid mixin, allowing you to set your breakpoints, container and gutters in seconds.

< 2kb in size.

## Usage

### HTML
This is the structure as to how the layout the grid

To remove gab between columns, set padding to false in scss.
```html
<!--Spacing between columns-->
<section>
    <div class="container">
        <div class="row">
            <div class="column">
                Left Column
            </div>
            <div class="column">
                Right Column
            </div>
        </div>
    </div>
</section>

<!--No spacing between columns-->
<section>
    <div class="container">
        <div class="row">
            <div class="column no-padding">
                Left Column
            </div>
            <div class="column no-padding">
                Right Column
            </div>
        </div>
    </div>
</section>
```

### scss
Items at mobile will be 100% unless defines otherwise.

Variables relate to mixin as such:
"@include grid(xs, sm, md, lg, xl, padding);"
```scss
@import "minigrid.scss";

//-- Deafults within minigrid.scss
//-- Overwrite with your own variables

//Container Widths
$mobileWidth:95vw;
$maxWidth: 1430px;

//Screen Breakpoint Sizes
$screen-xs: 500px;
$screen-sm: 768px;
$screen-md: 992px;
$screen-lg: 1230px;
$screen-xl: 1460px;

$gutter-width:15px;
$gutter-width-xl:25px;


.column{
    @include grid(12, 6, 6, 6, 6, true);

    &.no-padding{
        @include grid(12, 6, 6, 6, 6, false);
    }
}

```

## Contributing
Pull requests are welcome. For major changes, please open an issue first to discuss what you would like to change.

## License
[MIT](https://choosealicense.com/licenses/mit/)