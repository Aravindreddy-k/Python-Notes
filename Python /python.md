**python is a popular programming language.**<br>

**Indentation refers to the spaces at the beginning of a code line.The indentation in Python is very important.**<br>
 ```
 Example
 if 5 > 2:
     print("Five is greater than two!")
     
 Output: Five is greater than two!
  ```
  
   ```
   Example
   Syntax Error:
 if 5 > 2:
 print("Five is greater than two!")
     
 Output:IndentationError: expected an indented block
  ```
We want  to use the same number of spaces in the same block of code, otherwise Python will give you an error:  
   ```
   Example
   Syntax Error:
 if 5 > 2:
 print("Five is greater than two!")
     print("Five is greater than two!")
   
     
 Output:IndentationError: unexpected indent
  ```
**Creating a comment**<br>

Comments starts with a #, and Python will ignore them:<br>

for a multiline code u can use tripline quotes for comment (""" or''')
```
Example
"""
This is a comment
written in
more than just one line
"""
print("Hello, World!")
```
**Variable Name**<br>
A variable name must start with a letter or the underscore character<br>
A variable name cannot start with a number<br>
A variable name can only contain alpha-numeric characters and underscores (A-z, 0-9, and _ )<br>
Variable names are case-sensitive (age, Age and AGE are three different variables)<br>
A variable name cannot be any of the Python keywords.<br>

**Multi words Variable Name**<br>

**Camel Case**<br>
Each word, except the first, starts with a capital letter:<br>
```
myVariableName = "John"
```

**Pascal Case**<br>
Each word starts with a capital letter:<br>
```
MyVariableName = "John"
```

**Pascal Case**<br>
Each word is separated by an underscore character::<br>
```
my_variable_name = "John"
```
**Global Variables**<br>
Global variables are created outside the function, can be used by everyone, both inside of functions and outside.<br>

```
Example
Create a variable outside of a function, and use it inside the function

x = "awesome"

def myfunc():
  print("Python is " + x)

myfunc()
output:Python is awesome
```

```
Example
Create a variable inside a function, with the same name as the global variable
x = "awesome"

def myfunc():
x="fantastic"
  print("Python is " + x)

myfunc()
print("Python is " + x)
output:Python is fantastic
       Python is awesome
```
**The Global Keyword**

```
Example
If you use the global keyword, the variable belongs to the global scope:

def myfunc():
  global x
  x = "fantastic"

myfunc()

print("Python is " + x)
Output: Python is fantastic
```

```
Example
To change the value of a global variable inside a function, refer to the variable by using the global keyword:

x = "awesome"

def myfunc():
  global x
  x = "fantastic"

myfunc()

print("Python is " + x)
Output: Python is fantastic
```
**Python Data Types**<br>
Text Type:	str<br>
Numeric Types:	int, float, complex<br>
Sequence Types:	list, tuple, range<br>
Mapping Type:	dict<br>
Set Types:	set, frozenset<br>
Boolean Type:	bool<br>

**Float can also be scientific numbers with an "e" to indicate the power of 10.**<br>

**Complex numbers are written with a "j" as the imaginary part.**<br>

You can get the data type of any object by using the **type()** function:<br>

Python does not have a random() function to make a random number, but Python has a built-in module called random that can be used to make random numbers:<br>
```
Example
import random

print(random.randrange(1, 10))
output: Gets the Random value between (1,10)
```

  
