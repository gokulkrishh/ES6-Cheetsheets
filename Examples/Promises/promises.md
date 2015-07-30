## Promises

Promise helps to run a function asynchronously and return either success or failure, when they are done processing. We can listen to success or failure state using `then` callback. 

There are 3 States in promise

1. Pending   - Intial state which not fulfilled or rejected.

1. Fulfilled - async operation is completed successfully.

1. Rejected  -  async operation is failed.

>Note: A promise can either fullfilled or rejected only once.

<a href="http://goo.gl/kJQYrC" target="_blank">Demo</a>

```javascript
//Creating a promise object
var promise = new Promise(function(resolve, reject) {
  
  //Making an ajax call
  $.ajax({
    url : 'https://api.github.com/users/gokulkrishh',
    method: 'get'
  })
  .success(function (response) {
    resolve(response); //Return response
  })
  .error(function (error) {
    reject(error); //Return error
  });
});

//Then callback to listen to resolve or rejected state
promise.then(function (response) {
  console.log('Success -->', response);
},
//Reject callback
function (error) {
  console.log('Error -->', error);
})
//To handle error
.catch(function (e) {
	console.log(e);
});
````

## Promise all

To do multiple async calls you can use `promise.all()` which takes array of promises. And once all of them are fullfilled, an array of values are returned in the same order as you called.

<a href="http://goo.gl/5X3hmj" target="_blank">Demo</a>

```javascript
var promise = Promise.all([1, 2, 3, 4, 5]); //Passing an array of calls 

promise.then(function (response) {
  //All Response will be returned as an array in same order
  response.forEach(function (value) {
    console.log(value);
  });
},
//Reject callback
function (error) {
  console.log('Error -->', error);
})
//To handle error
.catch(function (e) {
	console.log(e);
});
````

## Reference

- <a href="http://www.2ality.com/2014/10/es6-promises-api.html" target="_blank">ES6 promises api</a>
- <a href="http://www.sitepoint.com/deeper-dive-javascript-promises/" target="_blank">Javascript promises</a>