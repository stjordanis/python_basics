<a name='0'></a>
# Basic of Python Programming Language

*[Status: Under Revision]*

This is a practical introduction to Python Programming Language. The style of this repo was inspired by [Chip Huyen Cool Python repo](https://github.com/chiphuyen/python-is-cool). You can find the companion notebook [here](https://github.com/Nyandwi/python_basics/blob/main/python-basics.ipynb).

Python is an interpreted, high-level, and general purpose programming language that was designed for efficiency, readability, and simplicity.

Python design philosophy emphasizes simplicity and code readability. There are about 19 Python design guiding principles, the top 5 being:

* Beautiful is better than ugly. 
* Explicit is better than implicit
* Simple is better than complex
* Complex is better than complicated
* Readability counts
* Now is better than ever
* If the implementation is hard to explain, it's a bad idea.
* If the implementation is easy to explain, it may be a good idea.

More design rules can be found in the [Zen of Python](https://en.wikipedia.org/wiki/Zen_of_Python). You can also display them by importing this(`import this`) in any Python interpreter. 


```python
import this
```

    The Zen of Python, by Tim Peters
    
    Beautiful is better than ugly.
    Explicit is better than implicit.
    Simple is better than complex.
    Complex is better than complicated.
    Flat is better than nested.
    Sparse is better than dense.
    Readability counts.
    Special cases aren't special enough to break the rules.
    Although practicality beats purity.
    Errors should never pass silently.
    Unless explicitly silenced.
    In the face of ambiguity, refuse the temptation to guess.
    There should be one-- and preferably only one --obvious way to do it.
    Although that way may not be obvious at first unless you're Dutch.
    Now is better than never.
    Although never is often better than *right* now.
    If the implementation is hard to explain, it's a bad idea.
    If the implementation is easy to explain, it may be a good idea.
    Namespaces are one honking great idea -- let's do more of those!


Python is a popular and go-to programming language in different tech communities, most notable in machine learning and data science. It is sometimes referred to as [“batteries included”](https://docs.python.org/3/tutorial/stdlib.html) due to its rich standard library. Below are more elaborated advantages of Python:

* It is simple to read and write: Python syntaxes are very easy to write and easy to recall as well. 
* It has a beautiful design and built-in data types. 
* It has thousands of great libraries in many disciplines.
* Supportive communities: Good documentation, courses, tutorials, social groups.
* Easy to learn and use due to its simple syntaxes which feel like a natural language. 

This introduction will cover the following: 


* [1. Variables, Numbers and Strings](#1)
    * [1.1 Variables](#1-1)
    * [1.2 Numbers](#1-2)
    * [1.3 Strings](#1-3)
* [2. Data Structures](#2)
    * [2.1 Lists](#2-1)
    * [2.2 Dictionaries](#2-2)
    * [2.3 Tuples](#2-3)
    * [2.4 Sets](#2-4)
* [3. Comparison and Logic Operators](#3)
* [4. Control Flow](#4)
    * [4.1 If Condition](#4-1)
    * [4.2 For Loop](#4-2)
    * [4.3 While Loop](#4-3)
* [5. Functions](#5)
* [6. Lambda Functions](#6)
* [7. Built in functions](#7)
    * [7.1 Map Function](#7-1)
    * [7.2 Filter Function](#7-2)

* [8. More Useful Python Functions](#8)
    * [8.1 List Comprehension](#8-1)
    * [8.2 Enumerate Function](#8-2)
    * [8.3 Zip Function](#8-3)

*******************
<a name='1'></a>

## 1. Variables, Numbers, and Strings

<a name='1-1'></a>


### 1.1 Variables

Below are quick notes about Python variables and other most important things to know before writing actual Python code:

* `A Variable` is a location in memory where we store the data. 
* `A variable` in Python can either be of 3 data types: `integer`, `float`, or a `string`.  Data type specifies the category of the variables.
* We can use `type(variable_name)` to find the type of given `variable_name`.
* In Python, we use `#` to add `comments`. Comments do not change anything and are not compiled.
* If your comment is longer than one line, you can use triple quotes. The lines inside triple quotes are ignore during runtime.

```
"""
In Python, there is no official way to write long comments, but you can use triple quotes.
The sentence between triple quote are ignored at runtime. You can also use single quote('''....'''). Python treats single quote as double quotes in many scanerios such as strings representation.

Guido also agreed it works: https://twitter.com/gvanrossum/status/112670605505077248 
"""
```

* We also use `=` to assign a value to the name of variable. Example: `var_name = 1`. Note that it's different to comparison operator of equal to (`==`).
* We can use `print()` to display the value of variable or the results of any expression.
* Each line of the code start on the new line.
* Be aware of indentations. Python is serious about them.


```python
# EXAMPLE OF CREATING A VARIABLE

# We use # to add comment, it won’t run or affect the code
# You use = to assign a value to the name of the variable. 
# Each code starts on the new line. No semicolon or {}
# Python is awesome. You do not need to provide the data type of variable when creating it.

int_var = 1
str_var = 'Hundred'
```
*******************

<a name='1-2'></a>

### 1.2 Numbers

Numbers in Python can either be integers `int` or floats `float`. Integer are real, finite, natural or whole numbers. Take an example: `1`,`2`,`3`,`4` are integers. Floats are numbers that have decimal points such as`4.6`, `6.0`, `7.7`. Note that `4.0` is considered as a float data type too. Recently, Karpathy, AI Director at Tesla posted that [floats are not real](https://twitter.com/karpathy/status/1475317897660612617).

We can perform operations on numbers. The operations that we can perform include addition, multiplication, division, modular, etc...


```python
int_var = 10
float_var = 12.8

type(int_var)
```




    int




```python
type(float_var)
```




    float




```python
# Numeric Operations 

# Addition

1 + 100
```




    101




```python
# Multiplication

1 * 100
```




    100




```python
# Division

1 / 100
```




    0.01




```python
# Floor division

7 // 2
```




    3




```python
# Modular (%)
# This is the remainder or a value remaining after dividing two numbers
# 100 / 1 = 100, remainder is 0

100 % 1
```




    0




```python
1 % 100
```




    1




```python
10 % 2
```




    0




```python
# Powers
# 1 power any number is 1 always

1 ** 100
```




    1




```python
2 ** 2
```




    4




```python
# We use print() to display the results of the operations or a variable

print(1 + 100)
```

    101

*******************

<a name='1-3'></a>

### 1.3 Strings

Python supports strings. String is a sequence of characters. 

Strings are one of the commonly used and important data types. Most problems involve working with strings. Thus, knowing how to work with strings is an incredible thing.

Strings are expressed in either `"..."` or `'...'`.

```
"text inside here will be a string"
'text inside here will also be a string'
```

We can manipulate strings in many ways. A simple example is to concat the strings. 


```python
str_var = 'One'
str_var2 = 'Hundred'
```


```python
str_var + str_var2
```




    'OneHundred'




```python
str_var + ' ' + 'and' + ' '+ str_var2 + '.'
```




    'One and Hundred.'




```python
# We can use print() to display a string

print(" This is a string")
```

     This is a string



```python
# We can also compare strings to check whether they are similar. 
# If they are similar, case by case, comparison operator returns true. Else false

"A string" == "a string"
```




    False




```python
"A string" == "A string"
```




    True



#### Strings Methods

Python provides many built-in methods for manipulating strings. As a programmer, knowing typical string methods and how to use them will give you a real leverage when working with strings.

There are many string methods. You can find them [here](https://docs.python.org/2.5/lib/string-methods.html). Let's see some common methods.


```python
sentence = 'This IS A String'
```


```python
# Case capitalization 
# It return the string with first letter capitalized and the rest being lower cases. 

sentence.capitalize()
```




    'This is a string'




```python
# Given a string, convert it into title (each word is capitalized)

sentence_2 = 'this is a string to be titled'
sentence_2.title()
```




    'This Is A String To Be Titled'




```python
# Converting the string to upper case

sentence.upper()
```




    'THIS IS A STRING'




```python
# Converting the string to upper case

sentence.lower()
```




    'this is a string'




```python
# Splitting the string

sentence.split()
```




    ['This', 'IS', 'A', 'String']



Lastly, we can use `replace()` method to replace some characters in string with another characters. Replace method takes two inputs: characters to be replaced, and new characters to be inserted in string, `replace('characters to be replaced', 'new characters')`. 

Example, given the string "This movie was awesome", replace the world `movie` with `project`. 


```python
stri = "This movie was awesome"
stri.replace('movie', 'project')
```




    'This project was awesome'




```python
# In the following string, replace all spaces with `%20'

stri_2 = "The future is great"
stri_2.replace(' ', '%20')
```




    'The%20future%20is%20great'



As you can see, strings methods are powerful and can save you time. Remember one of the Python philosophies that we saw in the beginning: `Simple is better than complex`. 

<a name='2'></a>
## 2. Data Structures

Data structures are used to organize and store the data. Algorithms supports operations on data.

Python has 4 main data structures: `Lists`, `Dictionaries`, `Tuples` and `Sets`. 

*******************

<a name='2-1'></a>

### 2.1 List

A list is a set of ordered values. Each value in a list is called an `element` or `item` and can be identified by an index. A list supports different data types, we can have a list of integers, strings, and floats. 

What we will see with Python lists:

- Creating a list
- Accessing elements in a list
- Slicing a list
- Changing elements in a list
- Traversing a list
- Operations on list
- Nested lists
- List methods
- List and strings

#### Creating a List

A python list can be created by enclosing elements of similar or different data type in square brackets `[...]`, or with `range()` function.


```python
# Creating a list

week_days = ['Mon', 'Tue', 'Wed', 'Thur','Fri']
even_numbers = [2, 4, 6, 8, 10]
mixed_list = ['Mon', 1, 'Tue', 2, 'Wed', 3]

# Displaying elements of a list
print(week_days)
```

    ['Mon', 'Tue', 'Wed', 'Thur', 'Fri']



```python
# Creating a list with range()

nums = range(5)

for i in nums:
    print(i)
```

    0
    1
    2
    3
    4


#### Accessing the elements of the list

We can access the a given element of the list by providing the index of the element in a bracket. The index starts at 0 in Python.


```python
# Accessing the first elements of the list

week_days[0]
```




    'Mon'




```python
even_numbers[2]
```




    6




```python
# Getting the last element of the list

print(even_numbers[-1])
```

    10


#### Slicing a list

Given a list, we can slice it to get any parts or combination of its elements forming another list.


```python
# Get the elements from index 0 to 2. Index 2 is not included.

week_days = ['Mon', 'Tue', 'Wed', 'Thur','Fri']
week_days[0:2]
```




    ['Mon', 'Tue']




```python
# Get elements from the last fourth elements to the first
# -1 starts at the last element 'Fri', -2 second last element `Thur'..... -4 to 'Tue'

week_days[-4:]
```




    ['Tue', 'Wed', 'Thur', 'Fri']




```python
# Get all elements up to the fourth index

week_days[:4]
```




    ['Mon', 'Tue', 'Wed', 'Thur']




```python
# Get all elements from the second to the last index

week_days[2:]
```




    ['Wed', 'Thur', 'Fri']



You can use `[:]` to copy the entire list. 


```python
week_days[:]
```




    ['Mon', 'Tue', 'Wed', 'Thur', 'Fri']



#### Changing elements in a list

Python lists are mutable. We can delete or change the elements of the list.


```python
names = ['James', 'Jean', 'Sebastian', 'Prit']
names
```




    ['James', 'Jean', 'Sebastian', 'Prit']




```python
# Change 'Jean' to 'Nyandwi' and 'Sebastian' to 'Ras'

names[1:3] = ['Nyandwi', 'Ras']
names
```




    ['James', 'Nyandwi', 'Ras', 'Prit']




```python
# Change 'Prit' to Sun

names[-1] = 'Sun'
names
```




    ['James', 'Nyandwi', 'Ras', 'Sun']




```python
# Change `James` to ``Francois`

names[0] = 'Francois'
names
```




    ['Francois', 'Nyandwi', 'Ras', 'Sun']



In order to delete a given element in a list, we can empty slice it but the better way to delete element is to use `del` keyword.


```python
# Delete Nyandwi in names list

del names[1]
names
```




    ['Francois', 'Ras', 'Sun']



If you know the index of the element you want to remove, you can use `pop()`. If you don't provide the index in pop(), the last element will be deleted.


```python
names = ['James', 'Jean', 'Sebastian', 'Prit']
names.pop(2)
names
```




    ['James', 'Jean', 'Prit']



Also, we can use `remove()` to delete the element provided inside the remove() method.


```python
names = ['James', 'Jean', 'Sebastian', 'Prit']
names.remove('James')
names
```




    ['Jean', 'Sebastian', 'Prit']



We can also use `append()` to add element to the list.


```python
# Adding the new elements in list

names = ['James', 'Jean', 'Sebastian', 'Prit']
names.append('Jac')
names.append('Jess')
names
```




    ['James', 'Jean', 'Sebastian', 'Prit', 'Jac', 'Jess']



#### Traversing a list

There are times that we may need to go over the list to read the elements of the list or perform iterative operations. We can use `for loop` to traverse through the list.


```python
# Given a list names, use for loop to display its elements

names = ['James', 'Jean', 'Sebastian', 'Prit']

for name in names:
    print(name)
```

    James
    Jean
    Sebastian
    Prit



```python
# Given a list nums, add 1 to the first element, 2 to the second, 3 to 3rd element, 4 to 4th element
# Example: nums = [1,2,3,6] will be nums_new = [2,4,6,10]

nums = [1, 2, 3, 6]
nums_new = []

for i in range(len(nums)): #len(nums) gives the length of the list
    num = nums[i] + i + 1
    nums_new.append(num)
    
nums_new
```




    [2, 4, 6, 10]



#### Operations on list


```python
# Concatenating two lists

a = [1,2,3]
b = [4,5,6]

c = a + b

c
```




    [1, 2, 3, 4, 5, 6]




```python
# We can also use * operator to repeat a list a number of times

[None] * 5
```




    [None, None, None, None, None]




```python
[True] * 4
```




    [True, True, True, True]




```python
[1,2,4,5] * 2
```




    [1, 2, 4, 5, 1, 2, 4, 5]



#### Nested lists


```python
# Creating a list in other list

nested_list = [1,2,3, ['a', 'b', 'c']]


# Get the ['a', 'b', 'c'] from the nested_list

nested_list[3]
```




    ['a', 'b', 'c']




```python
# Indexing and slicing a nested list is quite similar to normal list

nested_list[1]
```




    2



#### List Methods

Python also offers methods which make it easy to work with lists. We already have been using some list methods such as `pop()` and `append()` but let's review more other methods.


```python
# Sorting a list with sort()

even_numbers = [2,14,16,12,20,8,10]

even_numbers.sort()

even_numbers
```




    [2, 8, 10, 12, 14, 16, 20]




```python
# Reversing a string with reverse()

even_numbers.reverse()
even_numbers
```




    [20, 16, 14, 12, 10, 8, 2]




```python
# Adding other elements to a list with append()

even_numbers = [2,14,16,12,20,8,10]

even_numbers.append(40)
even_numbers
```




    [2, 14, 16, 12, 20, 8, 10, 40]




```python
# Removing the first element of a list

even_numbers.remove(2)
even_numbers
```




    [14, 16, 12, 20, 8, 10, 40]




```python
## Return the element of the list at index x

even_numbers = [2,14,16,12,20,8,10]

## Return the item at the 1st index

even_numbers.pop(1)
```




    14




```python
# pop() without index specified will return the last element of the list

even_numbers = [2,14,16,12,20,8,10]
even_numbers.pop()
```




    10




```python
# Count a number of times an element appear in a list

even_numbers = [2,2,4,6,8]
even_numbers.count(2)
```




    2



#### List and strings

We previously have learned about strings. Strings are sequence of characters. List is a sequence of values. 


```python
# We can convert a string into list

stri = 'Apple'

list(stri)
```




    ['A', 'p', 'p', 'l', 'e']




```python
# Splitting a string produces a list of individual words

stri_2 = "List and Strings"
stri_2.split()
```




    ['List', 'and', 'Strings']



The split() string method allows to specify the character to use a a boundary while splitting the string. It's called delimiter.


```python
stri_3 = "state-of-the-art"

stri_3.split('-')
```




    ['state', 'of', 'the', 'art']

**********************


<a name='2-2'></a>

### 2.2 Dictionaries

Dictionary stores keys and values. 


```python
# Example of Dictionary

# Countries codes: https://countrycode.org

countries_code = { "United States": 1,
                 "India": 91,
                 "Germany": 49,
                 "China": 86,
                 "Rwanda":250
            }
```


```python
countries_code
```




    {'United States': 1, 'India': 91, 'Germany': 49, 'China': 86, 'Rwanda': 250}




```python
countries_code.items()
```




    dict_items([('United States', 1), ('India', 91), ('Germany', 49), ('China', 86), ('Rwanda', 250)])




```python
countries_code.keys()
```




    dict_keys(['United States', 'India', 'Germany', 'China', 'Rwanda'])




```python
countries_code.values()
```




    dict_values([1, 91, 49, 86, 250])




```python
countries_code['India']
```




    91




```python
countries_code['Rwanda']
```




    250




```python
# Adding new country and code

countries_code['Cuba'] = 53

countries_code
```




    {'United States': 1,
     'India': 91,
     'Germany': 49,
     'China': 86,
     'Rwanda': 250,
     'Cuba': 53}



***Notes on Dictionary***

* Dictionary are not ordered and it can not be sorted - which is different to list. 

* Dictionary can hold data of different types: floats, integers and strings and can also store lists. 

**********************

<a name='2-3'></a>

### 2.3 Tuples

Tuple is similar to list but the difference is that you can't change the values once it is defined (termed as `immutability`). Due to this property it can be used to keep things that you do not want to change in your program. Example can be a country codes, zipcodes, etc...




```python
tup = (1,4,5,6,7,8)
```


```python
# Indexing

tup[4]
```




    7




```python
## Tuples are not changeable. Running below code will cause an error

# tup[2] = 10
```


```python
# You can not also add other values to the tuple. This will be error
#tup.append(12)
```
**********************
<a name='2-4'></a>

### 2.4 Sets

Sets are used to store the unique elements. They are not ordered like list. 


```python
set_1 = {1,2,3,4,5,6,7,8}

set_1
```




    {1, 2, 3, 4, 5, 6, 7, 8}




```python
set_2 = {1,1,2,3,5,3,2,2,4,5,7,8,8,5}
set_2
```




    {1, 2, 3, 4, 5, 7, 8}



As you can see, set only keep unique values. There can't be a repetition of values. 


```python
# List Vs Set

odd_numbers = [1,1,3,7,9,3,5,7,9,9]

print("List:{}".format(odd_numbers))

print("#####")

set_odd_numbers = {1,1,3,7,9,3,5,7,9,9}

print("Set:{}".format(set_odd_numbers))
```

    List:[1, 1, 3, 7, 9, 3, 5, 7, 9, 9]
    #####
    Set:{1, 3, 5, 7, 9}


<a name='3'></a>

## 3. Comparison and Logic operators

`Comparison` operators are used to compare values. It will either return true or false. 


```python
## Greater than 
100 > 1
```




    True




```python
## Equal to

100 == 1
```




    False




```python
## Less than

100 < 1
```




    False




```python
## Greater or equal to

100 >= 1
```




    True




```python
## Less or equal to

100 <= 1
```




    False




```python
'Intro to Python' == 'intro to python'
```




    False




```python
'Intro to Python' == 'Intro to Python'
```




    True



`Logic` operators are used to compare two expressions made by comparison operators. 

* Logic `and` returns true only when both expressions are true, otherwise false. 

* Logic `or` returns true when either any of both expressions is true. Only false if both expressions are false.

* Logic `not` as you can guess, it will return false when given expression is true, vice versa. 


```python
100 == 100 and 100 == 100
```




    True




```python
100 <= 10 and 100 == 100
```




    False




```python
100 == 10 or 100 == 100
```




    True




```python
100 == 10 or 100 == 10
```




    False




```python
not 1 == 2
```




    True




```python
not 1 == 1
```




    False



<a name='4'></a>
## 4. Control Flow
As an engineer, you will need to make decisions depending on the particular situation. You will also need to control the flow of the program and this is where `Control Flow` comes in. 

We will cover:

* If statement
* For loop
* While loop





<a name='4-1'></a>

### 4.1 If, Elif, Else



Structure of If condition:

```
if condition:
  do something

else:
  do this
```



```python
if 100 < 2:

  print("As expected, no thing will be displayed")
```


```python
if 100 > 2:

  print("As expected, no thing will be displayed")
```

    As expected, no thing will be displayed



```python
if 100 < 2:

  print("As expected, no thing will be displayed")

else:
  print('Printed')
```

    Printed



```python
# Let's assign a number to a variable name 'jean_age' and 'yannick_age'

john_age = 30
luck_age = 20

if john_age > luck_age:
  print("John is older than Luck")

else:
  print(" John is younger than Luck")
```

    John is older than Luck



```python
# Let's use multiple conditions 

john_age = 30
luck_age = 20
yan_age = 30

if john_age < luck_age:
  print("John is older than Luck")

elif yan_age == luck_age:
  print(" Yan's Age is same as Luck")

elif luck_age > john_age:
  print("Luck is older than John")

else:
  print("John's age is same as Yan")
```

    John's age is same as Yan


We can also put if condition into one line of code. This can be useful when you want to make a quick decision between few choices. 

Here is the structure:

`'value_to_return_if_true' if condition else 'value_to_return_if_false'`

Let's take some examples...


```python
# Example 1: Return 'Even' if below num is 'Even' and `Odd` if not. 

num = 45

'Even' if num % 2 == 0 else 'Odd'
```




    'Odd'




```python
# Example 2: Return True if a given element is in a list and False if not

nums = [1,2,3,4,5,6]

True if 3 in nums else False
```




    True



<a name='4-2'></a>
### 4.2 For Loop

For loop is used to iterate over list, string, tuples, or dictionary. 

Structure of for loop:

```
for item in items:
  do something
```




```python
even_nums = [2,4,6,8,10]

for num in even_nums:
  print(num)
```

    2
    4
    6
    8
    10



```python
week_days = ['Mon', 'Tue', 'Wed', 'Thur','Fri']

for day in week_days:
  print(day)
```

    Mon
    Tue
    Wed
    Thur
    Fri



```python
sentence = "It's been a long time learning Python. I am revisiting the basics!!"

for letter in sentence:
  print(letter)
```

    I
    t
    '
    s
     
    b
    e
    e
    n
     
    a
     
    l
    o
    n
    g
     
    t
    i
    m
    e
     
    l
    e
    a
    r
    n
    i
    n
    g
     
    P
    y
    t
    h
    o
    n
    .
     
    I
     
    a
    m
     
    r
    e
    v
    i
    s
    i
    t
    i
    n
    g
     
    t
    h
    e
     
    b
    a
    s
    i
    c
    s
    !
    !



```python
sentence = "It's been a long time learning Python. I am revisiting the basics!!"

# split is a string method to split the words making the string

for letter in sentence.split():
  print(letter)
```

    It's
    been
    a
    long
    time
    learning
    Python.
    I
    am
    revisiting
    the
    basics!!



```python
# For loop in dictionary 

countries_code = { "United States": 1,
                 "India": 91,
                 "Germany": 49,
                 "China": 86,
                 "Rwanda":250
            }

for country in countries_code:
  print(country)
```

    United States
    India
    Germany
    China
    Rwanda



```python
for code in countries_code.values():
  print(code)
```

    1
    91
    49
    86
    250


For can also be used to iterate over an sequence of numbers. `Range` is used to generate the sequence of numbers. 



```
for number in range: 
  do something
```




```python
for number in range(10):
  print(number)
```

    0
    1
    2
    3
    4
    5
    6
    7
    8
    9



```python
for number in range(10, 20):
  print(number)
```

    10
    11
    12
    13
    14
    15
    16
    17
    18
    19


One last thing about `for loop` is that we can use it to make a list. This is called list comprehension.


```python
letters = []

for letter in 'MachineLearning':
  letters.append(letter)

letters
```




    ['M', 'a', 'c', 'h', 'i', 'n', 'e', 'L', 'e', 'a', 'r', 'n', 'i', 'n', 'g']



The above code can be simplified to the following code:


```python
letters = [letter for letter in 'MachineLearning']

letters
```




    ['M', 'a', 'c', 'h', 'i', 'n', 'e', 'L', 'e', 'a', 'r', 'n', 'i', 'n', 'g']



<a name='4-3'></a>

### 4.3 While loop

While loop will executes the statement(s) as long as the condition is true.

Structure of while loop



```
while condition:
  statement(s)
```




```python
a = 10
while a < 20:
    print('a is: {}'.format(a))
    a = a + 1
```

    a is: 10
    a is: 11
    a is: 12
    a is: 13
    a is: 14
    a is: 15
    a is: 16
    a is: 17
    a is: 18
    a is: 19

**********************

<a name='5'></a>

## 5. Functions

Functions are used to write codes or statements that can be used multiple times with different parameters. 

One fundamental rule in programming is "DRY" or Do not Repeat Yourself. Functions will help to not repeat yourself. 

This is how you define a function in Python:

```
def function_name(parameters):

  """
  This is Doc String
  You can use it to notes about the functions
  """
  statements 

  return results
```
* `function_name` is the name of the function. It must not be similar to any built in functions. We will see built in functions later. 
* `parameters` are the values that are passed to the function.
* `Doc String` is used to add notes about the function. It is not a must to use it but it is a `good practice`. 

* `return` specify something or value that you want to return everytime you call or run your function. 




```python
# Function to add two numbers and return a sum

def add_nums(a,b):

  """
  Function to add two numbers given as inputs
  It will return a sum of these two numbers
  """

  sum = a+b
  
  return sum
```


```python
add_nums(2,4)
```




    6




```python
add_nums(4,5)
```




    9




```python
# Displaying the doc string noted early

print(add_nums.__doc__)
```

    
      Function to add two numbers given as inputs
      It will return a sum of these two numbers
      



```python
def activity(name_1, name_2):

  print("{} and {} are playing basketball!".format(name_1, name_2))
```


```python
activity("Chris", "Francois")
```

    Chris and Francois are playing basketball!



```python
activity("Kennedy", "Kleber")
```

    Kennedy and Kleber are playing basketball!


As you can see, functions do not need to always have `return`. When you only want to display the customized message (not involving expression), `print()` will be enough. 

<a name='6'></a>

## 6. Lamdba Functions

There are times that you want to create anonymous functions. These types of functions will only need to have one expressions. 



```python
## Sum of two numbers 

def add_nums(a,b):

  sum = a+b
  
  return sum

add_nums(1,3)
```




    4



We can use lambda to make the same function in just one line of code! Let's do it!!


```python
sum_of_two_nums = lambda c,d: c + d

sum_of_two_nums(4,5)
```




    9

**********************

## <a name='7'></a>

## 7. Built in Functions

Python being a high level programming language, it has bunch of built in functions which make it easy to get quick computations done. 

An example of built in functions we used is `len()` which gives the length of the string or the list given as the input to it. 

Here is a full preview on all [Python Built in functions](https://docs.python.org/3/library/functions.html). This is taken from that link. 

![Py Built in Functions](data:image/png;base64,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znsuATHeoZ+eW/93eufQnzsliOvvhAD0707o4do7IQDduxN6uLa4CYh+OlqsutU5uoDIHwRAAARAAARAAARAAARAAARKggCMo5KgjDxAAARAAARAAARAAARAAAScngCMI6evIhQQBEAABEAABEAABEAABECgJAjAOCoJysgDBEAABEAABEAABEAABEDA6QnAOHL6KkIBQQAEQAAEQAAEQAAEQAAESoIAjKOSoIw8QAAEQAAEQAAEQAAEQAAEnJ4AjCOnryIUEARAAARAAARAAARAAARAoCQIwDgqCcrIAwRAAARAAARAAARAAARAwOkJwDhy+ipCAUEABEAABEAABEAABEAABEqCAIyjkqCMPEAABEAABEAABApNYE9sMh0+nVLo63EhCIAACNhKoMSMo3kbj9CQGcvojV922lo2m+PFn0+jW7duFYifk3OLTianFghHgGcT2B93noa+vVzp47rIU3bBePvXXeo60eXHZ4fZda1p5OQrV0l01JLYEsfS9abn5Hcivxc9uZh+jS5lZOmd8uiwj5btUXX+2ar9xc6hMHmhTou9WpCBExB4df42mrXyQImV5MrV6yRtop5IG5ptpe3Wu87Tw6StOsfPPVsFdWArKcQragIlZhz1bV2P/H0r2vXDsOVmNx5KoEdmrqbr2TkFol+9fpMe43P2doALJIQAtyLQqGY1enpIG0pPzyJpfO2R0Z2DadKgNtSyQQ1KSkm359ICce9/fyWtP3i6QLhxgC1xjONbO35tYTjNXq3fwdh2LJHGzlxDF9IyrSXjUeeHd2hI3uW9KDm1+LkUJi/UqUepo8febGiTAOratGaJ3L8MEj3w0WraHZOsm99Hy/fSqwu2655DoHkCO6KS6N4Zy+mmTn/N9CrUgSkRfC9JAsViHOkpfpB/FWoYUMWue9NLxziBG9nZ9P7iCOrcqg6V9ypjfEodV/IuSx1b1qFPl+/HKE8BOp4bULlCWRrZMZjKlNFXf5mEzLqZrQuodaAf3dulEYU2DNA9bxpoSYezb+ZQetYN00vyfbclTr4L+Iu5PHdFn6ONESdpQLtA00vU97t5ACMzM4u+23BU97ynBrasX53q+lWmUnkAzPE15mMtjow6681225sX6tSYunsfi05pDhLy7DMncs7SjLSt6VhKQy/v4p5J+fCRu2hiv1Z6WRvCrN27IaKVgy/WRKq2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gAT8TYDGkb9LgNcnARIgARIgARIgARIgARIICAI0jgKiGJgJEiABEiABEiABEiABEiABfxOgceTvEuD1SYAESIAESIAESIAESIAEAoIAjaOAKAZmggRIgARIgARIgARIgARIwN8EaBz5uwR4fRIgARIgARIgARIgARIggYAgQOMoIIqBmSABEiABEiABEiABEiABEvA3ARpH/i4BXp8ESIAESIAESIAESIAESCAgCNA4CohiYCZIgARIgARIgARIgARIgAT8TYDGkb9LgNcnARIgARIgARIggXxAYEPMMdlx4GQ+uBPeQkEmEHItb35J1CF59+f1uKQN/wvJJ492k/rVK1zLLOTZtZIupYrNZpMyJYo6XWPNngR5/ac1UrJ4iEz72wCn/bnZcNe//5BzSZekfcPq8sbQTpanijt+TsKqlJFChQpl2Z+WZpO4E+ekbmi5LNv5wz2BY2cuSJWyJaVw4aw83R/lvNeb83iTxvnMrreojsafOC91qpZ1SpR4/qKhIxVLF3faV9A3vPnzWlkZddjAEFqxtEx8oo9fkeRFfqgbfi3SoL34mQspciUtTSqVKeF0D9r21KpcRorksq50OjE3BCyBFyaukLDq5WXCYz1znUfqVq4R8gQ5JHBNR46ah1WW0QNayB2RDeX0qSRJung5h9kOvMPe+2WDvDZljWXGGl1XUTo0qi7H0FD4Wh7v30K0s5aADruVLNp+UO4fN1tSrqQ57b6QkioPYt/8rfFO+7jBNYE735klC7YdcJ3Ayz3enMebNF5ezkj24qTV8snsLZaHrNh1RIaO+0NOnEu23F+QNw7pECEj+10vTetUloST5/2OIi/yQ93we7EGXQZOwTF313uzZX30Mcu8v/frRnnhh5WW+7gxfxJo3SBUOjWsluubo27lGiFPkAsCeWIcpVp0xDWPleFZGti2rgxoU8erLLs6j/3BvkiTknol85SXr1z9nrkx48vFy6736TmSLqY6HmL8rgBPfNuI0Mx96qHV/+5ER3W8ka5NrpMIeGmsRO/lnanrpEOzmlI8pIhTEh3late0prz/62Z4/ry7ntNJ8uEGLZpLdjrheItXUtPk/CXvDHt3+unNebxJ45g/V9dcu++oLFq3X/q0DHM8xPjdo3ktSU6+JN8u3Gm5vyBvbB5WRW7rWE9a1736HLvj4en51v3ePHOuyjI7+dHr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)


```python
# using len() to count the length of the string

message = 'Do not give up!'
len(message)
```




    15




```python
odd_numbers = [1,3,5,7]
len(odd_numbers)
```




    4




```python
# Using max() to find the maximum number in a list

odd_numbers = [1,3,5,7]
max(odd_numbers)
```




    7




```python
# Using min() to find the minimum number in a list

min(odd_numbers)
```




    1




```python
# Sorting the list with sorted()

odd_numbers = [9,7,3,5,11,13,15,1]

sorted(odd_numbers)
```




    [1, 3, 5, 7, 9, 11, 13, 15]



Let's learn two more useful built functions: they are `map` and `filter`. You can try to explore or use more built in functions on your own. 

**********************

<a name='7-1'></a>

### 7.1 Map function 

Map gives you the ability to apply a function to an iterable structures such as list. When used with a list for example, you can apply the function to every element of the list. 

Let's see how it works. 



```python
def cubic(number):
  return number ** 3
```


```python
num_list = [0,1,2,3,4]
```


```python
# Applying `map` to the num_list to just return the list where each element is cubed...(xxx3)

list(map(cubic, num_list))
```




    [0, 1, 8, 27, 64]



<a name='7-2'></a>

### 7.2 Filter function

Let's say that you have a list of numbers and you want to filter the list and remain with odd numbers. Odd number is any number which can not be divided by 2. 

You can develop a function to calculate it but you would have to always pass single value or values but not entire list. 

Using `filter`, you can return `true` for every element of list evaluated by the function. 


```python
def odd_check(number):
  
  return number % 2 != 0 

# != is not equal to operation
```


```python
num_list = [1,2,4,5,6,7,8,9,10,11]

list(filter(odd_check, num_list))
```




    [1, 5, 7, 9, 11]

**********************


<a name='8'></a>

## 8. More Useful Python Functions

Python is an awesome programming language that has a lot of useful functions.

Let's see more useful things you may need beyond what's we just saw already.

### 8.1 List Comprehension

List comprehension makes it easy to make a new list from an existing list based on a given conditions. It's very concise and readable.

Take an example for the following cases. 


```python
# Given a list of numbers, can you make a new list of even numbers from the list nums?
# Even numbers are numbers divisible by 2, and they give the remainder of 0

nums = range(1,20)
even_nums = []


# A traditional way to do it is:

for num in nums: 
  if num % 2 == 0: 
    even_nums.append(num)

print(even_nums)
```

    [2, 4, 6, 8, 10, 12, 14, 16, 18]


A more concise and easy way to do that is to use list comprehension. 


```python
even_nums = [num for num in nums if num % 2 == 0]
print(even_nums)
```

    [2, 4, 6, 8, 10, 12, 14, 16, 18]


You can see it's pretty simple. And more readable than the former. Let's take another example.


```python
days = ['Monday', 'Tuesday', 'Wednesday', 'Thursday', 'Friday', 'Saturday']
day_T = []

# Make a list of days that start with `T`

for day in days: 
  if day[0] == 'T':
    day_T.append(day)

print(day_T)
```

    ['Tuesday', 'Thursday']


A more concise way to do it would be: 


```python
day_T = [day for day in days if day[0] == 'T']
print(day_T)
```

    ['Tuesday', 'Thursday']


### 8.2 Enumerate Function

Enumerate function convert iterable objects into enumerate object. It basically returns a tuple that also contain a counter. 

That's sounds hard, but with examples, you can see how powerful this function is... 


```python
seasons = ['Spring', 'Summer', 'Fall', 'Winter']

list(enumerate(seasons))
```




    [(0, 'Spring'), (1, 'Summer'), (2, 'Fall'), (3, 'Winter')]



As you can see, each element came with index counter automatically. The counter initially start at 0, but we can change it. 


```python
list(enumerate(seasons, start=1))
```




    [(1, 'Spring'), (2, 'Summer'), (3, 'Fall'), (4, 'Winter')]



Here is another example: 


```python
class_names = ['Rock', 'Paper', 'Scissor']

for index, class_name in enumerate(class_names, start=0):
  print(index,'-',class_name)
```

    0 - Rock
    1 - Paper
    2 - Scissor


### 8.3 Zip Function

Zip is an incredible function that takes two iterators and returns a pair of corresponsing elements as a tuple. 


```python
name = ['Jessy', 'Joe', 'Jeannette']
role = ['ML Engineer', 'Web Developer', 'Data Engineer']

zipped_name_role = zip(name, role)
zipped_name_role
```




    <zip at 0x1080cb200>



The zip object return nothing. In order to show the zipped elements, we can use a list. It's also same thing for enumerate you saw above.


```python
list(zipped_name_role)
```




    [('Jessy', 'ML Engineer'),
     ('Joe', 'Web Developer'),
     ('Jeannette', 'Data Engineer')]



*This is the end of the lab. The basics of the programming are always good to have, and hopefully this single notebook provided all the necessary things to know about Python.*

## [BACK TO TOP](#0)
