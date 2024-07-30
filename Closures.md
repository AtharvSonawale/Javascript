## Closures

Let me tell the thing about Closure, basically there a two main types of scopes in Javascript.

Now a scope is the thing that write within the curly braces i.e {}.

Global Scope: Variables are defined outside the functions.
Global scope is a scope which contains variables that can be accessed by any function inside the scope.

Local Scope: Variables are defined inside the functions.
Local scope is a scope which contains variables that can only be accessed by the function itself.

Here's a code-implemention of Closure:

```javascript
function outerFunction() {
  let outerVariable = "I'm from outer function";
  console.log(typeof.outerVariable)

  function innerFunction() {
    console.log(outerVariable); // Accessing outerVariable
  }

  return innerFunction;
}

let myClosure = outerFunction();
myClosure(); // Output: "I'm from outer function"
```

Firstly there's a function named "outerFunction", then there's an initialization of a string variable named "outerVariable" it also contains a function inside itself named "innerFunction"

Inside function innerFunction there's a console.log method that logs a message to the console, in this case it is the outerVariable

Nextly, it contains a return statement, here it is innerFunction, i.e the return argument of outerFunction is the function innerFunction which logs out the variable outerVariable.

Now a variable named "myClosure" is declared and it contains the return value of outerFunction which has an another nested function innerfunction.

And lastly, myClosure() is the act of calling or executing that inner function.

and thats all.

![Alt text](https://ibb.co/G2YfrXH)