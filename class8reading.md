### SuperAgent Docs
[Source](https://visionmedia.github.io/superagent/)

                 request
                .post('/api/pet')
                .send({ name: 'Manny', species: 'cat' })
                .set('X-API-Key', 'foobar')
                .set('Accept', 'application/json')
                .then(res => {
                    alert('yay got ' + JSON.stringify(res.body));
                });



## Get Request
invoke the action onto the request object. Chain together with .then(), .end(), etc. invoke using ()=>{} in the action.

can pass HTTP as a string               request('GET', '/search').then(success, failure);


## Other requests - DELETE, HEAD, PATCH, POST, PUT

delete can be called as .del() for legacy. .set() wll set the header field with a name and value pair. 
                request
   .get('/search')
   .set({ 'API-Key': 'foobar', Accept: 'application/json' })
   .then(callback);

   ## .query()
   accepts objects, use with GET