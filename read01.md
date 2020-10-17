# summery
## What is “Float”?
### Float is a CSS positioning property. To understand its purpose and origin
![img](https://i1.wp.com/css-tricks.com/wp-content/csstricks-uploads/print-layout.png?resize=540%2C270&ssl=1)
#### In web design, page elements with the CSS float property applied to them are just like the images in the print layout where the text flows around them. 
#### Setting the float on an element with CSS happens like this:
` #sidebar {
  float: right;			
} `
#### There are four valid values for the float property. *Left* and *Right* float elements those directions respectively. *None* (the default) ensures the element will not float and *Inherit* which will assume the float value from that elements parent element.
### What are floats used for?
#### Aside from the simple example of wrapping text around images, floats can be used to create entire web layouts.
### Clearing the Float
#### Float’s sister property is clear. An element that has the clear property set on it will not move up adjacent to the float like the float desires, but will move itself down past the float
` #footer {
  clear: both;			
} `
#### clear has four valid values as well. Both is most commonly used
### Techniques for Clearing Floats
1. The Empty Div Method : Sometimes you’ll see a ` <br> ` element or some other random element used, but div is the most common because it has no browser default styling
2. The Overflow Method : relies on setting the overflow CSS property on a parent element
3. The Easy Clearing Method :  uses a clever CSS pseudo selector (:after) to clear floats. Rather than setting the overflow on the parent, you apply an additional class like “clearfix” to it. Then apply this CSS: ` .clearfix:after { 
   content: "."; 
   visibility: hidden; 
   display: block; 
   height: 0; 
   clear: both;
} `


### Problems with Floats
1. Pushdown Quick fix: Make sure you don’t have any images that do this, use overflow: hidden to cut off excess.
2. Double Margin Bug Quick fix: set display: inline on the float, and don’t worry it will remain a block-level element.

## Responsive Web Design
![img1](https://storage.googleapis.com/cw-p1w5jpim0sdhkccw8gr/media/blog-images/responsive-web-design-caktus.gif)
#### Responsive web design is the practice of building a website suitable to work on every device and every screen size, no matter how large or small, mobile or desktop.

### Flexible Layouts
#### Responsive web design is broken down into three main components,1. including flexible layouts,2.  media queries,3. and flexible media. 
#### The first part, flexible layouts, is the practice of building the layout of a website with a flexible grid, capable of dynamically resizing to any width. Flexible grids are built using relative length units, most commonly percentages or em units. These relative lengths are then used to declare common grid property values such as width, margin, or padding.
#### Flexible layouts do not advocate the use of fixed measurement units, such as pixels or inches. Reason being, the viewport height and width continually change from device to device. Website layouts need to adapt to this change and fixed values have too many constraints
#### The formula is based around taking the target width of an element and dividing it by the width of it’s parent element. The result is the relative width of the target element.
#### Taking the flexible layout concept, and formula, and reapplying it to all parts of a grid will create a completely dynamic website, scaling to every viewport size. For even more control within a flexible layout, you can also leverage the min-width, max-width, min-height, and max-height properties.

### Media Queries
![imag3](https://i0.wp.com/www.silocreativo.com/en/wp-content/uploads/2016/12/media-query-for-mobile-first.png?resize=666%2C500&quality=100&strip=all&ssl=1)

##### Media queries were built as an extension to media types commonly found when targeting and including styles.
##### Media queries provide the ability to specify different styles for individual browser and device circumstances, the width of the viewport or device orientation for example. Being able to apply uniquely targeted styles opens up a world of opportunity and leverage to responsive web design.
##### There are a couple different ways to use media queries
1. using the ` @media ` rule inside of an existing style sheet ` @media all and (max-width: 1024px) {...} @import url(styles.css) all and (max-width: 1024px) {...} `

2.  or by linking to a separate style sheet from within the HTML document ` <link href="styles.css" rel="stylesheet" media="all and (max-width: 1024px)"> `

#### Logical Operators in Media Queries
##### Logical operators in media queries help build powerful expressions.
##### There are three different logical operators available for use within media queries, including and, not, and only.
##### Within responsive design the most commonly used features include min-width and max-width. These help build responsive websites on desktops and mobile devices equally, avoiding any confusion with device features.



- The orientation media feature determines if a device is in the landscape or portrait orientation. The landscape mode is triggered when the display is wider than taller, and the portrait mode is triggered when the display is taller than wider.` @media all and (orientation: landscape) {...} `
- The aspect-ratio and device-aspect-ratio features specifies the width/height pixel ratio of the targeted rendering area or output device ` @media all and (min-device-aspect-ratio: 16/9) {...} `
- The resolution media feature specifies the resolution of the output device in pixel density, also known as dots per inch or DPI. ` @media print and (min-resolution: 300dpi) {...} ` 
### Mobile First
![image3](https://www.solodev.com/core/fileparse.php/131/urlt/media-queries-blog.jpg)
##### One popular technique with using media queries is called mobile first. The mobile first approach includes using styles targeted at smaller viewports as the default styles for a website, then use media queries to add styles as the viewport grows.

- Using the viewport meta tag with either the height or width values will define the height or width of the viewport respectively. ` <meta name="viewport" content="width=device-width"> `
- To control how a website is scaled on a mobile device, and how users can continue to scale a website, use the minimum-scale, maximum-scale, initial-scale, and user-scalable properties. ` <meta name="viewport" content="initial-scale=2"> `
- The viewport meta tag will accept individual values as well as multiple values, allowing multiple viewport properties to be set at once. ` <meta name="viewport" content="width=device-width, initial-scale=1"> `

### Flexible Media
![image4](https://www.designhill.com/design-blog/wp-content/uploads/2014/06/7-min.jpg)

##### The final, equally important aspect to responsive web design involves flexible media. As viewports begin to change size media doesn’t always follow suit. Images, videos, and other media types need to be scalable, changing their size as the size of the viewport changes.
##### One quick way to make media scalable is by using the max-width property with a value of 100%. Doing so ensures that as the viewport gets smaller any media will scale down according to its containers width
 ` img, video, canvas {
  max-width: 100%;
} `
### SMACSS 
#### What is it????
![image5](https://cdn-images-1.medium.com/fit/t/1600/480/1*EqNOOn4VG-c6dvMIEZGTRA.png)
#####  is more style guide than rigid framework. There is no library within here for you to download or install. There is no git repository for you to clone. SMACSS is a way to examine your design process and as a way to fit those rigid frameworks into a flexible thought process.

### Context
##### A block level element is as wide as the parent it’s inside (` width: auto; `). We can think of it as 100% wide. The wrapper for a grid probably don’t have much to do with semantics, it’s just a generic wrapper, so a div is fine.

### Columns

##### Let’s start with a practical and common need: a main content area being 2/3 the width and a sidebar being 1/3 the width. We just make two column divs with appropriate class names

` <div class="grid">
  <div class="col-2-3">
     Main Content
  </div>
  <div class="col-1-3">
     Sidebar
  </div>
</div> `


##### To make them next to each other

` [class*='col-'] {
  float: left;
} `

##### and individual width like this:


` .col-2-3 {
  width: 66.66%;
}
.col-1-3 {
  width: 33.33%;
} `

### Clearing Context
#### The parent element will collapse to zero height since it has only floated children. Let’s fix that by clearing it. These days all you need is this:
` .grid:after {
  content: "";
  display: table;
  clear: both;
} `
























