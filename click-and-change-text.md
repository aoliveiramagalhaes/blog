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

In the example above, when you click on the button, the text that is written in the `<P>` will change.
  
To make this happen, the `<p>` needs an `id`.

You need to add this `id` into the function ("result"), so that the function will know which `<p>` needs to change. You also need to write the message you want to display ("hello")
