## Modules

A module is just a javascript file which can be later imported by other javascript files.

## Export

Syntax `export` 

There are different ways to export a file.


```javascript
//Export a function
export function print(msg) {
	console.log(msg);
}

//Export a variable
export var myMsg = 'Hello ES6!!';

//Export a function without name
export default (function () { //some code })();

//Export a variable without name
export default 50;
````
<br>
> Note: In ES6 classes, let and const can also be exported. Also name of a function, class name or variable name are used as export name.


## Import

Syntax `import` 

There are different ways to import as well.

```javascript

//myFunz.js file
export function printName(msg) {
	console.log('My name is ' + msg);
}

export var myDefaultName = 'Foo';

//App.js file
import {myDefaultName, printName as printMyName} from './myFunz';

printMyName('Bar'); //print My name is Bar

console.log(myDefaultName); //print Foo
````

>Note: Import a module and change its name with `as` keyword.

<br>

Import a default module. Syntax `import default`


```javascript

//myDefault.js file
export default function printName(msg) {
	console.log(msg);
}

//App.js file
import printName from './myFunz';

printName('Default Module'); //print Default Module

````


## Reference

- <a href="http://www.2ality.com/2014/09/es6-modules-final.html" target="_blank">ES6 Modules</a>
- <a href="https://github.com/ModuleLoader/es6-module-loader/wiki/Brief-Overview-of-ES6-Module-syntax" target="_blank">Brief Overview of ES6 Module</a>
- <a href="http://babeljs.io/docs/usage/modules/" target="_blank">ES6 Module for CommonJS & AMD</a>