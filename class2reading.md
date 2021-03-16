##class 2 reading

rather than using functions, by transitioning to a Class extend for, you can add   

```
    constructor(props) {
    super(props);
    this.state = {date: new Date()};
  }
  (https://reactjs.org/docs/state-and-lifecycle.html) in the beginning. to create states fyou can pass within the render using this.state...
  ```
  
  For "lifecycle methods" you need to tell the class what to do when you mount or unmount the element. you can do so in the render section:
  
  ```
  componentDidMount() {
  }

  componentWillUnmount() {
  }
  ```
  
  for something like a clock, the componentdidmount can house a function to set funtion handling the date. The unmount will help clear that info so it doesn't interfere
  as you reload the page. 
  
  when it comes to working wit the state, do not directly touch. Instead use setState(). this.state can only be setin the constructor. When you are setting state for
  multiple elements that may update seperately, you shold not call them both with set state. Rather than:
  
  ```
  this.setState({
  counter: this.state.counter + this.props.increment,
  });
  ```

  and instead move it into a function to take both elements and deal with them together 

  ```
  this.setState((state, props) => ({
  counter: state.counter + props.increment
  }));
  ```

  The set state is a merge of the original object with the update. It will shallow replace the changes while not touching any other variables it might have.
    remember that the data being passed in can only flow down the tree.
    
    
**    
    React events are named using camelCase, rather than lowercase.**
  
   for react, rather than passing a "function()" as a string you pass it as a direct reference using {function}. for handling default actions, you must also use 
   .preventDefault() rather than returning false. For binary states, the handle function can set the state. Within the render you can then refernce that state
   either directly {} or using if statements. remember in JSX, this must be bound in the constructor. Any handler functions must be referenced in the constructor:
   (https://reactjs.org/docs/handling-events.html)
   
   ```
   class Toggle extends React.Component {
  constructor(props) {
    super(props);
    this.state = {isToggleOn: true};

    // This binding is necessary to make `this` work in the callback
    this.handleClick = this.handleClick.bind(this);
  }
   ```
   
   
   ##conditional Rendering
   
   If you are calling a function without (), you have to bind it by referencing in the constructor (va 'function()'). You can also use arrow function to bind
   it by writing this.function as the function element in the onClick call. 
   
   
   when it comes to states you toggle, one way to write in React is [state] && expression. If the state evaluates true, the following expression with trigger. 
   
   To keep something from rendering, have it return Null in the render. So for states that check (i.e. a flag rather than a series of choices) you can have a conditional on it. 
   
   
  
  

