# Programming Basics questions

## Computer science

### Data structures

#### What is the purpose of a list (array in some programming languages) data structure? Name some methods of it!
Main purpose of lists/arrays is to store other data types and work with them based on index.

Methods:
```
.append()
.insert()
.remove()
.sort()
.reverse()
.pop()
.count()
```
#### What is the difference between a list/array and a set?
Any data in a set is unique, compared to lists which are in sequence. Also in lists you can have same data for x number of times.
#### What is the purpose and methods of a dictionary/map data structure?
When you create a dictionary you use a key and value. You can access the value of that key by calling dictionary with key as index.
As a developer you use methods to acceess or modify keys, values or entire dictionary because this data type is a mutable one.

### Algorithms

#### Fibonacci sequences. Write a method (or pseudo code), that generates the Fibonacci sequences.
```python
def fibonnacci_seq(ntimes):
    number1, number2 = 0, 1
    for counter in range(ntimes):
        print(number1)
        result = number1 + number2
        number1 = number2
        number2 = result

fibonnacci_seq(25)
```
#### How do you find a max value in a list/array if you can’t use any built-in functions?
You need to assign first value of the list in a variable<br>
Itterate through the entire list and test if first element in the list is lower than each element<br>
If the expression is true then assign the value from list to the same variable<br>
After the loop is over print or return the variable<br>

```python
def find_max(data_list):
    FIRST_ELEMENT = 0
    max = data_list[FIRST_ELEMENT]
    for index in range(len(data_list)):
        if max < data_list[index]:
            max = data_list[index]
    return max

print(find_max([34,12,2,31223,5,21,23]))

```
#### How do you find the average of values in a list/array if you can’t use any built-in functions?
You need to declare 2 variables that will store the sum of elements and a variable that will count how many iteration the loop will execute.<br>
In that loop add each element from list based on index.<br>
Devide the sum of elements in list with the amount of iterations.<br>

```python
def find_average(data_list):
    sum, count = 0, 0
    for index in data_list:
        count += 1
        sum += index
    return sum / count

print(find_average([5,5,5,10]))
```
#### What do we call an *in-place* sort?
In place sort uses the minimum amount of computer resources to sort the values. <br>
When we use in place sort we modify the elements directly in list without assigning the values to another variable.<br>
#### Explain an algorithm which sorts a list!
We will use two loops to go throught the elements in the list.<br>
Compare first two elements of the list if first one is larger we swap if not we leave them as they are.<br>
Then we take the next pair compare them untill we arrive at the end of the list.<br>
To compare all elements in the list we need to use a variable that we assign a boolean value True so we can restart the loop.<br>
Now we compare the elements again, the difference is that the list is changed and elements in the list have different positions. This happens because we looped through all elements and swapped them.<br>
We itterate and swap elements untill the entire list is sorted. <br>

```python
def sort_method(data_list):
    swapped = True
    while swapped:
        swapped = False
        for index in range(len(data_list) - 1):
            if data_list[index] > data_list[index + 1]:
                data_list[index], data_list[index + 1] = data_list[index + 1], data_list[index]
                swapped = True
    return data_list

print(sort_method([223,4,1,2,3,212331,2351,1]))

```

### Programming paradigms - procedural

#### What is the call stack?

#### What is “Stack overflow”?
Is the biggest community for developers where you can find answers and questions of problems that other developers encountered.
#### What are the main parts of a function?
Python keyword `def` function_name, in some cases arguments and function body.
### Programming languages - Python  
#### How do you use a dictionary in Python?

we create a dictionary using {key:value}

```python
test_dict = {
    'first_key': 1,
    'second_key': 2
}
```
If we want to access a value o modify it from a specific key we will call the key as an index.<br>

```python
test_dict['first_key']
# change value
test_dict['first_key] = 4
```
#### What does it mean that an object is immutable in Python?

We can't change the value from the immutable object. For example built-in objects such as int, float, str, tuple are immutable.

#### What is conditional expression in Python?
A conditional expression returns a value a or b depending if expression is True or False.

#### What are different types of arguments in Python?
1. Default argument when you assgign a value of the argument inside the function

```python
def test_f(name='Jake'):
    print(name)

test_f()
```
2. Keyword argument when use different arguments for function

```python
def test_f(first_argument,second_argument_third_argument):
    print(f'{first_argument}, {second_argument}, {third_argument}')

test_f(1,2,3)
```

3. Multiple arguments using *

```python
def test_f(*args):
    return sum(args) / len(args)

print(test_f(1,2,3,5,12,121))
```
#### What is variable shadowing? (context: variable scope)

Variable shadowing takes place when a local variable has the same name as a global variable.

#### What can happen if you try to delete/drop/add an item from a List, while you are iterating over it in Python?

We will get and error 'index out of range'.

#### What is the "golden rule" of variable scoping in Python (context: LEGB)? What is the lifetime of variables?
#### If you need to access the iterator variable after a for loop, how would you do it in Python?
You simply call the iterator variable because the variable value is the last element in iterable data type.
#### What type of elements can a list contain in Python?
You can store any type of data in list because lists accepts any object.

#### What is slice operator in Python and how to use?

Slice operator is used to modify the data type based on index<br>
Slice format is `data_type[start:stop:step]`<br>
We can use negatives indexes with slice operator data[-1]

```python
name = 'Jake'
print(name[1:-1])
```

#### What arithmetic operators (+,*,-,/) can be used on lists in Python? What do they do?

We can use 2 arithmetic operators with lists. <br>
First operator is `+` that concatenates 2 different lists<br>
Second operator is `*` that creates a copy of the list x number of times and the result of this operation is a list with elements of that x times <br>

