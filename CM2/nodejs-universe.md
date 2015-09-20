# Node.js, Master of Universe?

> Trust me, Node is more than awesome.

The first time that I heard about a Web Server written in Javascript, I didn't believe it.

Yes. A Web Server. As Apache and IIS. Something for a novice web developer. Something a little bit obscur.

```txt
Node is more than awesome
```

## Numbers don't lie

### Real-Time Web

In 2012, 2 on 3 of americans connect to the Internet via a Mobile device.

And 34 of the world's Top 100 websites are using HTML (5).

What does it mean ?

```txt
The Web is Real-Time.
```

HTML 5 is *the new* HTML and the mobile usage is growing.

The real-time Web Application requires a real-time
technology.

### Node.js in 3 tweets

* Node.js uses an event driven, non-blocking I/O model.

* Node.js is build on JavaScript to unify front-end and server-side architectures.

* Node.js is ideal for high performace, highly scalable and distributed real-time Web Applications.

### Some Github stats

Second most popular projects on GitHub (in 2013, 4 years after its debut).

### Give me notable users

#### LinkedIn

On the server side, LinkedIn's entire mobile software stack is completely build in Node.js

LinkedIn went from running **15 servers** with **15 instances** on each physical machine to just **4 instances** that can handle **2x** the traffic.

#### Walmart

Walmart re-engineered their mobile app to the powered by Node.js

Walmart pushed all their JavaScript processing to the server for a rich and dynamic experience for customers.

#### Today

* Ebay
* NPR
* CBS Interactive
* Zappos.com
* General Motors
* Yahoo!
* Condé Nast
* Adobe
* DowJones
* Uber
* Dell
* Mozilla

For networked multiplayer games, interactive websites and tools, web analytics, chat system...

### Why you can't say no?

1. It's JavaScript
1. Code reuse at every level: browser and server
1. Strong community
1. Performance and scalability


## A Web Server in Javascript? WTF

### V8

In 2008, Google open-sourced V8, the JavaScript engine written in C++ that powers Chrome.

The first design of V8 is to increase the performance of the JavaScript execution inside web browsers.

How ?

Translate JavaScript code into more efficient machine code instead of using an interpreter.

```txt
It’s not just about making your current application run faster,
it’s about enabling things that you have never been able to do in the past.

Daniel Clifford (tech lead and manager of the V8 team)
```

### Node.js

Node.js was released in 2009 as an open source project designed to help you to write JavaScript programs that talk to networks, file systems or other I/O sources.

That's it!

**It is just a simple and stable I/O platform that you are encouraged to build modules on top of.**


## IO

[! IO](https://github.com/maxogden/art-of-node/blob/master/server-diagram.png)

To build a fast and robust web server, you have the choice:

1. Write from scratch in C: difficult to code but your web server will give you super fast results.
1.

Node was created to strike a balance between these two choices: to be relatively easy to understand and use and fast enough for most use cases.

### No no and no

* Node.js is not a web framework (like Rails or Django, though it can be used to make such things)
* Node.js is not programming language (it uses JavaScript but node isn't its own language)

### So, what?

Node.js is useful for I/O based programs that need to be fast and/or handle lots of connections

At a lower level, node can be described as a tool for writing two major types of programs:

* Network programs using the protocols of the web: HTTP, TCP, UDP, DNS and SSL
* Programs that read and write data to the filesystem or local processes/memory:
  * Databases (e.g. MySQL, PostgreSQL, MongoDB, Redis, CouchDB)
  * APIs (e.g. Twitter, Facebook, Apple Push Notifications)
  * HTTP/WebSocket connections (from users of a web app)
  * Files

## No-blocking

Node does I/O in a way that is **asynchronous** which lets it handle lots of different things simultaneously.

### Example

For example, if you go down to a fast food joint and order a cheeseburger they will immediately take your order and then make you wait around until the cheeseburger is ready.

In the meantime they can take other orders and start cooking cheeseburgers for other people.

Imagine if you had to wait at the register for your cheeseburger, blocking all other people in line from ordering while they cooked your burger!

This is called blocking I/O because all I/O (cooking cheeseburgers) happens one at a time. Node, on the other hand, is non-blocking, which means it can cook many cheeseburgers at once.

## Installation

Go to [https://nodejs.org](https://nodejs.org)

## The famous "Hello World"

If the following script is save in `index.js`

```js
console.log("Hello World");
```

```sh
❯ node index.js                                                                                                                                                                                    Hello World
```

0.30% of Node.

## Code modules

## Modularity

## Callbacks

## Asynchronous events

## NPM

## Kickstarter: HTTP server in node

## Rocket Launcher: Express!

## Deep diving

* [Teach Yourself Node.JS in 10 Steps](http://ponyfoo.com/articles/teach-yourself-nodejs-in-10-steps)
* [a short introduction to node.js](https://github.com/maxogden/art-of-node#the-art-of-node)
* [how to write node programs with streams](https://github.com/substack/stream-handbook)
* [Migrating from PHP to Node.js](https://medium.com/get-outside/migrating-from-php-to-node-js-522768ac482a)
* [How to Create and Publish Your First Node.js Module](https://medium.com/@jdaudier/how-to-create-and-publish-your-first-node-js-module-444e7585b738)
* [Node.js v4.0.0 — Node at its best](https://medium.com/@nodesource/node-js-v4-0-0-node-at-its-best-54a93fd2e0c6)
* [My 7 Node.js mantras](https://medium.com/@c2c/my-7-node-js-mantras-edd6c148e8dc)
* [The Node Beginner Book](http://www.nodebeginner.org/)
* [Introduction to Express](http://code.tutsplus.com/tutorials/introduction-to-express--net-33367)
* [Number don't lies](http://i.imgur.com/KCkIkcY.jpg)
* [Node Has Arrived](http://i.imgur.com/qrhh5Xk.jpg)
* [Simple NodeJS Application Examples](https://github.com/sourceful/learn-nodejs)
* [How the V8 engine works?](http://thibaultlaurens.github.io/javascript/2013/04/29/how-the-v8-engine-works/)
