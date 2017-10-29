![](https://www.google.com/url?sa=i&rct=j&q=&esrc=s&source=imgres&cd=&cad=rja&uact=8&ved=0ahUKEwiN9eeq3ZbXAhUKw4MKHcPOAWgQjRwIBw&url=https%3A%2F%2Fworldvectorlogo.com%2Flogo%2Freact&psig=AOvVaw12aMrl13G_MTitbK6k_l8r&ust=1509397321535111)

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
