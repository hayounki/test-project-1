# Pre-work - *Memory Game*

**Memory Game** is a Light & Sound Memory game to apply for CodePath's SITE Program. 

Submitted by: **Ha Young Kim**

Time spent: **1.25** hours spent in total

Link to project: https://glitch.com/edit/#!/organized-enchanted-tellurium

## Required Functionality

The following **required** functionality is complete:

* [ ] Game interface has a heading (h1 tag), a line of body text (p tag), and four buttons that match the demo app
* [ ] "Start" button toggles between "Start" and "Stop" when clicked. 
* [ ] Game buttons each light up and play a sound when clicked. 
* [ ] Computer plays back sequence of clues including sound and visual cue for each button
* [ ] Play progresses to the next turn (the user gets the next step in the pattern) after a correct guess. 
* [ ] User wins the game after guessing a complete pattern
* [ ] User loses the game after an incorrect guess

The following **optional** features are implemented:

* [ ] Any HTML page elements (including game buttons) has been styled differently than in the tutorial
* [ ] Buttons use a pitch (frequency) other than the ones in the tutorial
* [ ] More than 4 functional game buttons
* [ ] Playback speeds up on each turn
* [ ] Computer picks a different pattern each time the game is played
* [ ] Player only loses after 3 mistakes (instead of on the first mistake)
* [ ] Game button appearance change goes beyond color (e.g. add an image)
* [ ] Game button sound is more complex than a single tone (e.g. an audio file, a chord, a sequence of multiple tones)
* [ ] User has a limited amount of time to enter their guess on each turn

The following **additional** features are implemented:

- [ ] List anything else that you can get done to improve the app!

## Video Walkthrough

Here's a walkthrough of implemented user stories:
![]http://g.recordit.co/5wD97v7Grn.gif
<img src="http://g.recordit.co/5wD97v7Grn.gif" width=500> 


## Reflection Questions
1. If you used any outside resources to help complete your submission (websites, books, people, etc) list them here. 
W3Schools

2. What was a challenge you encountered in creating this submission (be specific)? How did you overcome it? (recommended 200 - 400 words) 
I struggled with handling the guess function logic. At first, I thought that the function would need to use a loop to run through the pattern to play and check the guess. Reading more closely, I noticed that the onclick attributes for each button meant that the guess(btn) would be called each time a button was clicked. 
The next challenge was understanding the logic of the flow chart. I didn’t understand what the end of a “turn” and “last turn” meant. I couldn’t figure it out from re-reading the spec, so I started writing out a diagram/pseudocode-of-sorts. As I did this, I understood that a “turn” meant a sequence of clues played, so the guessCounter needed to match the progress to end a turn, and the “last turn” happened when all of the clues had been played, so we reached the end of the pattern.
I struggled in making the pattern random and in reading in the input from the HTML to adjust the pattern length. For help on this, I went on W3Schools, played with the code on there, and adjusted it for the purposes of this game. Reading in the input was difficult because I didn’t know how to direct the data from the HTML input to the JavaScript. Their input examples directed code to an external file. Instead, I had to access the form field from with JavaScript.

3. What questions about web development do you have after completing your submission? (recommended 100 - 300 words) 
I enjoyed working through the logic of the flow chart, particularly in writing out my own diagram. Because this function’s logic is a specific part of the development process, it made me wonder how teams work together on full-stack web-development projects. How do they distribute work and move along the development process? When I worked on a website for a client for a past internship, I learned about the iterative design cycle and AGILE development. However, I only worked on building the website based off of wireframes I received from other team members. We had a little contribution to the wireframes, discussing what was feasible and not, but, other than that, the entire process felt like we were passing along work from one group to another. I’m interested in seeing what it is like being more deeply involved in all parts of a web-development project. 
	I’m also wondering what this looks like for a career. Which is more common, for people to work on full-stack web-development or to specialize in a part of web-development? What are reasons to choose one over the other? Which would I be better fit for and enjoy more?


4. If you had a few more hours to work on this project, what would you spend them doing (for example: refactoring certain functions, adding additional features, etc). Be specific. (recommended 100 - 300 words) 
I enjoyed working through the logic of the guess() function. If I had more time, I would work through the logic of all of the functions to see if there is a more efficient way of implementing them or perhaps in a way that would make it easier to add other features to the game. 
	First, I would implement a point tracker and scoreboard that records the top scores. This would mean changes to the HTML to leave room for a scoreboard, perhaps keeping it to the side of the page. To ensure proper arrangement of the buttons, I would need to work on the responsive design in CSS. I might need to export the scoreboard data so that it is preserved. Otherwise, reloading the page could mean resetting the data and an empty scoreboard.
I would implement a hint function that would play a few of the clues again. It would need to backtrack on which clues were played and which have been correctly guessed. For instance, to play the last few clues not yet guessed, I would start playing the clues from pattern[progress - guessCounter] till pattern[progress]. I might keep track of points for hints, allowing players to drop 2 points for one more clue to be played or 5 points for 3 clues to be played. To make this more interactive, I might include a slider so that players can decide how many clues they want. This would require the hint() to take in an int on the number of clues, calculate and remove the respective number of points as the cost for the hint, and then play that number of clues back starting from pattern[progress - guessCounter] to pattern[progress - guessCounter + clues].




## License

    Copyright Ha Young Kim

    Licensed under the Apache License, Version 2.0 (the "License");
    you may not use this file except in compliance with the License.
    You may obtain a copy of the License at

        http://www.apache.org/licenses/LICENSE-2.0

    Unless required by applicable law or agreed to in writing, software
    distributed under the License is distributed on an "AS IS" BASIS,
    WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND, either express or implied.
    See the License for the specific language governing permissions and
    limitations under the License.