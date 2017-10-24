# Function Arguments

 A function can be declared to receive any number of arguments. 
 Arguments can be from any type. An argument could be a string, a number, an array,  
 an object and even another function.  
  
 create a file function-arguments.js
 ```sh
 touch function-arguments.js
 ```
 
 define a function named math which takes three arguments
 
 ```sh
 function math(a, b, c) {
 }
 ```
 
  Within the math function, return the value obtained from multiplying the  
  second and third arguments and adding that result to the first argument.  
  
  ```sh
  function math(a,b,c) {
    return (b * c) + a;
  }
  
  ```
 
 inside the parentheses of console.log(), call the math() function:
- the number 53 as first argument
- the number 61 as second
- the number 67 as third argument

```sh
console.log(math(53,61,67));
```
 
