---
layout: post
title:  "Numpy and Pandas"
date:   2023-02-11 02:00:00 -0500
categories: Python
---

Numpy
=====

There will be two main libraries we will use for understanding our data. The first one we will learn about is Numpy. We learned about lists in the introduction to python, but using the built in python lists doesn't come with all the nice tools and speed that numpy arrays have. To use numpy you need to first install it using pip if you have not already. You should navigate to the terminal and type in

    pip install numpy

Understanding arrays
--------------------

Now that we have numpy downloaded we can use it when coding in python.

    import numpy as np
    a = np.array([2, 3, 4])

array transforms sequences of sequences into two-dimensional arrays, sequences of sequences of sequences into three-dimensional arrays, and so on

Try testing out the above code. What is inside a. Also try using other inputs into array. When applying operations to arrays it is applied element wise

    import numpy as np
    a = np.array([2, 3, 4])
    b = np.array([1, 5, 6])
    c = a*b;

At the end of this code c will hold the array \[2,15,24\] which is different than normal matrix multiplication

Higher Dimensional Arrays
-------------------------

We can create higher dimensional arrays:

    
    a = np.array([[1, 2, 3], [4, 5, 6]])
    print(a)
    # array([[1, 2, 3],
    #        [4, 5, 6]])
    a.shape # this gives the dimensions
    # (2, 3)

To access/index the arrays, we can use slice notation.

    a[0] # [1, 2, 3]
    a[1] # [4, 5, 6]
    a[:, 0] # [1, 4]
    a[:, 1] # [2, 5]
    a[:, 2] # [3, 6]
    a[0, 1:2] # [2, 3]

some useful properties of arrays:

\- `a.shape` gives you the size of the array

\- `a[:,4] < 5` is a boolean statement which will output an array comparing each number in a to 5 and returning true of false

\- `a.ravel()` will turn any array into a 1 dimensional array

Pandas
======

The second library is pandas. Like numpy, it comes with nice tools and speed. We need to first install it using pip if you have not already. You should navigate to the terminal and type in

    pip install pandas

Understanding Dataframes
------------------------

    import pandas as pd
    iris_df = pd.read_csv('https://raw.githubusercontent.com/mwaskom/seaborn-data/master/iris.csv')
    

Here we read in data stored at this URL (visit the url to see what it looks like!). Pandas is able to read data in a variety of formats - check the documentation to learn more.

We can take a quick peek at the data using the `head` command.

    iris_df.head()

Output:

       sepal_length  sepal_width  petal_length  petal_width species
    0           5.1          3.5           1.4          0.2  setosa
    1           4.9          3.0           1.4          0.2  setosa
    2           4.7          3.2           1.3          0.2  setosa
    3           4.6          3.1           1.5          0.2  setosa
    4           5.0          3.6           1.4          0.2  setosa

Accessing a specific column:
----------------------------

    iris_df['sepal_length']

Output:

    0      5.1
    1      4.9
    2      4.7
    3      4.6
    4      5.0
          ... 
    145    6.7
    146    6.3
    147    6.5
    148    6.2
    149    5.9
    Name: sepal_length, Length: 150, dtype: float64

Creating a new column
---------------------

Let's say we want to calculate the difference in `sepal_length` and `petal_length` and make it a new column:

    iris_df['length_diff'] = iris_df['sepal_length'] - iris_df['petal_length']
    iris_df.head()
    

Output:

       sepal_length  sepal_width  petal_length  petal_width species  length_diff
    0           5.1          3.5           1.4          0.2  setosa          3.7
    1           4.9          3.0           1.4          0.2  setosa          3.5
    2           4.7          3.2           1.3          0.2  setosa          3.4
    3           4.6          3.1           1.5          0.2  setosa          3.1
    4           5.0          3.6           1.4          0.2  setosa          3.6

Querying Elements
-----------------

Let's say we want to look at only the flowers that have a sepal\_length greater than 5

First, take a look at what `iris_df['sepal_length'] > 5` returns:

    iris_df['sepal_length'] > 5

Output:

    0       True
    1      False
    2      False
    3      False
    4      False
            ...  
    145     True
    146     True
    147     True
    148     True
    149     True
    Name: sepal_length, Length: 150, dtype: bool

It is a series of booleans that indicate whether a row has a sepal\_length of more than 5. How can we use this to subset our dataframe?

    big_sepal_df = iris_df[ iris_df['sepal_length'] > 5 ]
    big_sepal_df.head()
    

Output:

        sepal_length  sepal_width  petal_length  petal_width species  length_diff
    0            5.1          3.5           1.4          0.2  setosa          3.7
    5            5.4          3.9           1.7          0.4  setosa          3.7
    10           5.4          3.7           1.5          0.2  setosa          3.9
    14           5.8          4.0           1.2          0.2  setosa          4.6
    15           5.7          4.4           1.5          0.4  setosa          4.2


Note that the indices are no longer contiguous - this shows that we've taken out the rows with `sepal_length` less than 5.

Learn more
----------

Pandas has many many more functions that could be useful if you choose to work on data journalism projects. Use Google if you ever feel stuck. Here are some things to potentially look into:

*   `df.loc, df.iloc`
*   `df.merge, pd.concat`
*   `df.apply`