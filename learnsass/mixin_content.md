# Mixin Content


Content blocks to a Mixin. 

Modify the border-thickness mixin from the previous exercise:
- to also accept a @content, 
and invoke it by: 
- passing in a rule that sets the border-style of the img element to solid

```sh
@mixin border($thickness) {
  border-width: $thickness;
  @content;
}

img {
   @include border(10px) {
     border-style: solid;
     }
  }

```
