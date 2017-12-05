# JavaScript / Typescript Style Guide() {
Style Guides, snippets, and utilities

## <a name="js"></a>Javascript / Typescript

Key Sections:

* [Comparison Operators & Equality](#comparison)

## <a name="comparison"></a> Comparison Operators & Equality

[Reference: Truth equality and javascript](https://javascriptweblog.wordpress.com/2011/02/07/truth-equality-and-javascript/#more-2108)  
[Reference: Airbnb Style Guide - Comparison](https://github.com/airbnb/javascript#comparison-operators--equality)


### Booleans, Strings, and Numbers

Use shortcuts for booleans, but explicit comparisons for strings / numbers.

> Why? Using shortcuts for strings / numbers can get you into sticky situations with ``''`` and ``0`` results.

#### Booleans

```javascript
// bad
if (isValid === true) {
  // ...
}

// good
if (isValid) {
  // ...
}
```

#### Strings
```javascript

// bad
if (name) {
  // ...
}

// good
if (name !== '') {
  // ...
}
```

#### Numbers

```javascript
// bad
if (collection.length) {
  // ...
}

// good
if (collection.length > 0) {
  // ...
}
```

### Null and Undefined

Use truthy check for objects being null or undefined

> Why? These methods may be shadowed by properties on the object in question - consider { hasOwnProperty: false } - or, the object may be a null object (Object.create(null)).

```js
// bad
if (error === null) {
  // ...
}

// good
if (error) {
  // ...
}
```

#### Null is Bad
[Reference: Null vs Undefined](https://github.com/basarat/typescript-book/blob/master/docs/styleguide/styleguide.md#null-vs-undefined)  
[Reference: Null is Bad](https://github.com/basarat/typescript-book/blob/master/docs/tips/null.md)