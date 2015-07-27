# Arrows

Arrows `=>` are function shorthand.

## Table of Contents

1. [IIFE](#IIFE)
1. [Function Expression](#function-expression)
1. [this](#this)

## IIFE

Immediately invoked function expression (iife).

<a href="https://goo.gl/fd2qyI" target="_blank">Demo</a>

In ES6


````
() => { alert('Hello World!') }()

or 

(() => 7)()
````

*Converts into vanilla js as below*

````
'use strict';

(function () {
  alert('Hello World!');
})();

or

(function () {
  return 7;
})();

````
>You might have noticed `use strict` in coversion. ES6 transpilers adds it by default. But for upcoming examples I am going to simply ignore `use strict`


## Function Expression

<a href="https://goo.gl/0GUKlj" target="_blank">Demo</a>


````
var funz = () => someStatement

// equivalent to: => { return someExpression }
````

*Converts into vanilla js as below*

````
var funz = function funz() {
  return someStatement;
};

````

**[⬆ back to top](#table-of-contents)**

## this

the value of `this` is undefined in `use strict` mode function calls

#### Example in vanilla js

<a href="https://goo.gl/qx4TOB" target="_blank">Demo</a>

````
'use strict';

function father(){
  this.age = 0;

  function son() {
    console.log(this.age); //print undefined
  }
  
  son();
}

var f = new father();
````

<br>
>In ES6, `this` will be the value of its same context

<br>

##### In ES6

<a href="https://goo.gl/tvISlV" target="_blank">Demo</a>

````
function father() {
  this.age = 0;
  
  () => {console.log(this.age)}()
}

var f = new father();
````

*Converts into vanilla js as below*

````

function father() {
  var _this = this;

  this.age = 0;

  (function () {
    console.log(_this.age); //print 0
  })();
}

var f = new father();

````

**[⬆ back to top](#table-of-contents)**


## Reference

- <a href="https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Functions/Arrow_functions" target="_blank">Arrow functions</a>
- <a href="http://babeljs.io/docs/learn-es2015/" target="_blank">Learn es2015</a>







