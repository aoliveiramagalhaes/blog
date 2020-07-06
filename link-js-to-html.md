## How to link a javascript file into a HTML file

1. You need to create a `filename.js`
2. Go to your index.html and add the following command at the bottom of your HTML body.

**Note**

When you place your JavaScript links at the bottom of your HTML body, it gives the HTML time to load before any of the JavaScript loads, which can prevent errors, and speed up website response time. 

 ```html
 <script src="./filename.js"></script>
 ```
