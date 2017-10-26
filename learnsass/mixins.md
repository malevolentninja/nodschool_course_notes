# Mixins

Write a mixin border that accepts a variable $thickness 
- sets the border-width style to the value of $thickness
- Include the mixin in a rule for the img element
- set its border thickness to 10px

```sh
@mixin border ($thickness){
   border-width: $thickness
}
   img 
     @include border(10px);

}

```
