# Vanilla JavaScript Projects :coffee:

## Introduction
During the first four weeks of the bootcamp, we learned how to code with JavaScript using the NodeJS platform. But as you probably know, [JavaScript's beginnings were in the browser, in 1995](https://en.wikipedia.org/wiki/JavaScript#Beginnings_at_Netscape). At that time, personal computers were starting to become more powerful and there was a realization that **the web needed to become more dynamic**.

Before that time, web browsers were quite dumber than they are now. A browser would receive an HTML page from a web server -- either dynamically created or as a static file -- and [render the page](http://www.pathinteractive.com/blog/design-development/rendering-a-webpage-with-google-webmaster-tools/), making additional requests for every `<img>` element therein. After rendering a page, the possible interactions were limited:

* The user clicks on an `<a>` (anchor) element on the page, making the browser issue a **`GET`** request to the URL specified in the `href` attribute of the anchor, effectively loading another page
* The user fills out a `<form>` and submits it, making the browser issue either a **`GET`** or **`POST`** request -- depending on the `method` attribute of the `<form>` -- to the URL specified in the `action` attribute of the form. This would also result in another page load.

*(This method of creating web sites and rendering them is exactly how you built your [Reddit Clone Project](https://github.com/DecodeMTL/node-express-reddit-clone), using NodeJS, Express and Pug on the server side. In this model, the browser did very little.)*

This was fine for a while but with the advent of JavaScript in browsers in 1995, things would dramatically change. Browser JavaScript is the same language you learned while studying NodeJS, but it offers dynamic functionality that is meant for the browser.

While NodeJS gives you modules to [access the computer's file system](https://nodejs.org/api/fs.html), [create HTTP servers](https://nodejs.org/api/http.html), [lower level socket servers](https://nodejs.org/api/net.html), and a [huge library of modules](http://npmjs.com/) to [connect to databases](https://www.npmjs.com/package/mysql), [read the keyboard](https://www.npmjs.com/package/prompt) and even [control robots](https://www.npmjs.com/package/johnny-five), browser JavaScript gives you:

* **[The DOM](http://htmldog.com/guides/javascript/intermediate/thedom/)**: the DOM -- Document Object Model -- is accessible using the globally predefined `document` variable. It is a representation of the HTML document that your browser has rendered as a **tree of JavaScript objects**. With the DOM, you can change any part of an already rendered web page by writing code inside a `<script>` tag using the JavaScript language you already know.
* **[Events and Callbacks](http://htmldog.com/guides/javascript/intermediate/events/)**: through the DOM, you can make a page dynamic by *listening* to various events. You can execute callback functions on page load, page scroll, mouse move, mouse click, keyboard input and many more.
* **[AJAX](http://htmldog.com/guides/javascript/intermediate/ajax/)**: AJAX -- Asynchronous JavaScript And XML -- has become a buzzword over the years. It refers to a functionality that allows you to *dynamically make HTTP requests using JavaScript code* in a `<script>` tag, *without reloading the page*.

Throughout the years, various APIs were added to browser JavaScript allowing us to do things like [drawing on a web page](http://htmldog.com/guides/javascript/advanced/canvas/), [store user information in the browser](http://htmldog.com/guides/javascript/advanced/localstorage/), and [manipulate the browser history](https://developer.mozilla.org/en-US/docs/Web/API/History_API) to name a few. Together, this set of functionalities allows us to build things like Gmail, Netflix, Google Maps and pretty much any application we can imagine, all running inside a web browser. It is this set of functionalities that allows Facebook and Twitter to show you notifications without having to refresh the page. Same thing for upvoting things on Reddit while staying in place.

They are collectively referred to as ["Vanilla JS"](http://vanilla-js.com/), in contrast with the [many](https://angularjs.org/) [frameworks](http://emberjs.com/) and [libraries](https://jquery.com/) that are built on top of them. In this course, we will be looking at two libraries built on top of browser JavaScript:

* **[jQuery](https://jquery.com/)**: jQuery was created as a response to a huge problem at the time, namely the discrepancy between JavaScript implementations in browsers. It provided a unified API to access the DOM, events, AJAX and more without having to worry about browser differences.
* **[React](https://facebook.github.io/react/)**: React is a user interface library that was created as a response to the difficulty of managing big browser-based applications using the primitive Vanilla JS functions. It turns out that manipulating the DOM directly using the `document` object is error prone at scale, and becomes quickly unmanageable. React tries to solve this problem in a *declarative manner*, "similar to SQL". Rather than calling DOM functions to manipulate the content of a page, React allows us to define user interface components in a declarative way, and automatically takes care of calling the appropriate DOM functions. The similarity to SQL lies in the fact that we never have to tell an SQL database *how* we want things to be computed, but simply what to compute. Think of it as the difference between `ORDER BY createdAt DESC` and `data.sort(function(a, b) {...})`.

## Projects
Before learning any of these libraries, we will work on getting familiar with Vanilla JavaScript. Since everything is built on top of it, it will pay off to know how it works. In order to do this, we will be building three front-end projects that run completely in the browser. In these projects, our web server's only role will be to produce a static `index.html` file that contains a `<script>` tag *where everything will happen*. One implication of this is that search engine crawlers like Google Bot will not be able to view the content of our applications, since *everything will happen after the page has loaded*, long after the HTTP request/response cycle has ended.

### Weather application
We will start by building a first project **together**. It will be a simple weather application that asks the user for their city, and dynamically displays a weather box with the current temperature, basic weather conditions as well as an icon representing the current state of things.

### Flickr browser
Even though Flickr already has an excellent web app to browse photos, we will use the Flickr API to create an infinitely scrolling browser based on a search word.

### Custom Reddit browser
In week two, you built a [command-line Reddit browser](https://github.com/DecodeMTL/reddit-cli-project) using the Reddit JSON API. Here we will use the same API through AJAX and the DOM in order to create a simple but custom browser-based reddit app.

----------
## Project 1: Weather App
TODO

----------
## Project 2: Flickr Browser
TODO

----------
## Project 3: Custom Reddit Browser
TODO

