### Lifting state up

Rather than building a lot of functionality to reference and update different elements of a state, it is better to house info in oldest common ancestor.
This meanjs that when you are rendering something based on input and want to keep different elements of the state synced up, if you can pas a state to the 
parent that is updated  such that both child renders can keep track of them.  


### lists and keys

when  generating multiple components, remember to assign individual keys to each element so they are identifiable. So when maping over an array and making elements for each stop, 
each of those should have a key - worst case you can use the index but that has some serious issues if the order gets shuffled at any point. When generating, do it in the .map()
so they get passed already keyed. These keys can help react identify changes to individual elements, so they only have to update those. The ideal way would be to generate a 
unque string for each. Generally that will be IDs from the data object. These keys need to be unique to sibilings - so different trees can have overlapping keys. 

> A good rule of thumb is that elements inside the map() call need keys.  [source](https://reactjs.org/docs/lists-and-keys.html)


One thing to remember is that the keys do not get poassed into components automatically - they have to be passed if you need it. 

> JSX allows embedding any expression in curly braces so we could inline the map() result:

[source](https://reactjs.org/docs/lists-and-keys.html)

  function NumberList(props) {
    const numbers = props.numbers;
    return (
      <ul>
        {numbers.map((number) =>
          <ListItem key={number.toString()}
                    value={number} />
        )}
      </ul>
    );
    }
    
    
###Spread Operator
    
the ... operator is a way to expand an iterable Object (capital O a thing you can pass like an array). it is used to spread out the information so it can 
be referenced together rather than a series of separate iteratable objects. So upi can have [...[1,2,3,4]] evaluating as [1,2,3,4], or even [..."1234"] 
evaluating as ["1", "2", "3", "4"]. 

the other big use is for copying an array. you can say for 

        const ex = [2,4,6,8]
        const exex = [...ex]
        
these two arrays are now independant and mutating one is not an issue. It is telling JS to take the array in ex, and spread out the contents into a new array. 
Effectively copying it. This is great to truely break refernce rather than just exex=ex. This is a SHALLOW  copy and not a DEEP copy, so issues around bug differences are noted. 

For Math.(), the spread can help expand and consolidate an array of numbers. you cannot pass an array to Math.min(example). You can however pass it Math.min(...example. 
THat will spread the numbers in the array so they are evaluated together by the Math.() function. 

To aid in using arrays in arguments, if you are declaring a function that evaluates the items in an array. So if you need to pass elements to a function as separate aruments
the spread operator lets you house inputs in an array, and make edits with those commands, while still being able to feed it directly into a function:

        const fruitStand = ['🍏','🍊','🍌']
        const sellFruit = (f1, f2, f3) => { console.log(`Fruits for sale: ${f1}, ${f2}, ${f3}`) }
        sellFruit(...fruitStand) // Fruits for sale: 🍏, 🍊, 🍌
        fruitStand.pop()
        fruitStand.pop()
        fruitStand.push('🍉')
        fruitStand.push('🍍')
        sellFruit(...fruitStand) // Fruits for sale: 🍏, 🍉, 🍍
        fruitStand.pop()
        fruitStand.pop()
        sellFruit(...fruitStand,'🍋') // Fruits for sale: 🍏, 🍋, undefined
        view rawPassing an array as arguments using the spread operator.js hosted with ❤ by GitHub
    
 [source](https://medium.com/coding-at-dawn/how-to-use-the-spread-operator-in-javascript-b9e4a8b06fab)
 
 The most powerful for me when learning is in adding items to an array. if you have array e=[1,2,3] and you want to add it to anoither array as it is being defined, you 
 would have the new array writen as n=['a', 'b', ...e]
 
 Adding state to a react element with the spread is a good way of updating local storage efficiantly. so when handling an event where something would be added yo local state, 
 you could have the set function read setfunc(func => [...func, Q]) where Q is the element being added. (note to self - this element needs to be practiced)
 
 Chaining spreads are where it really shines. Note that in combining obj like this, name conflicts will be lost. In operators you can approach it like:
        const a={hello:"world"}
        const b={2B:"!2B"}
        const c={...a, ...b, relax:"Don't Do It"}
        const d={...c, newfunc:()=>{do a thing}}
        
        
 For using elements like a node list / arguments object in selector functions, the spread comes again. [...document.query('div')] will expand the results into an array. 
 
 
 Sadly backwards support isnt [great](https://miro.medium.com/max/2400/1*eqKBiABFRy_uEBdchVZ9Qw.png). In these cases Function.prototype.apply() will have the same effect.
 Note that the syntax is 
          FunctionName.apply(this.target, array)
          
 Or use a compiling tool to handle it. 
 
 
 
