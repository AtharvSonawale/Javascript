Here's the markdown text file with the changes and image added:

````markdown
## Closures

Let me tell you about closures! In JavaScript, there are two main types of scopes:

**Scope** refers to the accessibility of variables within your code. It's defined by curly braces (`{}`).

* **Global Scope:** Variables defined outside of functions are accessible by any function within the same script.
* **Local Scope:** Variables defined inside of functions are only accessible by that specific function.

Here's a code example demonstrating closures:

```javascript
function outerFunction() {
  let outerVariable = "I'm from outer function";
  console.log(typeof outerVariable);

  function innerFunction() {
    console.log(outerVariable); // Accessing outerVariable
  }

  return innerFunction;
}

let myClosure = outerFunction();
myClosure(); // Output: "I'm from outer function"
````

**Explanation:**

1.  We define a function named `outerFunction`.
2.  Inside `outerFunction`, we create a variable named `outerVariable` and another function named `innerFunction`.
3.  `innerFunction` logs the value of `outerVariable`.
4.  The `outerFunction` returns `innerFunction`.
5.  We call `outerFunction` and store the returned function (the closure) in `myClosure`.
6.  Finally, calling `myClosure()` executes the inner function, which can still access the `outerVariable` even though `outerFunction` has already finished running.

**In essence, a closure is a function that remembers variables from its outer function's scope, even after the outer function has returned.**

![Closure](https://ibb.co/G2YfrXH)