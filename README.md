## You Don't Need Lodash/Underscore 

Lodash and Underscore are great modern Javascript utility libraries, and they are widely used by Front-end developers. However, when you are targeting modern browers, you may find out that there are many methods which are already being supported natively thanks to ECMAScript5 [ES5] and ESCMAScript2015 [ES6]. Native implematations are simply faster and more convenient which can make code clearer.

Welcome to contribute more items which you find this list is missing.

## Quick Link

1. [_.each](#_.each)
1. [_.map](#_.map)
1. [_.every](#_.every)
1. [_.some](#_.every)
1. [_.reduce](#_.reduce)
1. [_.reduceRight](#_.reduceRight)
1. [_.filter](#_.filter)
1. [_.find](#_.find)
1. [_.findIndex](#_.find)
1. [_.indexOf](#_.indexOf)
1. [_.lastIndexOf](#_.lastIndexOf)
1. [_.contains](#_.contains)


## _.each

Iterates over a list of elements, yielding each in turn to an iteratee function.

  ```js
  // Underscore/Lodash
  _.each([1, 2, 3], function(value, index) {
    console.log(value);
  });
  // output: 1 2 3

  // Native
  [1, 2, 3].forEach(function(value, index) {
    console.log(value);
  });
  // output: 1 2 3
  ```
### Browser Support

![Chrome](https://raw.github.com/alrra/browser-logos/master/chrome/chrome_48x48.png) | ![Firefox](https://raw.github.com/alrra/browser-logos/master/firefox/firefox_48x48.png) | ![IE](https://raw.github.com/alrra/browser-logos/master/internet-explorer/internet-explorer_48x48.png) | ![Opera](https://raw.github.com/alrra/browser-logos/master/opera/opera_48x48.png) | ![Safari](https://raw.github.com/alrra/browser-logos/master/safari/safari_48x48.png)
--- | --- | --- | --- | --- |
  ✔  | 1.5 ✔ |  9 ✔  |  ✔  |  ✔  |   

## _.map

Translate all items in an array or object to new array of items.

  ```js
  // Underscore/Lodash
  var array1 = [1, 2, 3];
  var array2 = _.map(array, function(value, index) {
    return value*2;
  });
  console.log(array2);
  // output: [2, 4, 6]

  // Native
  var array1 = [1, 2, 3];
  var array2 = array.map(function(value, index) {
    return value*2;
  });
  console.log(array2);
  // output: [2, 4, 6]
  ```
### Browser Support

![Chrome](https://raw.github.com/alrra/browser-logos/master/chrome/chrome_48x48.png) | ![Firefox](https://raw.github.com/alrra/browser-logos/master/firefox/firefox_48x48.png) | ![IE](https://raw.github.com/alrra/browser-logos/master/internet-explorer/internet-explorer_48x48.png) | ![Opera](https://raw.github.com/alrra/browser-logos/master/opera/opera_48x48.png) | ![Safari](https://raw.github.com/alrra/browser-logos/master/safari/safari_48x48.png)
--- | --- | --- | --- | --- |
  ✔  | 1.5 ✔ |  9 ✔  |  ✔  |  ✔  |  

## _.every

Tests whether all elements in the array pass the test implemented by the provided function.

  ```js
  // Underscore/Lodash
  function isLargerThanTen(element, index, array) {
    return element >=10;
  }
  var array = [10, 20, 30];
  var result = _.every(array, isLargerThanTen);
  console.log(result);
  // output: true

  // Native
  function isLargerThanTen(element, index, array) {
    return element >=10;
  }

  var array = [10, 20, 30];
  var result = array.every(isLargerThanTen);
  console.log(result);
  // output: true
  ```
### Browser Support

![Chrome](https://raw.github.com/alrra/browser-logos/master/chrome/chrome_48x48.png) | ![Firefox](https://raw.github.com/alrra/browser-logos/master/firefox/firefox_48x48.png) | ![IE](https://raw.github.com/alrra/browser-logos/master/internet-explorer/internet-explorer_48x48.png) | ![Opera](https://raw.github.com/alrra/browser-logos/master/opera/opera_48x48.png) | ![Safari](https://raw.github.com/alrra/browser-logos/master/safari/safari_48x48.png)
--- | --- | --- | --- | --- |
  ✔  | 1.5 ✔ |  9 ✔  |  ✔  |  ✔  |  

## _.some

Tests whether some element in the array passes the test implemented by the provided function.
 
  ```js
  // Underscore/Lodash
  function isLargerThanTen(element, index, array) {
    return element >=10;
  }
  var array = [10, 9, 8];
  var result = _.every(array, isLargerThanTen);
  console.log(result);
  // output: true

  // Native
  function isLargerThanTen(element, index, array) {
    return element >=10;
  }

  var array = [10, 9, 8];
  var result = array.some(isLargerThanTen);
  console.log(result);
  // output: true
  ```
### Browser Support

![Chrome](https://raw.github.com/alrra/browser-logos/master/chrome/chrome_48x48.png) | ![Firefox](https://raw.github.com/alrra/browser-logos/master/firefox/firefox_48x48.png) | ![IE](https://raw.github.com/alrra/browser-logos/master/internet-explorer/internet-explorer_48x48.png) | ![Opera](https://raw.github.com/alrra/browser-logos/master/opera/opera_48x48.png) | ![Safari](https://raw.github.com/alrra/browser-logos/master/safari/safari_48x48.png)
--- | --- | --- | --- | --- |
  ✔  | 1.5 ✔ |  9 ✔  |  ✔  |  ✔  |  

## _.reduce

Applies a function against an accumulator and each value of the array (from left-to-right) to reduce it to a single value.

  ```js
  // Underscore/Lodash
  var array = [0, 1, 2, 3, 4];
  var result = _.reduce(array, function (previousValue, currentValue, currentIndex, array) {
    return previousValue + currentValue;
  });
  console.log(result);
  // output: 10

  // Native
  var array = [0, 1, 2, 3, 4];
  var result = array.reduce(function (previousValue, currentValue, currentIndex, array) {
    return previousValue + currentValue;
  });
  console.log(result);
  // output: 10
  ```
### Browser Support

![Chrome](https://raw.github.com/alrra/browser-logos/master/chrome/chrome_48x48.png) | ![Firefox](https://raw.github.com/alrra/browser-logos/master/firefox/firefox_48x48.png) | ![IE](https://raw.github.com/alrra/browser-logos/master/internet-explorer/internet-explorer_48x48.png) | ![Opera](https://raw.github.com/alrra/browser-logos/master/opera/opera_48x48.png) | ![Safari](https://raw.github.com/alrra/browser-logos/master/safari/safari_48x48.png)
--- | --- | --- | --- | --- |
  ✔  | 3.0 ✔ |  9 ✔  |  10.5  |  4.0  |  

## _.reduceRight

This method is like _.reduce except that it iterates over elements of collection from right to left.

  ```js
  // Underscore/Lodash
  var array = [0, 1, 2, 3, 4];
  var result = _.reduceRight(array, function (previousValue, currentValue, currentIndex, array) {
    return previousValue - currentValue;
  });
  console.log(result);
  // output: -2

  // Native
  var array = [0, 1, 2, 3, 4];
  var result = array.reduce(function (previousValue, currentValue, currentIndex, array) {
    return previousValue - currentValue;
  });
  console.log(result);
  // output: -2
  ```
### Browser Support

![Chrome](https://raw.github.com/alrra/browser-logos/master/chrome/chrome_48x48.png) | ![Firefox](https://raw.github.com/alrra/browser-logos/master/firefox/firefox_48x48.png) | ![IE](https://raw.github.com/alrra/browser-logos/master/internet-explorer/internet-explorer_48x48.png) | ![Opera](https://raw.github.com/alrra/browser-logos/master/opera/opera_48x48.png) | ![Safari](https://raw.github.com/alrra/browser-logos/master/safari/safari_48x48.png)
--- | --- | --- | --- | --- |
  ✔  | 3.0 ✔ |  9 ✔  |  10.5  |  4.0  |  

## _.filter

Creates a new array with all elements that pass the test implemented by the provided function.

  ```js
  // Underscore/Lodash
  function isBigEnough(value) {
    return value >= 10;
  } 
  var array = [12, 5, 8, 130, 44];
  var filtered = _.filter(array, isBigEnough);
  console.log(filtered);
  // output: [12, 130, 44]

  // Native
  function isBigEnough(value) {
    return value >= 10;
  } 
  var array = [12, 5, 8, 130, 44];
  var filtered = array.filter(isBigEnough);
  console.log(filtered);
  // output: [12, 130, 44]
  ```
### Browser Support

![Chrome](https://raw.github.com/alrra/browser-logos/master/chrome/chrome_48x48.png) | ![Firefox](https://raw.github.com/alrra/browser-logos/master/firefox/firefox_48x48.png) | ![IE](https://raw.github.com/alrra/browser-logos/master/internet-explorer/internet-explorer_48x48.png) | ![Opera](https://raw.github.com/alrra/browser-logos/master/opera/opera_48x48.png) | ![Safari](https://raw.github.com/alrra/browser-logos/master/safari/safari_48x48.png)
--- | --- | --- | --- | --- |
  ✔  | 1.5 ✔ |  9 ✔  |  ✔  |  ✔  |  

## _.find

Returns a value in the array, if an element in the array satisfies the provided testing function. Otherwise undefined is returned.

  ```js
  // Underscore/Lodash
  var users = [
    { 'user': 'barney',  'age': 36, 'active': true },
    { 'user': 'fred',    'age': 40, 'active': false },
    { 'user': 'pebbles', 'age': 1,  'active': true }
  ];

  _.find(users, function(o) { return o.age < 40; });
  // output: object for 'barney'

  // Native
  var users = [
    { 'user': 'barney',  'age': 36, 'active': true },
    { 'user': 'fred',    'age': 40, 'active': false },
    { 'user': 'pebbles', 'age': 1,  'active': true }
  ];

  var result = users.find(function(o) { return o.age < 40; });
  // output: object for 'barney'
  ```
### Browser Support

![Chrome](https://raw.github.com/alrra/browser-logos/master/chrome/chrome_48x48.png) | ![Firefox](https://raw.github.com/alrra/browser-logos/master/firefox/firefox_48x48.png) | ![IE](https://raw.github.com/alrra/browser-logos/master/internet-explorer/internet-explorer_48x48.png) | ![Opera](https://raw.github.com/alrra/browser-logos/master/opera/opera_48x48.png) | ![Safari](https://raw.github.com/alrra/browser-logos/master/safari/safari_48x48.png)
--- | --- | --- | --- | --- |
  45.0  | 25.0 ✔ |  Not supported  |  Not supported |  7.1  |  

## _.findIndex

Returns an index in the array, if an element in the array satisfies the provided testing function. Otherwise -1 is returned.

  ```js
  // Underscore/Lodash
  var users = [
    { 'user': 'barney',  'age': 36, 'active': true },
    { 'user': 'fred',    'age': 40, 'active': false },
    { 'user': 'pebbles', 'age': 1,  'active': true }
  ];

  var index =  _.findIndex(users, function(o) { return o.age >= 40; });
  console.log(index);
  // output: 1

  // Native
  var users = [
    { 'user': 'barney',  'age': 36, 'active': true },
    { 'user': 'fred',    'age': 40, 'active': false },
    { 'user': 'pebbles', 'age': 1,  'active': true }
  ];

  var index =  users.findIndex(function(o) { return o.age >= 40; });
  console.log(index);
  // output: 1
  ```
### Browser Support

![Chrome](https://raw.github.com/alrra/browser-logos/master/chrome/chrome_48x48.png) | ![Firefox](https://raw.github.com/alrra/browser-logos/master/firefox/firefox_48x48.png) | ![IE](https://raw.github.com/alrra/browser-logos/master/internet-explorer/internet-explorer_48x48.png) | ![Opera](https://raw.github.com/alrra/browser-logos/master/opera/opera_48x48.png) | ![Safari](https://raw.github.com/alrra/browser-logos/master/safari/safari_48x48.png)
--- | --- | --- | --- | --- |
  45.0  | 25.0 ✔ |  Not supported  |  Not supported |  7.1  |  

## _.indexOf

Returns the first index at which a given element can be found in the array, or -1 if it is not present.

  ```js
  // Underscore/Lodash
  var array = [2, 9, 9];
  var result = _.indexOf(array, 2);    
  console.log(result); 
  // output: 0

  // Native
  var array = [2, 9, 9];
  var result = array.indexOf(2);    
  console.log(result); 
  // output: 0
  ```
### Browser Support

![Chrome](https://raw.github.com/alrra/browser-logos/master/chrome/chrome_48x48.png) | ![Firefox](https://raw.github.com/alrra/browser-logos/master/firefox/firefox_48x48.png) | ![IE](https://raw.github.com/alrra/browser-logos/master/internet-explorer/internet-explorer_48x48.png) | ![Opera](https://raw.github.com/alrra/browser-logos/master/opera/opera_48x48.png) | ![Safari](https://raw.github.com/alrra/browser-logos/master/safari/safari_48x48.png)
--- | --- | --- | --- | --- |
  ✔  | 1.5 ✔ |  9 ✔  |  ✔  |  ✔  |  

## _.lastIndexOf

Returns the index of the last occurrence of value in the array, or -1 if value is not present.

  ```js
  // Underscore/Lodash
  var array = [2, 9, 9, 4, 3, 6];
  var result = _.lastIndexOf(array, 9);    
  console.log(result); 
  // output: 2

  // Native
  var array = [2, 9, 9, 4, 3, 6];
  var result = array.lastIndexOf(2);    
  console.log(result); 
  // output: 0
  ```
### Browser Support

![Chrome](https://raw.github.com/alrra/browser-logos/master/chrome/chrome_48x48.png) | ![Firefox](https://raw.github.com/alrra/browser-logos/master/firefox/firefox_48x48.png) | ![IE](https://raw.github.com/alrra/browser-logos/master/internet-explorer/internet-explorer_48x48.png) | ![Opera](https://raw.github.com/alrra/browser-logos/master/opera/opera_48x48.png) | ![Safari](https://raw.github.com/alrra/browser-logos/master/safari/safari_48x48.png)
--- | --- | --- | --- | --- |
  ✔  |  ✔ |  9 ✔  |  ✔  |  ✔  |  

## _.contains

Checks if value is in collection. 

  ```js
  var array = [1, 2, 3];
  // Underscore/Lodash
  _.includes(array, 1);
  // → true

  // Native
  var array = [1, 2, 3];
  array.includes(1);
  // → true
  ```
### Browser Support

![Chrome](https://raw.github.com/alrra/browser-logos/master/chrome/chrome_48x48.png) | ![Firefox](https://raw.github.com/alrra/browser-logos/master/firefox/firefox_48x48.png) | ![IE](https://raw.github.com/alrra/browser-logos/master/internet-explorer/internet-explorer_48x48.png) | ![Opera](https://raw.github.com/alrra/browser-logos/master/opera/opera_48x48.png) | ![Safari](https://raw.github.com/alrra/browser-logos/master/safari/safari_48x48.png)
--- | --- | --- | --- | --- |
  47✔  | 43 ✔ |  Not supported  |  34 |  9  |  


## Reference

* [Mozilla Developer Network](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference) 

* [Underscore.js](http://underscorejs.org) 

* [Lodash.js](https://lodash.com/docs) 

Inspired by: 

* [You-Dont-Need-jQuery](https://github.com/oneuijs/You-Dont-Need-jQuery)

# License

MIT