#### What is the purpose of the in and not in membership operators in Python?

We can use `in` or `not in` to return a boolean value if value is found in that data type.<br>
Also `in` is used in for loop to get each element from itterable type.<br>

#### What does the + operator mean when used with strings in Python?

Concatenates them.

#### Explain f strings in Python?

Introduced in Python 3 is used to print formated strings. Using f before string (`f''`) you can access a variable or function inside the formated string with {}.

#### Name 4 iterable types in Python!

Strings, lists, tuples, dictionaries.

#### What is the difference between list/set/dictionary comprehension and a generator expression in Python?
The difference between comprehension and generator expression is that comprehension returns a list and itterates over each element storing list in memory, compared to generator that yiels one item at a time.

#### Does the order of the function definitions matter in Python? Why?
It doesn't matter in what order do you declare a function, what matters is when you call it. Mainly because the functions are already declared
#### What does unpacking mean in Python?

We can assign different values from an itterable type to variables<br>

```python
list1 = [2,3,4,5]

var1, var2, var3, var4 = list1
```

#### What happens when you try to assign the result of a function which has no return statement to a variable in Python?

That variable has value `None`.

## Software engineering

### Debugging

#### What techniques can you use while debugging a program in Python?

Using `print()` function to see if the code executes as intended.<br>
Use the built in debugger in IDE.

#### What does step over, step into and step out mean while using the debugger?
For us to use a debugger we need to put breakpoints in code.
Using step over debugger will take each line and when the line is a function it wll jump over it and display results.<br>
Step in takes each line in sequence.<br>
Step out takes only the lines where we used breakpoints.

#### How can you start to debug a program from a certain line using the debugger?

We use a breakpoint on that line by clicking on the left of the code. If there is a red dot on that line that means we put a breakpoint there.

### Version control

#### What are the advantages of using a version control system?

There are several advantages of using verson control:
1. Environment for team collaboraton
2. Store version of code on server
3. Restore part of the code if something went wrong

#### What is the difference between the working directory, the staging area and the repository in git?

The working directory is local on pc, when we use git add <file> this file will be in staging area. If we commit and push the changes, the file will be found on github repository.

#### What are remote repositories in git?

Remote repositories are places where code is stored on Github.

#### Why does a merge conflict occur?

A merge conflict happens when two branches modify the same place in file and are merged.

#### Through what series of commands could you put a new file into a remote repository connected to your existing local repository?

```git
git add. <file_name>
git commit -m "Message"
git push origin master
```

#### What does it mean atomic commits and descriptive commit messages?

An atomic commit represents a small change, fix or feature on code that doesn't break the program. The commit must represent a descriptive message on changes made and a description in detail.

#### What’s the difference between git and GitHub?

Git is a VCS helping developers manage project files <br>
Github is a web based version and hosting service for Git.

## Software design

### Clean code

#### What does clean code mean?

Is a guideline that every developer should follow, basically clean code is easy to understand and change. 

#### What steps do we usually do during a clean code refactoring?

1. Read the entire code.
2. Make a summary of the purpose of the code in one sentence.
3. Run code to see what is the result.
4. Refactor it:

    1. Remove code that doesn't add value
        - delete long comments
        - format the code
    2. Remove / change complex names
        - long methods
        - bad variables names
        - inproper variable scope
    3. Remove duplicate code
        - make functions with code



### Error handling

#### What is exception handling?

Exception handling is the process to respond to exceptions. A common exception handling is when getting input from user.

#### What are the basics of exception handling in Python?

```python
try:
    <code we want to run>
except:
    <code we want to run if the code inside try failed>

```

#### In which case should we catch an exception? Why?

When getting input from user, he can enter wrong data type for example you ask for a number and he enters a string. Exception happens because is the wrong data type.<br>
When we work with data types such as lists and dictionaries. Code can access a key that doesn't exist or higher index than the lenght of list.


#### What can/should we do with an exception in the ‘except’ block?

Show user a message that an error has occured and the name of the exeception so it can be fixed later on by developers.

#### What does the else and finally statement do in a try-except block in Python?
Code inside `else` is executes if there is not exception found in `try`.<br>
Always run code inside `finnaly`

## Software Development Methodologies

#### What is the main goal of a retrospective meeting?
To have a clear understanding of the tasks that the team planed and worked and what can be improved on later planning sessions.
## Programming environment

### Unix

#### What is UNIX and what is Linux?
Linux is an open source basd on UNIX operating system that supports different system softwares and libraries.
#### What do we call the shell in Linux?
bash
#### What does root means in a Linux environment?
Root represents the user with the highest admin privileges on linux system.
#### How do you access your personal files in Linux?
Personal files can be found in /home. A shortcut for accessing /home is using `cd ~`
#### How can you install an application in Linux?
Using `sudo apt-get install` 
#### What is package management in Linux, what are repositories?

#### How do you navigate in the filesystem with the command line?
Linux provides a comamnd cd - change directory. We will use cd in terminal to access folders in filesystem.
#### What does the following commands do: mkdir, rm, cat, cp, touch?
`mkdir 'name of the folder'` - creates a directory with 'name of the folder` name

`rm file.txt` - removes file

`cat file.txt` - displays contents of text files

`cp` - copies file to another location

`touch <file_name>` - creates a file 
#### How can you look up what does a command do in Linux if you have no internet connection?
command --help
#### What does the following commands do: head, tail, more, less?
`head` - shows first 10 lines in file

`tail` - shows last 10 lines in file

`less` - read content of file one screen per time

`more` - same command but not with so many options as `less`
#### How do you download a file from internet using the terminal?
We can use `wget link_to_file` 
