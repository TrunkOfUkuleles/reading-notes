
### Questions

1. Name 3 real world use cases where you’d want to change the request with custom middleware
    - you need to add validation
    - you want to add some app level tracking
    - you need to set access

2. True or false: The route handler is middleware?
    TRUE

3. In what ways can a middleware function end the process and send data to the browser?
    If it sends an error through the next() function. Otherwise the erquest continues. 

4. At what point in the request lifecycle can you “inject” middleware?
    In the "middle". It is catching the request object basically right at the gates of the server, before it can fully handle the data,

5. What can cause express to error with “Request headers sent twice, cannot start a second response”
    Trying to setHeader after the .writeHead() was already declaired. So when it errors out, it will have the overlayed new header, and the error.


## Vocab

Middleware: a function designed to take an input, do an action using that input, and pass it along to another middleware / route
Request Object: The object generated on the call to the server
Response Object: The object sent back to the front after the call has been completed
Application Middleware: middleware to enhance an app
Routing Middleware: "Mini-app" style of function that handles a lot of the routing functions. 
Test Driven Development: the process of developing a set of tests you want to baseline meet - then build an app to pass them 
Behavioral Testing: Black Box / functional testing of the program's external behavior

## Preview

Which 3 things had you heard about previously and now have better clarity on?
    - routing logic
    - some of the weird ways they have piled classes into javascript.
    - TDD

Which 3 things are you hoping to learn more about in the upcoming lecture/demo?
    - testing logic
    - how the new routing interacts with route level middleware
    - better ways of doing the db, than my terrible memory sink

What are you most excited about trying to implement or see how it works?
    getting multiple route logic down

### Notes

## Classes
JS is base level is a classless system. That being said, that functionally was added in ES5. Note that the class declarations are not hoisted like a function declaratiuon would. Also note that the body of a class is executed in strict mode. the Constructor in these classes is a special method that creatiung and initializing a new object in that class. Super can be passed for the constructor props.

## Express Routing
how the app URIs respond to requests. by binding the express app, you gain acces to those methods. You can then pass it a handler function, or an invoced function to divy up what gets sent where, and what is sent back. And Express lets us add middleware directly in the middle for greater flexibility.

# [Response Methods](https://expressjs.com/en/guide/routing.html)


--Method--	            --Description--
res.download()	    Prompt a file to be downloaded.
res.end()	        End the response process.
res.json()	        Send a JSON response.
res.jsonp()	        Send a JSON response with JSONP support.
res.redirect()	    Redirect a request.
res.render()	    Render a view template.
res.send()	        Send a response of various types.
res.sendFile()	    Send a file as an octet stream.
res.sendStatus()    Set the response status code and send its string representation as the response body.

# Express.Router
by utilizing the Router Method from Express, you can make modular, mountable route handlers. It is a built in middleware (mini-app). Allows for cleaner implimentation in distributing route logic, and implimenting middleware on various layers. 