# AMA Questions and Answers

## What are `*` (star) and `#` (hash) in RabbitMQ Topic Exchange?

In a Topic Exchange, routing keys are matched using wildcards: - `*`
matches **exactly one word**. -

Example:

- `order.*` matches
`order.created` and `order.updated`, but not
`order.payment.completed`.

- `#` matches **zero or more words**. -
Example: `order.#` matches `order`, `order.created`, and
`order.payment.completed`.



## Why is Redis fast?

Redis is fast because: - It stores data **in memory (RAM)** instead of
on disk.

- Uses efficient data structures.
- Mostly single-threaded,
avoiding locking overhead.
- Supports optimized network I/O.



## How can we achieve data persistence in Redis?

Redis supports persistence using:

1. **RDB (Snapshotting)** -- saves the
dataset at intervals.
2. **AOF (Append Only File)** -- logs every write
operation.
3. **Both RDB + AOF** -- commonly used for better durability
and faster recovery.


## What is throughput in Kafka?

Throughput is the **amount of data Kafka can process in a given time**,
usually measured in **messages/second** or **MB/second**. Kafka achieves
high throughput through sequential disk writes, batching, partitioning,
and zero-copy transfer.



## What is a persistent message in RabbitMQ?

A persistent message is stored to disk (when sent with
`delivery_mode=2`) so it can survive a broker restart **if the queue is
also durable**.



## What is kubelet?

Kubelet is the **agent running on every Kubernetes worker node**. It:
- Receives Pod specifications from the API server.
- Starts and monitors
containers through the container runtime.
- Reports node and Pod status
back to the control plane.


## What is Round-Robin Dispatch?

Round-robin dispatch is RabbitMQ's default message distribution strategy
where messages are sent to consumers one after another in rotation,
regardless of whether a consumer is busy. Fair Dispatch (using
`prefetch`) is preferred when task durations vary.


## What are collections in MongoDB?

A **collection** is a group of related MongoDB documents, similar to a
table in relational databases. Unlike tables, documents in the same
collection can have different fields (schema is flexible).


## What is Kafka retention?

Kafka retention is the policy that determines **how long messages are
kept** in a topic before deletion. Retention can be configured by:
- Time (e.g., 7 days)
- Size (e.g., 100 GB)

Messages remain available for consumers until the retention limit is
reached, even if they have already been consumed.


## What is the Result Backend in Redis?

In Celery, the **Result Backend** stores the status and results of
tasks. When Redis is used as the result backend, it stores information
such as:
- Task state (`PENDING`, `STARTED`, `SUCCESS`, `FAILURE`)
- Return value - Exception details (if failed)

Workers write results to Redis, and clients retrieve them using the task
ID.
