# Learning how to use iterator methods to simplify the process of looping over arrays.

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

## The .filter() Method

Another useful iterator method is `.filter()`. Like `.map()`, `.filter()` returns a new array. However, `.filter()` returns an array of elements after filtering out certain elements from the original array. The callback function for the .filter() method should return true or false depending on the element that is passed to it. The elements that cause the callback function to return true are added to the new array. Take a look at the following example:

```javascript

const words = ['chair', 'music', 'pillow', 'brick', 'pen', 'door']; 

const shortWords = words.filter(word => {
  return word.length < 6;
});

```

words is an array that contains string elements.

const shortWords = declares a new variable that will store the returned array from invoking `.filter()`.

The callback function is an arrow function has a single parameter, word. Each element in the words array will be passed to this function as an argument.
word.length < 6; is the condition in the callback function. Any word from the words array that has fewer than 6 characters will be added to the shortWords array.

Let’s also check the values of words and shortWords:

```javascript

console.log(words); // Output: ['chair', 'music', 'pillow', 'brick', 'pen', 'door']; 
console.log(shortWords); // Output: ['chair', 'music', 'brick', 'pen', 'door']

```
