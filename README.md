# CSS GRID - CRASH COURSE

### Make it a grid
```css
.wrapper{
  display: grid;
}
```
`display: grid;` makes the thing you're working with a grid. Everything inside that wrapper is considered a grid item. Those grid items will follow the wrapper's rules.

### Give it a template
```css
.wrapper{
  display: grid;
  grid-template-columns: 1fr 1fr 1fr;
}
```
`grid-template-columns` will divide the window into separate columns. `fr` is a measurement in fractions. So in this case, there are 3 fractions so each column is 1/3 of the window.

You can use something like `grid-template-columns: repeat(3, 1fr)` for shorthand.

### Gap
```css
.wrapper{
  display: grid;
  grid-template-columns: 1fr 1fr 1fr;
  grid-gap: 1em;
}
```
`column-gap` determines the spacing between each column. Similarly, there is a `row-gap`. There is also
`grid-gap` which determines the spacing between each column and row.

### Auto 'Height'
```css
.wrapper{
  display: grid;
  grid-template-columns: 1fr 1fr 1fr;
  grid-gap: 1em;
  /* grid-auto-rows: 100px; */
  grid-auto-rows: minmax(100px, auto);
}
```
`grid-auto-rows` sets a fixed height for each grid item.

However, you may find that your content will overflow if it's more than the fixed height. You can use `grid-auto-rows: minmax(100px, auto);` which sets a minimum to 100px and `auto` stretches to fit the content.