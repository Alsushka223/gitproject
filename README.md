# Header Text

## Smaller Header text

**Bold text**

*Itelics text*

- bullet 1
- bullet 2

[ ] checkbox, unchecjed
[x] checkbox, checked

[google link] (https://www.google.com/)
! [picture_name_but_not displayed] (folder/picture.png)

# Using Git for Version Control
![git_overview](pictures./git-flow-header.jpeg)



# Week 4 Fall-2019
Functions Continued, Modules, Packages, Classes

### Chapter 8. Functions
In this chapter you’ll learn to write functions, which are named blocks of code that are designed to do one specific job. When you want to perform a particular task that you’ve defined in a function, you call the name of the function responsible for it. If you need to perform that task multiple times throughout your program, you don’t need to type all the code for the same task again and again; you just call the function dedicated to handling that task, and the call tells Python to run the code inside the function. You’ll find that using functions makes your programs easier to write, read, test, and fix.

#### Defining a Function
Here’s a simple function named greet_user() that prints a greeting:
 ```python
 def greet_user():
     """Display a simple greeting."""
     print("Hello!")

greet_user()
```

#### Passing Information to a Function
The function now expects you to provide a value for username each time you call it. When you call greet_user(), you can pass it a name, such as 'jesse', inside the parentheses:

```python
def greet_user(username):
    """Display a simple greeting."""
    print(f"Hello, {username.title()}!")

greet_user('jesse')
```

## Steps to clone the project 
1. Copy the url of the repository ending with .git (https://github.com/2019-Fall/week4.git)
2. GitHub Desktop: 
    * Go to Current Repository
    * click on Add drop down
    * Clone Repository
    * click on URL tab
    * paste the copied URL (https://github.com/2019-Fall/week4.git)
    * choose the location from your local machine `C:\dev\` then click on Clone.

    Git Bash: navigate to the right directory `C:\dev\` and enter following:
  ```bash
  git clone https://github.com/2019-Fall/week4.git
  ```

  3. [optional] Create your feature branch: 
  ```bash
  git checkout -b week4_john
  ```
  4. Open the `C:\dev\week4` folder from your VS Code and start modifying the code.

## Working with class file , get updates and make changes in your branch
1. clone the repository from asotools
```
git clone <url>
cd newrepo
git checkout -b 'yourbranch'
```
2. make changes in your repository, local changes.
3. Go to your github account create a new repository to save YOUR changes
4. Get the URL of that repository from Github
5. Set the your branch upstream to your Github repository that you just created.
```
git push --set-upstream  <url from your github repo>
```
6. To get he updates from asotoolsny repo switch to master branch and then git push
```
git checkout master
git pull
```
7. to get new changes from updated master to your branch:
```
git rebase master
```

## References

* [Python Documentation - Modules](https://docs.python.org/3/tutorial/modules.html)
* [Socratica - Recursion](https://youtu.be/Qk0zUZW-U_M)
* [Socratica - Classes and Objects](https://youtu.be/apACNr7DC_s)
* [Python Crash Course](http://bedford-computing.co.uk/learning/wp-content/uploads/2015/10/No.Starch.Python.Oct_.2015.ISBN_.1593276036.pdf)

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


# Week 3
Dictionaries, nested dictionaries, Functions

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

### Chapter 8. Functions
In this chapter you’ll learn to write functions, which are named blocks of code that are designed to do one specific job. When you want to perform a particular task that you’ve defined in a function, you call the name of the function responsible for it. If you need to perform that task multiple times throughout your program, you don’t need to type all the code for the same task again and again; you just call the function dedicated to handling that task, and the call tells Python to run the code inside the function. You’ll find that using functions makes your programs easier to write, read, test, and fix.

#### Defining a Function
Here’s a simple function named greet_user() that prints a greeting:
 ```python
 def greet_user():
     """Display a simple greeting."""
     print("Hello!")

greet_user()
```

## Steps to clone the project 
1. Copy the url of the repository ending with .git (https://github.com/2019-Fall/week3.git)
2. GitHub Desktop: 
    * Go to Current Repository
    * click on Add drop down
    * Clone Repository
    * click on URL tab
    * paste the copied URL (https://github.com/2019-Fall/week3.git)
    * choose the location from your local machine `C:\dev\` then click on Clone.

    Git Bash: navigate to the right directory `C:\dev\` and enter following:
  ```bash
  git clone https://github.com/2019-Fall/week3.git
  ```

  3. [optional] Create your feature branch: 
  ```bash
  git checkout -b week3_john
  ```
  4. Open the `C:\dev\week3` folder from your VS Code and start modifying the code.

// changes here 

## References
* [Python Documentation - Dictionaries](https://docs.python.org/3/tutorial/datastructures.html#dictionaries)
* [Socratica - Dictionaries](https://youtu.be/XCcpzWs-CI4)
* [Python Crash Course](http://bedford-computing.co.uk/learning/wp-content/uploads/2015/10/No.Starch.Python.Oct_.2015.ISBN_.1593276036.pdf)


## Week 4 (Afterword D)
Version control software allows you to take snapshots of a project whenever it’s in a working state. When you make changes to a project—for example, when you implement a new feature—you have the option of reverting back to a previous working state if the project’s current state isn’t functioning well. 
Using version control software gives you the freedom to work on improvements and make mistakes without worrying about ruining your project. This is especially critical in large projects, but can also be helpful in smaller projects, even when you’re working on programs contained in a single file.

The most popular source control tool is git nowadays. It is a distributed source control, which means multiple users/teams can work on the same repository (git’s term for folder/project) at the same time. It scales better than other tools.

**Agenda**
- [x] Introduction
- [x] Git
- [x] GitHub
- [x] git clone
- [x] git add
- [x] git commit
- [x] git status
- [x] git push
- [x] git pull
- [x] Merge Conflicts 
- [x] git log
- [x] Making Changes
- [ ] Branching


### Git: core commands
Adds files to a commit basket, in git it is called “staging”
    
    git add <file>

Commits staged changes
    
    git commit –m “message”

Pushes commits to the origin
    
    git push

### Git: first time in the project

We will start by preparing the project for git. First, we need to determine the root directory of the project. Then we will open terminal in that folder, and:
	
	git init
	
We just initialized the git for the project. It is called a git repository now. Next, we need to define which files will be stored in the repository:
	
	git add <file_path> (we do not need to manually add all the files in the directory, we can use . to add all of them (git add .), note the dot (.) after the git add command)
	
Now let’s make a first commit
	
	git commit –m “initial commit or some comment you prefer”
	
Yay, we have a commit! We can check the history:
	
	git log (you can quit git log by typing q)


### Git: remote server pushes

In the previous slide we created a git repository and we committed our first changes. To push them to a remote server, we need to connect our local repository to that remote server:
	
	git remote add origin https://our_preferred_server/repository.git
	
We can check if our remote is set:
	
	git remote –v
	
Now we can push our changes:
	
	git push

For more download the [git cheatsheet](https://github.github.com/training-kit/downloads/github-git-cheat-sheet.pdf).

Find [GitHub Desktop guide](https://help.github.com/en/desktop/getting-started-with-github-desktop/creating-your-first-repository-using-github-desktop) here.

##  Git Branch
Branching is a feature available in most modern version control systems. Git branches are effectively a pointer to a snapshot of your changes. When you want to add a new feature or fix a bug—no matter how big or how small—you spawn a new branch to encapsulate your changes. This makes it harder for unstable code to get merged into the main code base, and it gives you the chance to clean up your future's history before merging it into the main branch.

![git_branches](pictures/git-branches-merge.png)

**How it works**

A branch represents an independent line of development. Branches serve as an abstraction for the edit/stage/commit process. You can think of them as a way to request a brand new working directory, staging area, and project history. New commits are recorded in the history for the current branch, which results in a fork in the history of the project.

The git branch command lets you create, list, rename, and delete branches. It doesn’t let you switch between branches or put a forked history back together again. For this reason, git branch is tightly integrated with the git checkout and git merge commands.

### Common Options

    git branch
List all of the branches in your repository. This is synonymous with git branch --list.

    git branch <branch>
Create a new branch called <branch>. This does not check out the new branch.

    git branch -d <branch>
Delete the specified branch. This is a “safe” operation in that Git prevents you from deleting the branch if it has unmerged changes.

    git branch -D <branch>
Force delete the specified branch, even if it has unmerged changes. This is the command to use if you want to permanently throw away all of the commits associated with a particular line of development.

    git branch -m <branch>
Rename the current branch to <branch>.

    git branch -a
List all remote branches. 

**Checking out branches**

The git checkout command lets you navigate between the branches created by git branch. Checking out a branch updates the files in the working directory to match the version stored in that branch, and it tells Git to record all new commits on that branch. Think of it as a way to select which line of development you’re working on.

Having a dedicated branch for each new feature is a dramatic shift from a traditional SVN workflow. It makes it ridiculously easy to try new experiments without the fear of destroying existing functionality, and it makes it possible to work on many unrelated features at the same time. In addition, branches also facilitate several collaborative workflows.

The git checkout command may occasionally be confused with git clone. The difference between the two commands is that clone works to fetch code from a remote repository, alternatively checkout works to switch between versions of code already on the local system.

    git checkout -b <new-branch>
The above example simultaneously creates and checks out <new-branch>. The -b option is a convenience flag that tells Git to run git branch <new-branch> before running git checkout <new-branch>

Switching branches is a straightforward operation. Executing the following will point HEAD to the tip of <branchname>.

    git checkout <branchname>

Assuming the repo you're working in contains pre-existing branches, you can switch between these branches using git checkout. To find out what branches are available and what the current branch name is, execute git branch.

    $> git branch
    master
    another_branch
    feature_inprogress_branch
    $> git checkout feature_inprogress_branch

## Steps to clone the project 
1. Copy the url of the repository ending with .git (https://github.com/2020spring/gitproject.git)

2. [optional] GitHub Desktop: 
    * Go to Current Repository
    * click on Add drop down
    * Clone Repository
    * click on URL tab
    * paste the copied URL (https://github.com/2020spring/gitproject.git)
    * choose the location from your local machine `C:\dev\` then click on Clone.

    Git Bash: navigate to the right directory `C:\dev\` and enter following:
      ```bash
      git clone https://github.com/2020spring/gitproject.git
      ```
3. [optional] Create your feature branch: 
      ```bash
      git checkout -b gitproject_john
      ```
4. Open the `C:\dev\gitproject` folder from your PyCharm and start modifying the code.

## How to set up git project in PyCharm

You can find the full instruction and video [here](https://www.jetbrains.com/help/pycharm/set-up-a-git-repository.html#add-remote)

## References

* [GitHub Guides](https://guides.github.com/activities/hello-world/)
* [CS50 - Git and GitHub (video)](https://youtu.be/eulnSXkhE7I)
* [git cheatsheet](https://github.github.com/training-kit/downloads/github-git-cheat-sheet.pdf)



# Week 5
Python Functions, Modules, Packages, Classes

## Chapter 8. Functions
In this chapter you’ll learn to write functions, which are named blocks of code that are designed to do one specific job. When you want to perform a particular task that you’ve defined in a function, you call the name of the function responsible for it. If you need to perform that task multiple times throughout your program, you don’t need to type all the code for the same task again and again; you just call the function dedicated to handling that task, and the call tells Python to run the code inside the function. You’ll find that using functions makes your programs easier to write, read, test, and fix.

### Defining a Function
Here’s a simple function named greet_user() that prints a greeting:
 ```python
def greet_user():
    """Display a simple greeting."""
    print("Hello!")

greet_user()
```

### Passing Information to a Function
The function now expects you to provide a value for username each time you call it. When you call greet_user(), you can pass it a name, such as 'jesse', inside the parentheses:

```python
def greet_user(username):
    """Display a simple greeting."""
    print(f"Hello, {username.title()}!")

greet_user('jesse')
```


### Positional Arguments
When you call a function, Python must match each argument in the function call with a parameter in the function definition. The simplest way to do this is based on the order of the arguments provided. Values matched up this way are called positional arguments.

```python
def describe_pet(animal_type, pet_name):
    """Display information about a pet."""
    print("\nI have a " + animal_type + ".")
    print("My " + animal_type + "'s name is " + pet_name.title() + ".")

describe_pet('hamster', 'harry')
# I have a hamster.
# My hamster's name is Harry.
```

### Multiple Function Calls
You can call a function as many times as needed. Describing a second, different pet requires just one more call to describe_pet():
```python
def describe_pet(animal_type, pet_name):
    """Display information about a pet."""
    print("\nI have a " + animal_type + ".")
    print("My " + animal_type + "'s name is " + pet_name.title() + ".")

describe_pet('hamster', 'harry') # order matter in Positional Arguments
describe_pet('dog', 'willie')
```
### Keyword Arguments
A keyword argument is a name-value pair that you pass to a function. You directly associate the name and the value within the argument, so when you pass the argument to the function, there’s no confusion (you won’t end up with a harry named Hamster). Keyword arguments free you from having to worry about correctly ordering your arguments in the function call, and they clarify the role of each value in the function call. Let’s rewrite pets.py using keyword arguments to call describe_pet(): 
```python
def describe_pet(animal_type, pet_name):
    """Display information about a pet."""
    print("\nI have a " + animal_type + ".")
    print("My " + animal_type + "'s name is " + pet_name.title() + ".")

describe_pet(animal_type='hamster', pet_name='harry')
```
### Default Values
When writing a function, you can define a default value for each parameter. If an argument for a parameter is provided in the function call, Python uses the argument value. If not, it uses the parameter’s default value.

For example, if you notice that most of the calls to describe_pet() are being used to describe dogs, you can set the default value of animal_type to 'dog'. Now anyone calling describe_pet() for a dog can omit that information: 
```python
def describe_pet(pet_name, animal_type='dog'):
    """Display information about a pet."""
    print("\nI have a " + animal_type + ".")
    print("My " + animal_type + "'s name is " + pet_name.title() + ".")

describe_pet(pet_name='willie')

# I have a dog.
# My dog's name is Willie.
```
### Equivalent Function Calls
Because positional arguments, keyword arguments, and default values can
all be used together, often you’ll have several equivalent ways to call a function.

All of the following calls would work for this function:
```python
# A dog named Willie.
describe_pet('willie')
describe_pet(pet_name='willie')
# A hamster named Harry.
describe_pet('harry', 'hamster')
describe_pet(pet_name='harry', animal_type='hamster')
describe_pet(animal_type='hamster', pet_name='harry')
```
Each of these function calls would have the same output as the previous examples. 

*Note: It doesn’t really matter which calling style you use. As long as your function calls produce the output you want, just use the style you find easiest to understand.*

## Avoiding Argument Errors
When you start to use functions, don’t be surprised if you encounter errors about unmatched arguments. Unmatched arguments occur when you provide fewer or more arguments than a function needs to do its work.


### Return Values
A function doesn’t always have to display its output directly. Instead, it can process some data and then return a value or set of values. The value the function returns is called a return value. The return statement takes a value from inside a function and sends it back to the line that called the function. Return values allow you to move much of your program’s grunt work into functions, which can simplify the body of your program. 

### Returning a Simple Value
Let’s look at a function that takes a first and last name, and returns a neatly formatted full name:
```python
# formatted_name.py
def get_formatted_name(first_name, last_name):      # 1.
    """Return a full name, neatly formatted."""
    full_name = first_name + ' ' + last_name        # 2.
    return full_name.title()                        # 3.

musician = get_formatted_name('jimi', 'hendrix')    # 4.
print(musician)


```
The definition of get_formatted_name() takes as parameters a first and last name (1.) The function combines these two names, adds a space between them, and stores the result in full_name (2.) The value of full_name is converted to title case, and then returned to the calling line at (3.) w.When you call a function that returns a value, you need to provide a variable where the return value can be stored. In this case, the returned value is stored in the variable musician at (4.) The output shows a neatly formatted name made up of the parts of a person’s name:

    Jimi Hendrix


The **break** statement offers a straightforward way to exit the loop


```python
def find_num(num_list, number):
    for num in num_list:
        if num == number:
            print(f"{number} is found!!")
            break   # exits the loop as soon as first match to 'number' is found from 'num_list'


nums = [5, 55, 76, 1, -9, 0, 1, 456]
find_num(nums, 1)
find_num([45, 0, 'hello'], 7)
```


### Passing an Arbitrary Number of Arguments
Sometimes you won’t know ahead of time how many arguments a function needs to accept. Fortunately, Python allows a function to collect an arbitrary number of arguments from the calling statement. For example, consider a function that builds a pizza. It needs to accept a number of toppings, but you can’t know ahead of time how many toppings a person will want. The function in the following example has one parameter, *toppings, but this parameter collects as many arguments as the calling line provides:

```python
# pizza.py 
def make_pizza(*toppings):
    """Summarize the pizza we are about to make."""
    print("\nMaking a pizza with the following toppings:")
    for topping in toppings:
        print("- " + topping)

make_pizza('pepperoni')
make_pizza('mushrooms', 'green peppers', 'extra cheese')
```
The asterisk in the parameter name *toppings tells Python to make an empty tuple called toppings and pack whatever values it receives into this tuple. The print statement in the function body produces output showing that Python can handle a function call with one value and a call with three values. It treats the different calls similarly. Note that Python packs the arguments into a tuple, even if the function receives only one value:
    
    Making a pizza with the following toppings:
    - pepperoni
    Making a pizza with the following toppings:
    - mushrooms
    - green peppers
    - extra cheese

### Importing an Entire Module
To start importing functions, we first need to create a module. A module is a file ending in .py that contains the code you want to import into your program. Let’s make a module that contains the function make_pizza(). To make this module, we’ll remove everything from the file pizza.py except the function make_pizza().

Now we’ll make a separate file called making_pizzas.py in the same directory as pizza.py. This file imports the module we just created and then makes two calls to make_pizza(): 
```python
# making_pizzas.py
import pizza

pizza.make_pizza(16, 'pepperoni')
pizza.make_pizza(12, 'mushrooms', 'green peppers', 'extra cheese')
```
This first approach to importing, in which you simply write import followed by the name of the module, makes every function from the module available in your program. If you use this kind of import statement to import an entire module named module_name.py, each function in the module is available through the following syntax:

    module_name.function_name()

#### Importing Specific Functions
You can also import a specific function from a module. Here’s the general syntax for this approach:
from module_name import function_name You can import as many functions as you want from a module by separating each function’s name with a comma:

    from module_name import function_0, function_1, function_2
T
he making_pizzas.py example would look like this if we want to import just the function we’re going to use:

    from pizza import make_pizza
    make_pizza(16, 'pepperoni')
    make_pizza(12, 'mushrooms', 'green peppers', 'extra cheese')

With this syntax, you don’t need to use the dot notation when you call a function. Because we’ve explicitly imported the function make_pizza() in the import statement, we can call it by name when we use the function.


## Classes (Chapter 9)

Object-oriented programming is one of the most effective approaches to writing software. In object-oriented programming you write classes that represent real-world things and situations, and you create objects based on these classes. When you write a class, you define the general behavior that a whole category of objects can have.

![objects](pictures/object.png)

When you create individual objects from the class, each object is automatically equipped with the general behavior; you can then give each object whatever unique traits you desire. You’ll be amazed how well real-world situations can be modeled with object-oriented programming. Making an object from a class is called instantiation, and you work with instances of a class. In this chapter you’ll write classes and create instances of those classes. You’ll specify the kind of information that can be stored in instances, and you’ll define actions that can be taken with these instances.

You’ll also write classes that extend the functionality of existing classes, so similar classes can share code efficiently. You’ll store your classes in modules and import classes written by other programmers into your own program files.

![classes-and-object-in-python](pictures/classes-and-object-in-python.jpg)

### Class
A class is a user-defined blueprint or prototype from which objects are created. Classes provide a means of bundling data and functionality together. Creating a new class creates a new type of object, allowing new instances of that type to be made. Each class instance can have attributes attached to it for maintaining its state. Class instances can also have methods (defined by its class) for modifying its state.

To understand the need for creating a class let’s consider an example, let’s say you wanted to track the number of dogs which may have different attributes like breed, age. If a list is used, the first element could be the dog’s breed while the second element could represent its age. Let’s suppose there are 100 different dogs, then how would you know which element is supposed to be which? What if you wanted to add other properties to these dogs? This lacks organization and it’s the exact need for classes.

Class creates a user-defined data structure, which holds its own data members and member functions, which can be accessed and used by creating an instance of that class. A class is like a blueprint for an object.

### Class Objects
An Object is an instance of a Class. A class is like a blueprint while an instance is a copy of the class with actual values. It’s not an idea anymore, it’s an actual dog, like a dog of breed pug who’s seven years old. You can have many dogs to create many different instances, but without the class as a guide, you would be lost, not knowing what information is required.

An object consists of :
* **State** : It is represented by attributes of an object. It also reflects the properties of an object.
* **Behavior** : It is represented by methods of an object. It also reflects the response of an object with other objects.
* **Identity** : It gives a unique name to an object and enables one object to interact with other objects.

**Declaring Objects (Also called instantiating a class)**

When an object of a class is created, the class is said to be instantiated. All the instances share the attributes and the behavior of the class. But the values of those attributes, i.e. the state are unique for each object. A single class may have any number of instances.

---
**Example with Dog class:**

![dog_class_objects](pictures/dog_class_object.png)
---
**Example with Cars class:**

![car_class_objects](pictures/car_class_objects.png)
---
**Example with Students class:**

![student_class_objects](pictures/students.png)

---







## Steps to clone the project 
1. Copy the url of the repository (https://github.com/2020spring/week5.git)

Open Git Bash and navigate to the right directory `C:\dev\` and enter following:
```bash
cd /c/dev/
git clone https://github.com/2020spring/week5.git
```


## References

* [Python Documentation - Modules](https://docs.python.org/3/tutorial/modules.html)
* [Socratica - Pyton Functions](https://youtu.be/NE97ylAnrz4)
* [Socratica - Python Recursion](https://youtu.be/Qk0zUZW-U_M)
* [Socratica - Python Classes and Objects](https://youtu.be/apACNr7DC_s)
* [Python Crash Course](http://bedford-computing.co.uk/learning/wp-content/uploads/2015/10/No.Starch.Python.Oct_.2015.ISBN_.1593276036.pdf)


