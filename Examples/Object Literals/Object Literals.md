# Object Literals

Added a method in object become simple enough in ES6.

<a href="http://goo.gl/ObpLSN" target="_blank">Demo</a>

````
var foo = (name) => { return name };

var options = {name : 'Bar'};

var obj = {
    
    // Shorthand for options: options
    options,
    
    // Shorthand for Methods
    printName() {
     console.log(foo(options.name));
    }
};

obj.printName(); //print Bar
````

## Reference

- <a href="http://babeljs.io/docs/learn-es2015/#enhanced-object-literals" target="_blank">Enhanced object literals</a>