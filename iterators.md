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

* `fruits.forEach()` calls the forEach method on the fruits array.

* `.forEach()` takes an argument of callback function. Remember, a callback function is a function passed as an argument into another function.

* `.forEach()` loops through the array and executes the callback function for each element. During each execution, the current element is passed as an argument to the callback function.

* The return value for `.forEach()` will always be **undefined.**

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

* numbers is an array of numbers.

* bigNumbers will store the return value of calling `.map()` on numbers.

* `numbers.map` will iterate through each element in the numbers array and pass the element into the callback function.

* return number * 10 is the code we wish to execute upon each element in the array. This will save each value from the numbers array, multiplied by 10, to a new array.

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

## The .findIndex() Method

We sometimes want to find the location of an element in an array. That’s where the .findIndex() method comes in! Calling .findIndex() on an array will return the index of the first element that evaluates to true in the callback function.

```javascript

const jumbledNums = [123, 25, 78, 5, 9]; 

const lessThanTen = jumbledNums.findIndex(num => {
  return num < 10;
});

```

* jumbledNums is an array that contains elements that are numbers.

* const lessThanTen = declares a new variable that stores the returned index number from invoking `.findIndex()`.

* The callback function is an arrow function has a single parameter, num. Each element in the jumbledNums array will be passed to this function as an argument.

* num < 10; is the condition that elements are checked against. `.findIndex()` will return the index of the first element which evaluates to true for that condition.

Let’s take a look at what lessThanTen evaluates to:

```javascript

console.log(lessThanTen); // Output: 3 
If we check what element has index of 3:

console.log(jumbledNums[3]); // Output: 5
Great, the element in index 3 is the number 5. This makes sense since 5 is the first element that is less than 10.

```

If there isn’t a single element in the array that satisfies the condition in the callback, then `.findIndex()` will return -1.

```javascript

const greaterThan1000 = jumbledNums.findIndex(num => {
  return num > 1000;
});

console.log(greaterThan1000); // Output: -1

```

## The .reduce() Method

Another widely used iteration method is .reduce(). The .reduce() method returns a single value after iterating through the elements of an array, thereby reducing the array. Take a look at the example below:

```javascript

const numbers = [1, 2, 4, 10];

const summedNums = numbers.reduce((accumulator, currentValue) => {
  return accumulator + currentValue
})

console.log(summedNums) // Output: 17

```

Here are the values of accumulator and currentValue as we iterate through the numbers array:

Iteration	accumulator	currentValue	return value

![image](https://user-images.githubusercontent.com/66221314/89744218-d43e3a00-da78-11ea-987f-68e1376c8bc9.png)

Now let’s go over the use of `.reduce()` from the example above:

* numbers is an array that contains numbers.

* summedNums is a variable that stores the returned value of invoking .reduce() on numbers.

* `numbers.reduce()` calls the `.reduce()` method on the numbers array and takes in a callback function as argument.

* The callback function has two parameters, accumulator and currentValue. The value of accumulator starts off as the value of the first element in the array and the currentValue starts as the second element. To see the value of accumulator and currentValue change, review the chart above.

As `.reduce()` iterates through the array, the return value of the callback function becomes the accumulator value for the next iteration, currentValue takes on the value of the current element in the looping process.

The `.reduce()` method can also take an optional second parameter to set an initial value for accumulator (remember, the first argument is the callback function!). For instance:

```javascript

const numbers = [1, 2, 4, 10];

const summedNums = numbers.reduce((accumulator, currentValue) => {
  return accumulator + currentValue
}, 100)  // <- Second argument for .reduce()

console.log(summedNums); // Output: 117

```
Here’s an updated chart that accounts for the second argument of 100:

![image](https://user-images.githubusercontent.com/66221314/89744322-c1783500-da79-11ea-9bdf-0e72c7999e3e.png)

# Review

Awesome job on clearing the iterators lesson! You have learned a number of useful methods in this lesson as well as how to use the JavaScript documentation from the Mozilla Developer Network to discover and understand additional methods. Let’s review!

* `.forEach()` is used to execute the same code on every element in an array but does not change the array and returns undefined.

* `.map()` executes the same code on every element in an array and returns a new array with the updated elements.

* `.filter()` checks every element in an array to see if it meets certain criteria and returns a new array with the elements that return truthy for the criteria.

* `.filter()` checks every element in an array to see if it meets certain criteria and returns a new array with the elements that return truthy for the criteria.

* `.findIndex()` returns the index of the first element of an array which satisfies a condition in the callback function. It returns -1 if none of the elements in the array satisfies the condition.

* `.filter()` checks every element in an array to see if it meets certain criteria and returns a new array with the elements that return truthy for the criteria.

* `.reduce()` iterates through an array and takes the values of the elements and returns a single value.

All iterator methods takes a callback function that can be pre-defined, or a function expression, or an arrow function.

You can visit the Mozilla Developer Network to learn more about iterator methods (and all other parts of JavaScript!).

