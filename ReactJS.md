<img src="https://upload.wikimedia.org/wikipedia/commons/thumb/a/a7/React-icon.svg/512px-React-icon.svg.png" width="200" align="middle">

# React 

- [JSX](#jsx) 


## JSX
> - [JSX Elements](#jsx-elements)
> - [Render an element](#render-an-element)
> - [Variable Attributes JSX](#variable-attributes-jsx)
> - [Events in JSX](#events-in-jsx)

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











