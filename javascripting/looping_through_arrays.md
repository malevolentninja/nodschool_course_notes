# Looping through arrays

create a file looping-through-arrays.js

```sh
touch looping-through-arrays.js
```

define a variable named pets which references this array: ['cat', 'dog', 'rat']:

```sh
var pets =  ['cat', 'dog', 'rat'];
```

create a for loop that changes each string in the array so they are plural: 

```sh
for (var i = 0; i<pets.length; i++){
    pets[i] = pets[i] + 's';
}
```
after the for loop console.log() the pets array:

```sh
console.log(pets);
```
