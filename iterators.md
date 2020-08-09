### Learning how to use iterator methods to simplify the process of looping over arrays.

## The .forEach() Method

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

## The .map() Method

The second iterator we’re going to cover is `.map()`. When `.map()` is called on an array, it takes an argument of a callback function and returns a new array! Take a look at an example of calling `.map()`:

```javascript

const numbers = [1, 2, 3, 4, 5]; 

const bigNumbers = numbers.map(number => {
  return number * 10;
});

```
`.map()` works in a similar manner to `.forEach()`— the major difference is that `.map()` returns a new array.

In the example above:

numbers is an array of numbers.

bigNumbers will store the return value of calling `.map()` on numbers.

`numbers.map` will iterate through each element in the numbers array and pass the element into the callback function.

return number * 10 is the code we wish to execute upon each element in the array. This will save each value from the numbers array, multiplied by 10, to a new array.

```javascript

console.log(numbers); // Output: [1, 2, 3, 4, 5]
console.log(bigNumbers); // Output: [10, 20, 30, 40, 50]

```

