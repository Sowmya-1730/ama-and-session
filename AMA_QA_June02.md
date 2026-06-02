# June 02 2026 AMA Q&A

### Q: What are the CSS properties used for text color?

The `color` property is used to change the color of text.

```css
p {
    color: blue;
}
```


### Q: Can a website be responsive without media queries?

Yes. A website can be responsive using flexible layouts such as Flexbox, CSS Grid, percentages, viewport units (`vw`, `vh`), and responsive images. Media queries provide additional control but are not always required.



### Q: How can you change the image source using CSS?

You can use the content property to replace an image in certain situations, but it works only on replaced elements or pseudo-elements.

```html
img {
    content: url("new-image.jpg");
}
```
Explanation:

The content: url() property can display a different image without changing the HTML src attribute.

```html
<img src="old-image.jpg" alt="Image">
img {
    content: url("new-image.jpg");
}
```

The displayed image becomes new-image.jpg.



### Q: What is the difference between `<input type="button">` and `<button>`?

`<button>` can contain HTML elements and text, while `<input type="button">` can only display plain text.

**Explanation:**

```html
<input type="button" value="Click Me">

<button><strong>Click Me</strong></button>
```


### Q: How do you create a nested webpage structure?

A nested webpage can be created using the `<iframe>` tag, which embeds one webpage inside another webpage.

Example:
```html
<iframe src="https://example.com"></iframe>
```

Explanation:
The `<iframe>` (Inline Frame) element displays another HTML page within the current page. It is commonly used to embed websites, maps, videos, or external content.



### Q: What is the difference between `position: absolute` and `position: relative`?


- `relative` positions an element relative to its normal position.
- `absolute` positions an element relative to its nearest positioned ancestor.


```css
.box1 {
    position: relative;
}

.box2 {
    position: absolute;
}
```


### Q: What is the Mobile-First Approach in responsive web design?

Designing the website for mobile devices first and then adding styles for larger screens. This approach ensures better performance and usability on smaller devices.



### Q: What does `fr` mean in CSS Grid?

`fr` stands for Fractional Unit. It divides the available space proportionally among grid columns or rows.

```css
grid-template-columns: 1fr 2fr;
```

The second column gets twice as much space as the first.


### Q: What is the difference between `border: none` and `border: 0`?

Both remove the visible border.

- `border: none` removes the border style.
- `border: 0` sets the border width to zero. In most cases, they produce the same visual result. But, there is a small amount of border will be there.


### Q: What is `z-index` in CSS?

`z-index` controls the stacking order of overlapping elements.

Elements with a higher `z-index` appear above elements with a lower `z-index`.

```css
.modal {
    z-index: 1;
}
```

### Q: How do you create a sticky header that stays at the top while scrolling?

Use `position: sticky` with `top: 0`.

```css
header {
    position: sticky;
    top: 0;
}
```
The header remains visible at the top when the user scrolls.


### Q: Why is External CSS preferred over Internal and Inline CSS?

Because it improves maintainability, reusability, and organization. A single CSS file can be used across multiple pages, making updates easier and reducing code duplication.


### Q: Why do we use Reset CSS?

To remove browser default styles and create a consistent starting point. Different browsers apply different default margins, paddings, and styles. Reset CSS helps ensure consistent rendering.

```css
* {
    margin: 0;
    padding: 0;
}
```


