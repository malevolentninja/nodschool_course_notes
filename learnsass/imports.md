# Imports

Sass will take the file that you want to import and combine it with the file you're importing 
into so you can serve a single CSS file to the web browser.
Using the underscore leads to creating a partial

Write a partial:
- defines a variable $color and sets its value to '#ff0000',
- a stylesheet that imports the partial,
-  uses the variable to set the color style of the body element.

```sh
// _base.scss
$color: #ff0000;

// solution.scss
@import '_base.scss';

body {
  color: $color;
}
```
