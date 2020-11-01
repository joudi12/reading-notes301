# summery
## EJS Partials
![img](https://i.imgur.com/SLw76RB.jpg)
### Partials come in handy when you want to reuse the same HTML across multiple views. Think of partials as functions, they make large websites easier to maintain as you don’t have to go and change a piece of text in every page it appears in. Instead, you define that reusable bundle of code in a file andinclude it wherever you need it.

#### to understand you need example and i will share an example with you 
1. Let’s go ahead and create those partials. Under the views/partials/ directory create a file callednavbar.ejs which will contain only the HTML for the navigation bar at the top of the home and post pages:
`   <div class="header clearfix"> `
      `  <nav> `
         `   <ul class="nav nav-pills pull-right"> `
               `  <li role="presentation"><a href="/">Home</a></li> `
           ` </ul> `
         `   <h3 class="text-muted">Node.js Blog</h3> `
     `  </nav> `
 `   </div> `



2. and a file called footer.ejs in that same directory:
`  <footer class="footer"> `
      `  <p>© 90210 Lawyer Stuff.</p> `
  `  </footer> `
  #### Now that we have our partials defined, we can use them in our home.ejs and post.ejs templates! In EJS, any JavaScript or non-HTML syntax you include in your templates is always surrounded by <% %> delimiters (you could change these delimiters if you really wanted to).
  ## note : The <%- %> tags allow us to output the unescaped content onto the page (notice the -). This is important when using the include() statement since you don’t want EJS to escape your HTML characters like ‘<’, ‘>’, etc…
  3. Let’s create the homepage template in views/home.ejs and include the navbar and footer partial we just created:
  `   <body> `
      `  <div class="container"> `
         `   <%- include('partials/navbar') %> `
         `   <div class="jumbotron"> `
              `  <h1>All about Node</h1> `
               ` <p class="lead">Check out our articles below!</p> `
          `  </div> `
       `     <div class=" row"> `
             `   <div class="col-lg-12"> `
                   ` <div class="list-group"> `
                   `   <!-- loop over blog posts and render them --> `
                    ` LIST_OF_POSTS `
                  `  </div> `
              `  </div> `
         `   </div> `
           `  <%- include('partials/footer') %> `
     `   </div> `
  `  </body> `
  `  </html> `
  
  #### As you can see creating and including partials is very straightforward with EJS. I’ve intentionally left in some placeholders such as LIST_OF_POSTS, POST_TITLE, POST_AUTHOR, and POST_CONTENT so that we can take a look at how we can pass data from our Node + Express application to our views in the next section.
  ##### some quastion 
  1.  Do I need to know Angular 1 before taking this course?
  #### No! Angular 2 is an entirely new framework and this course assumes no prior knowledge of Angular.
  2. Why is the course with TypeScript? Why not Javascript?
  #### TypeScript is a superset of Javascript, meaning any valid Javascript code is valid TypeScript. If you can write Javascript code, you can write TypeScript code! So you don’t have to learn a new programming language. TypeScript brings many useful features to Javascript that are missing in the current version of Javascript. We get classes, modules, interfaces, properties, constructors, access modifiers (e.g. …
  ### dont forqet to install and make your reposetory 
  ## that's it for today if you fill you want to learn more this link will help you [link](https://www.youtube.com/watch?v=3_xEEH4fTEk&t=0s&index=7&list=PL7sCSgsRZ-slYARh3YJIqPGZqtGVqZRGt)
  
  
  
  
  
  
  
  
  
