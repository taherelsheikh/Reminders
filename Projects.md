# Projects 

- JavaScript Projects
 - [Rock, Paper, Scissors](#rock-paper-scissors) 
 - [Sleep Debt Calculator](#sleep-debt-calculator)






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
