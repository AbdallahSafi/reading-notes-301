# EJS template

EJS is among the most popular tempate view engines for node.js and expressjs with 4.2k stars at github and over 5.5m downloads per week at npm.

EJS simply stands for Embedded JavaScript templates, and we can use it both server-side or client-side. At this story, we’ll focus on the server-side.


### Basic Syntax(Tags):

- <% 'Scriptlet' tag, for control-flow, no output
- <%= Outputs the value into the template (HTML escaped)
- <%- Outputs the unescaped value into the template

```javascript
<% if (message) { %>
  <h2><%= message.name %></h2>
<% } %>
```

## Partials

``` javascript
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

EJS uses <%- include(‘’)-%> tag to include HTML from other files, in our app, we have the HTML templates at /views/template folder.


## Render Links

```javascript
<%- include('../template/head')-%>
<body class="text-center">
<div class="cover-container d-flex w-100 h-100 p-3 mx-auto flex-column">
<%- include('../template/nav')-%>
<main role="main" class="inner cover">
<h1 class="cover-heading">Example with Links</h1>
<ul class="list-group">
<% links.forEach(function(entry) {%>
<a href="<%= entry.url%>" class="list-group-item text-dark"><%=entry.name%></a>
<%});%>
</ul>
</main>
<%- include('../template/footer')-%>
</div>
</body>
<script>
//Set active nav link
window.onload = function() {
document.getElementById('links').classList.add('active');
};
</script>
</html>
```

This time at res.render function after the name of the file we want to render we pass a JSON object.

```javascript
res.render('pages/links',{
links:items
});
```

This JSON object will pass to the view pages/links.ejs. At this point, we use foreach function to iterate the links array and use “<%=” tag to output the properties url and name.

```javascript
<% links.forEach(function(entry) {%>
<a href="<%= entry.url%>" class="list-group-item text-dark"><%=entry.name%></a>
<%});%>
```

## Render List

```javascript
<%- include('../template/head')-%>
<body class="text-center">
<div class="cover-container d-flex w-100 h-100 p-3 mx-auto flex-column">
<%- include('../template/nav')-%>
<main role="main" class="inner cover">
<h1 class="cover-heading">List Example</h1>
<ul class="list-group">
<%list.forEach(function(entry) {%>
<li class="list-group-item text-dark"><%=entry%></li>
<%});%>
</ul>
</main>
<%- include('../template/footer')-%>
</div>
</body>
<script>
window.onload = function() {
document.getElementById('list').classList.add('active');
};
</script>
</html>
```

## Render Table

```javascript
<%- include('../template/head')-%>
<body class="text-center">
<div class="cover-container d-flex w-100 h-100 p-3 mx-auto flex-column">
<%- include('../template/nav')-%>
<h1 class="cover-heading">Table Example</h1>
<div class="container bg-light text-dark">
<table class="table table-striped">
<thead>
<tr>
<th>Framework</th>
<th>URL</th>
</tr>
</thead>
<tbody>
<%table.forEach(function(entry) {%>
<tr>
<td><%=entry.name%></td>
<td><%=entry.url%></td>
</tr>
<%});%>
</tbody>
</table>
</div>
<%- include('../template/footer')-%>
</div>
</body>
<script>
window.onload = function() {
document.getElementById('table').classList.add('active');
};
</script>
</html>
```

