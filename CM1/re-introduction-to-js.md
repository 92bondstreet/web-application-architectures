# Re-Introduction to JavaScript

> The World's Most Misunderstood Programming Language

## OO Programming

Object-oriented programming (OOP) is a programming paradigm that uses abstraction to create models and objects. Each object can be viewed as an independent little machine with a distinct role or responsibility.

OOP uses several techniques including modularity, polymorphism, and encapsulation.

Class, Object, Property, Constructor, Polymorphism... are well known  word in Java, C++, PHP. Also in JavaScript.

> Yes. JavaScript is a object-oriented language. Precisely a prototype-based language.

## Based prototype programming

Prototype-based programming is an OOP model that doesn't use classes but prototype.

Prototype is the set of object properties.

## (Custom) Objects in Detail

### Where is my `class` ?

JavaScript is a prototype-based language and contains no class statement, such as is found in C++ or Java.

Instead, JavaScript uses functions as classes. Defining a class is as easy as defining a function.

```js
var Mention = function () {};
```

For the next sections, `Mentions` is the smallest unit to define a message on social network. It means a tweet is a mention, a post is tweet, an instagram post is a mention...

#### Object vs Object

What the difference between

```js
var mention = {};
```

and

```js
var Mention = function () {};
```

You give an identity to the second object `Mention`: an OOP identify with properties and methods. (Notice the first letter in Uppercase);

The first notation object is a structure.

### Constructor

To create a new instance of an object, we use the statement `new` keyword.

```js
var pastMention = new Mention();
var nowMention = new Mention();
```

#### Adding properties

```js
var Mention = function (author) {
  this.author = author;
};

var mention1 = new Mention('@github');
var mention2 = new Mention('@airbnb');

// Show the author properties of the objects
console.log('author 1 of mention is ' + mention1.author); // logs "author 1 of mention is  @github"
console.log('author 2  of mention is ' + mention2.author); // logs "author 1 of mention is @airbnb"
```

#### Adding methods

```js
var Mention = function (author) {
  this.author = author;

  this.reply = function (from, message) {
    console.log(from + 'replies to ' + this.author )
  }
};
```

```js
var mention1 = new Mention('@github');
mention1.reply('@azzouty');
```

### Prototype

The previous example with `prototype`.

```js
var Mention = function (author) {
  this.author = author;
};

Mention.prototype.content = '';

Mention.prototype.reply = function (from, message) {
  console.log(from + 'replies to ' + this.author );
}

Mention.prototype.print = function () {
  console.log(this.author + ' ' + this.content );
}
```

You can refactor function inside the `prototype` property:

```js
var Mention = function (author) {
  this.author = author;
  this.content = '';
};

Mention.prototype = {
  'reply': function () {},
  'print': function () {}
}
```

#### My style

```js
var Mention = function Mention(options) {
  this.initialize(options);
}

var prototype = Mention.prototype;

/**
 * Reply a message to the mention author
 *
 * @param {String} from - author
 * @param {String} message - message to send
 *
 * return {Mention}
 */
prototype.reply = function (fromn message) {
  console.log(from + 'replies to ' + this.author );
  return this;
}

/**
 * Print and format the mention
 *
 * return {Mention}
 */
prototype.print = function () {
  return this;
}

var mention = new Mention('@github');

mentions.reply('azzouty', 'On the top').print();
```

### Inheritance

In JavaScript, you can create a new Object from an other version.

You do this by assigning an instance of the parent class to the child class, and then specializing it. In modern browsers you can also use `Object.create` to implement inheritance.

```js
var Tweet = function () {
  Mention.call(this); // Call the parent constructor
}

Tweet.prototype = Object.create(Mention.prototype);
Tweet.prototype.constructor = Tweet;

var Post = function (author, content) {
  Mention.call(this, author, content); // Call the parent constructor
}

Post.prototype = Object.create(Mention.prototype);
Post.prototype.constructor = Post;
```

Now, we can update the prototype by adding or modifying properties.

```js
Tweet.prototype = {
  'numberOfRetweets': 0,
  'favorite': function () {}
}

Post.prototype = {
  'numberOfLikes': 0,
  'like': function () {}
}

var post = new Post('pulv', 'ESILV in top #30');
post.like();
```

### Enumerate properties

In lot of cases, you need to enumerate properties or check their presence

#### in

To find out if a property exists on an object (either as an inherited or an own property)

```js
var tweet = new Tweet();

console.log('author' in tweet); // true
console.log('numberOfRetweets' in tweet); // true
```

#### hasOwnProperty

To find out if a property exists on an object and only itself.

```js
var tweet = new Tweet();

console.log(tweet.hasOwnProperty('author')); // false
console.log(tweet.hasOwnProperty('numberOfRetweets')); // true
```

### Serialize and Deserialize Objects

```js
var tweet = {
  'author': '@azzouty',
  'content': 'Markdown my new skill'
};

JSON.stringify(tweet);
// "{"author":"@azzouty","content":"Markdown my new skill"}"
```

You can load a stringified json object with `JSON.parse`.

## Functions in Detail

### function declaration

```js
function reply () {
  // ...
}
```

The only advantage is the hoisting of function `reply` in the scope.

```js
reply(); // Sent

function reply () {
  console.log('Sent');
}
```

### function expression

```js
var reply = function () {
  // ...
}
```

You can assign functions to variables in the same way you would assign values to variables.

It means you can assign function in an object literal.

```js
var TwitterApi = {
  'reply': function () {},
  'retweet': function () {},
  'favorite': function () {}
}
```

The disadvantage is function expression create anonymous function: hard to debug the browser stack trace for example.

