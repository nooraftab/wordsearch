# wordsearch

This application allow's one to play a word search (or word find) game in a browser! It was a summer project to teach myself the fundamentals of web development languages like HTML, CSS, and JavaScript, along with a heavy usage of jQuery to handle mouse events (mostly)!

## Setting up

First things first! [Click here](http://htmlpreview.github.io/?https://github.com/nooraftab/wordsearch/blob/master/wordsearch.html) to open the game in your browser!

## Playing

Now look at that hunk of letters! Scroll down and you'll see a handy little table full of words - your task is to find all of them! Put on your eagle eyes and start scanning the grid. 

When you see something that looks like it might be a word (or if you just feel like it - I can't tell you how to live your life), click and drag to select the letters you want in the particular direction you'd like (the directions are highlighted so you can see it easy!).

Let go of the mouse whenever you're ready and if you're in luck, the selected letters will outline themselves to show they've been found.

Keep going! You can always refer to the table at the bottom to see what you have left to find - found words will change color & have a strikethrough.

### Buttons!

**New Game** refreshes the game and give you another randomly generated theme of words to find! You can click it at any point in the game.

**Release the sacred answers** does the dirty work for you by finding all the words you haven't found for you! 

### Important Notes: 

- 'Backspace' functionality (going backwards to deselect a letter) is supported!
- Letters can overlap.
- Words can appear vertically, horizontally, or diagonally - backwards too!
- This is a completely mouse-based game.

## Now that the thrill-sekers are gone... 

This was my first proper brush with a dynamic programming language, so coming from a Java background made it a bit of a learning curve! I looked a lot into code organization and scope, as well as figuring out how to call functions as classes/objects. You'll notice I use the 'new' keyword to run my functions in my controller class, which I preferred to use since it gives the code a bit of logical flow (thanks Java!). 

I also used the MVC (Model-View-Controller) design pattern to help give the code and the different files structure! While it was difficult to  define a pure view, I decided to make the View class handle displaying words and the grid, as well as mouse events within the puzzle grid. The Model/logic class handles the nitty-gritty of setting up the puzzle grid while the Controller handles running the Model and View, and mouse events in the larger scope (e.g. the buttons!). 

### Things to address:
- A good deal into this project, I realized it would've made more sense to have `WordSearchView` call `WordSearchLogic` for data. When I find time to improve my game, I plan on trying to implement this!
- The general internet consensus seems to be 'avoid global variables' - I tried to keep this in mind but you'll notice `wordpaths.js` does consist of 3 global objects since they were important objects used in 2/3 files. I also wanted to cut down on parameters to enhance readability!
- For some functions consisting of long for-loops, I designated single letters to parameter names - I realize this doesn't make for very readable code, but I opted to do so to make the function more concise. My hope is to add functions to contain/return each for-loop component, making it easier to take in and understand! In the meanwhile, I tried to make my comments thorough so readers can understand the code better!
- If you played the game a couple of times, you may have noticed the words can sometimes favor horizontal/vertical words - I have a good feeling it's because of the order at which orientations are checked and added into the valid orientations array. In a future version, randomizing this process would ideally fix this problem and make the distribution of paths more even!

## Credit is due!

1) CodeAcademy's [Introduction to JavaScript](https://www.codecademy.com/learn/introduction-to-javascript) was a great resource for helping me start out the basics of JavaScript (like how the variables work, the different ways a function can be declared etc.)

2) bunkat's [wordfind game](https://github.com/bunkat/wordfind) was a great resource in helping me get started - while i didn't implement things quite the same way they did, it was a helpful resource nonetheless for figuring out bits and pieces! 

3) [W3Schools](https://www.w3schools.com/) helped me catch on to the basics of HTML/CSS and JavaScript/JQuery and was an all-around very helpful reference!

4) [Jack Harvatt's Moon](https://www.behance.net/gallery/23468357/www.studentshow.com/gallery/23468357/Moon-Free-Font) is the font used for the website and game! 

5) Without question, [StackOverflow!](https://stackoverflow.com/)
