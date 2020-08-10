# EJS Partials

In this section we’ll learn how to use <%- include(‘’)-%> tag.
Project structure:

```javascript
startEJS
|--public
|--views
  |--pages
     |--home.ejs
  |--template
     |--head.ejs
     |--nav.ejs
     |--footer.ejs 
|--index.js
|--package.json
```

- Head into the project directory:
Lets see our index.js file:

```javascript
const express = require('express')
var path = require('path');
const app = express();
const port = 3000;
// view engine setup
app.set('views', path.join(__dirname, 'views'));
app.set('view engine', 'ejs');
//setup public folder
app.use(express.static('./public'));
app.get('/',function (req, res) {
res.render('pages/home')
});
app.listen(port, () => console.log(`MasterEJS app Started on port ${port}!`));
```

- First we set up the view engine and the views directory

```javascript
// view engine setup
app.set('views', path.join(__dirname, 'views'));
app.set('view engine', 'ejs');
```

- We set up our public folder for static files

```javascript
//setup public folder
app.use(express.static('./public'));
```

- Last we add the ‘/’ route to render the views/pages/home.ejs page
```javascript
app.get('/',function (req, res) {
res.render('pages/home')
});
```
- home.ejs

```javascript
<%- include('../template/head')-%>
<body class="text-center">
<div class="cover-container d-flex w-100 h-100 p-3 mx-auto flex-column">
<%- include('../template/nav')-%>
<main role="main" class="inner cover">
<h1 class="cover-heading">MasterEJS</h1>
<p class="lead">This is a sample app to Master EJS view template engine with Expressjs and Node.js framework
</p>
<p class="lead">
<a href="https://medium.com/@pkoulianos/master-ejs-template-engine-with-node-js-and-expressjs" class="btn btn-lg btn-secondary">Read More At Medium</a>
</p>
</main>
<%- include('../template/footer')-%>
</div>
</body>
</html>
```

- EJS uses <%- include(‘’)-%> tag to include HTML from other files, in our app, we have the HTML templates at /views/template folder.