### Named function expression

```js
var reply = function reply () {
  // ...
}
```

### IIFE

```js
(funtion () {
  //... code to execute
})();
```

## bind, call, apply

`.bind`, `.call` and `.apply` are useful when you want call a function with a certain context and/or later.

```js
var reply = function (arg1, arg2) {
  var str = '<p>' + this.author + ' reply to ' + arg1 + ' with ' + arg2 + '</p>';
  document.body.innerHTML += str;
};

var context = {
  'author': '@substack'
};
```

### call

`.call` Calls a function with a given `this` value and arguments provided individually.

```js
reply.call(context, '@azzouty', 'I understand !');
```

### apply

`.apply` calls a function with a given `this` value and arguments provided as an array

```js
reply.apply(context, ['@azzouty', 'I understand !']);
```

### bind

`.bind` creates a new function that, when called, has its `this` keyword set to the
provided value, with a given sequence of arguments preceding any provided when the new function was called.

```js
var boundFn = reply.bind(context, '@azzouty', 'I understand !');
boundFn();
```

## Closure: Super power !

## Best practices and Code guidelines

### DRY - Don't repeat yourself

Save same code in shared function.

### DOT - Do One Thing

One method, one thing (well)

### KISS - Keep It Simple Stupid

If it's *too clever*, come back to fundamentals.

### LIM - Less Is More

Write just enough code.

Be lazy in number of lines.

### Javascript Code Guidelines

#### Objects

Use literal expression for object creation.

```js
var item = {};
```

#### Arrays

Use the literal syntax for array creation and push items

```js
var items = [];
someStack.push('abracadabra');
```

#### Strings

Use single quotes `''` for strings

```js
var name = 'Synthesio';
```

#### Functions

Camel case and descriptive vocabulary

```js
function sendVerbatim(){};
function getBestPractices(){};
```

#### Variables

Always use it and one per line

```js
var company = 'Synthesio';
var item = 0;
var stack = [];
var bestTeam = 'PSG';
```

#### Equality

Use `===` and `!==`

```js
if (company === 'Synthesio') {
  ...
}

if (items.length !== 5) {
  ...
}
```

#### Blocks

Use braces even for one line

```js
if (test) {
  return false;
}
```

#### Comments

Use // for one line and above. Use /* */ for multilines

```js
// Comment to explain code
var type = this._type || default;

/*
* A multiline comment
* to describe functions for example
*/
```

#### Whitespace

Set tabs to 2 spaces and be economic

```js

function() {
∙∙var name;
}
```

#### Semicolons

Always use it

```js
var bestTeam = 'PSG';
```

#### Modules

Always use it to be avoid conflict and scope hits

```js
(
  function()
  {
    ...
  }
)();
```

#### Inline

Always use bracket and space in line condition

```js
var variable = (condition) ? then_value : else_value;
```

#### JSDoc

Use JSDoc annotations to describe functions

```js
/* Describe the goal function in one sentence
 *
 * @method myFunction
 *
 * @param  {String}   param1      What is the param1
 * @param  {Array}    param2      What is the param2
 * @return {Boolean}  value       What is the return
 */
 myFunction: function(param1, param2) {
   ....
   return value;
 }
```

#### Early returns

Early returns promote code readability

```js
// Bad:
function returnLate( value ) {
  var ret;

  if ( value ) {
    ret = "value";
  } else {
    ret = "other_value";
  }

  return ret;
}

// Good:
function returnEarly( value ) {

  if ( value ) {
  	return "value";
  }

  return "other_value";
}
```

## Deep diving

* [The best free JavaScript resources](http://jsbooks.revolunet.com/)
* [JavaScript:
The World's Most Misunderstood Programming Language](http://javascript.crockford.com/javascript.html)
* [Introduction to Object-Oriented JavaScript]
(https://developer.mozilla.org/en-US/docs/Web/JavaScript/Introduction_to_Object-Oriented_JavaScript)
* [Eloquent JavaScript](http://eloquentjavascript.net/)
* [Speaking JavaScript](http://speakingjs.com/es5/index.html)
* [OOP In JavaScript: What You NEED to Know](http://javascriptissexy.com/oop-in-javascript-what-you-need-to-know/)
* [ECMAScript® 2015 Language Specification](http://www.ecma-international.org/ecma-262/6.0/index.html)
* [Different Ways of Defining Functions in JavaScript (This Is Madness!)](http://davidbcalhoun.com/2011/different-ways-of-defining-functions-in-javascript-this-is-madness/)
* [Bind, call, and apply. Oh my!](https://medium.com/@buddha_js/bind-call-and-apply-oh-my-8930faa4d173)
* [JavaScript’s Apply, Call, and Bind Methods are Essential for JavaScript Professionals](http://javascriptissexy.com/javascript-apply-call-and-bind-methods-are-essential-for-javascript-professionals/)
* [Understanding JavaScript closure](https://medium.com/@dinamk12/yet-another-closure-explanation-aa43087ac65e)
* [Javascript Closures
](https://medium.com/@ianprojones/javascript-closures-17f803f8fc1f)

### Style guide

* https://github.com/rwaldron/idiomatic.js/
* https://github.com/Seravo/js-winning-style
* https://github.com/airbnb/javascript
* http://sideeffect.kr/popularconvention
* http://google-styleguide.googlecode.com/svn/trunk/javascriptguide.xml
* https://www.npmjs.org/doc/coding-style.html
* http://nodeguide.com/style.html
* http://contribute.jquery.org/style-guide/js/
* http://javascript.crockford.com/code.html
