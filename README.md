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
![git_overview] (pictures/git-flow-header.jpeg)


# Week 4
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
