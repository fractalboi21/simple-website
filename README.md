# simple-website





var express = require("express");
var app = express();

app.listen(3000, () => {
 console.log("Server running on port 3000");
});

app.get('/', (req, res) => {
  res.json('Hello World!')
})

app.get("/url", (req, res, next) => {
 res.json(["Tony","Lisa","Michael","Ginger","Food"]);
});


app.get('/about', function (req, res) {
    res.render('index', { title: 'Hey', message: 'Hello there!' })

})

app.get('/ab?cd', function (req, res) {
  res.send('ab?cd')
})

app.get('/users/:userId/books/:bookId', function (req, res) {
  res.send(req.params)
})

app.get('/users/:userId/books/:bookId', function (req, res) {
  res.send(req.params)
})

app.get('/sum/a/:avar/b/:bvar', function (req, res) {
  sum = parseInt(req.params.avar)+parseInt(req.params.bvar);
  res.send({sum})
})

app.get('/moment', function (req, res) {
 console.log(require("moment"));
   res.send({"df":"nothing to show!"})

})

`bash tree -fi | grep  html` 
