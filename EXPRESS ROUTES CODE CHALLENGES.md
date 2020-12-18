1. Require the 'express' package and save it to a variable named express. Then, create an Express instance and save it to a variable called app.
```javascript
const express = require('express');
const app = express();

```

2. Start your server listening on the port defined by the PORT variable.
```javascript
const express = require('express');

const app = express();

const PORT = process.env.PORT || 4001;

// Add your code below:
app.listen(PORT, () => {
  console.log(`App is listening on Port ${PORT}`)
})

```

3. Write a GET /sausages route that sends back the whole sausageTypes array.
```javascript

const sausageTypes = ['bratwurst', 'andouille', 'chorizo', 'boudin', 'kielbasa'];

```

4. Fix the route so that it sends back the array of metal building materials.
```javascript

const express = require('express');
const app = express();

const PORT = process.env.PORT || 4001;

const buildingMaterials = {
  wood: ['plywood', '2x4s', 'cedar shingles'],
  metal: ['steel girders', 'wall studs', 'rebar'],
};

app.listen(PORT, () => {
  console.log(`Server is listening on port ${PORT}`);
});

app.get('/metals', (req, res, next) => {
  const arrayToSend = buildingMaterials.metal;

});

```
  
