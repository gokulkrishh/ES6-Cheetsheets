# Classes & Inheritance

ES6 supports classes using `class` keyword, for constructor `constructor` keyword and for the inheritance using `extends` keyword.


## Table of Contents

1. [Classes](#classes)
1. [Construtor & Inheritance](#construtor-inheritance)

# Classes

You cannot call a class like a normal function. But you can use `new` keyword to invoke a class.

<a href="http://goo.gl/l8mUwP" target="_blank">Demo</a>

```javascript
class Parent {
	print() {
		 console.log('I am a class');
	}
}

Parent(); //Type error: Cannot call a class as a function

var myParent = new Parent(); //Use `new` keyword to use class as construtor

new Parent().print(); //print I am a class

````

<br>

>Note: Class declarations are not hoisted like a function declaration and will be avaiable only after its execution. See the below example

<br>
##### Hoisting Example

<a href="http://goo.gl/QjjE99" target="_blank">Demo</a>

```javascript
new myClass().print(); //TypeError due to hoisting limitation in class

class myClass {
		print() {
		console.log('I am a class with a name myClass');
	}
}

new myClass().print(); //print I am a class with a name myClass
````

**[⬆ back to top](#table-of-contents)**

# Construtor & Inheritance

Using class we can create a base class or parent class which can be later inherited by an another class. See an example below.

<a href="http://goo.gl/O3YUUa" target="_blank">Demo</a>

```javascript
//Parent class
class Parent {
	constructor(myName) {
		this.name = myName;
	}
	
	print() {
		return 'My parent is ' + this.name;
	}
}

//Child class inheriting from a base class
class Child extends Parent {
	constructor(myName, newName) {
		super(myName); //Calling derived constructor using `super`
		this.newName = newName;
	}
	
	print() {
		console.log(super.print() + ' and My name is ' + this.newName);
	}
}

let myChild = new Child('Gokul', 'Krishh');

myChild.print(); //print My parent is Gokul and My name is Krishh
````

**[⬆ back to top](#table-of-contents)**


## Reference

- <a href="http://www.2ality.com/2015/02/es6-classes-final.html" target="_blank">es6 classes</a>