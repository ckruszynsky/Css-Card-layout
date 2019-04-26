# CSS Grid Notes

## Grid Container

A grid layout consists of a parent element, with one or more child elements.

```html
<div class="grid-container">
  <div class="card"></div>
</div>
```

```css
.grid-container {
  display: grid;
}
```

The parent element of a grid layout must have `display:grid` set

_grid-gap_: grid-gap is a gutter between rows and columns in a grid layout and it is also a shorthand property for :

- grid-row-gap
- grid-column-gap

## Grid Tracks

Rows and columns on our grid are defined with `grid-template-columns` and `grid-template-rows` properties. This defines our grid tracks.

A _grid track_ is the space between any lines on the grid.

_grid-template-columns_: grid template columns describe the line names and track sizing function of a grid's columns. The grid template column is one of the most important properties in the grid.

```css
grid-template-columns: 30vw 1fr 15vw;
grid-template-columns: [col1-start] [col2-start] [col3-start];
```

_grid-template-rows_: grid template rows property describes the line names and track sizing function of a grid's rows

```css
grid-template-rows: 30vw 1fr 15vw;
grid-template-rows: [row1-start] [row2-start] [row3-start];
```

_grid-auto-rows_ and _grid-auto-columns_
grid-auto-\* can define a set size for tracks created in the implicit grid.

When setting up an explicit grid or defining

_fr units_
_fr_ stands for "fraction of available space". The fr unit can be used for grid-rows and grid-column values.

_repeat()_
The `repeat()` CSS function represents a repeated fragment of the tracklist, allowing a large number of columns or rows that exhibit a recurring pattern to be written in a more compact form.

This function is used in the CSS grid properties grid-template-columns & grid-template-rows.

```css
grid-template-columns: repeat(3, 1fr, 2fr);
grid-template-columns: repeat(3, 1fr);
```

_minmax():_
minmax(smallest, largest) is replacing the size value in our repeat function.
minmax() allows you to specify the smallest and largest size of the column

```css
grid-template-columns: minmax(200px, 1fr);
```
