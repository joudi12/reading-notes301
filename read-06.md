# summery
## What Is Node and When Should I Use It?
![img](https://www.noupe.com/wp-content/uploads/2018/06/nodejs-whyandhow-featured.jpeg)
### So you’ve heard of Node.js, but aren’t quite sure what it is or where it fits into your development workflow. Or maybe you’ve heard people singing Node’s praises and now you’re wondering if it’s something you need to learn. Perhaps you’re familiar with another back-end technology and want to find out what’s different about Node.
### What Is Node.js?

#### Node Is Built on Google Chrome’s V8 JavaScript Engine
#### The V8 engine is the open-source JavaScript engine that runs in Google Chrome and other Chromium-based web browsers, including Brave, Opera, and Vivaldi. It was designed with performance in mind and is responsible for compiling JavaScript directly to native machine code that your computer can execute.
#### This means that Node.js is a program we can use to execute JavaScript on our computers. In other words, it’s a JavaScript runtime.

### How Do I Install Node.js?

#### Many websites will recommend that you head to the official Node download page and grab the Node binaries for your system. While that works, I would suggest that you use a version manager instead. This is a program that allows you to install multiple versions of Node and switch between them at will. There are various advantages to using a version manager. For example, it negates potential permission issues when using Node with npm and lets you set a Node version on a per-project basis.
#### you can check that Node is installed on your system by opening a terminal and typing ` node -v `. If all has gone well, you should see something like ` v12.14.1 ` displayed. This is the current LTS version at the time of writing.

 #### Next, create a new file ` hello.js ` and copy in the following code:

` console.log("Hello, World!"); `

#### This uses Node’s built-in console module to display a message in a terminal window. To run the example, enter the following command:

` node hello.js `
#### If Node.js is configured properly, “Hello, World!” will be displayed.
### Introducing npm, the JavaScript Package Manager
#### As I mentioned earlier, Node comes bundled with a package manager called npm. To check which version you have installed on your system, type ` npm -v. `

#### In addition to being the package manager for JavaScript, npm is also the world’s largest software registry. There are over 1,000,000 packages of JavaScript code available to download, with billions of downloads per week. Let’s take a quick look at how we would use npm to install a package.
### Working with the package.json File
#### f you look at the contents of the test directory, you’ll notice a folder entitled ` node_modules. ` This is where npm has saved lodash and any libraries that lodash depends on. The node_modules folder shouldn’t be checked in to version control, and can, in fact, be re-created at any time by running npm install from within the project’s root.

#### If you open the package.json file, you’ll see lodash listed under the dependencies field. By specifying your project’s dependencies in this way, you allow any developer anywhere to clone your project and use ` npm ` to install whatever packages it needs to run.
### The Node.js Execution Model
![img2](https://uploads.sitepoint.com/wp-content/uploads/2012/10/1516152673node_event_loop.png)
#### In very simplistic terms, when you connect to a traditional server, such as Apache, it will spawn a new thread to handle the request. In a language such as PHP or Ruby, any subsequent I/O operations (for example, interacting with a database) block the execution of your code until the operation has completed. That is, the server has to wait for the database lookup to complete before it can move on to processing the result. If new requests come in while this is happening, the server will spawn new threads to deal with them. This is potentially inefficient, as a large number of threads can cause a system to become sluggish — and, in the worst case, for the site to go down. The most common way to support more connections is to add more servers.

#### Node.js, however, is single-threaded. It’s also event-driven, which means that everything that happens in Node is in reaction to an event. For example, when a new request comes in (one kind of event) the server will start processing it. If it then encounters a blocking I/O operation, instead of waiting for this to complete, it will register a callback before continuing to process the next event. When the I/O operation has finished (another kind of event), the server will execute the callback and continue working on the original request. Under the hood, Node uses the libuv library to implement this asynchronous (that is, non-blocking) behavior.

