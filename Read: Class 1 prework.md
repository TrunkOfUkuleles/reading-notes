## JSX notes (https://reactjs.org/docs/introducing-jsx.html):

JSX is a syntax that is written like HTML but can be produced as react elements with JS abiliities. The main improvement being state tracking and automatic updating.
you can pass through dynamic information using {} within the html syntax. When rendered by the Dom it will be read as HTML with the variables filled in. This includes in HTML attributes.
it is functionally the same to use JSX syntax or using React.createElement().

''
const name = 'Josh Perez';
const element = <h1>Hello, {name}</h1>;

ReactDOM.render(
  element,
  document.getElementById('root')
);
''

Warning:

Since JSX is closer to JavaScript than to HTML, React DOM uses camelCase property naming convention instead of HTML attribute names.
For example, class becomes className in JSX, and tabindex becomes tabIndex.



## React Cheat Sheet (https://reactjs.org/tutorial/tutorial.html#setup-option-2-local-development-environment):

class Board extends React.Component {
  renderSquare(i) {
    return <Square value={i} />;
  }
}

//pass through props (i) to reference within nested react components. Passes it as a prop named 'value'

class Square extends React.Component {
  render() {
    return (
      <button className="square">
        {this.props.value}
      </button>
    );
  }
}

//the value can be referenced within as 'this.props.value'. Remember {} around props being passed in.

// ** In JavaScript classes, you need to always call super when defining the constructor of a subclass.
//    All React component classes that have a constructor should start with a super(props) call.

class Square extends React.Component {
  constructor(props) {
    super(props);
    this.state = {
      value: null,
    };
  }

  render() {
    return (
      <button className="square" onClick={() => alert('click')}>
        {this.props.value}
      </button>
    );
  }
}

// you can use constructors to assign states to elements. Referencing that state/displaing on change/click will add a lot of functionality to a page

onClick={() => this.setState({value: 'X'})}

// in this caseyou can change to .setState as the action. When called that will reload the react component without a manual reload.
// when tracking multiple children, keep overall info stored on the parent.

// when passing props via a click, try {() => this.handleClick(i)} where handleClick is a function defined on the parent element.
// remember .slice() to make compies of data before mutation. similarly concat() method doesn’t mutate the original array vd push().



function Square(props) {
  return (
    <button className="square" onClick={props.onClick}>
      {props.value}
    </button>
  );
}

//rather than extending classes, you can make them into function components. it will only render, so calling it will reload.
//use a Key prop with childs to keep location straight as changes are made. can pass prop info via {}


## Rendering elements (https://reactjs.org/docs/rendering-elements.html)

In react start with a single root DOM node

<div id='root>
         |    for an element containing HTML with a JSX prop
         V
ReactDOM.render ( el , document.getElementById('root')
                                                     
this is static and immutable. it must be recalled for the render update to take place unless a state is triggered. 
The update however will only take place on elements that have changed.
                                                     






