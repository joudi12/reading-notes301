# summery
## what is jquary ???
#### jQuery offers a simple way to achieve a variety of common JavaScript tasks quickly and consistently, across all major browsers and without any fallback code needed. 
![img](https://www.webdesignerdepot.com/cdn-origin/uploads/2019/07/featured_jquery.jpg)

#### how to write the function for jquary ??? ` $(css selector)
#### The jquery object has many methods that you can use to work with the element you select . The methods represent tasks that you commonly need to perform with element 
#### how to do somthing with the element using jQuary ????? ` $('css selector').addclass('complete'); `

#### example of jQuary 
` $(' :header').addClass('headline');
@ $(' l i : lt(3) ').hide(). fadeln(lSOO);
$('li').on('click', function() {
$(this) . remove();
} ) ; `

#### WHY USE JQUERY?
##### jQuery doesn't do anything you cannot achieve with pure JavaScript. It is just a JavaScript file but estimates show it has been used on over a quarter of the sites on the web, because it makes coding simpler. 
##### jQuery's motto is "Write less, do more," because it allows you to achieve the same goals but in fewer lines of code than you would need to write with plain JavaScript. 

#### FINDING ELEMENTS 
##### Using jQuery, you usually select elements using CSS-style selectors. It also offers some extra selectors, noted below with a 'jQ'
##### like : BASIC SELECTORS
1. *
2. element
3. #id
4. .class
5. selectorl, selector2
### LOOPING 
#### In plain JavaScript, if you wanted to do the same thing to several elements, you would need to write code to loop through all of the elements you selected. 
` $('l i em') .addClass('seasonal ') ;
$( ' li .hot') .addClass('favorite'); `

### CHAINING 
#### If you want to use more than one jQuery method on the same selection of elements, you can list several methods at a time using dot notation to separate each one, as shown below


### GETTING ELEMENT CONTENT 

#### The • htm 1 () and • text () methods both retrieve and update the content of elements. This page will focus on how to retrieve element content. To learn how to update element content,

### GETTING AT CONTENT 
#### On this page you can see variations on how the . html() and . text() methods are used on the same list (depending on whether <ul >or <l i > elements are used in the selector). 

### UPDATING ELEMENTS 
#### Here are four methods that update the content of all elements in a jQuery selection . 

1. . html() 
2. . text() 
3. . remove()
4. .replaceWith() 

### GETTING AND SETTING ATTRIBUTE VALUES
#### You can create attributes, or access and update their contents, using the following four methods. 
1. .attr() 
2. . removeAttr() 
3. . addCl ass() 
4. .removeClass() 

### GETTING & SETTING CSS PROPERTIES 

#### The . css () method lets you retrieve and set the values of CSS properties

` ${'li ' ).css( 'padding-left', '+=20' );  `
### LOADING JQUERY FROM A CDN

` <script src=" //ajax .googl eapi s . com/ ajax/l i bs/ jquery / 1.10. 2/ jquery .min. js ">
</ script>
<script>
window .jQuery 11 document. write (' <script src=" j s/j query- 1.10. 2 .j s 11><\jscri pt> ' )
</script> `

### 6 Reasons for Pair Programming

#### Pair programming touches on all four skills: developers explain out loud what the code should do, listen to others’ guidance, read code that others have written, and write code themselves.
#### Everyone has a different approach to problem solving; working with a teammate can expose developers to techniques they otherwise would not have thought of. If one developer has a unique approach to a specific problem, pair programming exposes the other developer to a new solution

#### Pair programming is great for improving social skills. When working with someone who has a different coding style, communication is key. This can become more difficult when two programmers have different personalities. 

