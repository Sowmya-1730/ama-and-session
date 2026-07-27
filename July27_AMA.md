# JavaScript AMA – Questions & Answers

## 1. What is the difference between `==` and `===`?

### Answer:

Both are comparison operators, but they behave differently.

- `==` (Loose Equality)
  - Compares values after performing **type conversion (type coercion)** if needed.
  - Can produce unexpected results.

- `===` (Strict Equality)
  - Compares both **value and data type**.
  - No type conversion is performed.
  - Recommended in modern JavaScript.



## 2. What is the difference between `for...of` and `for...in`?

### Answer

| `for...of` | `for...in` |
|------------|------------|
| Iterates over values | Iterates over keys/indexes |
| Used with Arrays, Strings, Maps, Sets | Used mainly with Objects |
| Returns actual element | Returns property name or index |



## 3. What is String Interpolation?

### Answer

String interpolation is a way of embedding variables or expressions directly inside a string using **Template Literals**.

It uses:

- Backticks (`` ` ``)
- `${}` syntax




## 4. What are Decorators?

### Answer

Decorators are a feature that allows you to add extra functionality to classes or methods **without modifying their original code**.

Think of them as wrappers that enhance existing behavior.

> **Note:** Decorators are not officially part of standard JavaScript yet. They are commonly used in **TypeScript**, **Angular**, and frameworks like **NestJS**.


## 5. What is Callback Hell?

### Answer

Callback Hell occurs when multiple asynchronous callbacks are nested inside one another, making the code difficult to read and maintain.

### Example

```javascript
login(function() {
    getProfile(function() {
        getPosts(function() {
            getComments(function() {
                console.log("Done");
            });
        });
    });
});
```

This pyramid-like structure is called **Callback Hell** or the **Pyramid of Doom**.


## 6. What is the difference between `shift()` and `unshift()`?

### Answer

Both methods work on the beginning of an array.

| shift() | unshift() |
|----------|-----------|
| Removes first element | Adds element(s) at beginning |
| Returns removed element | Returns new array length |
| Modifies original array | Modifies original array |



## 7. What are the different ES6 features?

### Answer

ES6 (ECMAScript 2015) introduced many modern JavaScript features.

Some important ones are:

- `let` and `const`
- Arrow Functions
- Template Literals
- Destructuring
- Spread Operator (`...`)
- Rest Parameters
- Default Parameters
- Classes
- Modules (`import` / `export`)
- Promises
- Enhanced Object Literals
- for...of loop
- Map
- Set
- Symbols


## 8. Vikas Mehta: What is Prototype Chaining in JavaScript?

### Answer

JavaScript uses **Prototype-based Inheritance**.

Every object has a hidden link to another object called its **prototype**.

When JavaScript cannot find a property on an object, it automatically searches in its prototype, then in that prototype's prototype, and so on. This process is called **Prototype Chaining**.
