# GSC Javascript Styleguide
This repo holds code samples and commonly used functions that can be grabbed and used on all of our internal projects. The guide itself serves as a quick reference for GSC developers looking to make sure their JavaScript matches GSC's coding standards.

This is anything but an exhaustive reference for all things JavaScript. When in doubt, make sure your JavaScript passes JSLint validation. We also recommend that you fill in any holes here (of which there are many) with the [excellent JavaScript styleguide](https://github.com/airbnb/javascript) put together by the folks at AirBnB.

## <a name="table-of-contents">Table of Contents</a>
1. [Comments](#comments)
2. Whitespace
3. Foo
4. 

## <a name="comments">Comments</a>
- 1.1 Use `//` for single-line comments. Place a newline above the comment, and place the comment directly above the code block being annotated.

**Bad**
```javascript
var mia = 'german shepherd'; // breed of my dog

function capitalize(str) {
  // untested, but should capitalize first letter of each word
  return str.charAt(0).toUpperCase() + str.slice(1);
}
// check if it worked
console.log(capitalize(mia));
```

**Good**
```javascript
// breed of my dog
var mia = 'german shepherd';

// untested, but should capitalize first letter of each word
function capitalize(str) {
  return str.charAt(0).toUpperCase() + str.slice(1);
}

// check if it worked
console.log(capitalize(mia));
```

- 1.2 For multi-line comments, use `/** ... */`. Describe the code block, and include types and values for all parameters and any return values. See [JS Doc](http://usejsdoc.org/) for types.

**Bad**
```javascript
var mia = 'German Shepherd'; // name of my dog
```

**Good**
```javascript
// name of my dog
var mia = 'German Shepherd';
```

// bad (no whitespace before comment)
function multiply (number) {
  number *= 2;
  return number;
}
// show number
alert(number);

// good
function multiply (number) {
  number *= 2;
  return number;
}

// show number
alert(number);
```
