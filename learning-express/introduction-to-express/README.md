Express.js, or simply Express, is a web application framework for Node.js, released as free and open-source software under the MIT License. It is designed for building web applications and APIs. It has been called the de facto standard server framework for Node.js.

[Express.js](https://en.wikipedia.org/wiki/Express.js)

# Installing Express
Installation of Express can be done through `npm`.

```Bash
npm install express --save
```

## Installing Nodemon
This is not a prerequisite, but it will make development process much easier. Nodemon is a utility that will monitor for any changes in your source and automatically restart your server. Perfect for development.

[nodemon](https://nodemon.io/)

Installation of Nodemon can be done through `npm`.

```Bash
npm install -g nodemon
```

# Hello Express

```JavaScript
// index.js
var express = require('express');
var app = express();

app.get('/', function (req, res) {
  res.send('Hello world!');
});

app.listen(3000);
```

run the above with `nodemon` like below.

```Bash
nodemon index.js
```

This will start the server. To test this app, open your browser and go to [http://localhost:3000](http://localhost:3000/) and a `Hello world!` message will be displayed.

## `app.get(route, callback)`
This function tells what to do when a get request at the given route is called. The `callback` function has two parameters:

- `req` (request), represents the HTTP request and has properties for the request query string, parameters, body, HTTP headers, etc.
- `res` (response), represents the HTTP response that the Express app sends when it receives an HTTP request.

## `res.send()`

This function takes an object as input and it sends this to the requesting client.

## `app.listen(port, [host], [backlog], [callback]])`

This function binds and listens for connections on the specified `host` and `port`. `port` is the only required parameter here.