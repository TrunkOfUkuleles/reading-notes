

### QUESTIONS

1. Explain what a “Singleton” is (in Computer Science terms)
    Design where you have a single instance of a class at instanciation for use throughout. 

2. Explain how the Singleton pattern can be used with Node modules, specifically with classes
    Node modules  have used class (or the versions of it that have come from react) to set a global state and have easy acces to information during production

3. If you were tasked with building a middleware system like Express uses, what approach might you take to construct/operate it?
    (knowing nothing) it might be a good idea to have a built in encryption and anonymizer layer on the client side so that the information is encrypted as a standard, and doesn't leave the computer without a check. Though that probably makes the threat of being cracked way too high. 


### Vocabulary

Router Middleware: a peice of software that is invoked on an incoming request object to help add logic based on client variables. 
Dynamic Module Loading: the require(...) and await import(...) syntax
Singleton Pattern: Something like an app object instantiation, a single instance of a thing that typically handles it's own launch. 
CRUD -> REST Method Matches {create: POST, read: GET, Update: PUT, Destroy: DELETE}
Mock Testing: Running tests on a virtual server instance, so any data you upload, will not clog up the main app. 

## Preview

Which 3 things had you heard about previously and now have better clarity on?
    hashing, 64 character max, dynamic vs static loading.
Which 3 things are you hoping to learn more about in the upcoming lecture/demo?
    hashing, middleware, singleton vs fuinctional
What are you most excited about trying to implement or see how it works?
    how much the hashing process clicks for me. 


### Securing Passwords

Hashing passwords is important part of security, but modern GPUs can brute force find the key for more simple encryption systems in about an hour. Key Stretching is one technique to increase the amout of complexity and time it takes to check a possiblepassword - making brute force attacks much harder. 

### Basic Access Authentication

method for providing a username and password in a request. The header field get an authorization id. This does not provide any security outside of some Base64 encryption in transit. 

## Server vs Client side
server side check means the user is sending auth info to the server, and the server response with the appropriate acction for the uders access. To handle it on the client side, you can encrypt the info and include in the header. 

### Security Tips
don't have internal and client side authorization solutions in the same place. similarly, keep those accounts completely off the public side. Password length these days is 8 min, and a common max is 64. the max helps agains DoS. 