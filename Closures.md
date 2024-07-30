## Closures with Image (Markdown)

**Closures**

Let's explore closures in JavaScript. Here's a breakdown:

**Scopes:**

In JavaScript, there are two main types of scopes:

* **Global Scope:** Variables defined outside functions are accessible to any function within the same scope.
* **Local Scope:** Variables defined inside functions are only accessible by that specific function.

**Understanding Closures:**

A closure is a function that has access to variables from its outer (enclosing) function, even after the outer function has returned. 

Here's an example:

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
```

**Explanation:**

1. `outerFunction` creates a variable `outerVariable`.
2. It defines an inner function `innerFunction`.
3. `innerFunction` accesses `outerVariable` even though it's defined in a different scope.
4. `outerFunction` returns `innerFunction`.
5. `myClosure` stores the returned function.
6. Calling `myClosure()` executes `innerFunction`, which can still access `outerVariable` due to the closure.

**Image:**

[Image of Closure](https://ibb.co/G2YfrXH)

**In summary:**

Closures are powerful tools for creating private variables and functions within functions. They are used extensively in JavaScript for various functionalities.