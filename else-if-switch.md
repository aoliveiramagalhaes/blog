## When should I use if/else if/else statements? When should I use switch statements?

Consider using `<switch>` statements for simple cases/conditions and every time you have more than 2 conditions on a single variable, take weekdays for example, 
if you have a different action for every weekday you should use a switch.

Consider using `<if/else if/else statements>` for complex if clauses or multiple variables and when your logic requires more complex conditions to check and/or when the conditions to check will evaluate to a boolean.

**Example 1:**

```javascript

const calculateWeight = (earthWeight, planet) => {
    switch (planet) {
        case "Mercury":
            return earthWeight * 0.378
        case "Venus":
            return earthWeight * 0.907
        case "Mars":
            return earthWeight * 0.377
        case "Jupiter":
            return earthWeight * 2.36
        case "Saturn":
            return earthWeight * 0.916
        default:
            return 'Invalid Planet Entry. Try: Mercury, Venus, Mars, Jupiter, or Saturn.'
    }
}

console.log(calculateWeight(100, 'Jupiter')) 
// Should print 236
console.log(calculateWeight(100, 'Mars'))
// Should print 37.7

```

**Note 1** 

We used *planet* inside the `<switch>`statement, because planet is the variable. The earthWeight will change based on the planet. 

We add the variable inside the switch or the `<randonNumber>` when we are guessing a number.

We can also read like this: if planet is Mercury, the earthWeight will be * 0.378, else if Venus will be * 0.907 and so on.

**Note 2** 

We do not use break, because we are using return. When we use return, the computer stops processing that statement, so there is no need for a break.

If you use console.log() or set a value, then you need to add a break after each statement.

**Example 2:**

```javascript

let athleteFinalPosition = 'first place';
  switch (athleteFinalPosition) {
    case 'first place':
    console.log('You get the gold medal!');
    break;
    case 'second place':
    console.log('You get the silver medal!');
    break;
    case 'third place':
    console.log('You get the bronze medal!');
    break;
    default:
      console.log('No medal awarded.');
      break;
}

```

**Example 3:**

```javascript

const randomNumber = Math.floor(Math.random() * 8);

let eightBall = "";

switch (randomNumber) {
  case 0:
  eightBall = 'It is certain';
  break;
  case 1:
  eightBall = 'It is decidedly so';
  break;
  case 2:
  eightBall = 'Reply hazy try again';
  break;
  case 3:
  eightBall = 'Cannot predict now';
  break;
  default: 
  eightBall = 'try again';
  break;
}

console.log(`The eight ball answered: ${eightBall}`); 

```

