# SMACSS and Responsive Web Design

## Responsive Web Design

### Responsive Overview

Responsive web design is the practice of building a website suitable to work on every device and every screen size, no matter how large or small, mobile or desktop.


### Flexible Layouts

Responsive web design is broken down into three main components, including flexible layouts, media queries, and flexible media.


### Relative Viewport Lengths

- vw : Viewports width
- vh : Viewports height
- vmin : Minimum of the viewport’s height and width
- vmax : Maximum of the viewport’s height and width


### Flexible Grid

The formula is based around taking the target width of an element and dividing it by the width of it’s parent element. The result is the relative width of the target element.

`target ÷ context = result`

```html
<div class="container">
  <section>...</section>
  <aside>...</aside>
</div>
```

```css
section,
aside {
  margin: 1.858736059%; /*  10px ÷ 538px = .018587361 */
}
section {
  float: left;
  width: 63.197026%;    /* 340px ÷ 538px = .63197026 */   
}
aside {
  float: right;
  width: 29.3680297%;  /* 158px ÷ 538px = .293680297 */
}
```

### Media Queries

Media query is a CSS technique introduced in CSS3.

It uses the @media rule to include a block of CSS properties only if a certain condition is true.
