## Functions

Remember, computers are stupid, they don't know what to do, you need to tell them step by step, otherwise, they won't figure it out.

You can tell what computers should do with statements, functions, conditions, and expressions. Don't worry about understanding the difference between them. You will get used to them like you use your own speaking language without remembering or even knowing all grammar rules that dictate the way you speak. 

Alright, let's go back to functions. I like to make analogies. You will see that going forward on my examples. 

Your daily schedule is a system composed of activities, I know, it is weird to express it like that, but in fact, it is, sometimes it is a bit dynamic, but for most people, it is a system that repeats every day.

* wake up
* turn off the alarm
* shower
* brush teeth 
* eat
* check phone
* go to work
* ... 

You do a lot of activities in your day. It tends to be a habit, a system you repeat consistently that system composed of activities, and some activities you can do more than once a day, for example, you can eat multiple times, for example, "I eat" and "I check my phone".

If you want to translate that to a computer system, you can turn you in a system that you can run every day, and it will invoke multiple activities in order.

```javascript
// me-app.js

const executeDay = () => {
  wakeUp()
  turnOffAlarm()
  shower()
  bruthTeeth()
  eat()
  checkPhone()
  goToWork()
  // ...
}

const wakeUp = () => {
  console.log('wake up')
}

const turnOffAlarm = () => {
  console.log('please stop ringing, I hate you')
}

const shower = () => {
  console.log('so relaxing! I am happy')
}

const bruthTeeth = () => {
  console.log('fresh and new')
}

const eat = () => {
  console.log('yummy')
}

// ... 
```



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

