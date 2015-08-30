# SUIT UP YOU APP

> The world is not (yet) dominated by JavaScript

## "Les 3 frères" of Front-end development

1. HMTL for Semantic structure
2. CSS for Presentation
3. Javascript Interactions

Think HTML and CSS first to develop a web app.

## How Browser works

When you navigate, we have 3 main areas:

* the network
* the server for request and responser
* the client for processing and rendering

With HTML and CSS, browser turn your code in web page.

### Minimalist

```html
<!DOCTYPE html>
<html>
  <head>
  </head>
  <body>
  </body>
</html>
```

### DOM Tree

The browser parse the HTML to construct the DOM Tree.

```html
<html>
  <head>
  </head>
  <body>
    <p>How browser works</p>
    <div>
      <span>with DOM and CSS tree</span>
    </div>
  </body>
</html>
```

* `<html>` - HTMLHtmlElement
* `<body>` - HTMLBodyElement
* `<p>` - HTMLParagraphElement - Text
* `<div>` - HTMLDivElement
* `<span>` - HTMLSpanElement

### Construction of Render Tree

> Render tree = Dom Tree + Style Structure

The same tree is build from CSS style called CSS Object Model.

Only visual elements are included in Render Tree.

### Layout of Render Tree

* size
* position

### Painting the Render Tree

Render in client device.

## HTML Coding standards and best practices

### Doctype

Start with a proper doctype declaration for browsers

```html
<!DOCTYPE html>
```

### Encoding

Use UTF-8 for internationalization

```html
<meta charset="utf-8">
```

### Indentation

Indent nested and child elements

```html
<div class="tweet">
	<a href="path/to/somewhere">
</div>
```

### Naming

Name class and id with meaning

```html
<div class="top light" id="tweet-list">
```

### Lower case

Lower case for tag and attribute

```html
<div class="top" id="header" attribute="value">
```

### Close tag

Place a comment on closing div/section tags to indicate closing elements

```html
</div> <!-- Facebook post list -->
```

### Double quotes

Double quotes on attributes value

```html
<img src="path.png" alt="Logo">
```

### Reducing markup

Simple DOM design: less is more in markups using

```html
<!-- Not so great -->
<span class="avatar">
	<img src="...">
</span >

<!-- Better -->
<img class="avatar" src="...">
```

## CSS Coding standards and best practices

### Selectors

Selectors are evaluated right to left and should be as broad as possible. Really specific selectors are unnecessary and hinder performance.

```css
a.nav {
  color: blue;
}
```

### Blocks

Use multi-line blocks and combination to make CSS cleaner and easier to read: Each style gets its own line

```css
.someDiv {
  background: red;
  padding: 2em;
  border: 1px solid black;
}

h1, h2, h3 {
  font-family: tahoma;
  color: #333
}
```

### Comments

Use comments to denote groups.

```css
/* Here's how you comment CSS */
```

### Whitespace

Put before and after each style block.

```css
a.nav {
  color: red;
}

.some-class {
  background: @purple;
}
```

### Naming conventions

Use meaningful class and id names

```css
.link.first {
  color: red;
}
```

### Reset

The reset allows your layout look consistent in all browsers.

```css
<link rel="stylesheet" type="text/css" href="reset.css" />
```

### Structure

Create Your HTML First and Organize the css file with a Top-down Structure.

```css
/* Generic classes */
Style goes here...

/* Header */
Style goes here...

/* Content */
Style goes here...
```

### Multiple classes

Add multiple classes to an element.

```css
div class="box right"></div>
```

### Shorthand

Combine styles in one line.

```css
#box {
  margin: 8px 7px 0px 5px; // top, right, bottom, and left values, respectively.
}
```

### Alphabetize your Properties

Improved readability

```css
#cotton-candy {
  color: #fff;
  float: left;
  font-weight:bold;
  height: 200px;
  margin: 0;
  padding: 0;
  width: 150px;
}
```

### Generic classes

Create generic classes to readability

```css
.left {
  float:left
}

.right {
  float:right
}
```

### Use Multiple Stylesheets

Make smaller and css multiple files.

```css
<link rel="stylesheet" type="text/css" href="reset.css"/>
<link rel="stylesheet" type="text/css" href="style.css"/>
<link rel="stylesheet" type="text/css" href="widget.css"/>
```

## Deep diving

* [Principle 1. Develop Coding Standards](https://github.com/92bondstreet/xp-front-end#principle-1-develop-coding-standards)
* [Principles of writing consistent, idiomatic HTML](https://github.com/necolas/idiomatic-html)
* [Github Scaffolding](http://primercss.io/scaffolding/)
* [Principles of writing consistent, idiomatic CSS](https://github.com/necolas/idiomatic-css)
* [https://github.com/necolas/idiomatic-css](https://speakerdeck.com/dmosher/so-you-want-to-be-a-front-end-engineer)
* [Web Style Guide](http://webstyleguide.com/wsg3/index.html)
* [Three Simple Techniques for Writing More Semantic and Maintainable JavaScript Apps](https://medium.com/space-camp/three-simple-techniques-for-writing-more-semantic-and-maintainable-javascript-apps-206b4fb89f15)
* [Comparing CSS code styles and deciding which is the best practice](https://medium.com/@WoloxEngineering/comparing-css-code-styles-and-deciding-which-is-the-best-practice-360a8e058988)
* [WordPress HTML Coding Standards](https://make.wordpress.org/core/handbook/best-practices/coding-standards/html/)
* [Code Guide by @mdo](http://mdo.github.io/code-guide/)
* [Isobar Front-end Code Standards](http://isobar-idev.github.io/code-standards/)
* [Your first lesson: Learning HTML and web page layout](https://medium.com/teach-yourself-web-development/your-first-day-learning-html-and-how-a-webpage-is-laid-out-41558ff08264)
[http://diveintohtml5.info/](http://diveintohtml5.info/)
