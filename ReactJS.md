![](https://upload.wikimedia.org/wikipedia/commons/thumb/a/a7/React-icon.svg/512px-React-icon.svg.png)

# React
- [JSX](#jsx)
- 


## JSX
> - [JSX Elements](#jsx-elements)
> - [Render an element](#render-an-element)


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
