# summery
## A Complete Guide to Grid
#### CSS Grid Layout is the most powerful layout system available in CSS. It is a 2-dimensional system, meaning it can handle both columns and rows, unlike flexbox which is largely a 1-dimensional system. You work with Grid Layout by applying CSS rules both to a parent element (which becomes the Grid Container) and to that element’s children (which become Grid Items). Get the poster! Reference this guide a lot? Pin a copy up on the office wall. Buy Poster
![img](https://i2.wp.com/codehints.in/wp-content/uploads/2018/02/responsive-grid-css.jpg?fit=1710%2C898)
#### Properties for the Parent(Grid Container)
- display  : `.container {
  display: grid | inline-grid;
} `
- grid-template-columns
- grid-template-rows
` .container {
  grid-template-columns:  ... |   ...;
  grid-template-rows:  ... |   ...;
} `
#### Properties for the Children (Grid Items)
 - grid-column-start
- grid-column-end
- grid-row-start
- grid-row-end

`.item {
  grid-column-start: <number> | <name> | span <number> | span <name> | auto;
  grid-column-end: <number> | <name> | span <number> | span <name> | auto;
  grid-row-start: <number> | <name> | span <number> | span <name> | auto;
  grid-row-end: <number> | <name> | span <number> | span <name> | auto;
} `


#### grid-column grid-row
` .item {
  grid-column: <start-line> / <end-line> | <start-line> / span <value>;
  grid-row: <start-line> / <end-line> | <start-line> / span <value>;
} `

## Common Responsive Layouts with CSS Grid

#### There’s a lot going on here, so let’s break it down -
#### The repeat() function takes two arguments, the first will define the number of column tracks and the second, what width the tracks should be.

### The Full Page Image Gallery
#### his image gallery layout uses features of CSS grid to create different sizes of grid cells. I’ve used the span value on grid-columnand grid-row to make individual cells stretch over two or more slots in the track. The line


