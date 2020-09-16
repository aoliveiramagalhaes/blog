## DOM EVENTS WITH JAVASCRIPT

To change the content of an element in JavaScript use the `.innerHTML` property:

```javascript
element.innerHTML = 'This is new text content.';
```

To access elements by their IDs use
```javascript
document.getElementByID('targetElement')
```
To change the content of an element in JavaScript use the `.innerHTML` property on the element.
You can combine both if necessary:

```javascript

document.getElementByID('targetElement').innerHTML = 'This is new text content.';

```

**Example**

Write anonymous event handler property and function for the second progress button
```javascript

nextTwo.onclick = function () {
  nextThree.hidden = false;
  nextTwo.hidden = true;
  document.getElementById('word-five').innerHTML = 'DEAR';
  document.getElementById('word-six').innerHTML = 'FRI-';
};
```
There are more three different ways of adding event listeners or event handler:

```javascript
const eventAssignment = function (note) {
 // example1
  note.onmousedown = keyPlay;
  note.onmouseup = keyReturn;
 };
  
  // example2
 const eventAssignment = function (note) {
  note.addEventListener('mousedown', keyPlay)
  note.addEventListener('mouseup', keyReturn)
};

  // example3
const eventAssignment = function (note) {
  note.onmousedown = function () {
    keyPlay(event)
  }
    note.onmouseup = function () {
    keyReturn(event)
    }
};
```
