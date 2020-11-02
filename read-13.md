# summery
## Sending form data
![img](https://developer.mozilla.org/files/4291/client-server.png)
#### Once the form data has been validated on the client-side, it is okay to submit the form. And, since we covered validation in the previous article, we're ready to submit! 
### now we will looks at what happens when a user submits a form — where does the data go, and how do we handle it when it gets there?
#### At it's most basic a client (usually a web browser) sends a request to a server (most of the time a web server like Apache, Nginx, IIS, Tomcat, etc.), using the HTTP protocol. 
#### An HTML form on a web page is nothing more than a convenient user-friendly way to configure an HTTP request to send data to a server. This enables the user to provide information to be delivered in the HTTP request.
1. i will start with the The action attribute
##### The action attribute defines where the data gets sent. Its value must be a valid relative or absolute URL. If this attribute isn't provided, the data will be sent to the URL of the page containing the form — the current page.
-  this is an example : ,the data is sent to an absolute URL — https://example.com: ` <form action="https://example.com"> `

-  Here, we use a relative URL — the data is sent to a different URL on the same origin: ` <form action="/somewhere_else"> `
-  and if we When specified with no attributes, as below, the <form> data is sent to the same page that the form is present on: ` <form> `
2. The method attribute
##### The method attribute defines how data is sent. The HTTP protocol provides several ways to perform a request; HTML form data can be transmitted via a number of different methods, the most common being the GET method and the POST method
- The GET method : The ` GET `  method  is the method used by the browser to ask the server to send back a given resource: "Hey server, I want to get this resource.
- The POST method : The ` POST ` method is a little different. It's the method the browser uses to talk to the server when asking for a response that takes into account the data provided in the body of the HTTP request: "Hey server, take a look at this data and send me back an appropriate result.
### summery 
#### As we'd alluded to above, sending form data is easy, but securing an application can be tricky. Just remember that a front-end developer is not the one who should define the security model of the data.
## that 's it for today if you feel you want to know more this link will help you [link](https://www.youtube.com/playlist?list=PL4cUxeGkcC9g5_p_BVUGWykHfqx6bb7qK)










