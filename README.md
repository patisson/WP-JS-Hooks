# WP-JS-Hooks
A lightweight JavaScript event manager for WordPress

### Introduction
See core ticket [#21170](http://core.trac.wordpress.org/ticket/21170) and our [WordSesh talk](http://www.youtube.com/watch?v=oEF7EBjZ-kE).

### API Usage
API functions can be called via the global `wp.hooks` like this `wp.hooks.addAction()`, etc.

* `addAction( 'tag', callback, priority )`
* `addFilter( 'tag', callback, priority )`
* `removeAction( 'tag', callback )`
* `removeFilter( 'tag', callback )`
* `doAction( 'tag', arg1, arg2, etc )`
* `applyFilters( 'tag', content )`

### Features
* Fast and lightweight, ~1.5kb
* Vanilla JS with no dependencies
* Hooks with lower integer priority are fired first.
* Uses native object hash lookup for finding hook callbacks.
* Utilizes insertion sort for keeping priorities correct. Best Case: O(n), worst case: O(n^2)
