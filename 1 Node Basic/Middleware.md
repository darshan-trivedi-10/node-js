## Middleware 
- Middleware in Express refers to a piece of code that sits between the server and the client and modifies the request or response in some way. 
- It can be used for tasks such as authentication, logging, and data validation. 
- Middleware functions are executed in the order they are defined, and can either modify the request and response objects, or end the request-response cycle altogether.
- Here is an example of a simple middleware function that logs the request method and URL:
```js
app.use(function(req, res, next) {
    console.log(req.method + ' ' + req.url);
    next();
});
```
- This middleware function uses the app.use() method to define the middleware, and the `next()` function to move on to the next middleware function in the chain.
- This function will be executed on every request made to the server, and will log the method and URL of the request to the console.
- Another example of middleware is an authentication middleware that checks whether the request contains a valid authentication token before allowing the request to continue:
```js
app.use(function(req, res, next) {
    if (!req.headers.authentication) {
        res.status(401).send('Unauthorized');
    } else {
        next();
    }
});
```
- This middleware check if the request has a valid authentication token and if not it sends the unauthorized status code and message.
