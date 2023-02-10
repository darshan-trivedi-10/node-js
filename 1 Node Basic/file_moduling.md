# CommonJS Modules in JavaScript

• CommonJS is a specification for writing modular code in JavaScript. It is widely used in Node.js and provides a simple way to export and require modules in your code.

• A CommonJS module can be created by using the module.exports object. You can add properties and functions to this object, which will be exposed as the public interface of the module.

Here's an example of a CommonJS module:
```
// math.js

module.exports = {
  add: function(a, b) {
    return a + b;
  },
  subtract: function(a, b) {
    return a - b;
  }
};
```
To use this module in another file, you can use the `require` function. The following code demonstrates how to use the `math` module from the previous example:


``` 
// index.js

const math = require('./math');

console.log(math.add(1, 2)); // 3
console.log(math.subtract(4, 2)); // 2

```

### ECMAScript 6 Modules in JavaScript

ECMAScript 6 (ES6) introduced a new way to define and use modules in JavaScript. The syntax is similar to that of CommonJS, but there are some key differences.

An ES6 module can be created using the `export` keyword. You can use export to `export` a single value, multiple values, or a whole module.

Here's an example of an ES6 module:

```
// math.js

export function add(a, b) {
  return a + b;
}

export function subtract(a, b) {
  return a - b;
}
```

To use this module in another file, you can use the `import` keyword.

The following code demonstrates how to use the `math` module from the previous example:

```
// index.js

import { add, subtract } from './math';

console.log(add(1, 2)); // 3
console.log(subtract(4, 2)); // 2
```

Note that ES6 modules are not natively supported by all browsers and require a build step to be used in the browser. However, they are supported in Node.js starting from version 14.

In the `package.json` file for an `ES6 module`, you can specify the module format using the `type` field. The type field should be set to `"module"` if your package uses ECMAScript 6 modules.

Here's an example of a `package.json` file that uses ECMAScript 6 modules:

```
{
  "name": "my-package",
  "version": "1.0.0",
  "type": "module",
  "main": "index.js"
}
```

In conclusion, both CommonJS and ES6 modules provide a way to organize your code into reusable and modular pieces. The choice between the two depends on your specific use case and the environment in which you are working.
