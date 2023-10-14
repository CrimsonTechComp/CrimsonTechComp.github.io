# Lab 2: javascript basics
In this lab, we will teach you how to use some HTML, CSS and Javascript by building a chat with baby Yoda!

Written by Richard "Rick" Xu.

The slides are [here](https://docs.google.com/presentation/d/1c_cJ3O9BvWNrVVOXSlzjmWT-Rkbbe_ruQNlPW5XBnzc/edit#slide=id.g28cc7345fd6_0_5). 

## A. Pull from upstream
Setup your upstream and pull from it using the instructions on the slides.

If you get any merge conflicts, you need to edit the files where the conflict occurs, following git's instructions. Afterwards, run `git commit` to fix the merge conflict.

## B. Developer Mode / Inspect
In this unit you will be using a browser. It is possible to do this using Chrome, Firefox, Edge or Safari, though we will be following Chrome in this assignment.

On any website, right click and choose the **"Inspect"** option. Welcome to inspect mode/developer panel! This is super useful for web development, and let us go through what a couple panels do. Some of them have exercises. Record your answers in `responses.md`.
0. You can adjust how the browser looks! On the upper bar, there is an option called "Responsive". You can change that to, say, an iPhone X to see how the page looks on an iPhone.
1. `Elements` contains the html source code of the website. 
2. `Console` allows you to type JavaScript expressions. Exercise: There is some javascript on the website that defined an extra variable. What is that variable, and what is its value?
3. A webpage can contain code stored on another webpage, such as `adservice.google.com`. `Sources` allows you to see what they are. Exercise: Go to `thecrimson.com`, look at sources and put the name of another source into your responses.

## C. Welcome to Javascript
All right, another language! Javascript is a widely popular language used for web scripting.

While it is possible to run Javascript code like you would Java or C code, we usually run the code in the web. Type your code in `test.html` and any responses in `lab2-responses.md`. *Throughout this entire section, Google is your friend*.
1. Open up `test.html` in the browser and visit the console.
2. Type `console.log("Hello World")` into the console.
3. Declare a variable `y` and set it equal to your favorite string.
    * Try outputing `y.includes("hello")` and `y.repeat(10)`. What do the two functions do? Record your answer in `lab2-responses.md`.
4. We can declare functions in Javascript! Complete the function `square` so that it takes in a variable `i` and outputs `i*i`.
    * What happens when you call `square(2.5)`? Or `square("hello")`? Record your answer in `lab2-responses.md`.
5. Change the function `square` so that if the input is not a number, the function returns `-1` instead. You may find googling "javascript find type of variable" helpful.
6. Construct a function `numberString`, that on input `i` a positive whole number, output the string `123...i`. For example, `numberString(10)="12345678910"`. 
    * Your function should not crash when `i` is not a positive whole number. Add some `if`-statements to check!

That was a lot. Give yourself a pat on the back for completing them!
