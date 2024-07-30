## Closures

### Understanding Scopes
JavaScript primarily operates with two types of scopes:

* **Global Scope:** Variables defined outside functions. They are accessible from anywhere within the code.
* **Local Scope:** Variables defined within functions. Their accessibility is limited to the function itself.

### Closure
A closure is a function that has access to variables from its outer (enclosing) function, even after the outer function has returned.

**Code Example:**

```javascript
function outerFunction() {
  let outerVariable = "I'm from outer function";

  function innerFunction() {
    console.log(outerVariable); // Accessing outerVariable
  }

  return innerFunction;
}

let myClosure = outerFunction();
myClosure(); // Output: "I'm from outer function"
```

### Breakdown
1. **Outer Function:**
   * Declares a variable `outerVariable`.
   * Defines an inner function `innerFunction` that accesses `outerVariable`.
   * Returns `innerFunction`.
2. **Assignment:**
   * Assigns the returned `innerFunction` to `myClosure`.
3. **Invocation:**
   * Calls `myClosure()`, which executes the `innerFunction`.

### Key Points
* The `innerFunction` forms a closure, retaining access to `outerVariable` even after `outerFunction` returns.
* Calling `myClosure()` effectively invokes the `innerFunction` in the closure's context.

**In essence,** closures provide a way to maintain data privacy and create functions with specific contexts.