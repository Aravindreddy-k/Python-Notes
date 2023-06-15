List is a collection which is ordered and changeable. Allows duplicate members.lists are created by square brackets [].<br>

List items are ordered, changeable, and allow duplicate values.<br>

**Ordered**: the items have a defined order, and that order will not change. <br>
If you add new items to a list, the new items will be placed at the end of the list.<br>

**Changeable**: The items in the list can be changeable, add or remove items from the list. <br>

**Allow Duplicates**: lists are indexed, it allows duplicates. <br>

["2","ad","True","2"]<br>

List Items have all data types: int, string, boolean values.<br>
```
mylist=["1","3","t","True"]
print(type(mylist))
Output:<class 'list'>
```

To convert other Data type into List we can use **list()** constructor. <br>
```
Example
Using the list() constructor to make a List:
 a = list(("apple", "banana", "cherry")) 
print(a)
Output:['apple', 'banana', 'cherry']
```
We can use slicing to refer exact value by index numbers. <br>

**Change Item Value**<br>

```
Example
Change the second value
a=["b","d","w"]
a[1]="s"
print(a)
Output:["b","s","w"]
```

```
Example
a=["b","d","w","t"]
a[2:4]=["q","r"]
print(a)
Output:["b","d","q","r"]
```

```
Example
a=["b","d","w"]
a[1:3]=["x"]
print(a)
Output: ["b","x"]
```
**Note**: The length of the list will change when the number of items inserted does not match the number of items replaced. <br>

**Insert Items** <br>

**insert()** method inserts the item at specified index without replacing. <br>

```
Example
a=["b","d","w"]
a.insert(2,"m")
print(a)
Output:["b","d","m","w"]
```

**Python - Add List Items**<br>

**append()** method add items at the end of the list. <br>

```
Example
a=["b","d","w"]
a.append("x")
print(a)
Output: ["b","d","w","x"]
```

**Difference**: insert() add the items at specified index whereas append() will add the item at the end of the list. <br>

**extend()** method append elements from another list to the current list.<br>

```
Example
a=["b","d","w"]
b=["f","h"]
a.extend(b)
print(a)
Output: ["b","d","w","f","h"]
```
**Note**: extend() method appends any iterable objects like tuples,set,dict,list. <br>

```
Example
a=["t","e","u"]
b=("n","i","d","l")
a.extend(b)
print(a)
Output:["t","e","u","n","i","d","l"]
```

**Python - Remove List Items**<br>

**remove()** method removes specified item <br>

```
Example
a=["t","e","u"]
a.remove("t")
print(a)
Output:["e","u"]
```

**pop()** method removes specified index.<br>

```
Example
a=["t","e","u"]
a.pop(1)
print(a)
Output:["t","u"]
```

**Note**: if we not specified any index ,pop() method removes the last item.<br>

```
Example
a=["t","e","u"]
a.pop()
print(a)
Output:["t","e"]
```

**del** keyword removes the specified index.<br>

```
Example
a=["t","e","u"]
del a[2]
print(a)
Output:["t","e"]
```

**Note**: if we not specified any index, del keyword delete the list completely. <br>

```
Example
a=["t","e","u"]
del a
print(a)
Output:this will cause an error because you have succsesfully deleted "a"
```

**clear()** method clears the list completely, it shows list without items. <br>

```
Example
a=["t","e","u"]
a.clear()
print(a)
Output: [ ]
```

**Python - Loop Lists** <br>

```
Example
a=["one","two","three"]
for x in a:
  print(a)
Output: one
        two
        three

```
We can also loop through the list items by referring to their index number using **len()** and **range()**. <br>

```
Example
a=["one","two","three"]
for i in range(len(a)):
print(a[i])
Output: one
        two
        three

```

```
Example
a=["one","two","three"]
i=0
while i<len(a):
  print(a[i])
   i=i+1
Output: one
        two
        three

```

**List Comprehension** <br>

```
The syntax
newlist=[expression for item in iterable if condition==True]

```

