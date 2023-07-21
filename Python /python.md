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

**Snake Case**<br>
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
**String**<br>
"Aravind" same as 'Aravind' <br>
for multi line string u can use("""/''')

```
a=""" cnslmlmsmhwjcwcw
wvvvedvevevevv
vcevevevvwfvwv
wf3wfghhhngff"""
print(a)
```
To get the length of a string, use the **len()** function (the length includes every space). <br>
```
Example
b="Aravind, Reddy!"
print(len(b))
Output:15
```

**Python - Slicing Strings**
It  can return a range of characters.Specify the start index and the end index, separated by a colon, to return a part of the string.<br>
**Note**: end index is not included<br>

```
Example
b="Aravind, Reddy!"
print(b[2:5])
Output:avi
```
**Note**: The first character starts with index 0

```
Example
b="Aravind, Reddy!"
print(b[:5])
Output:Aravi
```

```
Example
b="Aravind, Reddy!"
print(b[4:])
Output:nd, Reddy!
```
**Negative Indexing**<br>

starts from the end with index -1 <br>

```
Example
b="Aravind, Reddy!"
print(b[-5:-2])
Output:edd
```

**Python - Modify Strings**
```
Example
The upper() method returns the string in upper case:

a = "Hello, World!"
print(a.upper())
Output:HELLO, WORLD!
```

```
Example
The lower() method returns the string in lower case:

a = "Hello, World!"
print(a.lower())
Output:hello, world!
```

```
Example
The strip() method removes any whitespace from the beginning or the end:

a = " Hello, World! "
print(a.strip())
Output:Hello, World!
```

```
Example
The replace() method replaces a string with another string:

a = " Hello, World! "
print(a.replace("H","C"))
Output:Cello, World!
```

```
Example
The split() method splits the string into substrings if it finds instances of the separator:

a = " Hello, World! "
print(a.split(","))
Output:['Hello','World!']
```

```
Example
The swapcase() Swaps cases, lower case becomes upper case and vice versa.

a = " Hello, World! "
print(a.swapcase())
Output:hELLO, wORLD!
```


**String Concatenation**<br>

To concatenate, or combine, two strings you can use the + operator.<br>
```
Example
a = "Hello"
b = "World"
c = a + b
print(c)
Output:HelloWorld
```

```
Example
To add a space between them, add a " ":

a = "Hello"
b = "World"
c = a + " " + b
print(c)
Output:Hello World
```

**String Format** <br>

**format()** method used to combine string and numbers. <br>

```
Example
age=22
txt="My name is Aravind, I am {}"
print(txt.format(age))

Output: My name is Aravind, I am 22
```

```
Example
quantity = 3
itemno = 567
price = 49.95
myorder = "I want {} pieces of item {} for {} dollars."
print(myorder.format(quantity, itemno, price))
Output: I want 3 pieces of item 567 for 49.95 dollars.
```

```
Example
can also use index number {0}
quantity = 3
itemno = 567
price = 49.95
myorder = "I want to pay {2} dollars for {0} pieces of item {1}."
print(myorder.format(quantity, itemno, price))
Output: I want to pay 49.95 dollars for 3 pieces of item 567.
```

**Escape Character**<br>
\" Double Quote <br>
\'	Single Quote	<br>
\\	Backslash	<br>
\n	New Line<br>

```
txt = "We are the so-called \"Vikings\" from the north."
Output: We are the so-called "Vikings" from the north.
```

**Boolean Values**<br>

**bool()** function gives you **True** or **False** in return. <br>

```
Example
will return True.
bool("sda") 
bool(125)
bool(2.8844)
The following will return False:

bool(False)
bool(None)
bool(0)
bool("")
bool(())
bool([])
bool({})
```

**isinstance()** can be used to determine if an object is of a certain data type. <br>

```
Example
x=20
print(isinstance(x,int))
Output: True
```

**Python Operators**<br>

5/2=2.5<br>
5%2=1(gives remainder) <br>
5**2=5*5 <br>
5//2=2 (rounds to nearest number)<br>

and & ,or | , not ! <br>

 






  
