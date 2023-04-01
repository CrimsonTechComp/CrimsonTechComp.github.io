---
layout: post
title:  "Webscraping"
date:   2023-03-31 02:00:00 -0500
categories: Python
---

Let's learn how to webscrape!
=============================

What is Webscraping
-------------------

Web scraping is a tool that allows you to get information from websites and turn it into data that you can manipulate and draw analysis from. We eventually will want to visualize the data that we get.

A. Google Colab
---------------

We mainly use google colab for web scraping because it allows people to write code collaboratively and easier than GitHub. Search up Google colab

Then you are going to want to press new notebook. Which can be found under file. name the notebook and share with me

Name the notebook: Y/N Crimtech Webscraping and share it with naomi.kenyatta@thecrimson.com and kevin.luo@thecrimson.com.

B. BeautifulSoup and Requests
-----------------------------

For this assignment you should choose your favorite harvard department and find the website that has a list of staff members such as math.harvard.edu/people/. After choosing the website we are going to use the library called Beutiful Soup to collect information from the website. In the first code block you are going to import the library so we can use it

    import requests
    from bs4 import BeautifulSoup

we can run this code block by pushing the run button on the left side of the block. A green arrow will appear after running showing that it was completed. It is typically standard to have imports in a seperate code box. So now we want to press the +code button on the top of page to create a new code box.

C. Inspect
----------

Our goal is to collect the information of the names, offices and link of every member of a department. We can navigate back towards the website choosen at the begining. If you right click on any website there will be an option called inspect. When you click on inspect it will show you about the elements of the webpage. Pay around with it and become comfortable naviagting around. Eventually we want to find the information that we need to click. You can do this by naviagting throught the inspect or right clicking on the piece of information that you want and then inspect will open up to where that information is held. You should notice that when you hover over a piece of code the corresponding part of the website is highlighted. at the begining of every line theere is an arrow pointing either to the right or down. If the arrow is pointing right or you see ... then that means the block can be opened more by pressing the arrow or double clicking.

![Inspect](/assets/images/Auroux.png) 

To get auroux's email we see that it is inside the tag called icon icon email. Now we want to collect everyones's email so we will go back to colab and in our new block

    URL = url
    page = requests.get(URL)
    
    soup = BeautifulSoup(page.content, 'html.parser')
    results = soup.find_all(class_=‘name’)
    results
    

You should see a large list under the block after running. This is the information from inside results. You will probably notice that the list has a lot of other random information that we dont wan’t. A big part of web scraping is data cleaning. If you want to learn more about how BeautifulSoup and requests work you can read this: LINK MEDIUM PAGE OR SMTH. A brief explanation is that soup now holds all the information from inspect which is the websites HTML and XML pages. Now we can use find\_all to find any tags that we want and turns it into a list.

D. Data Cleaning
----------------

_HINT: Since we want to find 3 pieces of information for each person we should consider choosing a class that holds all of the information for example it would be info in the picture above. Then when cleaning using .find\_all() 3 times on the these blocks._

You should make a new block for data cleaning so that you dont have to request the webpage everytime. Now its time to use the python skills. By the end you want to have a list of lists. For example: \[\["aurox", "SC 539", auroux@math.harvard.edu\], ...\] which has every person in a department. If a piece of information is missing, put a 0 as a place holder.

Another helpful function to use is

    results[0].text.strip()
      results[0].get_text();
      results[0].get('href')
    

This is two ways to get out the piece of information inbetween the tags. The .get function allows you to get information from inside the tags such as a link. A friendly reminder is google will be your best friend for programming. If you want to find out how to do something a quick google search will help, but always feel free to ask NK or KL for help.

_HINT: You might need to use Try Except_

    
      Try:
          results[0].text.strip()
      Except Attribute Error:
          #what should it do if you get this error. Maybe figure out what is causing this error.
    

by: Naomi Kenyatta

Analysis Time
=============

Pandas
------

This portion of the assignment is very open ended. I would like you to come up with 1 question that can be answered from the data you collected

A. Google Colab
---------------

We will be working off of the colab that you made last time. Remember that every time you close out of colab you need to re run all the boxes to re get that information.

![Inspect](/assets/images/sad.png)
**SAD REACTS ONLYYYYY**

B. Questions
------------

Create a new text box and add the three questions you will try to answer.

C. Pandas
---------

For projects you will get to choose between numpy and pandas. I personally prefer pandas for data science so that is what we will be teaching. Now we need to add a new import statement. `import pandas as pd`. We have introduced lists, but pandas has a similar data structure that is more efficient when it comes to analysis called a data frame. The first thing we are going to do is convert our list into a data frame and appropriately name it.

    df = pd.DataFrame(list)
    df.columns = ["coulmn name 1","coulmn name 2","coulmn name 3"]

You can now name your columns.

D. Comparison and CSVs
----------------------

We have already compiled a second data set for you that is in a csv. You should come up with a second question that can be answered by comparing the two csvs.

E. Graphs
---------

We will talk more about graphs as we get into web design, but think of a useful graph

by: Naomi Kenyatta