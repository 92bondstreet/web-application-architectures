# HOW WEB (APP) WORKS ?

> What happens when you type a website address in your browser?

## What is Web ?

### The Surfer

In 2014, Around 40% of the world population (3 billions) using Internet in 2014.

We know how to use Internet everyday:

* A device as desktop, laptop, smartphone, tablet, watch...
* Internet connection: via a subscribed provider, a wifi connection...
* Open a browser with a specific website address
* or Proceed a google search
* or Send a message with Gmail, Facebook, Twitter, Instagram...
* or buy the last bestseller on Amazon

But do you know really how Internet works ?

### The Wire

**Disclaimer**

> Internet is not {a, in, the} cloud

The cloud is not Internet. The cloud is a new stack technology for on-demand network and storage access.

**Internet is a wire.**

Internet is a wire between servers that are directly connected to Internet.

Each server is identified by an address called IP (Interner Protocol).

Example:

* google.fr is `216.58.208.227`
* github.com is `192.30.252.130`
* leboncoin.fr is `193.164.197.82`
* esilv.fr is `194.254.135.68`

Each server can speak to each other using a protocol called TCP/IP

### The Rules

TCP/IP defined a set of rules to allow server and devices to send information and understand them.

Internet talk.

### The Client

At home, the device is called **Client** because it's not directly connected to internet.

The device needs a provider (as Free, Orange...) called ISP.

### The DNS

Of course, a french Surfer doesn't call the Google IP `216.58.208.227` to perform a research but a name google.fr.

The DNS is the link between the (website) name and the IP address.

The DNS check the browser and OS cache dictionary to find the IP address before to call the Resolver.

### The Resolver

The resolver is used by your provider. It knows just one thing: where to locate the calling server with the Root server helping (Currently 13 roots in Internet World).

### The Message

When the Client wants to send an email, he has to connect to the Inbox server, Gmail for example, through its provider.

He write email to recipient, the the provider dispatch the message to the recipient Inbox mail.

### The Packet

The message information is splitted in small pieces called packets.

Once received, the packets are reassembled to the initial message.

Image, mails, posts, tweets, videos... are sent packet by packet to the recipient.

### The Router

Imagine the results of a mix of packets between clients in same area or classroom:

* the teacher, surfing on [medium.com](http://medium.com), to illustrate a course speech
* student, post on Facebook a message about the teacher.

How to avoid that the teacher catch on his screen a message as "The teacher is boring. Please help me"?

**Thanks to the Router**

Everything connected directly or indirectly has an IP address: server, client, smartphone, any equipment between devices.

Routers help packages to find the path between you (the IP origin) and the IP destination and vice-versa for the response.

## What is Web App ?

App is a shortcut for Application.

Traditionally, Application were available, developed and designed only on and for desktop. We call them programs or software.

Today, Web Application run in the web browser and provide a rich and full interactive experience.

A new software was born: SAAS

> Software As A Service

### Static vs Dynamic

Before, to use Web Application, The Surfer used Web Site.

The experience was a static content and passive interaction: gallery, blog.

Today, The Surfer is an active resident in the World Wide Web: (awesome) games, Photo editor, Maps, Youtube, Market place as Amazon... etc.

The Surfer could interact with a map, for example, by zooming, panning, searching...

The Web Application focus to a single task: provide a map, send images to friends inside his network, etc...

### Data anywhere

The Surfer can access his photos, mails, any data when he needs and when he wants.

All the data is stored on the web. We could access them across different devices.

### App up to date

Web Application are always updated.

No need to update or install a new version manually.

### Everywhere

* A Web Application is available for you all devices (PC, Mac, smartphone, tablet). Do you remember that many programs written for PC don't work for Mac ?
* Anyone can reach the Web Application from any browser. It means on my tablet or a friend's laptop.
* Web Application is separated of the user computer. The Web App codebase don't overall the performance on the computer or insatll viruses, malware or spyware.

## Deep diving

* [How the Internet Works in 5 Minutes](https://www.youtube.com/watch?v=7_LPdttKXPc)
* [How DNS works](https://howdns.works/)
* [20 things I learned about browsers ans the web](http://www.20thingsilearned.com/en-US)
* [So, You Want to Be a Front-End Engineer?](https://speakerdeck.com/dmosher/so-you-want-to-be-a-front-end-engineer)
