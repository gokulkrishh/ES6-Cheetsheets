# Parameter Handling

In ES6, handling a parameter or defining a method has become lot easier.

## Table of Contents

1. [Default Parameter](#resting-parameter)
1. [Resting Parameter](#resting-parameter)
1. [Spread Parameter](#resting-parameter)

## Default Parameter

<a href="http://goo.gl/KwLYRu" target="_blank">Demo</a>

Your can passing a default parameter in function argument.

````
function funz(a, b = 5) {
	console.log(a + b); //print 6
}

// Equivalent to: b === 5 if b is undefined or not passed
funz(1);
````

*Converted as*

````
function funz(a) {
	var b = arguments.length <= 1 || arguments[1] === undefined ? 5 : arguments[1];

	console.log(a + b); //print 6
}

// Equivalent to: b === 5 if b is undefined or not passed
funz(1);

````

>From now on, converted venilla js code will not be added, Check the output in the demo link.


**[⬆ back to top](#table-of-contents)**


## Resting Parameter

<a href="http://goo.gl/gXtiBr" target="_blank">Demo</a>

Passing a `...` resting parameter at end of the function argument means that last argument will be received as an array.

````
function funz(a, ...b) {
	console.log(a, b); //print 1 [2, 3, 4]
}

funz(1, 2, 3, 4); // a = 1; b = [2, 3, 4]
````

## Spread Parameter

<a href="http://goo.gl/QzAY79" target="_blank">Demo</a>

Passing a `...` spread parameter in function argument means that passing each element of array as argument.

````
function funz(a, b, c, d) {
	console.log(a); //print 1
	console.log(b); //print 2
	console.log(c); //print 3
	console.log(d); //print 4
}

funz(...[1, 2, 3, 4]);
````

**[⬆ back to top](#table-of-contents)**

## Reference

- <a href="http://babeljs.io/docs/learn-es2015/#default-rest-spread" target="_blank">Rest Spread</a>