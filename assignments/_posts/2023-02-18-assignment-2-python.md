---
layout: post
title:  "Assignment 2: Python"
date:   2023-02-18 11:16:01 -0500
categories: assignments
---   


Python Programming
==================

You are welcome to work with other compers but everyone should submit there own code! This assignment will be on the github page. Remeber to use google and the python page if you get stuck for refrence!

A. Terminal
-----------

Open up your terminal. We are going to navigate to your forked crimtech repository (the one you cloned last week). Through the terminal using `cd crimtech-comp-s23` . Now you should be inside your repository. Now type in `git pull upstream main` . Now your repository should be up to date. It can be tricky working with the terminal and git so make sure to ask NK or KL if you get an error message. If you have a merge conflict make sure to edit the file where the conflict occcurs and git commit before trying to pull again.

B1. IDE
------

Now we are going to write code. There are many different platforms to write code in. The most popular of which are Visual Studio Code.

[You can download Visual Studio Code here.](https://visualstudio.microsoft.com/free-developer-offers/) _NK uses atom!!! which is just a text editor so you have to run your code in the terminal._

Make sure the version you download works with your computer. Getting an IDE is the hardest thing for new programmers! So don't get overwhelemd it gets way easier from here. After you download an IDE open up the python folder in the crimtech repo(repository)

B2. A note on running python scripts:
-------------
The easiest way to test your Python scripts for today will be to run the Python script itself, which contains a simple test suite that will make sure that your function is correct on common cases. Here is how you can do it

1. In the top bar in VSCode, go to `Terminal > New Terminal`
2. In the terminal window that appears within VSCode, run `python3 <script-name>`. For example, if you want to test the `sum.py` script, you would run `python3 sum.py`.


# Assignments


C1. Sum
--------------------
Write a function that, given a `list` of numbers, computes and returns the sum of all the elements in the list. Put your code in `sum.py`

C2. Square Root
--------------

Write a function that returns the square root of a given variable n. If n is negative or not a number, returns -1. Put your code in `square_root.py`

C3. Random Ints
--------------

Write a program that randomly generates numbers in the range \[1,10\] and appends them to a list, until it generates a 6, at which point it appends that to the list and returns. Put your code in `random_ints.py`.

_HINT: Look into the `random` library_  
_HINT: what does `(int) (random.random()\*10)` generate?_

C4. Remove Smallest
------------------

Write a function that given a dictonary removes the key corresponding to the minimum value and returns changed dictonary. If the dictionary is empty, return the original dictionary. Put your code in `rm_smallest.py`. For example input:

_HINT: Use Set_

 `sampleDict = {   'Physics': 82,   'Math': 65,   'history': 75 }  ` 

Output:

 `sampleDict = {   'Physics': 82,   'history': 75 }` 


C5. Optional
-----------

Define a class to represent companies. Companies will have a name (given at creation), a list of all sales for the year (string of a product), and a dictionary of products (strings, keys) and their prices (float like, values), as well as a list of employees. Define a function to add a new product. The function will take the name of the product and the price. Define a function to add an employee, given an employee. Define an employee class. Employees will have a name as a string, and a company, both given at creation. They will also have a role given at creation. A role is represented by a number, with 1 being a new hire, and 10 the ceo. Make the role value optional, with the default set to 1.

Make sure to test your code by writing some test cases!

D. Push
-------

When you are done make sure to push to github. The comp directors should talk about organizing your work on `git`, and how to push branches. 

by: Richard Xu, edited by Kevin Luo, Wittmann Goh
