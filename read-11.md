# summery 
## EJS
![img](https://miro.medium.com/max/720/1*DG4VA127mu4Fx2TrRIzskw.jpeg)
1. first to install EJS you have to write this ` npm install `
2.  then you have to require it in server.js so you have to write ` let ejs = require('ejs'); `
3.  then We also have to set EJS as the view engine for our Express application using ` app.set('view engine', 'ejs'); `
### before complete we have to know what is the EJS ???
#### EJS is a simple templating language that lets you generate HTML markup with plain JavaScript. No religiousness about how to organize things. No reinvention of iteration and control-flow. It's just plain JavaScript.
### the benefite of EJS is :
1. Use plain JavaScript 
2. Fast development time
3. Simple syntax
4. Active development : EJS has a large community of active users, and the library is under active development
5. Easy debugging
6. Speedy execution
### now let's complete about EJS how to use it :
4. we have to creat a file for html call it  ` index.ejs `
5. as we know every thing if we want to appear we have to use response so to appear our result we have to say inside a function ` response.render('index') `
### in the undex let's learn who to write inside it 
1. Use ` <%- include('RELATIVE/PATH/TO/FILE') %> ` to embed an EJS partial in another file.
2. in the ejs ther are a tage can help you like 
-  ` <% ` 'Scriptlet' tag, for control-flow, no output
- ` <%_ ` ‘Whitespace Slurping’ Scriptlet tag, strips all whitespace before it
- ` <%= ` Outputs the value into the template (HTML escaped)
- ` <%- ` Outputs the unescaped value into the template
- ` <%# ` Comment tag, no execution, no output
- ` <%% ` Outputs a literal ` '<%' `
- ` %> ` Plain ending tag
- ` -%> ` Trim-mode ('newline slurp') tag, trims following newline
- ` _%> ` ‘Whitespace Slurping’ ending tag, removes all whitespace after it
### now let's take an example if we want to Injecting values into the views
1. first in the index we have to add ` <h1> hello <%= foo %></h1> ` 
2. then in the server.js you have to write ` response.render('index' , { foo: (example) 'bar'} `
3. the rusalt it will be : 
# hello bar

### now let's learn if we want to make unorder list :
1. in the server we have to write ` response.render('index' , { people:[ { name : 'joudi'} { name : 'sami'}]} `
2. now in the index you have to write ` <ul>  <% for(var person of people ) { %> <li><%= person.name %></li>  <% }%>  </ul> `
3. this is will give unorder list like :
- joudi 
- sami

## i just now give you an example  about EJS if you you want to learn more this link will help you [link](https://www.youtube.com/watch?v=tJM2wqzPiJk&list=PL7sCSgsRZ-slYARh3YJIqPGZqtGVqZRGt&index=5)

### thanks for reading and have a good day ;)





















