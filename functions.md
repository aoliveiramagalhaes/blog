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

You do a lot of activities in your day. It tends to be a habit, a system you repeat consistently, and it is composed of activities, and some activities you can do more than once a day, for example, you will probably eat multiple a day.

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

Above, I created a function per activity. You may be wondering, why multiple functions and not just one:

```javascript
const executeDay = () => {
  console.log('wake up')
  console.log('please stop ringing, I hate you')
  console.log('so relaxing! I am happy')
  console.log('fresh and new')
  console.log('yummy')
  // ...
}
```

There a few arguments for breaking an activity (function) down into multiple activites. A few of them would be, sometimes you can make optional to take a shower, some days in you are in rush and you don't eat your breakfast, and also, what we talk you probably eat multiple times a day, so you do the same activity multiple times.


```javascript
const executeDay = () => {
  // ..
  eat()
  // ...
}

const takeABreak = () => {
  // ...
  eat()
  // ...
}
```

Well, the activity is the same, but I don't eat the same food for every meal. RIGHT!!! For that, you have parameters (often called arguments).  You can customize your activity with some additional input, for example, every time you go to the gym, you go to the gym. Still, it does not mean you do the same workout so that you can customize your activity behavior with parameters.

```javascript
const executeDay = () => {
  // ..
  eat('eggs and bacon')
  // ...
}

const takeABreak = () => {
  // ...
  eat('cookie')
  // ...
}
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
### Arrow function vs. Traditional function declaration

```javascript
// traditional function declaration
function functionName() {
// this is the function body
}

//arrow function declaration
const functionName = () => {
  // this is the function body
}

```
