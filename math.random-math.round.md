## what is Math.random()?

The random() method returns a random number that isn’t a whole number from 0 (inclusive) up to but not including 1 (exclusive).

To get it to be a whole number, i.e. an integer, apply `<Math.floor>`, which rounds down to the nearest whole number or `<Math.ceil>`, which rounds up to the nearest 
whole number.
  
**Example 1:**

Return a random number between 1 and 10:

```javascript

Math.floor((Math.random() * 10) + 1);

```

Since we actually wanted numbers from 1 to 10, inclusive, we added 1.

**Example 2:**

Return a random number between 0 and 10:

```javascript

console.log(Math.floor(Math.random() * 11))

```

Please note that `<Math.floor>` rounds down to the nearest whole number. 

If the random number is 9.9, `<Math.floor>` will round it to 9, so you will never get 10.

If you want the number 10, you need to write 11 in your code. It's always += 1.

**Note**

*Math.random() does not provide cryptographically secure random numbers. Do not use them for anything related to security.* 
*Use the Web Crypto API instead, and more precisely the window.crypto.getRandomValues() method.*

## what is Math.round()?

The Math.round() function returns the value of a number rounded to the nearest integer.

**Note**

2.49 will be rounded down (2), and 2.5 will be rounded up (3).

**Example 3:**

A person’s number of imaginary friends are always 33% of their total friends.

Write a function, numImaginaryFriends(), that takes in the total number of friends a person has and returns the number of imaginary friends they have.

Since friends can only come in whole numbers, be sure to round your result before returning it.

```javascript

const numImaginaryFriends = (totalFriends) => {
return Math.round(totalFriends * .33);
}

console.log(numImaginaryFriends(18)) // Should print 6

```

