# Templating with Mustache

Mustache is a logic-less template syntax. It can be used for HTML, config files, source code — anything. It works by expanding tags in a template using values provided in a hash or object.

```javascript
Mustache.render(“Hello, {{name}}”, { name: “Sherlynn” });
// returns: Hello, Sherlynn
```

![image](https://miro.medium.com/max/700/1*LbqYj87xlazySm6wE0Q2lA.png)

## Mustache-Express

If you intend you use mustache with Node and Express, you can use mustache-express. Mustache Express lets you use Mustache and Express together easily.

# CSS Flexbox

The Flexible Box Layout Module, makes it easier to design flexible responsive layout structure without using float or positioning.

To start using the Flexbox model, you need to first define a flex container.

![image](https://css-tricks.com/wp-content/uploads/2018/10/01-container.svg)

```html
<div class="flex-container">
  <div>1</div>
  <div>2</div>
  <div>3</div>
</div>
```

```css
.flex-container {
  display: flex;
}
```

**The flex container properties are:**

- flex-direction

![image](https://css-tricks.com/wp-content/uploads/2018/10/flex-direction.svg)

```css
.container {
  flex-direction: row | row-reverse | column | column-reverse;
}
```

- flex-wrap

![img](https://css-tricks.com/wp-content/uploads/2018/10/flex-wrap.svg)

```css
.container {
  flex-wrap: nowrap | wrap | wrap-reverse;
}
```

- flex-flow

```css
.container {
  flex-flow: column wrap;
}
```

- justify-content

![img](https://css-tricks.com/wp-content/uploads/2018/10/justify-content.svg)

```css
.container {
  justify-content: flex-start | flex-end | center | space-between | space-around
    | space-evenly | start | end | left | right ... + safe | unsafe;
}
```

- align-items

![img](https://css-tricks.com/wp-content/uploads/2018/10/align-items.svg)

```css
.container {
  align-items: stretch | flex-start | flex-end | center | baseline | first
    baseline | last baseline | start | end | self-start | self-end + ... safe |
    unsafe;
}
```

- align-content

![img](https://css-tricks.com/wp-content/uploads/2018/10/align-content.svg)

```css
.container {
  align-content: flex-start | flex-end | center | space-between | space-around |
    space-evenly | stretch | start | end | baseline | first baseline | last
    baseline + ... safe | unsafe;
}
```

**The flex item properties are:**

- order

![img](https://css-tricks.com/wp-content/uploads/2018/10/order.svg)

```css
.item {
  order: 5; /* default is 0 */
}
```

- flex-grow

![img](https://css-tricks.com/wp-content/uploads/2018/10/flex-grow.svg)

```css
.item {
  flex-grow: 4; /* default 0 */
}
```

- flex-shrink

```css
.item {
  flex-shrink: 3; /* default 1 */
}
```

- flex-basis

This defines the default size of an element before the remaining space is distributed

```css
.item {
  flex-basis: | auto; /* default auto */
}
```

- flex

This is the shorthand for flex-grow, flex-shrink and flex-basis combined.

```css
.item {
  flex: none | [ < "flex-grow" > < "flex-shrink" >? || < "flex-basis" > ];
}
```

- align-self

![img](https://css-tricks.com/wp-content/uploads/2018/10/align-self.svg)

```css
item {
  align-self: auto | flex-start | flex-end | center | baseline | stretch;
}
```
