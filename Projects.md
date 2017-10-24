# Projects 

## JavaScript Projects
- ### Functions
 > * [Rock, Paper, Scissors](#rock-paper-scissors) 
 > * [Sleep Debt Calculator](#sleep-debt-calculator)
- ### Loops
 > * [Whale Talk](#whale-talk)
- ### Iterations
 > * (Secret Message)(#secret-message)

<br>



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
  
                      
                  
                         
                         
                         
                         
              

