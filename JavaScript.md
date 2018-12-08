<p align="center">
<img src="http://www.userlogos.org/files/javascript-logo.png" width="200">
</p>



# JavaScript
- [Promises](#promises)
- [Data types](#data-types)
- [Methods](#methods)
- [Libraries](#libraries)
- [Comments](#comments)  
- [Variables](#variables)
- [Assigment](#assignment) 
- [String Interpolation](#string-interpolation)
- [Conditional](#conditional) 
- [Comparison](#comparison)
- [Logical Operators](#logical-operators)
- [Switch statment](#switch-statment)
- [Ternary Operator](#ternary-operator)
- [Functions](#functions)
- [Scope](#scope) 
- [Arrays](#arrays)
- [Loops](#loops)
- [Iterators](#iterators)
- [Objects](#objects)
- [Classes](#classes)
- [Browser Compatiblity](#browser-compatiblity)
- [Requests](#requests)
- [JS Cheat Sheet](https://www.codecademy.com/articles/bwa-javascript-reference)

# JavaScript Tools
- [Jupyter NoteBooks for JS](https://repl.it/languages/javascript)
- [Auto Organize JS, HTML, CSS code ](#Dirtymarkup.com)
- [Render JS with HTML with CSS](# Codepen.io)

<br>

#### Promises


```javascript
const inventory = {
  sunglasses: 1900,
  pants: 1088,
  bags: 1344
};

// Write your code below:
const myExecutor = (resolve, reject) => {
  if (inventory.sunglasses > 0) {
    resolve("Sunglasses order processed.")
  } else {
    reject("That item is sold out.")
  }
}

const orderSunglasses = () => {
  return (new Promise(myExecutor))
}

const orderPromise = orderSunglasses()

console.log(orderPromise)
```

<br>

#### Data Types

```javascript
console.log('JavaScript');
console.log(33.7);
console.log(true);
console.log(null);
```
<br>

#### Methods
> Methods have to have an instance for them to work 

```javascript
console.log('Codecademy'.length); 
console.log('Codecademy'.toUpperCase()); 
// Remove whitespace
console.log('    Remove whitespace   '.trim()); 
// Similar to raw_input() in Python
prompt('Whats up?');
```
<br>

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
<br>

#### Comments

```javascript
// Single line
/* 
Multi
line comment 
*/
```
<br>

***

#### Variables 
 - const
- let

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
<br>

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
<br>

#### String Interpolation
 Use ` which is located next to the one when using string interpolation

```javascript 
let myName = 'Taher';

let myCity = 'Dubai';

console.log(`my name is ${myName}. 
My faviorite city is ${myCity}`);
```
<br>

#### Conditional

```javascript
let isSoccerFan = true;

if (isSoccerFan == true) {
  console.log('Goal!');
} else {
  console.log('No goal!')
};
```
<br>

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
<br>

#### Logical Operators
 - "&&" is like and 
 - "||" is like or 

```javascript 
if (stopLight === 'green' && 
pedestrians === false) {
}
```
<br>

#### Switch Statment 
 - used instead of if and else statement cuz they're easier to read 
 - 'default' used at the end to check the truthfulness   

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
<br>

#### Ternary Operator
 '?' and ':' are used instead of if and else statment. Its easier for other people to read your code

```javascript 
let favoritePhrase = 'Love That!';

favoritePhrase === 'Love That!' ?
 console.log('I love that!') : 
 console.log("I don't love that!");
```
<br>

***


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
 Doesnt end with a semi-column  

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
 End with a semi-column  

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

##### Concise Functions
```javascript
const areaOfCircle = radius => Math.PI * radius * radius;
areaOfCircle(4);
```

### Scope 
> - Global Scope 
> - Block Scope 

##### Global Scope 
 Global Scope refers to variables that are accessible to every part of the program.



##### Block Scope 
 - Block Scope refers to variables that are accessible only within the block they are defined.
 - The below code prints "Northern Lights" "Moonlight"

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

***

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
push is similar to append in Python 

```javascript 
newYearsResolutions.push("book", "cook");
```

##### Pop

```javascript
newYearsResolutions.pop();

```

##### let and const
 
let and const are the same when creating an array but const cannot be reassignedLashan 
 
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
<br>

***

### Iterators
[more info](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Array)
> - .forEach()
> - .map()
> - .filter()
> - Other examples


##### .forEach()
This will execute the same code on each element of an array.

```javascript
let fruits = ['mango', 'papaya', 'pineapple', 'apple'];

// Method 1
fruits.forEach(function(fruitItem) {
  console.log(`I want to eat a ${fruitItem}`)
               });
// Method 2
fruits.forEach(fruitItem => {
  console.log('I want to eat ' + fruitItem);
});
```

##### .map()
- Use .map() as opposed to forEach() if you want to change the array  

- Here the code divides each element by 100 and puts it in a array smallNumbers

```javascript 
let bigNumbers = [100, 200, 300, 400, 500];
// Method 1 
let secretMessage = animals.map(function(animalItem) {
  return animalItem[0];
 })
 
// Method 2
let secretMessage = animals.map(animalItem => {
  return animalItem[0];
}) 

// Method 2 on a different problem 
let smallNumbers = bigNumbers.map(number => {
  return number/100;
})
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

// Other Examples
let interestingWords = words.filter(word => word.length > 5);

// Or
let interestingWords = words.filter(word => {return word.length > 5;})
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
<br>

***

### Objects
Is like dictionaries in Python so it has a key-value pairs but it can also contain functions
> - Simple object
> - Methods
> - this
> - set
> - get
> - inheritance


##### Simple object

```javascript
let person = {
  name:'Taher',
  age: 26
};
// Method 1 
console.log(person.name);
// Method 2
console.log(person['name']);
```

##### Methods
When an object has a function as a value. The function is then called a method

```javascript
// Method 1
let object = {
    sayHello : () => {
         return 'Hello, there'
    }
};
console.log(object.sayHello);

// Method 2
let object = {
    sayHello() {
         return 'Hello, there'
    }
};
console.log(object.sayHello);

```

##### this
this helps us with scope inside of object methods. <br>
example 1

```javascript
// this is correct 
let object = {
    name: 'Taher'
    sayHello() {return `Hello, my name is ${this.name}`}
};

// This will give an error
let object = {
    name: 'Taher'
    sayHello() {return `Hello, my name is ${name}`}
};
```
example 2 

```javascript
let person = {
    name: 'Taher'
    sayHello() {return `Hello, my name is ${name}`}
};

let friend = {
  name: 'karim'
};
// This would work 
friend.sayHello = person.sayHello;

console.log(friend.sayHello());
```

##### this - advanced feature
this is a dynamic variable that can change depending on the object that is calling the method

```javascript
// Object One
let person = {
  name: 'Tyron',
sayHello: function() {
    return `Hello, my name is ${this.name}`;
  }
// Object Two
let friend = {
  name: 'taher'
}

// Advanced this
friend.sayHello = person.sayHello;
// prints 'Hello my name is taher'
console.log(friend.sayHello());
```

##### set
Getter and setter methods allow you to process data before accessing or setting property values.
Developers use _ when setting property name to indicate a property or value should not be modified directly by other code.


```javascript
// Example 1 
let person = {
  _name: 'Lu Xun',
  _age: 137,
  
  set age(ageIn) {
    if (typeof ageIn === 'number') {
      this._age = ageIn;
    }
    else {
      return 'Invalid input';
    }
  }
};

// Example 2 
let person = {
  _name: 'Lu Xun',
  _age: 137,
  
  set age(ageIn) {
    if (typeof ageIn === 'number') {
      this._age = ageIn;
    }
    else {
      console.log('Invalid input');
      return 'Invalid input';
    }
  }

};

// not going to work 
person.age = 'Thirty-nine';
// this would work 
person.age = 39;
```

##### get
get is preffered to set beacuse you can do additional processing as opposed to just setting 

```javascript 
let person = {
  _name: 'Lu Xun',
  _age: 137,
   get age() {
  return `${this._name} is ${this._age} years old.`;
  }
};

console.log(person.age);
```
***

<br>

***


### Classes
- Introduction
- Constructor
- Instance
- Another Example
- Static
- Putting it all together

##### intorduction

```javascript
class Dog {
  constructor(name) {
    this._name = name;
    this._behavior = 0;
  }

  get name() {
    return this._name;
  }
  get behavior() {
    return this._behavior;
  }   

  incrementBehavior() {
    this._behavior ++;
  }
}

const halley = new Dog('Halley');
console.log(halley.name); // Print name value to console
console.log(halley.behavior); // Print behavior value to console
halley.incrementBehavior(); // Add one to behavior
console.log(halley.name); // Print name value to console
console.log(halley.behavior); // Print behavior value to
```
##### Constructor
JavaScript calls the constructor() method every time it creates a new instance of a class.

```javascript
class Surgeon {
  constructor(name, department) {
    this.name = name;
    this.department = department;
     }
}
```

##### Instance
Creating an instance is done by using the 'new' function

```javascript
// Example 1 
const surgeonCurry = new Surgeon('Curry', 
'Cardiovascular');

// Example 2
class Surgeon {
  constructor(name, department) {
    this.name = name;
    this.department = department;
  }
}

const surgeonCurry = new Surgeon('Curry', 'Cardiovascular');
const surgeonDurant = new Surgeon('Durant', 'Orthopedics');
```

##### Methods
methods in an classes are very similar to methods in objects but we dont use ','

```javascript
class Surgeon {
  constructor(name, department) {
    this._name = name;
    this._department = department;
    this._remainingVacationDays = 20;
  }
  
  get name() {
    return this._name;
  }
  
  get department() {
    return this._department;
  }
  
  get remainingVacationDays() {
    return this._remainingVacationDays;
  }
  
  takeVacationDays(daysOff) {
    this._remainingVacationDays -= daysOff;
  }
}

const surgeonCurry = new Surgeon('Curry', 'Cardiovascular');
const surgeonDurant = new Surgeon('Durant', 'Orthopedics');

console.log(surgeonCurry.name);
surgeonCurry.takeVacationDays(3);
console.log(surgeonCurry.remainingVacationDays);
```
##### Method Calls
 
```javascript
 class Surgeon {
  constructor(name, department) {
    this._name = name;
    this._department = department;
    this._remainingVacationDays = 20;
    }
  // get 
  get name() {
    return this._name;
  }
  get department() {
    return this._department;
  }
  get remainingVacationDays() {
    return this._remainingVacationDays;
  }
  // Method 
  takeVacationDays(daysOff) {
    this._remainingVacationDays = this._remainingVacationDays - daysOff;
  } 
}

const surgeonCurry = new Surgeon('Curry', 'Cardiovascular');
const surgeonDurant = new Surgeon('Durant', 'Orthopedics');


console.log(surgeonCurry.name);
surgeonCurry.takeVacationDays(3);
console.log(surgeonCurry.remainingVacationDays);
```

##### Inheritance
Create a parent class or super class and child classes that inherites the properties of the parent
- **extends** makes the subcalss inheite all methods, getters, and setters from the parent
- **super** sets the propetries from the parent class into the subclass
- '_' identifies a method as private not public 
 
```javascript
class HospitalEmployee {
  constructor(name) {
    this._name = name;
    this._remainingVacationDays = 20;
  }
  
  get name() {
    return this._name;
  }
  
  get remainingVacationDays() {
    return this._remainingVacationDays;
  }
  
  takeVacationDays(daysOff) {
    this._remainingVacationDays -= daysOff;
  }
}

class Nurse extends HospitalEmployee {
  constructor(name, certifications) {
    super(name);
    this._certifications = certifications;
    }  
}

const nurseOlynyk = new Nurse('Olynyk', ['Trauma', 'Pediatrics']);
```

##### Another Example

```javascript
class HospitalEmployee {
  constructor(name) {
    this._name = name;
    this._remainingVacationDays = 20;
  }
  
  get name() {
    return this._name;
  }
  
  get remainingVacationDays() {
    return this._remainingVacationDays;
  }
  
  takeVacationDays(daysOff) {
    this._remainingVacationDays -= daysOff;
  }
}

class Nurse extends HospitalEmployee {
  constructor(name, certifications) {
    super(name);
    this._certifications = certifications;
  } 
  get certifications() {
    return this._certifications;
  }
  addCertification(newCertification) {
    this._certifications.push(newCertification);
  }
}

const nurseOlynyk = new Nurse('Olynyk', ['Trauma','Pediatrics']);
nurseOlynyk.takeVacationDays(5);
console.log(nurseOlynyk.remainingVacationDays);
nurseOlynyk.addCertification('Genetics');
console.log(nurseOlynyk.certifications);
```

##### Static
Static like .now() are only called from the class not the intance. This wont work for example tyson.generateName(); bu this will Animal.generateName();

```javascript
class HospitalEmployee {
  constructor(name) {
    this._name = name;
    this._remainingVacationDays = 20;
  }
  static generatePassword() {
    return Math.floor(Math.random() * 10000);
  }

console.log(HospitalEmployee.generatePassword());
```

##### Putting it all together

```javascript
class HospitalEmployee {
  constructor(name) {
    this._name = name;
    this._remainingVacationDays = 20;
  }
  static generatePassword() {
    return Math.floor(Math.random() * 10000);
  } 
  
  get name() {
    return this._name;
  }
  
  get remainingVacationDays() {
    return this._remainingVacationDays;
  }
  
  takeVacationDays(daysOff) {
    this._remainingVacationDays -= daysOff;
  }
}

class Nurse extends HospitalEmployee {
  constructor(name, certifications) {
    super(name);
    this._certifications = certifications;
  } 
  
  get certifications() {
    return this._certifications;
  }
  
  addCertification(newCertification) {
    this.certifications.push(newCertification);
  }
}

const nurseOlynyk = new Nurse('Olynyk', ['Trauma','Pediatrics']);
nurseOlynyk.takeVacationDays(5);
console.log(nurseOlynyk.remainingVacationDays);
nurseOlynyk.addCertification('Genetics');
console.log(nurseOlynyk.certifications);
```

### Browser Compatibility
- Badel translates from new JS to older JS. In order to work on all browsers
- caniuse.com is used to check if a function is available in certain browsers 

<br>

***

### Module

Modules are reusable pieces of code that can be exported from one program and imported for use in another program
> - module.exports
> - require()
> - export default
> - import
> - named exports
> - named import
> - export as 
> - import as

##### module.exports

```javascript
let Airplane = {};
// Add property
Airplane.myAirplane = 'StarJet';
// Export to module
module.exports = Airplane;
```

##### require()
this is like import in python 

```javascript
const Airplane = require('./1-airplane.js');

function displayAirplane() {
  console.log(Airplane.myAirplane);
}

displayAirplane();
```

##### export default
This is similar to module.exports but with the new JS syntax

```javascript
let Airplane = {};

Airplane.availableAirplanes = [
{
  name: 'AeroJet',
  fuelCapacity: 800
 }, 
 {name: 'SkyJet',
  fuelCapacity: 500
 }
];

export default Airplane;
```

##### import 
This is similar to require but with the new JS syntax

```javascript
// Airplane specifies the name of the variable to store the default export in.

import Airplane from './airplane'; 

function displayFuelCapacity() {
Airplane.availableAirplanes.forEach(function(element){
  console.log(`Fuel Capacity of ${element.name} : ${element.fuelCapacity}`);
  });
}

displayFuelCapacity();
```

##### Named Exports 
This is used to name a export spicific functions, variables, objects etc

```javascript
let specialty = '';
function isVegetarian() {
}; 
function isLowSodium() {
}; 

export { specialty, isVegetarian };
```
##### Named imports

```javascript
// Simple Example
import { specialty, isVegetarian } from './menu';

console.log(specialty);

// Advanced Example
import {availableAirplanes, flightRequirements, meetsStaffRequirements} from './airplane';

function displayFuelCapacity() {
  availableAirplanes.forEach(function(element) {
    console.log('Fuel Capacity of ' + element.name + ': ' + element.fuelCapacity);
  });
}

displayFuelCapacity();

function displayStaffStatus() {
  availableAirplanes.forEach(function(element) {
   console.log(element.name + ' meets staff requirements: ' + meetsStaffRequirements(element.availableStaff, flightRequirements.requiredStaff) );
  });
}

displayStaffStatus();
```

##### Export as 

```javascript 
let availableAirplanes = [
{name: 'AeroJet',
 fuelCapacity: 800,
 availableStaff: ['pilots', 'flightAttendants', 'engineers', 'medicalAssistance', 'sensorOperators'],
 maxSpeed: 1200,
 minSpeed: 300
}, 
{name: 'SkyJet',
 fuelCapacity: 500,
 availableStaff: ['pilots', 'flightAttendants'],
 maxSpeed: 800,
 minSpeed: 200
}
];

let flightRequirements = {
  requiredStaff: 4,
  requiredSpeedRange: 700
};

function meetsStaffRequirements(availableStaff, requiredStaff) {
  if (availableStaff.length >= requiredStaff) {
    return true;
  } else {
    return false;
  }
};

function meetsSpeedRangeRequirements(maxSpeed, minSpeed, requiredSpeedRange) {
  let range = maxSpeed - minSpeed;
  if (range > requiredSpeedRange) {
    return true;
    } else {
    return false;
  }
};

// Export as function
export { availableAirplanes as aircrafts, flightRequirements as flightReqs, meetsStaffRequirements as meetsStaffReqs, meetsSpeedRangeRequirements as meetsSpeedRangeReqs };
```

#### import as
based on the above example 

```javascript 
import {aircrafts, flightReqs, meetsStaffReqs} from './airplanes'
```

### Export as soon as they are decalred
```javascript 
export let flightRequirements = {
  requiredStaff: 4,
  requiredSpeedRange: 700
};

export function meetsStaffRequirements(availableStaff, requiredStaff) {
  if (availableStaff.length >= requiredStaff) {
    return true;
  } else {
    return false;
  }
};
```

#### Combining import statments
```javascript 
import { specialty, isVegetarian, isLowSodium } from './menu';

import GlutenFree from './menu';
```

### Requests
- GET
- POST
- fecth GET request
- fecth POST request
- async GET Requests
- async POST Requests

> jQuery provides other helper methods that can further reduce boilerplate such as `$.get()`, `$.post()`, and `$.getJSON()`

- GET - [codeacademy link](https://s3.amazonaws.com/codecademy-content/courses/intermediate-javascript-requests/diagrams/diagram3.svg)

```javascript
$.ajax({
  url: 'https://api-to-call.com/endpoint',
  type: 'GET',
  dataType: 'json',
  
  success(response) {
    console.log(response)
  },
  
  error(jqXHR, status, errorThrown) {
 console.log(jqXHR)
  } 
})
```

- POST - [codeacademy link](https://s3.amazonaws.com/codecademy-content/courses/intermediate-javascript-requests/diagrams/diagram4.svg)

```javascript
$.ajax({
  url: 'https://api-to-call.com/endpoint',
  type: 'POST',
  data: JSON.stringify({id: 200}),
  dataType: 'json',
  
  success(response) {
    console.log(response)
  },
  
  error(jqXHR, status, errorThrown) {
    console.log(jqXHR)
  }
})
```

- GET - an easier method 

```javascript 
  $.getJSON(urlToExpand, response => {
  	$responseField.append('<p>Your expanded url is: </p><p>' +
  	response.longUrl + '</p>');
	});
```

- POST - an easier method 

```javascript 
 $.post({
    url: urlWithKey,
    data: JSON.stringify({longUrl: urlToShorten}), 
    dataType: 'json', 
    contentType: 'application/json', 
    success(response) {
      $responseField.append('<p>Your shortened url is: </p><p>' + response.id + '</p>');
    },
    error(jqXHR, status, errorThrown) {
      console.log(jqXHR);
```

- fetch get - [codeacademy link](https://s3.amazonaws.com/codecademy-content/courses/intermediate-javascript-requests/diagrams/diagram5.svg)

> `fetch()` is a web API that can be used to create requests. `fetch()` will return Promises

```javascript 
fetch('https://api-to-call.com/endpoint').then(response => {
  if (response.ok) {
    return response.json()
  }
c}, 
  networkError => console.log(networkError.message)
  ).then(jsonResponse => jsonResponse)
```

- fecth POST request - [codeacademy link](https://s3.amazonaws.com/codecademy-content/courses/intermediate-javascript-requests/diagrams/diagram6.svg)

```javascript 
fetch('https://api-to-call.com/endpoint', 
      {
      method: 'POST',
      body: JSON.stringify({id: '200'})
      }
     ).then(response => { 
                if (response.ok) {
                                  return response.json()
                                   } 
                throw new Error("Request failed!")
                            }, 
            networkError => console.log(networkError.message)
     ).then(jsonResponse => jsonResponse)
```

- async GET Requests - [codeacademy link](https://s3.amazonaws.com/codecademy-content/courses/intermediate-javascript-requests/diagrams/diagram7.svg)

> - `async` is a keyword that is used to create functions that will return Promises.
> - `await` is a keyword that is used to tell a program to continue moving through the message queue while a Promise resolves
> - `await` can only be used within functions declared with `async`

```javascript 
async function getData() {
  try {
    let response = await fetch('https://api-to-call.com/endpoint')
    if (response.ok) {
      let jsonResponse = await response.json()
      return jsonResponse
    }
    throw new Error('Request failed!')
  } catch (error) {
    console.log(error)
  }
}
```

- async POST Request - [code academy link](https://s3.amazonaws.com/codecademy-content/courses/intermediate-javascript-requests/diagrams/diagram8.svg)

```javascript 
async function getData() {
  try {
    let response = await fetch ('https://api-to-call.com/endpoint',
                                {method: 'POST',
                                body: JSON.stringify({id: 200}) }
                                 )
    if (response.ok) {
      let jsonResponse = await response.json()
      return jsonResponse
    } throw new Error('Request failed!')
    
  } catch (error) {
    console.log(error)
  }
}
```



