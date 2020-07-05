This is an example of handling a click on a button and changing a `<p>` content.

```html
<button onClick="handleButtonClick()">Click Here</button>
<p id="result"></p>

<script>
const handleButtonClick = () => {
  document.getElementById("result").innerHTML = "hello"
}
</script>
```
