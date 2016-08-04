app.js

```
var express = require('express');
var app = express();

//Import our DIY template engine
var templateEngine = require('./templateEngine.js');

//define app engine
app.engine('joe', templateEngine);

//specify views directory
app.set('views', './views');

//register template engine
app.set('view engine', 'joe');

app.get('/', function(req, res, next) {
  res.render(
    //filepath
    'index',
    //options - this what we will replace in our temaplte
    {
      title : 'Templating Exercise',
      message : ' Hello World',
      name : 'Joe'
    }
    //,callbackFunc
  )
})

//Callback function example - you don't need to use this in the wild, unless you need to override default rendering functionality
// function callbackFunc(err, data) {
//   console.log(data, 'data &&&&&&')
// }

app.listen(6969, function() {
  console.log('Server started on 6969')
});

```

index.joe

```
<title> $$title$$ </title>

<h1> $$message$$ </h1>

<p>My name is $$name$$, and this is my template engine.</p>

```

templateEngine.js

```
'strict mode'

//Template Engine module

// this engine requires the fs module
var fs = require('fs');

//Simple templating engine
function templatingEngine2(filePath, options, callback) {
  fs.readFile(filePath, function (err, content) {
    if (err) return callback(new Error(err));

    var rendered = content.toString()
    .replace('$$title$$', '<title>' + options.title + '</title>')
    .replace('$$message$$', '<h1>' + options.message + '</h1>')
    .replace('$$name$$', '' + options.name + '');
    return callback(null, rendered);
  })
}

```