# SI 507 JavaScript assignment

**To complete and submit this assignment, you should:**

- [x] Fork (and clone) this repository

- [x] Add our instructional team as a collaborator to your fork (see instructions for adding collaborators on Canvas)

- [ ] Edit this `README.md` file with answers to the questions/prompts, briefly, using Markdown formatting so that the questions appear in bulletpoints and the answers appear clearly below each respective question, *not* as bulletpoints.

- [ ] Add all names of those who worked on this (as indicated below)

- [ ] Make the changes that are indicated below to each of the `.html` files with JavaScript programs provided. (You'll probably do this concurrently with answering questions)

- [ ] Commit (as you go) and push your changes to all three files to your GitHub forked repository.

- [ ] Submit a link to your repository on Canvas. (This HW doesn't have an autograder -- it will be graded by hand/by humans this time.)

### Who worked on this assignment?
* **Maggie Davidson (jmaggie)**
* Avery Gleason (averyag) - first couple questions only
* Cara Canady (caraca) - first couple questions only

## Questions & Answers

### `jsPracticeLab.html`

* **What does a code comment look like in JavaScript? What character/s do you have to put before a comment?**

You put `//` before a comment

* **Explain what needs to happen to get a JavaScript program to "run", given the JavaScript you've seen in this assignment.**

A function or functions need to be defined, and then called as part of the HTML.

* **What functions in JavaScript seem to be similar in function to the `print` function in Python? (There are two.) Why might you use one and not the other? Explain briefly.**

`document.querySelector('').innerHTML` allows the user to add HTML while writing in JavaScript, which can include simply printing text -- this is good for fairly static items

`document.getElementsByTagName('tagname').length` displays a list of all elements with the defined tag -- this is good for displaying lists of items that could be dynamically changing

* **What code would have to comment out to get rid of the pop-up box when you load the page? (Related to the last question.) Do that in the code file, and then, add code so that a text box will appear that contains the current date and time! *HINT:* Look through the rest of the code first...**

Line 12, `alert("hello");`

Code added to create new alert on line 13, this code is: `alert(new Date())` which I got from line 20 (line 19 before I added the new line)

* **How can you put your own name at the top where it currently says "A name"? Explain very briefly how to do so, and replace `A name` in the web page with your own name.**

I replaced the string "A name" on line 17 with "Maggie"

* **What does the word `document` represent in this code? Explain briefly.**

`document` refers to the jsPracticeLab.html document that is being displayed on the page. Just like a .doc or .txt file, a .html file is a document.

* **What is happening in line 12 (
		`document.querySelector('#items').innerHTML = document.getElementsByTagName('li').length`
)? Explain, briefly (<= 2 sentences).**

Counting all items tagged "li" and storing it in what is essentially an  "items" variable to be called later on line 59.

* **What color would the background of this page be <u>if there were no JavaScript in this page</u>?**

White because no other color is specified for the background.

* **Why are there a couple of gray boxes on the screen with a different colored border? How could you edit this code to make them a different color? Explain briefly. Then edit the code to make those boxes some shade of blue, of your choosing.**

The style that is "called" for the boxes is defined in lines 45-53 so that if the tag `<p>` is used, it will make everything match the defined style until `</p>` is used. You could change the colors defined on lines 47-48 to other Hex colors.

* **Edit the code so that, if you highlight `McGill University` and copy it, you see the text `O Canada` near the bottom of the page. Briefly explain why you made the edits that you did -- how did you know/figure out what to do?**

I looked at how it was being done with the University of Michigan Go Blue example and created a new function that would print "O Canada" instead of "Go Blue". I had to define a function and then call it below where the Go Blue example is called.

* **In the original code, when you click the button that says `Wow`, you see a text box! Wow. Explain briefly in your own words why the following code causes that to happen:**

```js
function handleClick(){
	alert("hello");
}
```
**and**

```js
<button onclick=handleClick() id="wow-button">Wow</button>
```

A function is defined, `handleClick`, that, when called, will produce an alert that says 'hello'. Then, the way the button is defined, when it is clicked (`onclick`), it will execute that function and thus display the alert.

* **Knowing what you learned from the previous question, add code/markup to the `jsPracticeLab.html` file *so that* there is a button with the text `Spring Equinox 2019` on it somewhere on the page, and when that button is clicked, a text box containing the text `March 20, 2019` appears. (There's no function -- that I am aware of -- to automatically get this info, you've got to type it yourself.)**

Done on lines 40-42 (function definition) and 67 (button)

### The next few questions address the `jquerylib_submit_example.html` file.

* **Check out the file `jquerylib_submit_example.html`. This is an example of code that uses a package called `jQuery` (and this will need you to have an internet connection to run it properly, although the other file does not). Check out resources above for more on jQuery!**

* **When you enter input that isn't valid, you see an error that is red. Why is the error in red? Why is the response for valid inputs blue?**

* **What is this line `var regex = /^[a-zA-Z]+$/;` helping with? And if you googled something to figure that out, what did you google, and what, briefly, did you learn? (If you didn't need to google, you can leave that out, but explain briefly what that line is helping the program do, anyway.)**

* **What's different about the syntax of conditional statements in JavaScript, compared to Python?**

* **What do you think the `10000` refers to in the code `.fadeOut(10000)`?**

* **What do you think is going on with the following code at the beginning of the program? Note that the most important thing to do for answering this question is to be thoughtful and clear, not to be absolutely correct:**

```js
$(document).ready(function(){
    $("form").submit(function(event){
```


* **Add some code to the `jquerylib_submit_example.html` file so that, if the input is valid and is specifically the text `hello`, rather than the visible output being `Nice!` in blue, the visible output should be `Hello to you too!`, also in blue, just like `Nice!` is.**
	* *HINT:* You'll have to make some changes to the conditional statement, and possibly look up some JavaScript conditional syntax. You'll also need to look carefully at what generates visible output right now.
