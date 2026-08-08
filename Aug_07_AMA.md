# Aug 08 AMA

## 1. What is React prompting?

**Answer:** React prompting generally means using prompts to guide an AI tool to generate, explain, or modify React code. A good prompt clearly describes the component, required behavior, UI, inputs, and constraints so the AI can produce useful React code.

## 2. What do you use a view for in PostgreSQL?

**Answer:** A **view** is a virtual table based on a SQL query. It is used to simplify complex queries, reuse commonly needed data, hide unnecessary columns or rows, and provide controlled access to data.

```sql
CREATE VIEW active_users AS
SELECT id, name, email
FROM users
WHERE is_active = true;
```

## 3. What is the difference between Direct Exchange and Topic Exchange?

**Answer:** Both are RabbitMQ exchange types, but they route messages differently.

- **Direct Exchange:** Routes a message when the routing key exactly matches the queue's binding key.
- **Topic Exchange:** Routes messages using pattern matching. `*` matches one word and `#` matches zero or more words.

**Example:**
- Direct: `order.created` → exact match.
- Topic: `order.*` → can match `order.created` and `order.cancelled`.

## 4. What are zero-shot and chain of thought?

**Answer:**

- **Zero-shot prompting:** Asking an AI model to perform a task without giving examples of the expected answer.

  **Example:** `Translate "Hello" into French.`

- **Chain-of-thought:** A reasoning approach where a model works through multiple steps to solve a problem. In practice, it is better to ask a model to reason carefully rather than request or expose private internal reasoning.

**Simple difference:** Zero-shot describes **the amount of example guidance**; chain-of-thought describes **a reasoning approach**.

## 5. How do you create an empty set in Python?

**Answer:** Use `set()`.

```python
my_set = set()
```

Do **not** use `{}` because `{}` creates an empty dictionary.

```python
print(type(set()))  # <class 'set'>
print(type({}))     # <class 'dict'>
```

## 6. List the stages of Git.

**Answer:** The main stages in a typical Git workflow are:

1. **Working Directory** – Where files are created or modified.
2. **Staging Area (Index)** – Changes are prepared for a commit using `git add`.
3. **Local Repository** – Changes are stored as commits using `git commit`.
4. **Remote Repository** – Changes are shared with a remote such as GitHub using `git push`.

**Typical flow:**

`Working Directory → Staging Area → Local Repository → Remote Repository`
