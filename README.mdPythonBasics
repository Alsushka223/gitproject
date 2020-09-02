# Python Basics
This part teaches you the basic concepts you’ll need to write Python programs. Many of these concepts are common to all programming languages, so they’ll be useful throughout your life as a programmer or QA Engineer.
In Chapter 1 you’ll install Python on your computer and run your first program, which prints the message Hello world! to the screen. 
In Chapter 2 you’ll learn to store information in variables and work with text and numerical values.
Chapters 3 and 4 introduce lists. Lists can store as much information as you want in one variable, allowing you to work with that data efficiently. You’ll be able to work with hundreds, thousands, and even millions of values in just a few lines of code.
In Chapter 5 you’ll use if statements to write code that responds one way if certain conditions are true, and responds in a different way if those conditions are not true.
Chapter 6 shows you how to use Python’s dictionaries, which let you make connections between different pieces of information. Like lists, dictionaries can contain as much information as you need to store.

## Week 1

### Chapter 2 - Variables and Simple Data Types
In this chapter you’ll learn about the different kinds of data you can work with in your Python programs. You’ll also learn how to store your data in variables and how to use those variables in your programs.

#### Strings

```python
name = "ada lovelace"
print(name.title())
print(name.upper())
print(name.lower())

# Stripping Whitespace
favorite_language = 'python '
favorite_language.rstrip()  # >> 'python'

```

#### Numbers
You can add (+), subtract (-), multiply (*), and divide (/) integers in Python.

```python
>>> 2 + 3
5
>>> 3 - 2
1
>>> 2 * 3
6
>>> 3 / 2
1.5

# Floats
>>> 0.1 + 0.1
0.2
>>> 0.2 + 0.2
0.4
>>> 2 * 0.1
0.2
>>> 2 * 0.2
0.4

age = 23
message = "Happy " + str(age) + "rd Birthday!"
print(message)
```
#### Boolean
Binary data type that can be True or False only.

```python
boolean_variable = True
print(boolean_variable) # >>> True

boolean_variable = False
print(boolean_variable) # >>> False

```

### Chapter 3 - Introducing Lists 
A list is a collection of items in a particular order. You can make a list that includes the letters of the alphabet, the digits from 0–9, or the names of all the people in your family. You can put anything you want into a list, and the items in your list don’t have to be related in any particular way. Because a list usually contains more than one element, it’s a good idea to make the name of your list plural, such as letters, digits , or names. 
In Python, square brackets ([]) indicate a list, and individual elements in the list are separated by commas. Here’s a simple example of a list that contains a few kinds of bicycles:

```python
bicycles.py bicycles = ['trek', 'cannondale', 'redline', 'specialized']
print(bicycles)

print(bicycles[1])  # accessing second element on index 1
print(bicycles[3])
print(bicycles[-1])  # accessing the last element
```
**Changing, Adding, and Removing Elements**

Most lists you create will be dynamic, meaning you’ll build a list and then add and remove elements from it as your program runs its course.

```python
motorcycles = ['honda', 'yamaha', 'suzuki']
print(motorcycles)

# updating first element
motorcycles[0] = 'ducati' 
print(motorcycles)

# adding to the end of the list
motorcycles.append('ducati') 
# adding as a fist element and shifting the rest to right
motorcycles.insert(0, 'ducati') 

# removing the element under index 1
del motorcycles[1] 
# removing the last element and assigning the same value to new variables
popped_motorcycle = motorcycles.pop() 
# removing by value 
motorcycles.remove('ducati') 

```
**Organizing a List**

Often, your lists will be created in an unpredictable order, because you can’t always control the order in which your users provide their data. Although this is unavoidable in most circumstances, you’ll frequently want to present your information in a particular order.

```python
cars = ['bmw', 'audi', 'toyota', 'subaru']
cars.sort() # permenant sorting that effects original list
print(cars)
cars.sort(reverse=True) # sorting in descending order

print(sorted(cars)) # sorted temporarily 
cars.reverse() # To reverse the original order of a list,
```
**Finding the Length of a List**

