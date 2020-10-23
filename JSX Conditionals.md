## JSX Conditionals: The Ternary Operator

The ternary operator works the same way in React as it does in regular JavaScript. However, it shows up in React surprisingly often.

```javascript

const headline = (
  <h1>
    { age >= drinkingAge ? 'Buy Drink' : 'Do Teen Stuff' }
  </h1>
);

```
In the above example,
if `age` is greater than or equal to `drinkingAge`, then `headline` will equal `<h1>Buy Drink</h1>`. Otherwise, `headline` will equal `<h1>Do Teen Stuff</h1>`.
