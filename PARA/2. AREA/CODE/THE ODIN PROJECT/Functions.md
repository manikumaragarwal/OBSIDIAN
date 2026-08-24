
Tags: [[CODING]] [[THE ODIN PROJECT]]

---

# JavaScript Functions Quick Reference

## 🏗️ Two Main Types

### Function Declaration

```javascript
function myFunc() {
  return "hello";
}
myFunc(); // Can call before declaration (hoisted)
```

- **Hoisted** (available before declaration)
- **Must be named**
- Use when: Need function available throughout scope

### Function Expression

```javascript
const myFunc = function () {
  return "hello";
};
myFunc(); // Can only call after declaration
```

- **Not hoisted** (only variable is hoisted)
- **Can be anonymous or named**
- Use when: Want control over when function becomes available

## 🏹 Arrow Functions (Always Expressions)

```javascript
const add = (a, b) => a + b;
const greet = (name) => `Hello ${name}`;
const complex = (x, y) => {
  const result = x + y;
  return result * 2;
};
```

- Always anonymous
- No `this` binding (inherits from parent)
- Cannot be constructors

## 🎯 Function vs Method

```javascript
// Function (independent)
function greet() {
  return "Hello";
}

// Method (part of object)
const person = {
  name: "Alice",
  greet: function () {
    return `Hello ${this.name}`;
  },
};
```

**Method** = function that's a property of an object

## 🔄 Common Patterns

### Callbacks

```javascript
setTimeout(function () {
  console.log("done");
}, 1000);
arr.map((x) => x * 2);
button.onclick = () => alert("clicked");
```

### IIFE (Immediately Invoked Function Expression)

```javascript
(function () {
  console.log("runs immediately");
})();
```

### Higher-Order Functions

```javascript
function createMultiplier(n) {
  return function (x) {
    return x * n;
  };
}
const double = createMultiplier(2);
```

### Named Function Expression

```javascript
const myFunc = function namedFunc() {
  // namedFunc only available inside function
  // Useful for debugging and recursion
};
```

## 🌍 Scope Quick Facts

- **Global**: Accessible everywhere
- **Function**: Accessible within function only
- **Block**: `let`/`const` respect `{}`, `var` doesn't
- **Closure**: Inner functions remember outer variables

```javascript
function outer() {
  let x = 1;
  return function inner() {
    return x; // Remembers x even after outer() ends
  };
}
```

## ⚡ Hoisting Behavior

```javascript
// This works (declaration hoisted)
sayHi(); // "Hi"
function sayHi() {
  return "Hi";
}

// This fails (only variable hoisted, not function)
sayBye(); // TypeError
var sayBye = function () {
  return "Bye";
};
```

## 🚨 Common Gotchas

### Arrow Function `this`

```javascript
const obj = {
  name: "Alice",
  greet: () => console.log(this.name), // undefined! (inherits global this)
};

// Use regular function for methods
const obj = {
  name: "Alice",
  greet: function () {
    console.log(this.name);
  }, // "Alice"
};
```

### Loop Callbacks with `var`

```javascript
// Wrong - all buttons log same number
for (var i = 0; i < 3; i++) {
  buttons[i].onclick = function () {
    console.log(i);
  }; // Always 3
}

// Fix 1: Use let
for (let i = 0; i < 3; i++) {
  buttons[i].onclick = function () {
    console.log(i);
  }; // 0, 1, 2
}

// Fix 2: Use closure
for (var i = 0; i < 3; i++) {
  buttons[i].onclick = (function (index) {
    return function () {
      console.log(index);
    };
  })(i);
}
```

## 📋 Quick Decision Guide

| Need                                 | Use                                |
| ------------------------------------ | ---------------------------------- |
| Function available anywhere in scope | Declaration                        |
| Conditional function creation        | Expression                         |
| Callback/event handler               | Arrow (if no `this` needed)        |
| Object method                        | Regular function                   |
| Short transformation                 | Arrow function                     |
| Constructor function                 | Declaration/Expression (not arrow) |
| Immediate execution                  | IIFE                               |




---
[[THE ODIN PROJECT]]
[[Javascript]]
[[CODING]]