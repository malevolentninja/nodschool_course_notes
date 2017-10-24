# for loop

create a file  for-loop.js
```sh
touch for-loop.js
```

define a variable total make it equal to 0
```sh
var total = 0;
```
define a second variable  limit and make it equal to 10
```sh
var limit = 10;
```

 Create a for loop with a variable i starting at 0 and increasing by 1 each  
  time through the loop:
  - The loop should run as long as i is less than  
  limit
  - On each iteration of the loop, add the number i to the total variable
  - To do this, you can use this statement: total += i
  
```sh
for (var i = 0; i < limit; i++){
   //log the numbers through to 9
   total += i;
}
```

console.log() the total:

```sh
console.log(total);
```
