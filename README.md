# GSC Javascript Styleguide
This repo holds code samples and commonly used functions that can be grabbed and used on all of our internal projects. The guide itself serves as a quick reference for GSC developers looking to make sure their JavaScript matches GSC's coding standards.

This is anything but an exhaustive reference for all things JavaScript. When in doubt, make sure your JavaScript passes JSLint validation. We also recommend that you fill in any holes here (of which there are many) with the [excellent JavaScript styleguide](https://github.com/airbnb/javascript) put together by the folks at AirBnB.

## <a name="table-of-contents">Table of Contents</a>
1. [Comments](#comments)
2. Whitespace
3. Foo
4. 

## <a name="comments">Comments</a>
- **<a href="#1.1">1.1 Single-Line</a><a name="user-content-1.1"></a>** Use `//` for single-line comments. Place a newline above the comment, and place the comment directly above the code block being annotated.

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

- [1.2 Multi-Line](#1.2) For multi-line comments, use `/** ... */`. Describe the code block, and include types and values for all parameters and any return values. See [JS Doc](http://usejsdoc.org/) for types.

  **Bad**
  ```javascript
  //  This function doesn't do anything yet, but
  //  I feel inclined to write comments about it
  //  just as an example
  function knowNothing(stuff) {
    // ... stuff ...
    return something;
  }
  ```

  **Good**
  ```javascript
  /**
   *  This function doesn't do anything yet, but
   *  I feel inclined to write comments about it
   *  just as an example
   *
   *  @param {String} stuff
   *  @return {Object} something
   */
  function knowNothing(stuff) {
    
    // ... stuff ...
    
    return something;
  }
  ```
- [1.3 Comment Length](#1.3) Keep comments concise, generally to 7-10 words per line. Also, avoid adding comments where the code is self explanatory. In general, however, it is better to err on the side of commenting too much than not enough.

  **Bad**
  ```javascript
  // add the two integers together, then multiply them, then divide them, and finally write to the console for debugging
  var grumbling = ((pug1 + pug2) * 2) / 0.5;
  console.log(grumbling);
  ```
  
  **Good**
  ```javascript
  // create a group of pugs
  var grumbling = ((pug1 + pug2) * 2) / 0.5;
  console.log(grumbling);
  ```
- [1.4 To Do](#1.4) Flag code that should be fixed or improved with `TODO`.

  ```javascript
  // TODO: clean up variable declarations
  var officeDogs = array('Charlie', 'Mia', 'Duke', 'Ninja', 'Butters');
  var daysOfWeek = array('M', 'T', 'W', 'Th', 'F');
  var beersOnTap = array('Titan IPA' => 'Great Divide', 'Unfiltered Wheat' => 'Boulevard');
  ```
