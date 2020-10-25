# summery
## How does The web work , anyway?
### Well, it's all pretty amazing really. And the funny thing is that it's all very undervalued. The protocol I mentioned, that he helped write, HTTP, it's capable of all sorts of neat stuff that people ignore for some reason.
## What other kinds of representations are there?
###  Actually, representations is one of these things that doesn't get used a lot. In most cases, a resource has only a single representation. But we're hoping that representations will be used more in the future because there's a bunch of new formats popping up all over the place.
### Well, there's this concept that people are calling “Web Services” or "APIs". It means a lot of different things to a lot of different people but the basic concept is that machines could use the web just like people do.
### The URL, of course. If everything that machines need to talk about has a corresponding URL, you've created the machine equivalent of a noun. That you and I and the rest of the world have agreed on talking about nouns in a certain way is pretty important,
### Machines don't have a universal noun - that's why they suck. Every programming language, database, or other kind of system has a different way of talking about nouns. That's why the URL is so important. It let's all of these systems tell each other about each other's nouns.
### So anyway, HTTP—this protocol Fielding and his friends created—is all about applying verbs to nouns. For instance, when you go to a web page, the browser does an HTTP GET on the URL you type in and back comes a web page.

### Web pages usually have images, right? Those are separate resources. The web page just specifies the URLs to the images and the browser goes and does more GETs using the HTTP protocol on them until all the resources are obtained and the web page is displayed. But the important thing here is that very different kinds of nouns can be treated the same. Whether the noun is an image, text, video, an mp3, a slideshow, whatever. I can GET all of those things the same way given a URL.
## SuperAgent
![img](https://previews.123rf.com/images/noravector/noravector1709/noravector170900217/86271996-super-agent-comic-book-style-word-on-abstract-background-.jpg)
### SuperAgent is light-weight progressive ajax API crafted for flexibility, readability, and a low learning curve after being frustrated with many of the existing request APIs. It also works with Node.js!

`  request
   .post('/api/pet')
   .send({ name: 'Manny', species: 'cat' })
   .set('X-API-Key', 'foobar')
   .set('Accept', 'application/json')
   .then(res => {
      alert('yay got ' + JSON.stringify(res.body));
   }); `
   ### Request basics
   #### A request can be initiated by invoking the appropriate method on the request object, then calling ` .then() `  (or ` .end() `  or  ` await) ` to send the request. For example a simple GET request:
   
   ` request
   .get('/search')
   .then(res => {
      // res.body, res.headers, res.status
   })
   .catch(err => {
      // err.message, err.response
   }); `
   
   ### Absolute URLs can be used. In web browsers absolute URLs work only if the server implements CORS.

`  request
   .get('https://example.com/search')
   .then(res => {

   }); `
   #### DELETE, HEAD, PATCH, POST, and PUT requests can also be used, simply change the method name:

` request
  .head('/favicon.ico')
  .then(res => {

  }); `
  #### Setting header fields Setting header fields is simple, invoke .set() with a field name and val
   `  request
   .get('/search')
   .set('API-Key', 'foobar')
   .set('Accept', 'application/json')
   .then(callback); ` 
    
    
  ###  GET requests
 #### The .query() method accepts objects, which when used with the GET method will form a query-string. The following will produce the path /search?query=Manny&range=1..5&order=desc.

 ` request
   .get('/search')
   .query({ query: 'Manny' })
   .query({ range: '1..5' })
   .query({ order: 'desc' })
   .then(res => {

   }); `
 ###  Setting Accept
##### In a similar fashion to the .type() method it is also possible to set the Accept header via the short hand method .accept(). Which references request.types as well allowing you to specify either the full canonicalized MIME type name as type/subtype, or the extension suffix form as "xml", "json", "png", etc. for convenience:

` request.get('/user')
   .accept('application/json')

 request.get('/user')
   .accept('json')

 request.post('/user')
   .accept('png') `
   
   
   
   
   
   
   
