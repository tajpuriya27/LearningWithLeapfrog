
# Day18- Python Class & OOPS

#### Can I use OOP with Python?
Yes, Python supports object-oriented programming (OOP). OOP is a development model which lets a programmer focus on producing reusable code. It is different from the procedural model which follows a sequential approach.

OOP is useful when you have a large and complicated project to work. There will be multiple programmers creating reusable code, sharing and integrating their source code. Reusability results in better readability and reduces maintenance in the longer term.
<br>
<br>

#### **What is a Python class?**
A class is an arrangement of variables and functions into a single logical entity. It works as a template for creating objects. Every object can use class variables and functions as its members.

The object is a working instance of a class created at runtime.   
<br>
<br>

#### **How to create a class in Python?**
There are some terms which you need to know while working with classes in Python.

1. The “class” keyword
2. The instance attributes
3. The class attributes
4. The “self” keyword
5. The “__init_” method

Let’s now have a clear understanding of each of the above points one by one.

The “class” keyword
With the class keyword, we can create a Python class as shown in the example below.

```python
class BookStore:
    pass
```

#### **What is "self" keyword?**
Python provides the “self” keyword to represent the instance of a class. It works as a handle for accessing the class members such as attributes from the class methods.

Also, please note that it is implicitly the first argument to the __init__ method in every Python class. You can read about it below.

<br>   

#### **What is __init__ (constructor) in Python?**
The “__init__()” is a unique method associated with every Python class.

Python calls it automatically for every object created from the class. Its purpose is to initialize the class attributes with user-supplied values.

It is commonly known as Constructor in object-oriented programming. See the below example.

```python
class BookStore:
    def __init__(self):
        print("__init__() constructor gets called...")
        
B1 = BookStore()
```
Output
```
__init__() constructor gets called...
```

**The instance attributes**   
These are object-specific attributes defined as parameters to the __init__ method. Each object can have different values for themselves.

In the below example, the “attrib1” and “attrib2” are the instance attributes.

```python
class BookStore:
    def __init__(self, attrib1, attrib2):
        self.attrib1 = attrib1
        self.attrib2 = attrib2
```
The class attributes
Unlike the instance attributes which are visible at object-level, the class attributes remain the same for all objects.

Check out the below example to demonstrate the usage of class-level attributes.

```python
class BookStore:
    instances = 0
    def __init__(self, attrib1, attrib2):
        self.attrib1 = attrib1
        self.attrib2 = attrib2
        BookStore.instances += 1

b1 = BookStore("", "")
b2 = BookStore("", "")

print("BookStore.instances:", BookStore.instances)
```

In this example, the “instances” is a class-level attribute. You can access it using the class name. It holds the total no. of instances created.

We’ve created two instances of the class <Bookstore>. Hence, executing the example should print “2” as the output.

#### output
```
BookStore.instances: 2
```

Python class demo
Given here is an example where we are building a BookStore class and instantiating its object with different values.

Create a BookStore class in Python
```python
class BookStore:
    noOfBooks = 0
 
    def __init__(self, title, author):
        self.title = title
        self.author = author
        BookStore.noOfBooks += 1
 
    def bookInfo(self):
        print("Book title:", self.title)
        print("Book author:", self.author,"\n")
 
# Create a virtual book store
b1 = BookStore("Great Expectations", "Charles Dickens")
b2 = BookStore("War and Peace", "Leo Tolstoy")
b3 = BookStore("Middlemarch", "George Eliot")
 
# call member functions for each object
b1.bookInfo()
b2.bookInfo()
b3.bookInfo()

print("BookStore.noOfBooks:", BookStore.noOfBooks)
```

You can open IDLE or any other Python IDE, save the above code in some file, and execute the program.

In this example, we have created three objects of the BookStore class, i.e., b1, b2, and b3. Each of the objects is an instance of the BookStore class.

```
# output
Book title: Great Expectations
Book author: Charles Dickens 

Book title: War and Peace
Book author: Leo Tolstoy 

Book title: Middlemarch
Book author: George Eliot 

BookStore.noOfBooks: 3
```