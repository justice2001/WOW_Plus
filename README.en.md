# WOW.js Plus

Language: [中文](README.md) | [English](README.en.md)

Temporary deprecation:
======================

wow.js is temporarily deprecated in favour of AOS (Animate on Scroll). Feel free to ignore the warning if you can't use AOS.

Plans for 3.0 include:

* Breaking out the shims into an optional module
* Using the AOS approach for most functionality
* Remain completely backwards compatible and a drop-in replacement for GPL wowjs, but issue warning on durations of higher granularity than 50ms
  or longer than 3s
* Detect Firefox for Android as mobile.


Reveal CSS animation as you scroll down a page.
By default, you can use it to trigger [animate.css](https://github.com/daneden/animate.css) animations.
But you can easily change the settings to your favorite animation library.

Advantages:
- 100% MIT Licensed, not GPL keep your code yours.
- Naturally Caffeine free
- Smaller than other JavaScript parallax plugins, like Scrollorama (they do fantastic things, but can be too heavy for simple needs)
- Super simple to install, and works with animate.css, so if you already use it, that will be very fast to setup
- Fast execution and lightweight code: the browser will like it ;-)
- You can change the settings - [see below](#advanced-usage)

### [LIVE DEMO ➫](https://graingert.co.uk/WOW/)

## Live examples
- [MaterialUp](http://www.materialup.com)
- [Fliplingo](https://www.fliplingo.com)
- [Streamline Icons](http://www.streamlineicons.com)
- [Microsoft Stories](http://www.microsoft.com/en-us/news/stories/garage/)


## Documentation

It just take seconds to install and use WOW.js!
[Read the documentation ➫](https://graingert.co.uk/WOW/docs.html)

### Plus Edition Feature

#### Animation Order

Use Count To Define Animation LoadingOrder

- Demo

```html
<section class="animation__animated animation__fadeIn wow" data-wow-order="1"></section>
<section class="animation__animated animation__fadeIn wow" data-wow-order="2"></section>
<section class="animation__animated animation__fadeIn wow" data-wow-order="3"></section>
```

let 3 section show animation In turn

- Interval Config

```js
new WOW({
  orderDuration: 400
}).init()
```

change order interval timing to 400ms

### Dependencies
- [animate.css](https://github.com/daneden/animate.css)

### Installation

- Bower

```bash
   bower install wow-mit
```

- NPM

```bash
   npm install wow.js
```

### Basic usage

- HTML

```html
  <section class="wow animate__animated animate__slideInLeft"></section>
  <section class="wow animate__animated animate__slideInRight"></section>
```

- JavaScript

```javascript
new WOW().init();
```

### Advanced usage

- HTML

```html
  <section class="wow animate__animated animate__slideInLeft" data-wow-duration="2s" data-wow-delay="5s"></section>
  <section class="wow animate__animated animate__slideInRight" data-wow-offset="10"  data-wow-iteration="10"></section>
  <section class="wow animate__animated animate__slideInRight" data-wow-order="1"  data-wow-iteration="10"></section>
  <section class="wow animate__animated animate__slideInRight" data-wow-order="2"  data-wow-iteration="10"></section>
```

- JavaScript

```javascript
var wow = new WOW(
  {
    boxClass:     'wow',      // animated element css class (default is wow)
    animateClass: 'animated', // animation css class (default is animated)
    offset:       0,          // distance to the element when triggering the animation (default is 0)
    mobile:       true,       // trigger animations on mobile devices (default is true)
    live:         true,       // act on asynchronously loaded content (default is true)
    callback:     function(box) {
      // the callback is fired every time an animation is started
      // the argument that is passed in is the DOM node being animated
    },
    scrollContainer: null,    // optional scroll container selector, otherwise use window,
    resetAnimation: true,     // reset animation on end (default is true)
    orderDuration: 200,       // order interval timing (ms)
  }
);
wow.init();
```

### Asynchronous content support

In IE 10+, Chrome 18+ and Firefox 14+, animations will be automatically
triggered for any DOM nodes you add after calling `wow.init()`. If you do not
like that, you can disable this by setting `live` to `false`.

If you want to support older browsers (e.g. IE9+), as a fallback, you can call
the `wow.sync()` method after you have added new DOM elements to animate (but
`live` should still be set to `true`). Calling `wow.sync()` has no side
effects.


## Contribute

The library is transpiled using Babel, please update `wow.js` file.

We use grunt to compile and minify the library:

Install needed libraries

```
npm install
```

Get the compilation running in the background

```
grunt watch
```

Enjoy!

## Bug tracker

If you find a bug, please report it [here on Github](https://github.com/graingert/WOW/issues)!

## Developer

Originally Developed by Matthieu Aussaguel, [mynameismatthieu.com](http://mynameismatthieu.com)
Forked to remain under the MIT license by Thomas Grainger, https://graingert.co.uk
Plus Edition By Zhengyi_OvO [https://blog.mczhengyi.top](https://blog.mczhengyi.top)

+ [Github Profile](//github.com/graingert)

## Contributors

Thanks to everyone who has contributed to the project so far:

- Attila Oláh - [@attilaolah](//twitter.com/attilaolah) - [Github Profile](//github.com/attilaolah)
- [and many others](//github.com/graingert/WOW/graphs/contributors)

Initiated and designed by [Vincent Le Moign](//www.webalys.com/), [@webalys](//twitter.com/webalys)
