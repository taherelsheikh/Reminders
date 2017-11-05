<p align="center">
<img src="https://upload.wikimedia.org/wikipedia/commons/thumb/a/a7/React-icon.svg/512px-React-icon.svg.png" width="350">
</p>


# React 

#### This is how React works
- A JSX element renders.
- The entire virtual DOM updates.
- The virtual DOM "diffs," comparing its current self with its previous self.
- Part of the real DOM updates.
- The screen looks different than it used to.



## React Outline  

- [JSX](#jsx) 
- [Components](#components)
- [Props](#props)
- [State](#state)
- [Passing Info](#passing-info)


## JSX
- [JSX Elements](#jsx-elements)
- [Render an element](#render-an-element)
- [Variable Attributes JSX](#variable-attributes-jsx)
- [Events in JSX](#events-in-jsx)
- [Conditionals JSX](#conditionals-jsx)
- [&& Conditionals](#&&-conditionals)
- [map in JSX](#map-in-jsx)

#### JSX Elements
```javascript 
// Elelment One
const h1 = <h1> Hello World </h1>;

// Elelment Two
let myDiv = (
  <div>
    <h1>
      Hello World
    </h1>
  </div> 
);
```
#### Render an element 

```javascript
// Example 1
import React from 'react';
import ReactDOM from 'react-dom';

ReactDOM.render(<h1>Hello world</h1>,
document.getElementById('app'));

// Example 2
import React from 'react';
import ReactDOM from 'react-dom';

let myList = (
<ul>
  <li>I</li> 
  <li>AM</li> 
  <li>THE BEST</li> 
</ul> 
);

ReactDOM.render(myList,
 document.getElementById('app'));
```

#### Variable Attributes JSX
```javascript 
import React from 'react';
import ReactDOM from 'react-dom';

const goose = 'https://s3.amazonaws.com/codecademy-content/courses/React/react_photo-goose.jpg';

// Declare new variable here:
let gooseImg = (
<img src={goose} />
);

ReactDOM.render(gooseImg, 
document.getElementById('app'));
```

#### Events in JSX
events is like onClick or onMouseOver

```javascript 
import React from 'react';
import ReactDOM from 'react-dom';

function makeDoggy(e) {
  // Call this extremely useful function on an <img>.
  // The <img> will become a picture of a doggy.
  e.target.setAttribute('src', 'https://s3.amazonaws.com/codecademy-content/courses/React/react_photo-puppy.jpeg');
  e.target.setAttribute('alt', 'doggy');
}

const kitty = (
	<img 
		src="https://s3.amazonaws.com/codecademy-content/courses/React/react_photo-kitty.jpg" 
		alt="kitty"
    // Event
    onClick = {makeDoggy}/>
);

ReactDOM.render(kitty,
document.getElementById('app'));
```

#### Conditionals JSX

```javascript 
// Example 1

const headline = (
  <h1>
    { age >= drinkingAge ? 'Buy Drink' : 'Do Teen Stuff' }
  </h1>
);

// Example 2
import React from 'react';
import ReactDOM from 'react-dom';

let message;

if (user.age >= drinkingAge) {
  message = (
    <h1>
      Hey, check out this alcoholic beverage!
    </h1>
  );
} else {
  message = (
    <h1>
      Hey check out these earrings I got at Claires!
    </h1>
  );
}

ReactDOM.render(
  message, 
  document.getElementById('app')
);

// Example 3
import React from 'react';
import ReactDOM from 'react-dom';

function coinToss () {
  // Randomly return either 'heads' or 'tails'.
  return Math.random() < 0.5 ? 'heads' : 'tails';
}

const pics = {
  kitty: 'https://s3.amazonaws.com/codecademy-content/courses/React/react_photo-kitty.jpg',
  doggy: 'https://s3.amazonaws.com/codecademy-content/courses/React/react_photo-puppy.jpeg'
};

const img = <img src={pics[coinToss() === 'heads' ? 'kitty' : 'doggy']} />;

ReactDOM.render(
	img, 
	document.getElementById('app')
);
```

#### && conditionals
Every time that you see && in this example, either some code will run, or else no code will run.

```javascript 
import React from 'react';
import ReactDOM from 'react-dom';

// judgmental will be true half the time.
const judgmental = Math.random() < 0.5;

const favoriteFoods = (
  <div>
    <h1>My Favorite Foods</h1>
    <ul>
      <li>Sushi Burrito</li>
      <li>Rhubarb Pie</li>
      {!judgmental && <li>Nacho Cheez Straight Out The Jar</li>}
      <li>Broiled Grapefruit</li>
    </ul>
  </div>
);

ReactDOM.render(
	favoriteFoods, 
	document.getElementById('app')
);
```

#### map in JSX 

```javascript 
import React from 'react';
import ReactDOM from 'react-dom';

const people = ['Rowe', 'Prevost', 'Gare'];

const peopleLis = people.map(person =>
  // expression goes here:
  <li>{person}</li>
);

// ReactDOM.render goes here:
ReactDOM.render(<ul>{peopleLis}</ul>, document.getElementById('app'));
```

## Components 
- [Create a component](#create-a-component)
- [Render Function](#render-function)
- [Component](#component)
- [Conditional Render](#conditional-render)

#### Create a Component

```javascript 
import React from 'react';
import ReactDOM from 'react-dom';

class MyComponentClass extends React.Component {
 
}
```

##### Render Funtion 
```javascript 
import React from 'react';
import ReactDOM from 'react-dom';

class MyComponentClass extends React.Component {
  render() {
    return ( <h1>Hello world</h1>);
  }
}
```

###### Component 
```javascript 
import React from 'react';
import ReactDOM from 'react-dom';


const owl = {
  title: "Excellent Owl",
  src: "https://s3.amazonaws.com/codecademy-content/courses/React/react_photo-owl.jpg"
};

// Component class starts here:
class Owl extends React.Component {
  render() {
    return (
      <div>
        <h1>
          {owl.title}
        </h1>
        <img src={owl.src} alt={owl.title} /> 
      </div>
    );
  }
}

ReactDOM.render(<Owl/>,
           document.getElementById('app'));
```

#### Conditional Render 

```javascript 
import React from 'react';
import ReactDOM from 'react-dom';

const fiftyFifty = Math.random() < 0.5;

// New component class starts here:
class TonightsPlan extends React.Component {
  render() {
    if ({fiftyFifty}) {
      return (<h1>Tonight I'm going out WOOO</h1>) ;
    } else {
      return (<h1>Tonight I'm going to bed WOOO</h1>);
    }
  }
}


ReactDOM.render(
	<TonightsPlan />,
	document.getElementById('app')
);
```
#### this 
```javascript 
import React from 'react';
import ReactDOM from 'react-dom';

class MyName extends React.Component {
	// name property goes here:
  get name() {
  	return 'Taher';
  }

  render() {
    return <h1>My name is {this.name}.</h1>;
  }
}

ReactDOM.render(<MyName />, document.getElementById('app'));
```
#### Functions in components
```javascript 
import React from 'react';
import ReactDOM from 'react-dom';

class Button extends React.Component {
  scream() {
    alert('AAAAAAAAHHH!!!!!');
  }

  render() {
    return <button onClick={this.scream}>AAAAAH!</button>;
  }
}

ReactDOM.render(<Button />, document.getElementById('app'));
```

## Props
props are used to pass info across component. The most common use of props is to pass information to a component
- Render a Component's props
- Pass props From Component To Component
- Receive an Event Handler as a prop
- defaultProps
- this.props.children


##### Render a Component's props
```javascript
import React from 'react';
import ReactDOM from 'react-dom';

class Greeting extends React.Component {
  render() {
    return <h1>Hi there, {this.props.firstName}</h1>;
  }
}

ReactDOM.render(
  <Greeting firstName='Taher' />, 
  document.getElementById('app')
);
```

##### Pass props From Component To Component

Greetings.js
```javascript
import React from 'react';

export class Greeting extends React.Component {
  render() {
    return <h1>Hi there, {this.props.name}!</h1>;
  }
}
```

Apps.js
```javascript
import React from 'react';
import ReactDOM from 'react-dom';
import { Greeting } from './Greeting';

class App extends React.Component {
  render() {
    return (
      <div>
        <h1>
          Hullo and, "Welcome to The Newzz," "On Line!"
        </h1>
        <Greeting name="Ruby" />
        <article>
          Latest newzz:  where is my phone?
        </article>
      </div>
    );
  }
}

ReactDOM.render(
  <App />, 
  document.getElementById('app')
);
```

##### Receive an Event Handler as a prop
Talker.js
```javascript
import React from 'react';
import ReactDOM from 'react-dom';
import { Button } from './Button';

class Talker extends React.Component {
  talk() {
    let speech = '';
    for (let i = 0; i < 10000; i++) {
      speech += 'blah ';
    }
    alert(speech);
  }
  
  render() {
    return <Button talk={this.talk}/>;
  }
}

ReactDOM.render(
  <Talker />,
  document.getElementById('app')
);
```
Button.js
```javascript
import React from 'react';

export class Button extends React.Component {
  render() {
    return (
      <button onClick={this.props.talk} >
        Click me!
      <button />

    );
  }
}
```

##### defaultProps
> this prints a button
```javascript 
import React from 'react';
import ReactDOM from 'react-dom';

class Button extends React.Component {
  render() {
    return (
      <button>
        {this.props.text}
      </button>
    );
  }
}

// defaultProps goes here:
Button.defaultProps = { text: 'I am a button' };

ReactDOM.render(
  <Button />, 
  document.getElementById('app')
);
```

##### this.props.children
> This displays all the data within two tags 
- 


## State
- [Setting Initial State](#setting-initial-state)
- Access a componenets state is similar to props 
- Update state with this.setstate
- [Set State](#set-state)
- [Pass a Component's State](#pass-a-components-state)


##### Setting Initial State
- A React component should use props to store information that can be changed, but can only be changed by a different component.
- A React component should use state to store information that the component itself can change.
```javascript
import React from 'react';
import ReactDOM from 'react-dom';

class App extends React.Component {
	// constructor method begins here:
  constructor(props) {
    super(props);
    this.state = { title: 'Best App' };
  }
	
  render() {
    return (
      <h1>
        Wow this entire app is just an h1.
      </h1>
    );
  }
}
```

##### Access a componenets state is similar to props 
```javascript
import React from 'react';
import ReactDOM from 'react-dom';

class App extends React.Component {
	// constructor method begins here:
  constructor(props) {
    super(props);
    this.state = { title: 'Best App' };
  }
	
  render() {
    return (
      <h1>
        {this.state.title}
      </h1>
    );
  }
}

ReactDOM.render(<App />, document.getElementById('app'));
```

##### Update state with this.setstate
```javascript 
this.setState({ hungry: true });
```

##### Set State 
```javascript
import React from 'react';
import ReactDOM from 'react-dom';

const green = '#39D1B4';
const yellow = '#FFD712';

class Toggle extends React.Component {
    constructor(props) {
      super(props);
      this.state = { color: green };
      this.changeColor = this.changeColor.bind(this);
    }
  
  changeColor() {
    this.setState({ color: yellow });
  }
  
  render() {
    return (
      <div style={{background: this.state.color}}>
        <button onClick = {this.changeColor}>
        Change color
        </button>
      </div>
    );
  }
}

ReactDOM.render(<Toggle />, document.getElementById('app'));
```

##### Pass a Component's State
child.js
```javascript
import React from 'react';
import ReactDOM from 'react-dom';

export class Child extends React.Component {
  render() {
  return (
    <h1>
    Hey, my name is {this.props.name}!
    </h1>
  );
  }
}
```

Parent.js
```javascript
import React from 'react';
import ReactDOM from 'react-dom';
import { Child } from './Child';


// stateful component 
class Parent extends React.Component {
  constructor(props) {
  super(props)
    this.state = {name: 'Frarthur'};
  }
  render() {
  return <Child name={this.state.name}/>;
}
} 

ReactDOM.render(<Parent />, 
               document.getElementById('app'))
```

## Passing info
- That means that a Parent is going to render a Child. Rendering is the only way for a component to pass props to another component
- Any component rendered by a different component must be included in an export statement.
- A React component should use props to store information that can be changed, but can only be changed by a different component.
- A React component should use state to store information that the component itself can change

##### Passing info 1
> In the last lesson, you passed information from a stateful, parent component to a stateless, child component.
<br>
Child.js
```javascript
import React from 'react';

export class Child extends React.Component {
  render() {
    return <h1>Hey, my name is {this.props.name}!</h1>;
  }
}
```
Parent.js
```javascript
import React from 'react';
import ReactDOM from 'react-dom';
import { Child } from './Child';

class Parent extends React.Component {
  constructor(props) {
    super(props);
    this.state = { name: 'Frarthur' };
  }

  render() {
    return <Child name={this.state.name} />;
  }
}
ReactDOM.render(<Parent />, document.getElementById('app'));
```