You can quickly find the length of a list by using the len() function. The list in this example has four items, so its length is 4:
```python
>>> cars = ['bmw', 'audi', 'toyota', 'subaru']
>>> len(cars)
4
```
## Week 2 
### Chapter 4 - Working with Lists
In this chapter you’ll learn how to loop through an entire list using just a few lines of code regardless of how long the list is. Looping allows you to take the same action, or set of actions, with every item in a list. As a result, you’ll be able to work efficiently with lists of any length, including those with thousands or even millions of items.

```python
magicians = ['alice', 'david', 'carolina']
for magician in magicians:
    print(magician.title() + ", that was a great trick!") # this is repeatitive code, see the indentation after 'for' line
print("Thank you, everyone. That was a great magic show!") # this is outside of the loop and executed once only
```
**Forgetting to Indent Additional Lines**

Sometimes your loop will run without any errors but won’t produce the expected result. This can happen when you’re trying to do several tasks in a loop and you forget to indent some of its lines.

### Chapter 5. IF Statements
Programming often involves examining a set of conditions and deciding which action to take based on those conditions. Python’s if statement allows you to examine the current state of a program and respond appropriately to that state.

In this chapter you’ll learn to write conditional tests, which allow you to check any condition of interest. You’ll learn to write simple if statements, and you’ll learn how to create a more complex series of if statements to identify when the exact conditions you want are present. You’ll then apply this concept to lists, so you’ll be able to write a for loop that handles most items in a list one way but handles certain items with specific values in a different way. 

#### Simple Example
The following short example shows how if tests let you respond to special situations correctly. Imagine you have a list of cars and you want to print out the name of each car. Car names are proper names, so the names of most cars should be printed in title case. However, the value 'bmw' should be printed in all uppercase. The following code loops through a list of car names and looks for the value 'bmw'. Whenever the value is 'bmw', it’s printed in uppercase instead of title case:

 ```python
cars = ['audi', 'bmw', 'subaru', 'toyota']
for car in cars:
    if car == 'bmw':
        print(car.upper())
    else:
        print(car.title())
```

### Chapter 9. Dictionaries
In this chapter you’ll learn how to use Python’s dictionaries, which allow you to connect pieces of related information. You’ll learn how to access the information once it’s in a dictionary and how to modify that information. Because dictionaries can store an almost limitless amount of information, I’ll show you how to loop through the data in a dictionary. Additionally, you’ll learn to nest dictionaries inside lists, lists inside dictionaries, and even dictionaries inside other dictionaries.

#### A Simple Dictionary
```python 
alien_0 = {'color': 'green', 'points': 5}
print(alien_0['color'])
print(alien_0['points'])
```

The dictionary alien_0 stores the alien’s color and point value. The two print statements access and display that information, as shown here:
```python
green
5
```

#### Looping Through All Key-Value Pairs
```python
for key, value in alien_0.items():
    print("Key: " + key)
    print("Value: " + value)
````

#### Looping Through All Keys
```python
for key in alien_0.keys():
    print("Key: " + key)
````

#### Looping Through All Values
```python
for value in alien_0.values():
    print("Value: " + value)
````

### Steps to clone the project 
1. Copy the url of the repository ending with '.git' (https://github.com/2020spring/PythonBasics.git)
2. GitHub Desktop: 
    * Go to Current Repository
    * click on Add drop down
    * Clone Repository
    * click on URL tab
    * paste the copied URL (https://github.com/2020spring/PythonBasics.git)
    * choose the location from your local machine `C:\dev\` then click on Clone.

    Git Bash: navigate to the right directory `C:\dev\` and enter following:
    ```bash
    git clone https://github.com/2020spring/PythonBasics.git
    ```

3. [optional] Create your feature branch: 
    ```bash
    git checkout -b pythonbasics_akmal
    ```
4. Open the `C:\dev\PythonBasics` folder from your PyCharm and start modifying the code.

## References
* [Python Documentation - Lists](https://docs.python.org/3/tutorial/datastructures.html#more-on-lists)
* [Socratica - If, Then, Else in Python (video)](https://youtu.be/f4KOjWS_KZs)
* [Socratica - Lists (video)](https://youtu.be/ohCDWZgNIU0)
* [Socratica - Dictionaries](https://youtu.be/XCcpzWs-CI4)
* [Python Crash Course](http://bedford-computing.co.uk/learning/wp-content/uploads/2015/10/No.Starch.Python.Oct_.2015.ISBN_.1593276036.pdf)
