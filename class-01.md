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

## What is “Float”?

![image](https://i1.wp.com/www.tutorialbrain.com/wp-content/uploads/2019/03/css-float-left-right.jpg?fit=443%2C392&ssl=1)

The float property is used for positioning and formatting content e.g. let an image float left to the text in a container.

The float property can have one of the following values:

- left - The element floats to the left of its container
- right - The element floats to the right of its container
- none - The element does not float (will be displayed just where it occurs in the text). This is default
- inherit - The element inherits the float value of its parent
- In its simplest use, the float property can be used to wrap text around images.

#### Clearing the Float

Float’s sister property is clear. An element that has the clear property set on it will not move up adjacent to the float like the float desires, but will move itself down past the float. Again an illustration probably does more good than words do.

![image](https://css-tricks.com/wp-content/csstricks-uploads/unclearedfooter.png)

![image](https://css-tricks.com/wp-content/csstricks-uploads/clearedfooter.png)