## JavaScript 
> 
 - Data types
 - Methods
 - Libraries
 - Comments  
 - Variables
 - Assigment 
 - String Interpolation
 - if / else 
 - Comparison
 - Logical Operators
 - Switch statment
 - Ternary Operator

  


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
// This wouldnt work 
taher = 'girl';

```

let can be reassigned

```javascript
let taher = false;
// This would work 
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

if / else

```javascript
let isSoccerFan = true;

if (isSoccerFan == true) {
  console.log('Goal!');
} else {
  console.log('No goal!')
};
```

Comparison
> - '==='
> - '!moonPhase' this will give us false 
> - '!=='

```javascript
let moonPhase = 'full';

if (moonPhase === 'full') {
  console.log('Howl!');
} else {
  console.log('swear I am not a werewolf');
}
```

Logical Operators
> - "&&" is like and 
> - "||" is like or 

```javascript 
if (stopLight === 'green' && 
pedestrians === false) {
}
```

Switch Statment 
> - used instead of if and else statement cuz they're easier to read 
> - 'default' used at the end to check the truthfulness   

```javascript
let moonPhase = 'full';

switch (moonPhase) {
  case 'full':
    console.log('Howl!');
    break;
  case 'mostly full':
    console.log('Arms and legs are getting hairier');
    break;
  default: 
    console.log('Invalid moon phase');
    break;
}
```

Ternary Operator
> '?' and ':' are used instead of if and else statment. Its easier for other people to read your code

```javascript 
let favoritePhrase = 'Love That!';

favoritePhrase === 'Love That!' ?
 console.log('I love that!') : 
 console.log("I don't love that!");
```
