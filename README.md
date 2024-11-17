 The original objective of this is to prepare code blocks in JavaScript supported by html + CSS that are going to display a game for a user.

CSS note: Retro style to make the game more immerse

 The game rules are simple: Guess a number between 1 and 20.

 Page has got a HighScore counter and a "Again" button to repeat the game after finished one, to avoid unnecessary manual page refresh

In the code & console a secret number variable is stored - this is visible in the UX side through the question mark 

The code has been refactored to become more dry. This can be observed by the greyed out lines in certain places.
Technique used to refactor: 
- bundle multiple repetitive line codes in a function. More specifically

const displayMessage = function (message) {
  document.querySelector('.message').textContent = message;
};

to replace:

document.querySelector('.message').textContent =

- compress code at the level of "else if" statements. More specifically/ for example:

displayMessage(guess > secretNumber ? '📈 Too high!' : '📉 Too low!');
      score--;

contrary to prior breakdown to separate conditions (one for "Too high", another for "Too low")

------------


* For future self. There is a potential to combine & expand this attempt to one- step larger exercises such as:

  1) Rearrange the code to guess your phone number instead of guessing a number between 1-20
  2) Add to the code a former test (prototype) repo no 1. As a result I'd like to achieve a browser page that engages the user with a little game and perhaps as a reward for successful guess assigns a -15% discount on the next online shop
 
  2.1) I would also add to that a better looking UX that is circulating offline and hasn't been published here (The one produced during my HTML & CSS crash course)

   
