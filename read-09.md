# sammury

## Concepts of Functional Programming in Javascript
![img](https://miro.medium.com/max/800/1*JyVlvqwsCBYl2FuvPFVRZQ.png)
### What is functional programming?
#### Functional programming is a programming paradigm — a style of building the structure and elements of computer programs — that treats computation as the evaluation of mathematical functions and avoids changing-state and mutable data 
### Pure functions benefits
### The code’s definitely easier to test. We don’t need to mock anything. So we can unit test pure functions with different contexts:Given a parameter` A `→ expect the function to return value B Given a parameter` C `→ expect the function to return value D
### A simple example would be a function to receive a collection of numbers and expect it to increment each element of this collection.
` let list = [1, 2, 3, 4, 5]; const incrementNumbers = (list) => list.map(number => number + 1); `
### Immutability
![img1](https://www.cronj.com/blog/wp-content/uploads/immutable-3.png)
#### When data is immutable, its state cannot change after it’s created. If you want to change an immutable object, you can’t. Instead, you create a new object with the new value.
#### It is also very common to build up the final state of an object. Imagine we have a string, and we want to transform this string into a url slug.
#### In OOP in Ruby, we would create a class, let’s say, UrlSlugify. And this class will have a slugify! method to transform the string input into a url slug.
#### Here we have:
1. toLowerCase: converts the string to all lower case
2. trim: removes whitespace from both ends of a string
3. split and join: replaces all instances of match with replacement in a given string
#### We combine all these 4 functions and we can "slugify" our string.
## Higher-order functions
![img3](https://i.morioh.com/b8d4a314b2.png)
### When we talk about higher-order functions, we mean a function that either: takes one or more functions as arguments, or returns a function as its result The doubleOperator function we implemented above is a higher-order function because it takes an operator function as an argument and uses it.
## Filter
![img5](https://i.ytimg.com/vi/EzB6Pk66XW8/maxresdefault.jpg)
### Given a collection, we want to filter by an attribute. The filter function expects a` true ` or` false ` value to determine if the element should or should not be included in the result collection. Basically, if the callback expression is true, the filter function will include the element in the result collection. Otherwise, it will not.

## Map
![img6](https://media.proglib.io/wp-uploads/2019/08/js-map-reduce-filter-2.png)
### The` map ` method transforms a collection by applying a function to all of its elements and building a new collection from the returned values.
### First, we learned about immutability. We know how immutability is important to make our functions more consistent and predictable. The idea is to build a new collection with all absolute values.
## Reduce
### The idea of reduce is to receive a function and a collection, and return a value created by combining the items.
### A common example people talk about is to get the total amount of an order. Imagine you were at a shopping website. You’ve added Product 1, Product 2, Product 3, and Product 4 to your shopping cart (order). Now we want to calculate the total amount of the shopping cart.
### thanks for reading if you want to know more this link will help you [link](https://medium.com/the-renaissance-developer/concepts-of-functional-programming-in-javascript-6bc84220d2aa)
