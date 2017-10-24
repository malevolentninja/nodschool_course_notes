# Array Filtering 

one common way of filtering is using the .filter() method


create a file array-filtering.js
```sh
touch array-filtering.js
```

define a variable numbers referencing the following array: [1, 2, 3, 4, 5, 6, 7, 8, 9, 10]:

```sh
var numbers = [1, 2, 3, 4, 5, 6, 7, 8, 9, 10];

```

Variable named filtered referncing the result of numbers.filter()

var filtered = numbers.filter();


 The function that you pass to the .filter() method will look something  
  like this:  
```sh
  function evenNumbers (number) {
    return number % 2 === 0;
  }
```

my code: 
var filtered = numbers.filter(function (number) {
    return (number % 2) === 0;
  });



console.log() to print the filtered array: 

console.log(filtered);
