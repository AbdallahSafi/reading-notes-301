# Node, Express, and APIs 

## What Is Node.js?

- Node.js is a JavaScript runtime built on Chrome’s V8 JavaScript engine.

- **The V8 engine** is the open-source JavaScript engine that runs in Google Chrome and other Chromium-based web browsers

- This means that Node.js is a program we can use to execute JavaScript on our computers. In other words, it’s a JavaScript runtime.



## Node.js Has Excellent Support for Modern JavaScript

- Node has excellent support for ECMAScript 2015 (ES6) and beyond. As you’re only targeting one runtime (a specific version of the V8 engine)

## Introducing npm, the JavaScript Package Manager

- Node comes bundled with a package manager called npm

## What Is Node.js Used For?

- Installing (via npm) and running (via Node) various build tools — designed to automate the process of developing a modern JavaScript application.

- Node.js Lets Us Run JavaScript on the Server

## The Node.js Execution Model

Node.js, however, is single-threaded. It’s also event-driven, which means that everything that happens in Node is in reaction to an event. 

For example, when a new request comes in (one kind of event) the server will start processing it. If it then encounters a blocking I/O operation, instead of waiting for this to complete, it will register a callback before continuing to process the next event. When the I/O operation has finished (another kind of event), the server will execute the callback and continue working on the original request. 

Under the hood, Node uses the libuv library to implement this asynchronous (that is, non-blocking) behavior.


![image](https://dab1nmslvvntp.cloudfront.net/wp-content/uploads/2012/10/1516152673node_event_loop.png)

## Are There Any Downsides?

The fact that Node runs in a single thread does impose some limitations. For example, blocking I/O calls should be avoided, CPU-intensive operations should be handed off to a worker thread, and errors should always be handled correctly for fear of crashing the entire process.

## “Hello, World!” — Server Version

```javascript
const http = require('http');

http.createServer((request, response) => {
  response.writeHead(200);
  response.end('Hello, World!');
}).listen(3000);

console.log('Server running on http://localhost:3000');
```


## What Kind of Apps Is Node.js Suited To?

- Node is particularly suited to building applications that require some form of real-time interaction or collaboration — for example, chat sites, or apps such as CodeShare

- It’s also a good fit for building APIs where you’re handling lots of requests that are I/O driven 

## What Are the Advantages of Node.js?

Aside from speed and scalability, an often-touted advantage of using JavaScript on a web server — as well as in the browser — is that your brain no longer needs to switch modes. You can do everything in the same language, which, as a developer, makes you more productive (and hopefully, happier). For example, you can easily share code between the server and the client.

