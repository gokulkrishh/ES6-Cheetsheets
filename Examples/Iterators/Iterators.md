# Iterators

`For of` is used to iterate over the property values, instead of property names which is	`for in` loop.


## For in

`For in` loop prints property name. See below example

*Written in venilla js*

```javascript
var arr = [1, 2, 3, 4, 5, 6];

arr.obj = 'I am a string';

for (var i in arr) {
	console.log(i); //print 0 1 2 3 4 5 obj, property names
}

````

## For of

`For of` loop prints property values.

<a href="http://goo.gl/3SSWzy" target="_blank">Demo</a>


```javascript
var arr = [1, 2, 3, 4, 5, 6];

arr.obj = 'I am a string';

for (var i of arr) {
	console.log(i); //print 1 2 3 4 5 6, values not property name
}

````

**[⬆ back to top](#table-of-contents)**

## Reference

- <a href="https://developer.mozilla.org/en/docs/Web/JavaScript/Reference/Statements/for...of" target="_blank">let</a>