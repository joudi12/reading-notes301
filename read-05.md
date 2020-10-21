# summery
## Node.js For Beginners. Deploy Your Blog to Heroku
![img](https://miro.medium.com/max/1200/0*vu5pZbwHCCKbkAPh.png)
### Error pages are not what typically appear on your screen when you're surfing the web, but when it happens it's so annoying! To see how servers work from within, we will build a simple web server by ourselves. We will use Node.js as a server part technology for that task. Then we'll use Heroku cloud application platform to turn this local server into a world wide server.
#### First of all, we need to create a JavaScript file. Let's name it server.js:
` var http = require("http");

http.createServer(function(request, response) {
  response.writeHead(200, {"Content-Type": "text/plain"});
  response.write("It's alive!");
  response.end();
}).listen(3000); `
#### It's simple. It's tiny. But it's a server! Let's make sure it's working. Run at your terminal:
` node server.js `
#### But you should notice something, before we go further. Let's look more closely at our first Node server. This is an example of how Node provides you with non-blocking and event-driven behavior. Let me explain:
` $.post('/some_requested_resource', function(data) {
  console.log(data);
}); `
#### First step after Heroku installation is to log in to the system from your computer:
` heroku login `
#### reate your project directory. And then create the server.js file inside of it. First of all, let's declare some variables:
` var http = require("http");
var fs = require("fs");
var path = require("path");
var mime = require("mime"); `
 #### Create the package.json file and fill it with proper information. Here's mine:
 ` {
  "name" : "blog",
  "version" : "0.0.1",
  "description" : "My minimalistic blog",
  "dependencies" : {
    "mime" : "~1.2.7"
  }
} `

#### We will now create send404() function. It will handle the sending of 404 error, which usually appears when requested file doesn't exist:
` function send404(response) {
  response.writeHead(404, {"Content-type" : "text/plain"});
  response.write("Error 404: resource not found");
  response.end();
} ` 
#### Now we will define sendPage() function. It first writes the header and then sends the contents of the file:
` function sendPage(response, filePath, fileContents) {
  response.writeHead(200, {"Content-type" : mime.lookup(path.basename(filePath))});
  response.end(fileContents);
} ` 
#### Now we'll define how our server will handle responses. This function will return the content of the requested file or the 404 error otherwise:
` function serverWorking(response, absPath) {
  fs.exists(absPath, function(exists) {
    if (exists) {
      fs.readFile(absPath, function(err, data) {
        if (err) {
          send404(response)
        } else {
          sendPage(response, absPath, data);
        }
      });
    } else {
      send404(response);
    }
  });
} `
#### And now it's time to create the HTTP server:
` var server = http.createServer(function(request, response) {
  var filePath = false;

  if (request.url == '/') {
    filePath = "public/index.html";
  } else {
    filePath = "public" + request.url;
  }

  var absPath = "./" + filePath;
  serverWorking(response, absPath);
}); `
#### Now we need to start our server. And here's the tricky part. Do you remember how we told the server to listen to the 3000th port in our first example? No? I'll remind you:
` http.createServer(<some code here>).listen(3000) `
#### We can do it when we run our server locally. But Heroku sets a dynamically assigned port number to your app. That's why we need to handle all this mess with ports as it’s shown below:
` var port_number = server.listen(process.env.PORT || 3000); `
### It's Heroku time!
#### Open your terminal within your project folder. For my Linux it's:
` cd /path/to/my/project` 
#### Then run: ` git init `
#### Then run: ` git add . `
#### Now commit your files to the initialized Git repo: `git commit -m "Simple server functionality added" `
#### ` heroku create `
#### Now we can deploy our project. Every Heroku app starts with no branches and no code. So, the first time we deploy our project, we need to specify a remote branch to push to:
` git push heroku master `
#### The application is now deployed. Ensure that at least one instance of the app is running:
` heroku ps:scale web=1 `
#### And now, before we open it, it's time to choose a proper name for our first creation. I called it myfirstserver:
` heroku apps:rename myfirstserver `
#### Everything is done. You can try it now:
` heroku open `
#### This command will open your Heroku project in your web browser. In this particular case, server address is https://myfirstserver.herokuapp.com/. Now you can share your first web application with any person you want.
 


















