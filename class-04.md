# CSS Grid Layout

Create a grid container by setting the display property with a value of grid or inline-grid. All direct children of grid containers become grid items.

![image](https://www.w3.org/TR/css-grid-1/images/game-smaller.png)

## Grid Columns

The vertical lines of grid items are called columns.

## Grid Rows

The horizontal lines of grid items are called rows.

## Grid Gaps
The spaces between each column/row are called gaps.

### You can adjust the gap size by using one of the following properties:

```css
grid-column-gap
grid-row-gap
grid-gap
```


## Grid Lines
The lines between columns are called column lines.

The lines between rows are called row lines


## Grid Container

To make an HTML element behave as a grid container, you have to set the display property to grid or inline-grid.

Grid containers consist of grid items, placed inside columns and rows.

## The grid-template-columns Property

The grid-template-columns property defines the number of columns in your grid layout, and it can define the width of each column.

The value is a space-separated-list, where each value defines the width of the respective column.

If you want your grid layout to contain 4 columns, specify the width of the 4 columns, or "auto" if all columns should have the same width.

## The justify-content Property

The justify-content property is used to align the whole grid inside the container.

## The align-content Property

The align-content property is used to vertically align the whole grid inside the container.


## Child Elements (Items)

A grid container contains grid items.

By default, a container has one grid item for each column, in each row, but you can style the grid items so that they will span multiple columns and/or rows.

## The grid-column Property:

The grid-column property defines on which column(s) to place an item.

You define where the item will start, and where the item will end.

## The grid-row Property:

The grid-row property defines on which row to place an item.

You define where the item will start, and where the item will end.

## The grid-area Property

The grid-area property can be used as a shorthand property for the grid-row-start, grid-column-start, grid-row-end and the grid-column-end properties.

## Naming Grid Items

The grid-area property can also be used to assign names to grid items.