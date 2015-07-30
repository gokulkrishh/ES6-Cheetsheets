## Templates & Strings

Variable bindings are possible in ES6 using `${}`.

<a href="http://goo.gl/u4v8MF" target="_blank">Demo</a>

```javascript
let name = 'Foo';

var myMsg = `Hello ${name}`;

alert(myMsg); //alert Hello Foo
````

>Note: I have not used single quote here.

## Multiline strings

In vanilla JS, to create multiline we have to use `\n`. But in ES6, writing in next line will be taken new line.

<a href="http://goo.gl/7Zat5y" target="_blank">Demo</a>

```javascript
let myMsg = `In ES6 multi line 
 is so easy to create.`

alert(myMsg); 
//alert In ES6 multi line 
// is so easy to create.
````