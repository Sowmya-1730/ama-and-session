# AMA
# 1. What is Docker?

### Answer

Docker is an open-source platform used to develop, package, and run applications inside **containers**.

A container contains:
- Application code
- Runtime
- Libraries
- Dependencies
- Configuration files

This ensures the application runs the same way on every machine.



# 2. How to get ASCII value of a character in Python?

### Answer

Use the built-in `ord()` function.

### Example

```python
print(ord('A'))
```

Output

```
65
```


# 3. What is Port Mapping in Docker?

### Answer

Port mapping connects a port inside the Docker container to a port on the host machine.

Syntax:

```bash
docker run -p HOST_PORT:CONTAINER_PORT image_name
```

Example

```bash
docker run -p 8000:80 nginx
```

Meaning:

- Host port → 8000
- Container port → 80

Now opening:

```
http://localhost:8000
```

actually accesses port **80** inside the container.

### Why is it needed?

Containers have their own network.

Without port mapping, applications running inside containers cannot be accessed from outside.

---

# 4. What is `serializer.is_valid()`?

### Answer

`serializer.is_valid()` validates incoming request data before saving it to the database.

It checks:

- Required fields
- Data types
- Field validations
- Custom validations
- Unique constraints



# 5. What are the types of Exchanges in RabbitMQ?

### Answer

RabbitMQ has **four main exchange types**.

## 1. Direct Exchange

Routes messages using an exact routing key.


## 2. Fanout Exchange

Broadcasts messages to **all connected queues**.


## 3. Topic Exchange

Uses pattern matching.



## 4. Headers Exchange

Routes messages based on headers instead of routing keys.



# 6. What are the three parts of JWT?

### Answer

JWT (JSON Web Token) has **three parts** separated by dots.

```
Header.Payload.Signature
```

Example

```
xxxxx.yyyyy.zzzzz
```

# 7. What is the use of a Channel in RabbitMQ?

### Answer

A **Channel** is a lightweight virtual connection inside a RabbitMQ connection.

Instead of creating multiple TCP connections, multiple channels can share a single connection.

Channels are used to:

- Publish messages
- Consume messages
- Declare queues
- Declare exchanges
- Acknowledge messages



# 8. hat are the core components of RabbitMQ?

### Answer

The main components are:

## 1. Producer

Sends messages.


## 2. Exchange

Receives messages from producers and decides where to send them.


## 3. Queue

Stores messages until consumers receive them.

## 4. Binding

Connects an exchange to a queue.

## 5. Routing Key

Helps exchanges decide which queue should receive a message.


## 6. Consumer

Receives and processes messages.


## 7. Channel

A lightweight communication path over a single TCP connection.


## 8. Connection

A TCP connection between the application and RabbitMQ server.


# 9. Vikas Mehta: Difference between Docker Image and Docker Container

| Docker Image | Docker Container |
|--------------|------------------|
| Blueprint of an application | Running instance of an image |
| Read-only | Read and write |
| Cannot execute by itself | Executes the application |
| Created using Dockerfile | Created from an image |
| Multiple containers can use the same image | Each container has its own state |
