## Create server in node js 
##### Creating a server in Node.js using the built-in `http` module is a straightforward process. 
1. Include the Built-in Node.js module, HTTP, using require function as shown below.
```js
const http = require('http');
```
2. Create Server using the method `createServer()` to listen at `port` numbered at `3000`
```js
var http = require('http');
// create a server
http.createServer(function (req, res) {
    // code to feed or request and prepare response
}).listen(3000);
```
3. Prepare response
```js
http.createServer(function (req, res) {
    if (req.url == '/home') {
        res.end("Welcome to Home");
    } else if (req.url == '/faq') {
        res.end("List of FAQs");
    } else {
        res.end("Hello World!!");
    }
}).listen(3000)
```
4. Run the Web Server
`node httpWebServer.js`

5. Test the Web Server
   1. Open a browser and hit the url, [[http://localhost:3000/](http://localhost:3000/faq),[http://localhost:3000/home](http://localhost:3000/faq),[http://localhost:3000/faq](http://localhost:3000/faq)], to trigger a request to our Web Server.

## httpWebServer.js
```js
const http = require('http');
const PORT = 3000;

const server = http.createServer(function exec(req, res) {
    console.log(req.method);
    if (req.url == '/home') {
        res.end("Welcome to Home");
    } else if (req.url == '/faq') {
        res.end("List of FAQs");
    } else {
        res.end("Hello World!!");
    }
});

server.listen(PORT, function process() {
    console.log('Server Started on port ', PORT);
})
```
