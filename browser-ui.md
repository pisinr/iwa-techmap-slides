## How do you do UI?

* VanillaJS
* Angular
* React

^^^

## VanillaJS

* Just plain javascript. (<small>*with a bit of Babel</small>)
* Use `querySelector`, `createElement` and `fetch`.
  * No need for jQuery
* Only way if you want progressive enhancement.
  * BTW, give up trying to progressively enhance SPA.

^^^

## React

* View UI Library
* Virtual DOM
  * You can mindlessly re-render everything.
  * The virtual DOM engine will reconcile the change.
* Need other libraries

^^^

## Angular

* Complete Framework for App development
  * Include DI system, testing and HTTP client
* Can compile to WebComponent
* Almost direct DOM manipulation

---

## Common JS lib.

* momentjs/js-joda
* numeral
* lodash

^^^

```javascript
// "4 years ago"
moment().add(-4, 'years').fromNow()

// "1,200.00"
numeral('1,000').add(200).format('0,0.00')

// { a: 1, c: 3 }
_.pick({a: 1, b: 2, c: 3}, ['a', 'c'])

```