![](https://facebook.github.io/react/tutorial/tutorial.html)

# React
- [JSX](#jsx)
- 


## JSX
> - [JSX Elements](#jsx-elements)
> - [Render an element](#render-an-elment)


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
import React from 'react';
import ReactDOM from 'react-dom';

ReactDOM.render(<h1>Hello world</h1>,
document.getElementById('app'));
```