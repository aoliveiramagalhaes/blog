### Learning how to use iterator methods to simplify the process of looping over arrays.

The first iteration method that we’re going to learn is `.forEach()`. Aptly named, `.forEach()` will execute the same code for each element of an array.

```javascript

const fruits = ['mango', 'papaya', 'pineapple', 'apple'];

// Iterate over fruits below

fruits.forEach(fruitsItem => console.log(`I want to eat a ${fruitsItem}`));

//I want to eat a mango
//I want to eat a papaya
//I want to eat a pineapple
//I want to eat a apple

```

**Let’s explore the syntax of invoking** `.forEach()`

`fruits.forEach()` calls the forEach method on the fruits array.

`.forEach()` takes an argument of callback function. Remember, a callback function is a function passed as an argument into another function.

`.forEach()` loops through the array and executes the callback function for each element. During each execution, the current element is passed as an argument to the callback function.

The return value for `.forEach()` will always be **undefined.**
