# Object Properties

You can access and manipulate object properties –– the keys and values  
  that an object contains –– using a method very similar to arrays.  
  
  create a file object-properties.js
  
  ```sh
  touch object-properties.js
  ```
  
  define a variable food:
  
  ```sh
  var food = {
    types: 'only pizza'
  };
  ```
  
  console.log() to print types of food
  
  console.log(food['types']);
  
  // or alternatively dot notation:
  
  console.log(food.types);
