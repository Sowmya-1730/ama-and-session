# AMA Questions & Answers

## 1. What is Polymorphism?

**Answer:** Polymorphism is an OOP concept where the same interface or
method can have different behaviors depending on the object. Examples
include method overriding (runtime polymorphism) and method overloading
(compile-time polymorphism, language-dependent).


## 2. In SOLID, what does **S** stand for?

**Answer:** **Single Responsibility Principle (SRP)**. A class should
have only one reason to change, meaning it should have one well-defined
responsibility.


## 3. What is the Event Loop in JavaScript?

**Answer:** The Event Loop allows JavaScript to perform asynchronous
operations even though it is single-threaded. It continuously checks the
Call Stack and moves ready callbacks from queues to the stack when it
becomes empty.



## 4. What are the different types of exchanges in RabbitMQ?

**Answer:**
- **Direct Exchange** - Routes messages based on an exact
routing key.
- **Fanout Exchange** -- Broadcasts messages to all bound
queues.
- **Topic Exchange** -- Routes messages using wildcard patterns
(`*` and `#`).
- **Headers Exchange** -- Routes messages based on
message headers instead of routing keys.



## 5. How many ways can we access the value of an object in JavaScript?

**Answer:** Two common ways:
1. **Dot notation:** `obj.name`
2. **Bracket notation:** `obj["name"]`

Bracket notation is useful for dynamic property names or properties
containing spaces/special characters.


## 6. Why do we use PropTypes in React?

**Answer:** PropTypes are used for **runtime type checking** of React
component props during development. They help catch invalid prop types,
improve code readability, and make components easier to maintain. They
do not replace TypeScript but provide lightweight validation.
