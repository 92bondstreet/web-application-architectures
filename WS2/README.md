# superhero.js

## Intro

*La cote Argus* is a reference for used vehicles prices for professionals and the general public.

Very useful to check if a classified ad is a good deal. You could use the free website [lacentrale.fr](http://www.lacentrale.fr/lacote_origine.php)

In France, [leboncoin.fr](http://www.leboncoin.fr/) is the website leader of classified ad: minimalist UX and UI without registry.

## Workshop in 1 sentence

**Determine the "Cote Argus" of a given car from its leboncoin.fr classified ad.**

## How to do that?

By creating a link between [leboncoin.fr](http://www.leboncoin.fr/), [lacentrale.fr](http://www.lacentrale.fr/lacote_origine.php) and the end-user.

## Stack

```txt
node.js + NPM + Material Design (mdl, bootstrap...) + Vanilla JS
```

## Steps and exercises

### Step 1 - Classified ad car definition

What are the given properties for a car ad: brand, models, km...

For example: http://www.leboncoin.fr/voitures/852693116.htm?ca=12_s


#### Exercise 1

```txt
Define the JSON schema for a car leboncoin.fr classified ad.
```

Example of JSON Schema: [Basic example](http://json-schema.org/examples.html)

### Step 2 - "La Cote Argus"

What are the car properties we need to provide to lacentrale.fr](http://www.lacentrale.fr/lacote_origine.php).

#### Exercise 2

```txt
Define the JSON schema to determine the Code Argus for a given car.
```

### Step 3 - UX/UI

How to create a connexion between the leboncoin ad and lacentrale?

#### Exercise 3

```txt
Write a User Flow
```

### Step 4 - require('leboncoin')

Create a module called `leboncoin`


#### Exercice 4

```txt
From the ad url, scrap the webpage and return the car properties in JSON format.
```

### Step 5 - require('lacentrale')

Create a module called `lacentrale`.


#### Exercice 5

```txt
From a car JSON object, determine "La Cote Argus".
```


### Step 6 - node app.js

Build the node server.

#### Exercice 6

```txt
Build the Node server with Express.
```

### Step 7 - UX/UI

Let's go for the Web App !!

#### Exercice 7

```txt
From a leboncoin car ad url, determine "La Cote Argus" and give a feedback to the user about the deal (good or not).
```

#### Exercice 8

```txt
From a leboncoin car search (example: http://www.leboncoin.fr/voitures/offres/ile_de_france/hauts_de_seine/?f=a&th=1&pe=33&rs=2005&me=100000&q=lexus), determine "La Cote Argus" for all given ads and give a feedback to the user about the deal (good or not).
```
