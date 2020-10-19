# summery 
## Javascript Templating
#### Javascript templating is a fast and efficient technique to render client-side view templates with Javascript by using a JSON data source. The template is HTML markup, with added templating tags that will either insert variables or run programming logic.
## Mustache
#### Mustache is a logic-less template syntax. It can be used for HTML, config files, source code — anything. It works by expanding tags in a template using values provided in a hash or object.
It is often referred to as “logic-less” because there are no if statements, else clauses, or for loops. Instead, there are only tags. Some tags are replaced with a value, some nothing, and others a series of values.
` Mustache.render(“Hello, {{name}}”, { name: “Sherlynn” });
// returns: Hello, Sherlynn `
## Flexbox
![img](https://miro.medium.com/max/5992/1*gaN7h99jHpTAP1ba3AWKng.png)
` .container {
  display: flex; /* or inline-flex */
} `
#### Properties for the Children(flex items)
` .item {
  order: 5; /* default is 0 */
} `
#### flex-direction
` .container {
  flex-direction: row | row-reverse | column | column-reverse;
} `
-  row (default): left to right in ltr; right to left in rtl
- row-reverse: right to left in ltr; left to right in rtl
- column: same as row but top to bottom
- column-reverse: same as row-reverse but bottom to top
#### flex-grow
` .item {
  flex-grow: 4; /* default 0 */
} `
#### flex-wrap
` .container {
  flex-wrap: nowrap | wrap | wrap-reverse;
} `
- nowrap (default): all flex items will be on one line
- wrap: flex items will wrap onto multiple lines, from top to bottom.
- wrap-reverse: flex items will wrap onto multiple lines from bottom to top.

#### flex-shrink
![imag1](https://cdn-media-1.freecodecamp.org/images/RITwrqDlcobhm-nFslcJ4ItB3yXdJbXNcAjy)


` .item {
  flex-shrink: 3; /* default 1 */
} `

#### flex-basis
![image3](https://media.geeksforgeeks.org/wp-content/uploads/flexbasis1.png)
` .item {
  flex-basis:  | auto; /* default auto */
} `
#### flex-flow
` .container {
  flex-flow: column wrap;
} `
#### flex
![imag4](https://encrypted-tbn0.gstatic.com/images?q=tbn%3AANd9GcQslwtRwy6CJI3vzAc0-YmQYqPT5a2QBksgYg&usqp=CAU)

` .item {
  flex: none | [ <'flex-grow'> <'flex-shrink'>? || <'flex-basis'> ]
} `




#### align-self
![imag5](https://encrypted-tbn0.gstatic.com/images?q=tbn%3AANd9GcRyDo8oBNZimtW1L_rW0EwZiBp6MYE-pJtFLA&usqp=CAU)


` .item {
  align-self: auto | flex-start | flex-end | center | baseline | stretch;
} `



#### align-content
` .container {
  align-content: flex-start | flex-end | center | space-between | space-around | space-evenly | stretch | start | end | baseline | first baseline | last baseline + ... safe | unsafe;
} `























