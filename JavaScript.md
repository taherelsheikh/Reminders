# JavaScript 
- [Data types](#### Data-Types)
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
- Functions
- Scope 
- Arrays
- Loops
- Iterators

  


#### Data Types

```javascript
console.log('JavaScript');
console.log(33.7);
console.log(true);
console.log(null);
```

#### Methods
> Methods have to have an instance for them to work 

```javascript
console.log('Codecademy'.length); 
console.log('Codecademy'.toUpperCase()); 
// Remove whitespace
console.log('    Remove whitespace   '.trim()); 

```

#### Libraries
> Libraries dont have to have an instance for them to work 

```javascript
// Math.random gives number between 0 and 1
console.log(Math.random()); 
// Number between 0 an d 5
console.log(Math.random() * 50); 
// Gives true or false 
console.log(Number.isInteger(2017))
```

#### Comments

```javascript
// Single line
/* 
Multi
line comment 
*/
```

#### Variables 
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

#### Assignment 

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

#### String Interpolation
> Use ` which is located next to the one when using string interpolation

```javascript 
let myName = 'Taher';

let myCity = 'Dubai';

console.log(`my name is ${myName}. 
My faviorite city is ${myCity}`);
```

#### if / else

```javascript
let isSoccerFan = true;

if (isSoccerFan == true) {
  console.log('Goal!');
} else {
  console.log('No goal!')
};
```

#### Comparison
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

#### Logical Operators
> - "&&" is like and 
> - "||" is like or 

```javascript 
if (stopLight === 'green' && 
pedestrians === false) {
}
```

#### Switch Statment 
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

#### Ternary Operator
> '?' and ':' are used instead of if and else statment. Its easier for other people to read your code

```javascript 
let favoritePhrase = 'Love That!';

favoritePhrase === 'Love That!' ?
 console.log('I love that!') : 
 console.log("I don't love that!");
```
<br>


### Functions 
> - Simple Function
> - Functions with argumnets
> - Pizza Function
> - Function Declaration 
> - Function Experssion
> - Arrow Functions 


##### Simple function 

```javascript
const takeOrder = () => {
  console.log('Order: pizza');
};

takeOrder()
```

##### Functions with arguments

```javascript
const takeOrder = (topping) => {
  console.log(`Order: pizza topped with ${topping}`);
};

// Mushrooms is known as an argumnet 
takeOrder("Mushrooms")
```

##### Pizza Function 

```javascript 
let orderCount = 0 
const takeOrder = (topping, crustType) => {
  orderCount ++ ;
  console.log(`Order: ${crustType} pizza topped with ${topping}`);
};

const getSubTotal = (itemCount)  => {
  return itemCount * 7.5
}

takeOrder('mushroom', 'thin crust');
takeOrder('spinach', 'whole wheat');
takeOrder('pepperoni', 'brooklyn style');

console.log(getSubTotal(orderCount));
```
			
##### Function Declaration
> Doesnt end with a semi-column  

```javascript 
function isGreaterThan (numberOne, numberTwo) {
  if (numberOne > numberTwo)  {
    return true;
  }  else {
    return false;
  }
}

isGreaterThan(1, 0);
```
##### Function Experations
> End with a semi-column  

```javascript 
const isGreaterThan = (numberOne, numberTwo) => {
  if (numberOne > numberTwo)  {
    return true;
  }  else {
    return false;
  }
};

isGreaterThan(1, 0);
```

##### Arrow Functions  

```javascript 
const volumeOfSphere = diameter => {
   (1/6) * Math.PI * diameter * diameter * diameter;
}

console.log('The volume of a sphere is ' + volumeOfSphere(10) + ' cubic centimeters');
```
<br>

### Scope 
> - Global Scope 
> - Block Scope 

##### Global Scope 
> Global Scope refers to variables that are accessible to every part of the program.



##### Block Scope 
> - Block Scope refers to variables that are accessible only within the block they are defined.
> - The below code prints "Northern Lights" "Moonlight"

```javascript
const visibleLightWaves =() => {
  let lightWaves = 'Moonlight';
  let region = 'The Arctic';
  
  if (region === 'The Arctic') {
    let lightWaves = 'Northern Lights';
    console.log(lightWaves);
  } 
  console.log(lightWaves);
};

visibleLightWaves();
```
<br>

### Arrays
> - Create an Array
> - Update Array
> - Array Methods [click here for more](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Array)

>  - push ==== append
>  - pop 
> - let and const arrays


##### Create an Array
```javascript
let newYearsResolutions = ['tennis', 'job', 'website'];
```

##### Update Array
```javascript
let newYearsResolutions = ['tennis', 'job', 'website'];
newYearsResolutions[1] = 'Learn a new language';
```
##### Push
> - Push if similar to append in Python 

```javascript 
newYearsResolutions.push("book", "cook");
```

##### Pop

```javascript
newYearsResolutions.pop();

```

##### let and const
 
 > let and const are the same when creating an array but const cannot be reassignedLashan 
 
 ```javascript
 const utensils = ['Fork', 'Knife', 'Chopsticks', 'Spork'];
 // this wont work 
 condiments = ['Sriracha'];
 let utensils = ['Fork', 'Knife', 'Chopsticks', 'Spork'];
 // this would work  
 condiments = ['Sriracha'];
 ```
 <br>
 
### Loops
> - for 
> - while

##### for

```javascript
let vacationSpots = ['Mozambique', 'Thailand', 'Bolivia'];

for (let vacationSpotIndex = 0; 
vacationSpotIndex < vacationSpots.length; 
vacationSpotIndex++) {
  console.log('I would love to visit ' + 
  vacationSpots[vacationSpotIndex]);
}
```
##### while 

```javascript
while (condition) {
  // code block that loops until condition is false
}
```

### Iterators - [more info](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Array)
> - .forEach()
> - .map()
> - .filter()
> - Other examples


##### .forEach()
> Will execute the same code on each element of an array.

```javascript
let fruits = ['mango', 'papaya', 'pineapple', 'apple'];

// Method 1
fruits.forEach(function(fruitItem) {
  console.log(`I want to eat a ${fruitItem}`)
               });
// Method 2
fruits.forEach(fruitItem => console.log(
`- ${fruitItem}`));
```

##### .map()
> Use .map() as opposed to forEach() if you want to change the array  

Here the code divides each element by 100 and puts it in a array smallNumbers

```javascript 
let bigNumbers = [100, 200, 300, 400, 500];
let smallNumbers = bigNumbers.map(num => num/100);

```

##### .filter()
```javascript
// Method 1 - an array of all elements with a length > 7
let longFavoriteWords = favoriteWords.filter(
word => word.length > 7);
// Method 2
let longFavoriteWords = favoriteWords.filter(function(word) {
  return word.length > 7;
});
```

##### Other Examples
```javascript
let cities = ['Nashville', 'Charlotte', 'Asheville', 'Austin', 'Boulder'];

let nums = [1, 50, 75, 200, 350, 525, 1000];

//  Choose a method that will return undefined
cities.forEach(city => console.log(`Have 
you visited ${city}`));

// Choose a method that will return a new array
let longCities = cities.filter(city => city.length > 7);

// Choose a method that will return a new array
let smallerNums = nums.map(num => num - 5);

// Choose a method that will return a boolean value
nums.every(num => num < 0);

```