```
Example
fruits with the letter "a" in the name
fruits = ["apple", "banana", "cherry", "kiwi", "mango"]
newlist=[x for x in fruits if "a" in x]
print(newlist)
Output: ["apple", "banana", "mango"]
```


```
Example
fruits that are not apple
fruits = ["apple", "banana", "cherry", "kiwi", "mango"]
newlist=[x for x in fruits if x!= "apple"]
print(newlist)
Output: ["banana","cherry", "kiwi", "mango"]
```

```
Example
a=[x for x in range(10)]
print(a)
Output:[0, 1, 2, 3, 4, 5, 6, 7, 8, 9]
```

```
Example
a=[x for x in range(10) if x<5]
print(a)
Output:[0, 1, 2, 3, 4]
```

```
Example
a=["one","two","three"]
newlist=[a.upper() for x in a]
print(newlist)
Output:["ONE","TWO","THREE"]
```

**Note**: You can use same for lower or swapcase also. <br>

```
Example
Set all values in the new list to "hi"
a=["one","two","three"]
newlist=["hi" for x in a]
print(newlist)
Output:["hi","hi","hi"]

```

```
Example
Return "orange" instead of "banana":
fruits = ["apple", "banana", "cherry", "kiwi", "mango"]
newlist=[x for x in fruits if x!="banana" else "orange"]
print(newlist)
Output:["apple", "orange", "cherry", "kiwi", "mango"]
```

**Python-Sort list**<br>

**sort()** method sorts alphanumeric in ascending order.<br>

```
Example
fruits = ["orange", "mango", "kiwi", "pineapple", "banana"]
fruits.sort()
print(fruits)
Output:[ "banana","kiwi", "mango","orange","pineapple"]
```

```
Example
a=[14,53,2,37,93,78,46]
a.sort()
print(a)
Output:[2,14,37,46,53,78,93]
```

**To get the list items in descending order use reverse=True**<br>


```
Example
fruits = ["orange", "mango", "kiwi", "pineapple", "banana"]
fruits.sort(reverse=True)
print(fruits)
Output:[ "pineapple","orange","mango","kiwi","banana"]
```

```
Example
a=[14,53,2,37,93,78,46]
a.sort(reverse=True)
print(a)
Output:[93,78,53,46,37,14,2]
```

**Note**: By default sort() is a case-sensitive. <br>

```
Example
t = ["banana", "Orange", "Kiwi", "cherry"]
t.sort()
print(t)
Output:['Kiwi', 'Orange', 'banana', 'cherry']
```

**key=str.lower** make a case-insensitive sort function. <br>


```
Example
t = ["banana", "Orange", "Kiwi", "cherry"]
t.sort(key=str.lower)
print(t)
Output:['banana', 'cherry', 'Kiwi', 'Orange']

```

**reverse()** method reverses the current sorting order of the elements. <br>

```
Example
t = ["banana", "Orange", "Kiwi", "cherry"]
t.reverse()
print(t)
Output:['cherry', 'Kiwi', 'Orange', 'banana']

```

**Copy List** <br>

```
Example
t = ["banana", "Orange", "Kiwi", "cherry"]
a=t.copy()
print(a)
Output: ["banana", "Orange", "Kiwi", "cherry"]
```

```
Example
can copy list using list() method
t = ["banana", "Orange", "Kiwi", "cherry"]
a=list(t)
print(a)
Output: ["banana", "Orange", "Kiwi", "cherry"]
```

**Joining List**

```
Example
using + operator
a=["f","s","i"]
b=[2,5,1]
c=a+b
print(c)
Output:["f","s","i",2,5,1]
```

```
Example
using append() method
a=["f","s","i"]
b=[2,5,1]
for x in b:
  a.append(b)
 print(a)
Output:["f","s","i",2,5,1]
```


```
Example
using extend() method
a=["f","s","i"]
b=[2,5,1]
a.extend(b)
print(a)
Output:["f","s","i",2,5,1]
```















       












