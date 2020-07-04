### Where's my cat?

Let's display three boxes, and hide a cat in one of them. Then let's find out in which box the cat is hidden.

1. Create a `where-is-my-cat.html`. See [sample.html](./sample.html)
2. Create an empty `where-is-my-cat.js` 
3. Add `<script src='./where-is-my-cat.js'></script>` in your new HTML file
4. Find a cool box image
5. Display your images
6. Create a function to pick a random number
7. Create a click handler
8. Link the boxes with your click handler
9. Make it work :pray:
10. Profit :tada:
11. Bonus :star:


#### Display your images

```html
<img src="./images/box1.png">
<img src="./images/box2.png">
<img src="./images/box3.png">
```

#### Create a function to pick a random number

```javascript
const randomBox = (max) => {
  // this function returns a random number from 1 to max
  // for example, if max is 3, it can return 1, 2 or 3
  
  return Math.ceil(Math.random() * max)
}
```

#### Create a click handler


```javascript
const handleBoxClick = (boxNumber) => {
   // placeholder alert to check if the click handling is working
   alert(boxNumber)
}
```

#### Link the boxes with your click handler


```html
<a href="javascript:handleBoxClick(1)"><img src="./images/box.png"></a>
<a href="javascript:handleBoxClick(2)"><img src="./images/box.png"></a>
<a href="javascript:handleBoxClick(3)"><img src="./images/box.png"></a>
```

Open the HTML in the browser and test if clicking on the images, an alert is displayed with the box index.

#### Make it work

```javascript
const handleBoxClick = (boxNumber) => {
  // calls randomBox asking for a number from 1 to 3 and save into `boxWithCat`
  const boxWithCat = randomBox(3)
  
  if(boxNumber === boxWithCat) {
    alert('Cat found. congrats! Can you see through boxes?!')
  } else {
    alert(`NOPE. Try it again. The cat was in the box ${boxWithCat}`)
  } 
}
```

#### Bonus

You can change your function to instead of using `alert` to print out the answer in the screen.

```html
<a href="javascript:handleBoxClick(1)"><img src="./images/box1.png"></a>
<a href="javascript:handleBoxClick(2)"><img src="./images/box2.png"></a>
<a href="javascript:handleBoxClick(3)"><img src="./images/box3.png"></a>

<p id="result"></p>
```

```javascript
const handleBoxClick = (boxNumber) => {
  // calls randomBox asking for a number from 1 to 3 and save into `boxWithCat`
  const boxWithCat = randomBox(3)
  let result
  
  if(boxNumber === boxWithCat) {
    result = 'Cat found. congrats! Can you see through boxes?!'
  } else {
    result = `NOPE. Try it again. The cat was in the box ${boxWithCat}`
  } 
  
  document.getElementById('result').innerHTML = result
}
```


