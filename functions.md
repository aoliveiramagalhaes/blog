## Functions

### How to declare an arrow function

The example below, create a function named `sum` and it takes two parameters `a` and `b` and it returns the sum of them.

```javascript
const functionName = (paramOne, paramTwo) => {
  // this is the function body
}


const sum = (a, b) => {
  return a + b
}
```

### How to invoke/call a function

For invoking a function we call the function using its name, in this case `sum` then we pass the parameters needed.

```javascript
sum(1, 2)
```

Referencing a function without using `()`, for example `sum` does not call the function.

If a function has no arguments, we need to call it passing empty parenthesis.


```javascript
// function declaration
const sayHello = () => {
  console.log('hello')
}

// function invocation
sayHello()
```

