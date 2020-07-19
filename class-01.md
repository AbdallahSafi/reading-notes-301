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
  width: 63.197026%; /* 340px ÷ 538px = .63197026 */
}
aside {
  float: right;
  width: 29.3680297%; /* 158px ÷ 538px = .293680297 */
}
```

### Media Queries

Media query is a CSS technique introduced in CSS3.

It uses the @media rule to include a block of CSS properties only if a certain condition is true.

```css
@media only screen and (max-width: 600px) {
  body {
    background-color: lightblue;
  }
}
```

#### Media queries are used for the following:

- To conditionally apply styles with the CSS @media and @import at-rules.
- To target specific media for the <style>, <link>, <source>, and other HTML elements with the media= attribute.
- To test and monitor media states using the Window.matchMedia() and MediaQueryList.addListener() JavaScript methods.

#### Logical Operators in Media Queries

The logical operators not, and, and only can be used to compose a complex media query. You can also combine multiple media queries into a single rule by separating them with commas.


- and
The and operator is used for combining multiple media features together into a single media query, requiring each chained feature to return true in order for the query to be true. It is also used for joining media features with media types.

- not
The not operator is used to negate a media query, returning true if the query would otherwise return false. If present in a comma-separated list of queries, it will only negate the specific query to which it is applied. If you use the not operator, you must also specify a media type.

- only
The only operator is used to apply a style only if an entire query matches, and is useful for preventing older browsers from applying selected styles. When not using only, older browsers would interpret the query screen and (max-width: 500px) simply as screen, ignoring the remainder of the query, and applying its styles on all screens. If you use the only operator, you must also specify a media type.

- , (comma)
Commas are used to combine multiple media queries into a single rule. Each query in a comma-separated list is treated separately from the others. Thus, if any of the queries in a list is true, the entire media statement returns true. In other words, lists behave like a logical or operator.