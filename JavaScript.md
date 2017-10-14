## JavaScript 
> - Data types
> - Methods
> - Libraries
> - Comments  
> - Variables
> - Assigment 
> - String Interpolation

Data Types

```javascript
console.log('JavaScript');
console.log(33.7);
console.log(true);
console.log(null);
```

Methods
> Methods have to have an instance for them to work 

```javascript
console.log('Codecademy'.length); 
console.log('Codecademy'.toUpperCase()); 
// Remove whitespace
console.log('    Remove whitespace   '.trim()); 

```

Libraries
> Libraries dont have to have an instance for them to work 

```javascript
// Math.random gives number between 0 and 1
console.log(Math.random()); 
// Number between 0 an d 5
console.log(Math.random() * 50); 
// Gives true or false 
console.log(Number.isInteger(2017))
```

Comments

```javascript
// Single line
/* 
Multi
line comment 
*/
```

Variables 
> - const
> - let

const cant be reassigned 

```javascript
const taher = 'boy';
```

let can be reassigned

```javascript
let taher = false;
taher = true;
```

Assignment 

```javascript
let x = 4;
x += 2;
// Mutiply by 2
x *= 2;
// Add by 1
x ++;
// Subtract by 1
x --;
```

String Interpolation
> Use ` which is located next to the one when using string interpolation

```javascript 
let myName = 'Taher';

let myCity = 'Dubai';

console.log(`my name is ${myName}. 
My faviorite city is ${myCity}`);
```