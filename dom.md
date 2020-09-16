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
