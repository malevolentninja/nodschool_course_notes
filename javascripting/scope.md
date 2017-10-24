# Scope

 Scope is the set of variables, objects, and functions you have access to.  
   
  JavaScript has two scopes: 
  - global: A variable that is declared outside a function definition is a global variable, and its value is  
  accessible and modifiable throughout your program 
  - local: A variable that is declared inside a function definition is local. It is created and  
  destroyed every time the function is executed, and it cannot be accessed  
  by any code outside the function.  
   
  Functions defined inside other functions, known as nested functions, have  
  access to their parent function's scope.  
  
### IIFE = Immediately Invoked Function Expression
Thiis a common pattern for creating local scopes.  
   
  Example:  
 ```sh  
         (function(){ // the function expression is surrounded by parenthesis  
             // variables defined here  
             // can't be accessed outside  
         })(); // the function is immediately invoked  
 ```
 
 
 create a file named scope.js
 ```sh
 touch scope.js
 ```
 Put the following code: 
 ```sh
 var a = 1, b = 2, c = 3;  
       
     (function firstFunction(){  
         var b = 5, c = 6;  
       
         (function secondFunction(){  
             var b = 8;  
       
             (function thirdFunction(){  
                 var a = 7, c = 9;  
       
                 (function fourthFunction(){  
                     var a = 1, c = 8;  
       
                 })();  
             })();  
         })();  
     })();  
 
 ```
 
 place the following code inside one of the functions in scope.js 
 - so the output is a: 1, b: 8, c: 6  
  ```sh
     console.log("a: "+a+", b: "+b+", c: "+c);  
```

put it in the secondFunction. At that point c had already been changed to = 6 and b was being changed to = 8. 

```sh
var a = 1, b = 2, c = 3;

  (function firstFunction(){
     var b = 5, c = 6;

     (function secondFunction(){
        var b = 8;
        console.log("a: "+a+", b: "+b+", c: "+c);
        (function thirdFunction(){
            var a = 7, c = 9;

            (function fourthFunction(){
                var a = 1, c = 8;

            })();
        })();
     })();

  })();
```
