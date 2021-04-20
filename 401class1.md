

### Array.map()

a built in javascript function that will take an array, and apply a callback function to each element, and returns a new array with the rsults of each element. 

### Array.reduce()

a built in javascript function that takes an array, and passes each element of the array through a callback, and will carry over the results through the chain. The results returned at the end have to be in the form of one thing - that can be an object, or a number, etc.

### superagent()
    
```
                superagent.get(url).then(res => {do a thing}).catch(err => {console.log(err)}) 


                function test (){
                    return new Promise(res => {console.log('test')})}

                async function testerer(){const test = await test()}
```

### Promises

    Promises are the sneaky little way JS can handle so many things these days. It is a system where you can send for a peice of information
    and instead of waiting for the information to come back from a server (let's say), it will generate a promise - marking where the information is expected. This gives the engine some time to continue running oter functions that do not have the same requirements. When the data
    arrives, it is slotted into the proper place, and when the event loop is clear, it will start to handle promises.

### Callbacks

    No, callback functions are not asynchronous. The async nature itself was built for that very reason. JS is very regimented in timing - at least that is what single threaded operations have been limited by. The promise structure gave an ability to spin more plates. A callback is just a function that you are referencing in state by it's "key". It can be async, but more often than not it will be operating within it's own Execution context and will not need to wait on a call. 