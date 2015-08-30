# Introduction to Javascript

> The World's Most Used Programming Language

## JS in the field

One of goals of Web Application building is to develop a codebase

* flexible
* modular
* scalable
* reusable
* maintenable
* readable
* ...able

As developer, you're spoilt for choice for programming languages: `Java`, `.Net`, `PHP`, `Ruby`, `Python`, `Go`...etc.

> But JavaScript is over.

Javascript is in the fields.

Every browsers support it. You just need a browser and a text editor to start to code with JavaScript (and HTML and CSS). No need SDK or Framework to install or download.

Today, everything in browser could be done with modern JavaScript ecosystem except Data persistence (need a server side data storage even though we could use local storage).

JavaScript is also native for Windows 8, Chrome OS and Gnome.

## History

JavaScript was created in 1995 by [Brendan Eich](https://fr.wikipedia.org/wiki/Brendan_Eich), an engineer at Netscape, and first released with Netscape 2 early in 1996.

The first originally name was to be `LiveScript` but the marketing won the final answer: `JavaScript` to capitalize on the popularity of Java.

> Java !== JavaScript

All JavaScript is validated by Ecma International. The last major edition, 6th, is called ES6 or ECMAScript 2015 (After 6 years of stability for ES5).

## Anatomy of Modern Web Application

Before modern Web Application, it was no way to save an application state. We had to refresh all the part of application.

Today with a single page application, everything work together but independently. The best example is `Gmail`. You don't need to refresh all your page to receive new mails, you can type message and continue to receive notifications...

```txt
client + {CMS, APP} + API + firewall + Datastore  
```

## JavaScript in 1 tweet

```txt
Nearly everything in JavaScript is an object, including functions.
```


## Overview

```txt
JavaScript is an object oriented dynamic language with types and operators, standard built-in objects, and methods.
```

JavaScript doesn't have classes but we can found the functionality with object prototypes.

### The types

* Number
* String
* Boolean
* *Symbol (new in ES6)*
* Object
  * Function
  * Array
  * Date
  * RegExp
* null
* undefined

### Number

Numbers in JavaScript are **double-precision 64-bit format IEEE 754 values**, according to the spec.

```js
+ - / * % ** ++ -- +=
```

With some built-in object as `Math` or function as `parseInt()`

```js
Math.sin(3.5);
```

```js
parseInt("33 years old")
```

You can test for `Infinity`, ``-Infinity` and `NaN` values using the built-in `isFinite()` function:

```js
isFinite(1/0); // false
isFinite(-Infinity); // false
isFinite(NaN); // false
```

### String

Strings are sequences of Unicode characters (16-bit number).

```js
'Javascript on the rock.'
```

Give me the length:

```js
'Javascript on the rock.'.length; // 23
```

Yes. String is object too. You can also call methods from String prototype.

```js
'Javascript on the rock.'.replace('Javascript, Yassine'); // Yassine on the rock.
'js'.toUpperCase(); // 'JS'
```

### Boolean

The famous `true` and `false` with `&&`, `||` and `!` operators.

Any value can be converted to a boolean according to the following rules:

1. false, 0, the empty string (''), NaN, null, and undefined all become false.
1. all other values become true.

### null

`null` is a declared value with a deliberate non-value.

### undefined

`undefined` is an uninitialized value: nothing has been assigned.

## Variables

To declare a new variables in Javascript, use the `var` keyword (`let` and `const` for ES6);

```js
var school;
var course = 'Web App Architectures';
```

## Control Structures.

The same as `C` with conditional statement and loop.

### Conditional statement

* With the traditional `if`

```js
var mercato = 'om';

if (job === 'psg'){
  return 'di-maria';
} else if (job === 'om'){
  return 'bye bye bielsa';
} else {
  return 'martial wtf !!?';
}
```

Some advanced pattern with `&&`, `||` and ternary operator:

```js
var name = school && school.getName();

var name = school.getName() || 'esilv';

var who = school.getName() === 'esilv' ? 'engineering' : 'management';
```

* With the traditional `switch`

`switch` statement can be used with number or string

```js
switch(action) {
  case 'render':
    renderHeader();
    break;
  case 'update':
    updateContent();
    break;
  default:
    renderEverything();
}
```

```js
switch(id) {
  case 1:
    renderHeader();
    break;
  case 2:
    updateContent();
    break;
  default:
    renderEverything();
}
```

#### Loops

```js
for (var i = 0; i < 5; i++) {
  // excute 5 times
}
```

## Objects

Object is a simple unordered collection of name-value pairs.

The more basic way to create an empty object is

```js
var myObj = {};
```

You can start with an item, `name` for example called property simply (functions are called methods):

```js
var mySchool = {'name': esilv};
```

Or more:

```js
var mySchool = {
  'name': 'esilv',
  'details': {
    'town': 'La défense',
    'creation': '1995'
  }
};
```

Now to get/set values, you can chain key calls with `dot` or `bracket` notation:

```js
var name = mySchool.name;
var town = mySchool.details.town;
var date = mySchool.['details'].['creation'];

mySchool.name = 'emlv';

```

## Arrays

Arrays is an ordered collection with a property called `length`.

Each array items can be accessed with `[]` syntax (and only).

The more basic way to create an empty array is

```js
var myArray = [];
```

You can fill it literally:

```js
var languages = ['js', 'php', 'ruby'];
languages.length; // 3

languages = [
  {
    'name': 'php',
    'version': '5.6'
  },
  {
    'name': 'js',
    'version': '6'
  },
  'push everything in array'
]
```

and add (push) new elements:

```js
languages.push('python');
languages.push(10);
```

And you can parse it with a `for` loop:

```js
for (var index = 0, length = languages.length; index < length; index++) {
  // Do something with languages[index]
}
```

## Using functions

Functions are part of JavaScript core.

A simple function example:

```js
function (x, y) {
  return x + y;
}
```

A Function can take 0 or more parameters and can contains as many statement as you like.

```js
function whoAmI(firstName, lastName) {
  var iam = 'nobody';

  if(firstName === 'yassine') {
    iam = firstName + ' ' + lastName;
  }

  return iam;
}
```


## Dom selector

Javascript is today, the only language to manipulate DOM directly in the browser.

You can listen events as click, modify content and interact with users.

> And jQuery ?

Five main methods in VanillaJS to access to a DOM element:

1. getElementById(idValue)

1. getElementsByTagName(tagName)

1. getElementsByClassName(className)

1. querySelector(cssSelector)

1. querySelectorAll(cssSelector)

`jQuery` is a (micro) library to help developers to manipulate DOM regardless of Browser.

### Create a DOM Element

```js
var link = document.createElement('a');
```

### Add a DOM Element

```js
var child = div.appendChild(span);
```

### Element style

```js
element.style.color = "#28aadc";
element.style.marginTop = "10px";
```

### Some getter and setter

```js
// HTML
var content = element.innerHTML;
element.innerHTML = '<div class="introduction"><p>My JS Tribute</p></div>'

// Class name
var className = element.className;
otherElement.className = 'left';
```

### Selector

```js
document.getElementById('introduction');
document.getElementsByTagName('div');
document.getElementsByClassName('.result');
document.querySelector('div.result');
document.querySelectorAll('div.result > li');
```

## Deep Diving

* [JavaScript The Right Way](http://jstherightway.org/)
* [Awesome JavaScript](https://github.com/sorrycc/awesome-javascript)
* [JavaScript For Cats](JavaScript For Cats)
* [JavaScript Objects in Detail](http://javascriptissexy.com/javascript-objects-in-detail/)
* [JavaScript Prototype in Plain Language](http://javascriptissexy.com/javascript-prototype-in-plain-detailed-language/)
* [The Basics of JavaScript DOM Manipulation](http://callmenick.com/post/basics-javascript-dom-manipulation)
