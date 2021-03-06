# Projects

## JavaScript Projects
### Functions
 > * [Rock, Paper, Scissors](#rock-paper-scissors)
 > * [Sleep Debt Calculator](#sleep-debt-calculator)
### Loops
 > * [Whale Talk](#whale-talk)
### Iterations
 > * [Secret Message](#secret-message)
### Scope
 > * [Training Days](#training-days)
### Objects
 > * [Team Stats](#team-stats)
### Classes
 > * [Build Library](#build-library)
 > * [School Catalogue](#school-catalogue)
### Modules
> * [Work Around One](#work-around-one)
> * [Work Around Two](#work-around-two)
> * [Work Around Three](#work-around-three)

<br>

## React Projects
### Components
> * [Authorization Form](#authorization-form)
### States and Props
> * [Random Color Picker](#random-color-picker)
### Passing info
> * [Video Player](#video-player)


### Rock Paper Scissors

```javascript
const getUserChoice = (userInput) => {
  userInput = userInput.toLowerCase();
  if (userInput === 'rock' || userInput === 'paper'
   || userInput === 'scissors' || userInput === 'bomb') {
    return userInput;
  } else {
    return 'Error!'
  }
};

const getComputerChoice = () => {
  let number =  Math.floor(Math.random() * 3);
  switch (number) {
    case 1:
      return 'rock';
    case 2:
      return 'paper';
    case 0:
      return 'scissors';
                }
};

const determineWinner = (userChoice, computerChoice) => {
  if (userChoice === computerChoice) {
    return 'Both Winners!'
  }
  else {
    if (userChoice === 'rock') {
      if (computerChoice == 'scissors') {
        return 'You Won!';
      } else {
        return 'Computer Won!';
      }
    }
   else if (userChoice === 'paper') {
     if (computerChoice === 'rock') {
       return 'You Won!';
     } else {
       return 'Computer Won!';
     }
   }
  else if (userChoice === 'scissors') {
     if (computerChoice === 'paper') {
       return 'You Won!';
     } else {
       return 'Computer Won!';
     }
   }
  if (userChoice === 'bomb') {
    return "You Won! ;)";
  }

  }

};

const playGame = () => {
  const userChoice = getUserChoice('bomb');
  const computerChoice = getComputerChoice();
  console.log(`your choice was ${userChoice}`);
  console.log(`your computer's choice was ${computerChoice}`);
  console.log(determineWinner(userChoice, computerChoice));
};

playGame();

```


### Sleep Debt Calculator

```javascript
const getSleepHours = (day) => {
  switch (day) {
   case 'Monday':
      return 6;
   case 'Tuesday':
      return 6;
   case 'Wednesday':
      return 7;
   case 'Thursday':
      return 7;
  case 'Friday':
      return 7;
  case 'Saturday':
      return 7;
  case 'Sunday':
      return 8;    
         }
};

const getActualSleepHours = () => {
   return getSleepHours('Monday') + getSleepHours('Tuesday')
   + getSleepHours('Wednesday') + getSleepHours('Thursday') +
   +  getSleepHours('Friday') + getSleepHours('Saturday') +
   +  getSleepHours('Sunday');
};

const getIdealSleepHours = () => {
  const idealHours = 8;
  return idealHours * 7;
};

const calculateSleepDebt = () => {
  const actualSleepHours = getActualSleepHours();
  const idealSleepHours = getIdealSleepHours();
  const amountNeeded = idealSleepHours - actualSleepHours;
  if (actualSleepHours === idealSleepHours) {
    console.log('Perfect amount of sleep!');
  }
  else if (actualSleepHours > idealSleepHours) {
    console.log('You got more sleep than needed!')
    ;
  }
  else {
    console.log(`You need more rest! your sleep debt is ${amountNeeded}`);
  }
};


calculateSleepDebt();

```

### Whale Talk

```javascript
let input = 'Turpentine and turtles';

let vowels = ['a', 'u', 'o', 'i', 'e'];

let resultArray = [];

for (let inputIndex = 0;
    inputIndex < input.length;
    inputIndex++) {
  for (let vowelsIndex = 0;
      vowelsIndex < vowels.length;
      vowelsIndex++) {
    if (input[inputIndex] === vowels[vowelsIndex]) {
      resultArray.push(input[inputIndex]);
    }

  }

  if (input[inputIndex] === 'e' || input[inputIndex] === 'u') {
    resultArray.push(input[inputIndex]);
  }
};

console.log(resultArray.join('').toUpperCase());
```

### Secret Message

```javascript
let story = 'Last weekend, I took literally the most beautiful bike ride of my life. The route is called "The 9W to Nyack" and it actually stretches all the way from Riverside Park in Manhattan to South Nyack, New Jersey. It\'s really an adventure from beginning to end! It is a 48 mile loop and it basically took me an entire day. I stopped at Riverbank State Park to take some extremely artsy photos. It was a short stop, though, because I had a really long way left to go. After a quick photo op at the very popular Little Red Lighthouse, I began my trek across the George Washington Bridge into New Jersey.  The GW is actually very long - 4,760 feet! I was already very tired by the time I got to the other side.  An hour later, I reached Greenbrook Nature Sanctuary, an extremely beautiful park along the coast of the Hudson.  Something that was very surprising to me was that near the end of the route you actually cross back into New York! At this point, you are very close to the end.';

let overusedWords = ['really', 'very', 'basically'];

let unnecessaryWords = ['extremely', 'literally', 'actually' ];

let storyWords = story.split(' ');
console.log(storyWords.length);

let betterWords = storyWords.filter(word => {
  if (!unnecessaryWords.includes(word)) {
    return word;
  }
})

unnecessaryWords.forEach(
  word => console.log(word));
```

### Training Days

```javascript
const getAllEvents = () => {
  return ['Marathon', 'Triathlon', 'Decathlon'];
};

const getRandomEvent = () => {
  const allEvents =  getAllEvents();
  const event = allEvents[Math.floor(Math.random() * allEvents.length)];
  return event;

};


const getEventActivities = (event) => {
  const allEvents =  getAllEvents();

  if (!allEvents.includes(event)) {
    return null;
  }
  let activities;
  if (event === 'Marathon') {
    activities = ['Running'];
    return activities.join(', ');
  }
  if (event === 'Triathlon') {
    activities = ['Running', 'Cycling', 'Swimming'];
    return activities.join(', ');
  }
  if (event === 'Decathlon') {
    activities = ['Running', 'Hurdles', 'Javelin throw', 'Discus Throw', 'Shot put', 'High Jump'];
    return activities.join(', ');
  }

};

const getDaysToTrain = (event) => {
  const allEvents =  getAllEvents();
  if (!allEvents.includes(event)) {
    return null;
  }
  const eventTrainingTimes = {'Marathon': 50, 'Triathlon': 100, 'Decathlon': 200 };

  return eventTrainingTimes[event];
};

const getEventMessage = () => {
  const myEvent = getRandomEvent();
  console.log('Your event is a ' + myEvent + '. Your event activities consist of ' + getEventActivities(myEvent) + '. You have ' + getDaysToTrain(myEvent) +  ' days to train.');
};

getEventMessage();
```

### Team Stats                     

```javascript
const team = {
  _players: [
    {firstname: 'Serena',
     lastname: 'Williams',
     age: 36},
    {firstname: 'Roger',
     lastname: 'Federer',
     age: 36},
     {firstname: 'Rafeal',
     lastname: 'Nadal',
     age: 35},
            ],
  _games: [
      {opponent: "Ahly",
         teamPoints: 44,
         opponentPoints:27},
      {opponent: "Zamalik",
         teamPoints: 20,
         opponentPoints:27},
      {opponent: "Real",
         teamPoints: 30,
         opponentPoints:27}    
  ],
  get players() {
    return this._players
  },
  get games() {
    return this._games
  },
  addPlayer(firstName, lastName, age) {
    let player = {
      firstname: firstName,
      lastName: lastName,
      age: age
    }
    this.players.push(player);
  },
  addGame (opponent, teamPoints, opponentPoints) {
     let game = {
           opponent: opponent,
           teamPoints: teamPoints,
            opponentPoints: opponentPoints  
          }
     this.games.push(game);
    }
};


team.addPlayer("Steph", "Curry", 30);
team.addGame("Steph",40, 30);
console.log(team._games);
console.log(team._players);
```                    
### Build Library                         

```javascript
class Media {
  constructor(title) {
    this._title = title;
    this._ratings = [];
    this._isCheckedOut = false;
  }
  get title() {
    return this._title;
  }
  get isCheckedOut() {
    return this._isCheckedOut;
  }
  get ratings() {
    return this._ratings;
  }
  toggleCheckOutStatus() {
    if (this._isCheckedOut) {
      this._isCheckedOut = false;
    } else {
      this._isCheckedOut = true
    }
  }
  getAverageRating() {
    let ratingsSum = this.ratings.reduce((currentSum, rating) => currentSum + rating, 0);  
    let lengthOfArray = this.ratings.length;
    return Math.floor(ratingsSum / lengthOfArray);
  }
  addRating(name) {
    this.ratings.push(name);
  }
}

class Book extends Media {
   constructor(title, author, pages) {
     super(title);
     this._author = author;
     this._pages = pages;
 }
  get author() { return this._author;}
  get pages() {return this._pages;}
}

class Movie extends Media {
  constructor(title, director, runTime) {
    super(title);
    this._director = director;
    this._runTime = runTime;
  }
  get director() {return this._director}
  get runTime() {return this._runTime}
}


const historyOfEverything = new Book( "A Short History of Nearly Everything","Bill Bryson",  544);

historyOfEverything.toggleCheckOutStatus();
console.log(historyOfEverything.isCheckedOut);

historyOfEverything.addRating(4)
historyOfEverything.addRating(5)
historyOfEverything.addRating(5)

console.log(historyOfEverything.getAverageRating());

const speed = new Movie("Speed","Jan de Bont", 116);
speed.toggleCheckOutStatus();
console.log(speed.isCheckedOut);


speed.addRating(1);
speed.addRating(1);
speed.addRating(5);

console.log(speed.getAverageRating());
```              
### School Catalogue

```javascript
class Media {
  constructor(title) {
    this._title = title;
    this._ratings = [];
    this._isCheckedOut = false;
  }
  get title() {
    return this._title;
  }
  get isCheckedOut() {
    return this._isCheckedOut;
  }
  get ratings() {
    return this._ratings;
  }
  toggleCheckOutStatus() {
    if (this._isCheckedOut) {
      this._isCheckedOut = false;
    } else {
      this._isCheckedOut = true
    }
  }
  getAverageRating() {
    let ratingsSum = this.ratings.reduce((currentSum, rating) => currentSum + rating, 0);  
    let lengthOfArray = this.ratings.length;
    return Math.floor(ratingsSum / lengthOfArray);
  }
  addRating(name) {
    this.ratings.push(name);
  }
}

class Book extends Media {
   constructor(title, author, pages) {
     super(title);
     this._author = author;
     this._pages = pages;
 }
  get author() { return this._author;}
  get pages() {return this._pages;}
}

class Movie extends Media {
  constructor(title, director, runTime) {
    super(title);
    this._director = director;
    this._runTime = runTime;
  }
  get director() {return this._director}
  get runTime() {return this._runTime}
}


const historyOfEverything = new Book( "A Short History of Nearly Everything","Bill Bryson",  544);

historyOfEverything.toggleCheckOutStatus();
console.log(historyOfEverything.isCheckedOut);

historyOfEverything.addRating(4)
historyOfEverything.addRating(5)
historyOfEverything.addRating(5)

console.log(historyOfEverything.getAverageRating());

const speed = new Movie("Speed","Jan de Bont", 116);
speed.toggleCheckOutStatus();
console.log(speed.isCheckedOut);


speed.addRating(1);
speed.addRating(1);
speed.addRating(5);

console.log(speed.getAverageRating());
```

### Work Around One

employee.js
- payGrades wasn't exported or imported since its already in the same file, all the code has access to it
- Usually we import and export only the variables used in the workAround.js file

```javascript
let Employee = {
  salary: 100000
};


let payGrades = {
  entryLevel: { taxMultiplier: .05, benefits: ['health'], minSalary: 10000, maxSalary: 49999 },
  midLevel: { taxMultiplier: .1, benefits: ['health', 'housing'], minSalary: 50000, maxSalary: 99999 },
  seniorLevel: { taxMultiplier: .2, benefits: ['health', 'housing', 'wellness', 'gym'], minSalary: 100000, maxSalary: 200000 }
};

Employee.getCadre =
function() {
  if (Employee.salary >= payGrades.entryLevel.minSalary && Employee.salary <= payGrades.entryLevel.maxSalary) {
    return 'entryLevel';
  } else if (Employee.salary >= payGrades.midLevel.minSalary && Employee.salary <= payGrades.midLevel.maxSalary) {
    return 'midLevel';
  } else return 'seniorLevel';
}

Employee.calculateTax =
function() {
  return payGrades[Employee.getCadre()].taxMultiplier * Employee.salary;
}

Employee.getBenefits =
function() {
  return payGrades[Employee.getCadre()].benefits.join(', ');
}

Employee.calculateBonus =
function() {
  return .02 * Employee.salary;
}

Employee.reimbursementEligibility =
function() {
  let reimbursementCosts = { health: 5000, housing: 8000, wellness: 6000, gym: 12000 };
  let totalBenefitsValue = 0;
  let employeeBenefits = payGrades[Employee.getCadre()].benefits;
  for (let i = 0; i < employeeBenefits.length; i++) {
    totalBenefitsValue += reimbursementCosts[employeeBenefits[i]];
  }
  return totalBenefitsValue;
}

export default Employee;
```
workAround.js
```JavaScript
import Employee from './employee.js'


function getEmployeeInformation(inputSalary) {
  Employee.salary = inputSalary;
  console.log('Cadre: ' + Employee.getCadre());
  console.log('Tax: ' + Employee.calculateTax());
  console.log('Benefits: ' + Employee.getBenefits());
  console.log('Bonus: ' + Employee.calculateBonus());
  console.log('Reimbursement Eligibility: ' + Employee.reimbursementEligibility() + '\n');
}

getEmployeeInformation(10000);
getEmployeeInformation(50000);
getEmployeeInformation(100000);
```

### Work Around Two

employee.js

```JavaScript
let Employee = {
  salary: 100000
};


let payGrades = {
  entryLevel: { taxMultiplier: .05, benefits: ['health'], minSalary: 10000, maxSalary: 49999 },
  midLevel: { taxMultiplier: .1, benefits: ['health', 'housing'], minSalary: 50000, maxSalary: 99999 },
  seniorLevel: { taxMultiplier: .2, benefits: ['health', 'housing', 'wellness', 'gym'], minSalary: 100000, maxSalary: 200000 }
};

function getCadre() {
  if (Employee.salary >= payGrades.entryLevel.minSalary && Employee.salary <= payGrades.entryLevel.maxSalary) {
    return 'entryLevel';
  } else if (Employee.salary >= payGrades.midLevel.minSalary && Employee.salary <= payGrades.midLevel.maxSalary) {
    return 'midLevel';
  } else return 'seniorLevel';
}

function calculateTax() {
  return payGrades[getCadre()].taxMultiplier * Employee.salary;
}

function getBenefits() {
  return payGrades[getCadre()].benefits.join(', ');
}


function calculateBonus() {
  return .02 * Employee.salary;
}

function reimbursementEligibility() {
  let reimbursementCosts = { health: 5000, housing: 8000, wellness: 6000, gym: 12000 };
  let totalBenefitsValue = 0;
  let employeeBenefits = payGrades[getCadre()].benefits;
  for (let i = 0; i < employeeBenefits.length; i++) {
    totalBenefitsValue += reimbursementCosts[employeeBenefits[i]];
  }
  return totalBenefitsValue;
}

export {Employee, getCadre as cadre, calculateTax as tax, getBenefits as benefits,calculateBonus as bonus, reimbursementEligibility as reimbursement } ;
```
workAround.js
```javascript
import {Employee, cadre, tax, benefits, bonus, reimbursement
} from './employee.js'


function getEmployeeInformation(inputSalary) {
  Employee.salary = inputSalary;
  console.log('Cadre: ' + cadre());
  console.log('Tax: ' + tax());
  console.log('Benefits: ' + benefits());
  console.log('Bonus: ' + bonus());
  console.log('Reimbursement Eligibility: ' + reimbursement() + '\n');
}

getEmployeeInformation(10000);
getEmployeeInformation(50000);
getEmployeeInformation(100000);
```

### Work Around Three
Employee.js

```javascript
let Employee = {
  salary: 100000
};


let payGrades = {
  entryLevel: { taxMultiplier: .05, benefits: ['health'], minSalary: 10000, maxSalary: 49999 },
  midLevel: { taxMultiplier: .1, benefits: ['health', 'housing'], minSalary: 50000, maxSalary: 99999 },
  seniorLevel: { taxMultiplier: .2, benefits: ['health', 'housing', 'wellness', 'gym'], minSalary: 100000, maxSalary: 200000 }
};

export function getCadre() {
  if (Employee.salary >= payGrades.entryLevel.minSalary && Employee.salary <= payGrades.entryLevel.maxSalary) {
    return 'entryLevel';
  } else if (Employee.salary >= payGrades.midLevel.minSalary && Employee.salary <= payGrades.midLevel.maxSalary) {
    return 'midLevel';
  } else return 'seniorLevel';
}

export function calculateTax() {
  return payGrades[getCadre()].taxMultiplier * Employee.salary;
}

export function getBenefits() {
  return payGrades[getCadre()].benefits.join(', ');
}


export function calculateBonus() {
  return .02 * Employee.salary;
}

export function reimbursementEligibility() {
  let reimbursementCosts = { health: 5000, housing: 8000, wellness: 6000, gym: 12000 };
  let totalBenefitsValue = 0;
  let employeeBenefits = payGrades[getCadre()].benefits;
  for (let i = 0; i < employeeBenefits.length; i++) {
    totalBenefitsValue += reimbursementCosts[employeeBenefits[i]];
  }
  return totalBenefitsValue;
}

export default Employee ;
```
workAround.js
```javascript
import {getCadre, calculateTax, getBenefits, calculateBonus, reimbursementEligibility } from './employee';

import Employee from './employee';


function getEmployeeInformation(inputSalary) {
  Employee.salary = inputSalary;
  console.log('Cadre: ' + getCadre());
  console.log('Tax: ' + calculateTax());
  console.log('Benefits: ' + getBenefits());
  console.log('Bonus: ' + calculateBonus());
  console.log('Reimbursement Eligibility: ' + reimbursementEligibility() + '\n');
}

getEmployeeInformation(10000);
getEmployeeInformation(50000);
getEmployeeInformation(100000);
```

### Authorization Form

```javascript
import React from 'react';
import ReactDOM from 'react-dom';

class Contact extends React.Component {
  constructor(props) {
    super(props);
    this.state = {
      password: 'swordfish',
      authorized: false
    };
    this.authorize = this.authorize.bind(this);
  }

  authorize(e) {
    const password = e.target.querySelector(
      'input[type="password"]').value;
    const auth = password == this.state.password;
    this.setState({
      authorized: auth
    });
  }

  render() {
    const login = (
        <form action="#" onSubmit={this.authorize}>
        <input
          type="password"
          placeholder="Password"/>
        <input type="submit" />
        </form>)
    const contactInfo = (        
        <ul>
          <li>
            client@example.com
          </li>
          <li>
            555.555.5555
          </li>
        </ul>);
    return (
      <div id="authorization">
        <h1>
          {this.state.authorized ? 'Contact' : 'Enter the Password'}
  { this.state.authorized ? contactInfo : login }        </h1>
      </div>
    );
  }
}

ReactDOM.render(
  <Contact />,
  document.getElementById('app')
);
```

### Random Color Picker
Random.js
```javascript
import React from 'react';
import ReactDOM from 'react-dom';
import { Button } from './Button';

class Random extends React.Component {
  constructor(props){
    super(props);
    this.state = {color:[300,240,71]};
    this.handleClick = this.handleClick.bind(this);
    
  }
  componentDidMount() {
    this.applyColor();
  }

  componentDidUpdate(prevProps, prevState) {
    this.applyColor();
  }

  formatColor(ary) {
    return 'rgb(' + ary.join(', ') + ')';
  }

  isLight() {
    const rgb = this.state.color;
    return rgb.reduce((a,b) => a+b) < 127 * 3;
  }

  applyColor() {
    const color = this.formatColor(this.state.color);
    document.body.style.background = color;
  }

  chooseColor() {
    const random = [];
    for (let i = 0; i < 3; i++) {
      random.push(Math.floor(Math.random()*256));
    }
    return random;
  }
  
  handleClick() {
    this.setState({color: this.chooseColor()})
  }

  render() {
    return (
      <div>
        <h1 className={this.isLight() ? 'white' : 'black'}>
          Your Color is {this.formatColor(this.state.color)}
        </h1>
        <Button light={this.isLight()} onClick={this.handleClick}/>
      </div>
    );
  }
}

ReactDOM.render(
  <Random />, 
  document.getElementById('app')
);
```
Button.js
```javascript
import React from 'react';

export class Button extends React.Component {
	render() {
		return (
			<button 
				className={ this.props.light ? 'light-button' : 'dark-button' }
        onClick= {this.props.onClick}>
				Refresh
			</button>
		);
	}
}
```

### Video Player
> App passes down this.state.src to Video. Video uses this info to display the chosen video. App also passes down the ability to change this.state.src to Menu. Menu uses this ability to let a user to select a new video.

<br>

App.js

```javascript
import React from 'react';
import ReactDOM from 'react-dom';
import { Video } from './Video';
import { Menu } from './Menu';

const VIDEOS = {
  fast: 'https://s3.amazonaws.com/codecademy-content/courses/React/react_video-fast.mp4',
  slow: 'https://s3.amazonaws.com/codecademy-content/courses/React/react_video-slow.mp4',
  cute: 'https://s3.amazonaws.com/codecademy-content/courses/React/react_video-cute.mp4',
  eek: 'https://s3.amazonaws.com/codecademy-content/courses/React/react_video-eek.mp4'
};

class App extends React.Component {
  constructor(props) {
    super(props);

    this.state = { src: VIDEOS.fast };
    this.chooseVideo = this.chooseVideo.bind(this);  }
  
  chooseVideo(newVideo){
    this.setState({src: VIDEOS[newVideo]})
  }

  render() {
    return (
      <div>
        <h1>Video Player</h1>
        <Menu chooseVideo={this.chooseVideo}/>
        <Video src={this.state.src} />
      </div>
    );
  }
}

ReactDOM.render(
  <App />, 
  document.getElementById('app')
);
```
Video.js

```javascript
import React from 'react';

export class Video extends React.Component {
  render() {
    return (
      <div>
        <video controls autostart autoplay src = {this.props.src}/>
      </div>
    );
  }
}
```
Menu.js
```javascript
import React from 'react';

export class Menu extends React.Component {
  constructor(props){
    super(props)
    this.handleClick = this.handleClick.bind(this)
  }
  
  handleClick(e) {
    let text = e.target.value
    this.props.chooseVideo(text);
  }
  
  
  render() {
    return (
      <form onClick = {this.handleClick}>
        <input type="radio" name="src" value="fast" /> fast
        <input type="radio" name="src" value="slow" /> slow
        <input type="radio" name="src" value="cute" /> cute
        <input type="radio" name="src" value="eek" /> eek
      </form>
    );
  }
}
```
