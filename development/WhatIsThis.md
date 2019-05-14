# what Is This in JavaScript?

Let's talk about the `this` keyword in JavaScript. The concept of the `this` keyword can be very confusing for young developers and sometimes even experienced developers. But before we dive into `this` we must first understand that `this` behaves a little differently in JS than in other programming languages. In JavaScript, the value of `this` is determined by it's lexical scope. So for those who don't know let's define what a lexical scope or whether in strict mode or not,

## Closure

A closure in JavaScript can be represented by two different types, the global namespace and the lexical context. The global space is where we access things like the DOM (Document Object Model), using the `document` or `window` keywords. Let's further explain this with a code example.

```
function Person(pname) {
    var name = pname; // name is a local variable used by the Person function
    function getName () { // getName is an inner function, this is a closure
        console.log(name); // logs the variable name supplied by parent function to the console
    }
    getName();
}
Person();
```

Within the example above, `Person()` creates the local variable, `name`, and an inner function, `getName()`, that is defined within the `Person()` function and is only available within it. The `getName` function does not have any variables of it's own, it's only job is to display the variable supplied to it from it's parent. As for the variable `name` it is only available to it's children and it doesn't pollute the global environment. If we were to run this code we would see that the `console.log` successfully runs with the variable `name` that is stated within the parent's scope. This shows us how *lexical scoping* works.

For more information check out [Mozilla's Documentation](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Closures).

## Let's Talk About This

Now that we've dealt a little with lexical scoping and closures, we'll dive more into the `this` keyword. As stated before, the value of `this` is mostly determined by the context of the environment that it's declared in and how it's called. We must remember that `this` cannot be assigned during execution, and it could change each time that it's called.

### Global Context
```
console.log(this === window); // true
console.log(this.document === document); // true
this.a = 37;
console.log(this.a === 37); // true
```
In the global context the `this` refers to the global object whether we're in strict mode or not.

### Inside a Function

If `this` is called inside a function, it's value depends on *how* it's called within the function.

#### Simple Call
```
// Not in strict mode
function f1() {
    return this;
}
/* Since strict mode isn't set and 'this' isn't set by the call
'this' will default to the global object */
console.log(f1() === window);
```
Since the preceding code wasn't in strict mode and the value of `this` was not set by the call the value defaults to it's global object. On the other hand, In the following code, we see that when we are in strict mode and the value is still unset by the call, the value of `this` is now `undefined`.

```
// Strict Mode Enabled
function f2() {
    'use strict';
    return this;
}
// In strict mode, 'this' remains whatever it is when entering the execution context
console.log(f2() === undefined); // 'this' is undefined
```

#### The `bind` Method

ES5 introduced 'Function.prototype.bind'. Calling
'f.bind(someObject)' creates a new function with the same
body and scope as 'f', but where 'this' occurs in the
original function, in the new function it is permanently
bound to the first argument of 'bind', regardless of How
the function is being used.

ES5 introduced us to `Function.prototype.bind`. Calling `f.bind(something)` creates a new function with the same body and scope as `f`, but where `this` occurs in the original function, in the new function it is permanently bound to the first argument of `bind`, no matter how it's being used.

```
function f() {
    return this.a;
}
var g = f.bind({a: 'azerty'});
console.log(g()); //azerty

var h = g.bind({a: 'yoo'}); // bind only works once
console.log(h()); //azerty

var o = {a: 37, f: f, g: g, h: h};
console.log(o.f(), o.g(), o.h()); // 37, azerty, azerty
```

We must take note that when we use `bind` on a function to bind the `this` keyword, then `this` will __always__ be in the context of it's parent, and no longer will be you be able to use this in any other way inside that function.

References:
- [Closures](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Closures).
- [`this`](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Operators/this).

If this explanation was helpful (or not), please comment below how so, or how it can be improved upon. Thank You.