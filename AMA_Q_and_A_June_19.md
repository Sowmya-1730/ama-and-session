# Interview Questions and Answers

## 1. What is the use of `if __name__ == "__main__"` in Python?

It is used to check whether a Python file is being run directly or imported as a module.

- When the file is run directly, `__name__` becomes `"__main__"`.
- When the file is imported, `__name__` becomes the module name.

Example:

```python
def greet():
    print("Hello")

if __name__ == "__main__":
    greet()
```

---

## 2. What is the output of `console.log(false + false)`?

**Output:**

```javascript
0
```

Explanation:

- `false` is converted to `0`.
- `0 + 0 = 0`.

---

## 3. Are there any protocols other than HTTP?

Yes. Some common protocols are:

- HTTPS – Secure HTTP
- FTP – File Transfer Protocol
- SFTP – Secure File Transfer Protocol
- SMTP – Email Sending Protocol
- POP3 – Email Retrieval Protocol
- IMAP – Email Access Protocol
- TCP – Transmission Control Protocol
- UDP – User Datagram Protocol
- DNS – Domain Name System Protocol
- SSH – Secure Shell

---

## 4. What is DNS?

**DNS (Domain Name System)** translates human-readable domain names into IP addresses.

Example:

```text
google.com → 142.250.xxx.xxx
```

Without DNS, users would need to remember IP addresses instead of domain names.

---

## 5. Why do we use ORM?

**ORM (Object Relational Mapping)** allows developers to interact with databases using programming language objects instead of writing raw SQL.

Benefits:

- Less SQL code
- Better readability
- Database abstraction
- Faster development
- Protection against SQL Injection (when used properly)

Examples:

- Django ORM
- SQLAlchemy
- Hibernate
- Sequelize

---

## 6. Status codes starting with 3xx represent what?

**3xx = Redirection Responses**

Examples:

- 301 – Moved Permanently
- 302 – Found (Temporary Redirect)
- 304 – Not Modified
- 307 – Temporary Redirect
- 308 – Permanent Redirect

These tell the client that the requested resource is located elsewhere.

---

## 7. Why do we use Middleware?

Middleware is software that executes between receiving a request and sending a response.

Uses:

- Authentication
- Authorization
- Logging
- Error Handling
- Request Validation
- CORS Handling

Example:

```text
Request → Middleware → Controller → Response
```

---

## 8. What is the default phase of Event Listeners?

By default, event listeners work in the **Bubbling Phase**.

Example:

```javascript
element.addEventListener("click", handler);
```

Equivalent to:

```javascript
element.addEventListener("click", handler, false);
```

Event Flow:

1. Capturing Phase
2. Target Phase
3. Bubbling Phase (Default)

---

## 9. What is the Request-Response Cycle?

The request-response cycle describes how a client communicates with a server.

Flow:

1. Client sends a request.
2. Server receives the request.
3. Server processes it.
4. Server sends a response.
5. Client receives and displays the response.

Example:

```text
Browser → Request → Server
Browser ← Response ← Server
```

---

## 10. Difference Between PUT and PATCH

| PUT | PATCH |
|------|--------|
| Replaces the entire resource | Updates only specified fields |
| Send complete object | Send only changed fields |
| Idempotent | Usually idempotent |
| Larger payload | Smaller payload |

Example:

PUT:

```json
{
  "name": "John",
  "age": 25
}
```

PATCH:

```json
{
  "age": 26
}
```

---

## 11. What is Cache?

Cache is temporary storage used to store frequently accessed data for faster retrieval.

Benefits:

- Faster response times
- Reduced server load
- Improved performance

Examples:

- Browser Cache
- DNS Cache
- Redis Cache
- CDN Cache

---

## 12. What does Content-Type represent?

The `Content-Type` header tells the receiver the format of the data being sent.

Examples:

```http
Content-Type: application/json
Content-Type: text/html
Content-Type: text/plain
Content-Type: image/png
Content-Type: multipart/form-data
```

This helps the client or server correctly process the data.

---

## 13. Can we do a GET call using a browser?

Yes.

Whenever you enter a URL in the browser and press Enter, the browser sends a GET request.

Example:

```text
https://example.com/users
```

Browser:

```http
GET /users HTTP/1.1
```

You can also perform GET requests using:

- Address Bar
- Anchor Tags (`<a>`)
- Fetch API
- Postman
