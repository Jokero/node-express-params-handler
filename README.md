express-params-handler
============

Express.js v4+ params handler

This lib is replacement of [express-params](https://www.npmjs.com/package/express-params) which is made for Express 2.5. Express v4+ deprecated number of features which are in use of that original library. This lib offers similar functionality but doesn't use deprecated methods of new Express.


## Installation

    npm i express-params-handler


## Usage

```javascript
var expressParams = require('express-params-handler')

var app = express()
expressParams(app)('id', Number)
expressParams(app)('date', /^\d{4}-\d{2}-\d(2)$/)

app.get('/:id', function(req, res, next) {
  // req.params.id will be a number
})

app.get('/:date', function(req, res, next) { 
  // req.params.date will be a string with YYYY-MM-DD format
})

```


## Licence 

MIT
