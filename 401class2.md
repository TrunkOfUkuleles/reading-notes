



## Questions

1. What’s the difference between PUT and PATCH?
    Both are set as an "update", but PUT will replace the resouce with a modified version. PATCH will modify the resource directly. 

2. Provide links to 3 services or tools that allow you to “mock” an API for development like json-server

    [Swagger](https://inspector.swagger.io/builder)
    [apiDoc](https://apidocjs.com/)
    [Postman](https://www.postman.com/)
    [Insomnia](https://insomnia.rest/)


3. Compare and contrast Swagger and APIDoc.js 
    API doc is more granular amd rigid, whereas Swagger is a little more flexible about keeping everything updated for params/auths

4. Which HTTP status codes should be sent with each type of (un)successful API call?
        200 - ok
        201 - created
        204 - no content

        404 - not found
        500 - server error
        400 - bad request


5. Compare and contrast SOAP and ReST
    REST BEGINS WHERE SOAP LEFT OFF. but really SOAP is the classic protocol using other standardized protocols, with advanced security features. REST is an architectural style. This gives you guidlines to build a system that  can interact in the basic ways you need, with less stringent needs and complexity. 

## Document terms

Web Server: where the rout handler lives to accept calls and supply the response
Express: a Node framework to help backend servers speak to each other
Routing: the process by which you link a call sent to a place, and the logic that directs where the information is "sent"
WRRC: Web Request Response Cycle

### Notes

## Express / Node

# Node
Open Source, run-time environment for javascript. designed for use on an OS, not server - very scale-able. Also gives you npm to get tools easily.

# Express
Node web framework. Standardization of handling requests with different paths. inserts data into templates. Midleware integration

## npm 
Largest software repo. consists of the website, CLI, and registry. the website allows you to discover packages and set up profiles. 
The CLI is when you call from the terminal. and the registery is a large public db with the packages and metatdata availible. YOu can integrate from the command line, download packages without installing them, share code, virtual teams, update apps, etc.

## TDD
Test driven [development](https://www.agilealliance.org/glossary/tdd/#q=~(infinite~false~filters~(postType~(~'page~'post~'aa_book~'aa_event_session~'aa_experience_report~'aa_glossary~'aa_research_paper~'aa_video)~tags~(~'tdd))~searchTerm~'~sort~false~sortDirection~'asc~page~1)):

1. write a “single” unit test describing an aspect of the program
2. run the test, which should fail because the program lacks that feature
3. write “just enough” code, the simplest possible, to make the test pass
4. “refactor” the code until it conforms to the simplicity criteria
5. repeat, “accumulating” unit tests over time

you can fall into issues where you forget testing along the way, so are not sure where it is breaking. Or being overly ambitious with how many testsyou develope. Or testing very simple/non critical parts. This is made worse when the team doesn't all adopt it. That leaves less info about which tests are passing, and what still needs to be addressed. Or just a test suite that is not updated to keep up with the functional requirements.

## CI / CD
Continuous Integration / Continuous Delivery/Deployment. Workflow to keep merge conflicts to a minimum. Keeps dev branches from wandering too far from the common main. A CI server will have the information to test against the common main, so every step further still maintains checks to merge back to the main. Continuous delivery is a style where you code in such a way where you can deploy at anytime while some development continues. Continuous Delivery adds automation to the workflow where you can see where branches cannot merge by automatically getting the current main, merging, and deploying in a virtual environment to test the ability to merge back. 