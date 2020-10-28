# summery 
## The JavaScript Call Stack - What It Is and Why It's Necessary
![img](https://cdn-media-1.freecodecamp.org/images/1*-WOpjPy_2Idl4jIAzPokRQ.jpeg)
#### The JavaScript engine (which is found in a hosting environment like the browser), is a single-threaded interpreter comprising of a heap and a single call stack. The browser provides web APIs like the DOM, AJAX, and Timers.
#### also the A call stack is a mechanism for an interpreter (like the JavaScript interpreter in a web browser) to keep track of its place in a script that calls multiple functions — what function is currently being run and what functions are called from within that function

#### At the most basic level, a call stack is a data structure that uses the Last In, First Out (LIFO) principle to temporarily store and manage function invocation (call).
##### Let us take a look at a code sample to demonstrate LIFO by printing a stack trace error to the console.
` function firstFunction(){
  throw new Error('Stack Trace Error');
}function secondFunction(){
  firstFunction();
}
function thirdFunction(){
  secondFunction();
}thirdFunction();`

#### When the code is run, we get an error. A stack is printed showing how the functions are stack on top each other.
#### Temporarily store: When a function is invoked (called), the function, its parameters, and variables are pushed into the call stack to form a stack frame. This stack frame is a memory location in the stack. The memory is cleared when the function returns as it is pop out of the stack.
![img2](https://cdn-media-1.freecodecamp.org/images/QgR2uIk7tW0YNz0Xm8g0jAPeRFI0e4sCejsv)
### What causes a stack overflow?
#### A stack overflow occurs when there is a recursive function (a function that calls itself) without an exit point. The browser (hosting environment) has a maximum stack call that it can accomodate before throwing a stack error.
## In summary
1. It is single-threaded. Meaning it can only do one thing at a time.
2. Code execution is synchronous.
3. A function invocation creates a stack frame that occupies a temporary memory.
4. It works as a LIFO — Last In, First Out data structure.
## JavaScript error messages && debugging
![img3](https://miro.medium.com/max/2100/1*LHpmsxV3f2znpxhuAFuIqA.png)
#### Most of your time as a developer is spent reading code followed by debugging that same code, most likely to be able to read it or solve an “unexpected feature” (which, joking aside, is more correctly known as a “bug”).
### Types of error messages
1. The first thing that indicates you that something is wrong with your code is the (in)famous error message that the one we saw just moments ago, it usually appears on your console
2. Syntax errors I know it’s in the name of the errors, but like it says itself, this occurs when you have something that cannot be parsed in terms of syntax, like when you try to parse an invalid object using JSON.parse.
3. Range errors Try to manipulate an object with some kind of length and give it an invalid length and this kind of errors will show up.
## Debugging
![img4](https://www.jrebel.com/sites/rebel/files/image/2019-11/image-blog-5-java-debugging-problems.jpg)
#### To debug your JS code, the easiest and maybe the most common way its to simply console.log() the variables you want to check or, by using chrome developer tools,
#### hint about it :
- If the line you selected was run you will be able to see what has happened before that point and you can try and evaluate the next lines to check if everything is outputting what you are expecting.
- You can also add conditional breakpoints by right-clicking a previous set breakpoint, 


#### thanks for reading have a good day ....joudi ......







