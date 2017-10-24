
# Hello World


create a directory and have a folder to install future packages
mkdir learnyoureact
cd learnyoureact 
npm init -y


install required modules:
```sh
npm install --save react react-dom express body-parser express-react-views@0.9.0 babel@5.8.23
```

Create program.js 
```sh
touch program.js
```


put following code into program.js:
```sh
var express = require('express');
var app = express();

app.set('port', (process.argv[2] || 3000));
app.set('view engine', 'jsx');
app.set('views', __dirname + '/views');
app.engine('jsx', require('express-react-views').createEngine({transformViews: false}));

require('babel/register')({
    ignore: false
});

app.use('/', function (req, res) {
    res.render('index', '');
});

app.listen(app.get('port'), function () {
});
```    

The code above creates a small Express server that renders our React
components. If someone navigates to /, views/index.jsx will be rendered. This program uses the express-react-views module.


create a views directory in the same directory as program.js.



After that, create index.jsx in the 'views' directory.
Please copy the code below into index.jsx:
```sh
    import React from 'react';
    
    export default class TodoBox extends React.Component{
      render() {
        return <div className="todoBox">
            Hello, world!
          </div>
      }
    }
```
This code uses the optional React.js JSX syntax to create our views, which we
shall use throughout the rest of this workshop.

Once all setup run 
```sh
node program.js
```
access localhost: 3000 to see the HTML output 

verify program worked:
```sh
learnyoureact verify program.js
```


