# AMA Questions and Answers

## 1. Why do we use DEBUG = False in production?
In Django, DEBUG = False disables detailed error pages and debug information.
- Prevents exposure of sensitive system data (paths, settings, SQL queries).
- Improves performance.
- Shows custom error pages (404, 500) instead of stack traces.


## 2. What is the use of build.sh?
build.sh is a shell script used to automate build steps like:
- Installing dependencies
- Running migrations/tests
- Collecting static files
- Preparing deployment environment
It ensures consistent deployment steps.

## 3. What is a context processor?
A context processor in Django is a function that adds data to all templates automatically.
Example use cases:
- User authentication info
- Site-wide settings
- Notifications count


## 4. What is the use of widgets in forms.py?
Widgets define how form fields are rendered in HTML.
Examples:
- TextInput, PasswordInput, FileInput
- Customize attributes like class, placeholder, styles


## 5. When do we use enctype?
enctype specifies how form data is encoded when submitting.
Used when:
- file uploads → enctype="multipart/form-data"
- default is application/x-www-form-urlencoded


## 6. What is a Many-to-Many field?
A Django model relationship where multiple records in one table relate to multiple records in another.
Example:
- Students ↔ Courses
Implemented using an intermediate join table.


## 7. What is toast in JavaScript?
A toast is a small popup notification that disappears automatically.
Used for:
- success messages
- error alerts
- warnings


## 8. What is the use of __init__.py file?
- Marks a directory as a Python package
- Allows module imports from that folder
- Can execute package initialization code


## 9. Why use collectstatic in Django?
collectstatic gathers all static files from apps into a single directory.
Used for:
- Production deployment
- Serving CSS, JS, images efficiently via web server


## 10. What is currying in JavaScript?
Currying is a technique where a function takes arguments one at a time instead of all at once.

Example:
```js
function add(a) {
    return function(b) {
        return a + b;
    }
}

add(2)(3); // 5
```

---
