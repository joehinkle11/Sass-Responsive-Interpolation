# Sass Responsive Interpolation
Linear interpolation of any CSS attribute between two breakpoints in SCSS (Sass). No JavaScript is used!

## Demo
[![Demo Gif](https://github.com/joehinkle11/Sass-Responsive-Interpolation/raw/master/demo.gif)](https://www.joehinkle.io/responsiveinterpolationdemo)

[Try the demo here!](https://www.joehinkle.io/responsiveinterpolationdemo)

## Example

```scss
@import 'responsive-interpolation';

$left-breakpoint: 800px;
$right-breakpoint: 2000px;

$top-breakpoint: 800px;
$bottom-breakpoint: 2000px;

#my-responsive-box {
    // This will interpolate the box's width and height to go from 150px to 350px from the left breakpoint
    // to the right breakpoint.
    @include responsive-interpolate-x( ("width","height"), 150px, 350px, $left-breakpoint, $right-breakpoint );
}

#my-responsive-text {
    // This will interpolate the text's font size to go from 32px to 55px from the left breakpoint
    // to the right breakpoint.
    @include responsive-interpolate-x( "font-size", 32px, 55px, $left-breakpoint, $right-breakpoint );
}

#my-responsive-moving-box {
    // This will interpolate the box's x and y position by using the margin left and
    // margin top going from 250px to 0px from the top breakpoint to the bottom breakpoint.
    @include responsive-interpolate-y( ("margin-left","margin-top"), 250px, 0px, $top-breakpoint, $bottom-breakpoint );
}
```
