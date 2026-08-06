# AMA Questions & Answers

## 1. What is Base64?

**Answer:**

Base64 is an encoding technique used to convert binary data (such as images, files, or PDFs) into text using 64 printable ASCII characters.

It is commonly used because some systems can only transmit text data.

**Example:**

Original Text:
```
Hello
```

Base64 Encoded:
```
SGVsbG8=
```

## 2. Why do we use Prompt Engineering?

**Answer:**

Prompt Engineering is the process of writing clear and structured instructions so AI models can produce more accurate and useful responses.

A well-written prompt helps the AI understand:
- What you want
- The expected format
- The level of detail
- The role it should assume

**Example:**

Poor Prompt:
```
Explain React.
```

Good Prompt:
```
Explain React to a beginner with examples and compare it with JavaScript.
```



## 3. What is UTF-8?

**Answer:**

UTF-8 (Unicode Transformation Format - 8 bit) is the most widely used character encoding standard.

It allows computers to store and display text from almost every language in the world.

**Examples:**

```
A
```
Uses 1 byte

```
₹
```
Uses 3 bytes





## 4. What is Chain of Thought?

**Answer:**

Chain of Thought (CoT) is a reasoning technique where an AI solves a problem by breaking it into smaller logical steps before arriving at the final answer.

Instead of answering immediately, it reasons through the problem internally.

**Example:**

Question:
```
If a train travels 60 km in 1 hour,
how far will it travel in 5 hours?
```

Reasoning:
```
Distance = Speed × Time
60 × 5 = 300 km
```

Answer:
```
300 km
```

## 5. What is Infinite Currying?

**Answer:**

Infinite currying is a JavaScript technique where a function can be called repeatedly with one argument at a time until the final value is requested.

**Example:**

```javascript
function add(a) {
    return function(b) {
        if (b !== undefined) {
            return add(a + b);
        }
        return a;
    };
}

console.log(add(2)(3)(4)()); // 9
```

Calls:
```
add(2)
      ↓
add(2)(3)
      ↓
add(2)(3)(4)
      ↓
add(2)(3)(4)()
```

Output:
```
9
```


## 6. What is Stale Closure in React?

**Answer:**

A stale closure happens when a function remembers an old value of a state or variable instead of the latest one.

This commonly occurs inside:
- `setTimeout()`
- `setInterval()`
- Event listeners
- `useEffect()`

**Example:**

```jsx
function Counter() {
  const [count, setCount] = React.useState(0);

  function handleClick() {
    setTimeout(() => {
      console.log(count);
    }, 2000);
  }

  return (
    <>
      <button onClick={() => setCount(count + 1)}>
        Increase
      </button>

      <button onClick={handleClick}>
        Log Count
      </button>
    </>
  );
}
```
