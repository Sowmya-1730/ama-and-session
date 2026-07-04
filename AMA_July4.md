# AMA July 4, 2026

## 1. Can we have one `urls.py` in a Django project?

Yes. A Django project can work with a single `urls.py` if the project is
small. However, in real-world applications, each app usually has its own
`urls.py`, and the project's main `urls.py` includes them using
`include()`. This keeps routing modular, maintainable, and easier to
scale.



## 2. What is `get_object_or_404()`?

`get_object_or_404()` is a Django shortcut that tries to retrieve a
single object from the database.

-   If the object exists, it returns it.
-   If it does not exist, it automatically raises an HTTP 404 (Not
    Found) error instead of crashing.

Example:

``` python
from django.shortcuts import get_object_or_404

problem = get_object_or_404(Problem, slug=slug)
```


## 3. What happens if we don't have `manage.py` in production?

Normally, `manage.py` is mainly a development utility.

In production: - The application is usually started using Gunicorn,
uWSGI, Daphne, etc. - Requests are handled through WSGI or ASGI. - The
application can still run without `manage.py`.

However, `manage.py` is still useful for: - `python manage.py migrate` -
`python manage.py collectstatic` - `python manage.py createsuperuser`

So production servers don't depend on it for serving requests, but
administrators often keep it for management commands.


## 4. What is `get_or_create()`?

`get_or_create()` either: 1. Retrieves an existing object, or 2. Creates
a new one if it doesn't exist.

It returns:

``` python
(object, created)
```

where `created` is `True` if a new object was created.

Example:

``` python
category, created = Category.objects.get_or_create(
    name="Array"
)
```


## 5. What is `bulk_create()`?

`bulk_create()` inserts multiple database records using a single SQL
query.

Example:

``` python
Problem.objects.bulk_create([
    Problem(title="Two Sum"),
    Problem(title="Reverse String"),
    Problem(title="Binary Search")
])
```


## 6. What is CSRF?

CSRF stands for **Cross-Site Request Forgery**.

It is an attack where a malicious website tricks a logged-in user into
performing unwanted actions on another website.

Django protects against CSRF using:

``` html
{% csrf_token %}
```

The browser sends the CSRF token with POST requests, and Django verifies
it before processing the request.


## 7. Tell me some built-in Django signals.

Common built-in signals include:

-   `pre_save` -- before saving an object
-   `post_save` -- after saving an object
-   `pre_delete` -- before deleting
-   `post_delete` -- after deleting
-   `m2m_changed` -- when a many-to-many relationship changes
-   `pre_migrate` -- before migrations
-   `post_migrate` -- after migrations
-   `request_started` -- request processing begins
-   `request_finished` -- request processing completes



## 8. What is Message Middleware?

Django's Message Middleware allows temporary messages to be stored and
displayed to users.

Examples: - Login successful - Profile updated - Password changed - Form
submitted successfully

Example:

``` python
from django.contrib import messages

messages.success(request, "Profile updated successfully.")
messages.error(request, "Invalid credentials.")
```

Messages are typically displayed on the next page after a redirect.


## 9. Difference between `appendChild()` and `append()` in JavaScript

- appendChild() accepts only a node. It returns the appended node. This is older one.
- append() accepts nodes and string, returns 'undefined' and newer API