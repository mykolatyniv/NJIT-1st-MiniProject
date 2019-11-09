# 2nd Mini Project Part <a name="top">

Return to Readme Page [Click Here](/README.md)

* [How Python uses Indentation to control Flow](#cd)
* [Don't Repeat Yourself](#2)
* [Design Patterns from Gang of Four](#cp)
* [Class](#pwd)
* [Object](#mv)
* [Static](#rm)
* [Property / Attribute](#history)
* [Method](#home)
* [Exception](#file)
* [Unit Test](#path)
* [Constructor](#arrow)
* [Factory](#vi)
* [Decorator](#Decorator)
* [Extend Class](#class)
* [CSV Files](#csv)
* [Reading Files](#reading)
___________________________________________________________________________________________________________________________________
</br>
<a name="cd">
  
## How Python uses Indentation to Control Flow 
Python uses indentation. A code block (body of a function, loop etc.) starts with indentation and ends with the first unindented line. The amount of indentation is up to you, but it must be consistent throughout that block. Generally four whitespaces are used for indentation and is preferred over tabs.

A code block (body of a function, loop etc.) starts with indentation and ends with the first unindented line. The amount of indentation is up to you, but it must be consistent throughout that block.

- Python uses whitespace (i.e. indentation) to delimit scope:
- Rulet: One or more whitespace characters (spaces or tabs) is sufficient to serve as indentation. A given indented block must use a uniform level of indentation.

### Example:
<pre>
for i in range(1,11):
    print(i)
    if i == 5:
        break
</pre>
In the above code, four whitespaces are used for indentation and is preferred over tabs.
</a>

<a href="#top">Return</a>
<br>
<br>
___________________________________________________________________________________________________________________________________
<a name="2"> 
  
## Don't Repeat Yourself (DRY)
- DRY principle is a software development practice aimed at reducing repetition of information. 
 It is a good idea to adhere to the DRY principle when writing computer code: don’t repeat yourself. If we cut and paste code to reuse it in various places, we may at some point realise our code contains an error and have to fix the error in all the places we pasted and used our code. Below, is an example of a function using DRY to replace a list of information.

### Example:
####  name = 'Mahdi'
####  people_i_like = ['Mahdi', 'John', 'Linda']
####  if name in people_i_like:
####  print 'yay!'

</a>

<a href="#top">Return</a>
<br>
<br>
___________________________________________________________________________________________________________________________________


<a name="cp"> 
  
## Design Patterns from Gang of Four

The Gang of Four are the four authors of the book, "Design Patterns: Elements of Reusable Object-Oriented Software". There are twenty-three design patterns described by the Gang of Four.

Design patterns provide solutions to common software design problems. In the case of object-oriented programming, design patterns are generally aimed at solving the problems of object generation and interaction, rather than the larger scale problems of overall software architecture. They give generalised solutions in the form of templates that may be applied to real-world problems.

The three pattern types are: 	Creational, Structural, Behavioral
Which are further broken down by their characteristics: (see the table below. 

|Creational|Structural|Behavioral|
|----------|----------|-----------|
|Abstract factory groups object factories that have a common theme.|Adapter allows classes with incompatible interfaces to work together by wrapping its own interface around that of an already existing class.|Chain of responsibility delegates commands to a chain of processing objects.|
|Builder constructs complex objects by separating construction and representation.|Bridge decouples an abstraction from its implementation so that the two can vary independently.|Command creates objects which encapsulate actions and parameters.|
|Factory method creates objects without specifying the exact class to create.|Composite composes zero-or-more similar objects so that they can be manipulated as one object.|Interpreter implements a specialized language.|
|Prototype creates objects by cloning an existing object.|Decorator dynamically adds/overrides behaviour in an existing method of an object.|Iterator accesses the elements of an object sequentially without exposing its underlying representation.|
|Singleton restricts object creation for a class to only one instance.|Facade provides a simplified interface to a large body of code.|Mediator allows loose coupling between classes by being the only class that has detailed knowledge of their methods.|
|..   |Flyweight reduces the cost of creating and manipulating a large number of similar objects.|Memento provides the ability to restore an object to its previous state (undo).|
|..|Proxy provides a placeholder for another object to control access, reduce cost, and reduce complexity.|Observer is a publish/subscribe pattern which allows a number of observer objects to see an event.|
|..  |..  |State allows an object to alter its behavior when its internal state changes.|
|..  |..  |Strategy allows one of a family of algorithms to be selected on-the-fly at runtime.|
|..  |..  |Template method defines the skeleton of an algorithm as an abstract class, allowing its subclasses to provide concrete behavior.|
|..  |..  |Visitor separates an algorithm from an object structure by moving the hierarchy of methods into one object.|
</a>

<a href="#top">Return</a>
<br>
<br>
___________________________________________________________________________________________________________________________________


<a name="pwd"> 
  
## Class 
- A class is a code template for creating objects. Objects have member variables and have behaviour associated with them. In python a class is created by the keyword class.
An object is created using the constructor of the class. This object will then be called the instance of the class. In Python we create instances in the following manner

### Example:
#### Instance = class(arguments)

#### How to create a class
The simplest class can be created using the class keyword. 
<pre>
>>> class Books:
...     pass
... 
>>> books = Books()
>>> print(books)
<__main__.Books object at 0x7X415268741>

</pre>

</a>

<a href="#top">Return</a>
<br>
<br>
___________________________________________________________________________________________________________________________________


<a name="mv"> 
  
## Object
In computer science, an object can be a variable, a data structure, a function, or a method, and as such, is a value in memory referenced by an identifier.
In the class-based object-oriented programming paradigm, object refers to a particular instance of a class, where the object can be a combination of variables, functions, and data structures.

- Simply put, an Object is simply a collection of data (variables) and methods (functions) that acts on data.

### Example:
#### ob = MyClass()

The command statement above will create a new instance object named ob.
</a>

<a href="#top">Return</a>
<br>
<br>
___________________________________________________________________________________________________________________________________


<a name="rm"> 
  
## Static
- The third method, MyClass.staticmethod was marked with a @staticmethod decorator to flag it as a static method. Static means, that the member is on a class level rather on the instance level. Static variables exist only in single instance per class and are not instantiated.

### Example:
####  print Example.staticVariable

</a>

<a href="#top">Return</a>
<br>
<br>
___________________________________________________________________________________________________________________________________


<a name="history"> 
  
## Property / Attribute
#### Property
In Python, property() is a built-in function that creates and returns a property object. The signature of this function is. property(fget=None, fset=None, fdel=None, doc=None)


#### Class Attribute vs. Instance Attribute

An instance attribute is a Python variable belonging to one, and only one, object. This variable is only accessible in the scope of this object and it is defined inside the constructor function, __init__(self,..) of the class.

A class attribute is a Python variable that belongs to a class rather than a particular object. It is shared between all the objects of this class and it is defined outside the constructor function, __init__(self,...), of the class.

### Example:
####  print (foo.istance_attr)
####  print (ExampleClass.instance_attr)

##### The below ExampleClass is a basic Python class with two attributes: class_attr and instance_attr. 
<Pre>
class ExampleClass(object):
  class_attr = 0 
  
  def __init__(self, instance_attr):
    self.instance_attr = instance_attr
</pre>
</a>

<a href="#top">Return</a>
<br>
<br>
___________________________________________________________________________________________________________________________________


<a name="home"> 
  
## Method
- A method is a function that takes a class instance as its first parameter. Methods are members of classes

### Example:
#### class C: def method(self, possibly, other, arguments): pass 

Characteristics of Python Method:
* Method is called by its name, but it is associated to an object (dependent).
* A method is implicitly passed the object on which it is invoked.
* It may or may not return any data.
* A method can operate on the data (instance variables) that is contained by the corresponding class

</a>

<a href="#top">Return</a>
<br>
<br>
___________________________________________________________________________________________________________________________________


<a name="file"> 
  
## Exception
An exception is an error that happens during execution of a program. When that error occurs, Python generate an exception that can be handled, which avoids your program to crash.

#### Why use Exceptions?
Exceptions are convenient in many ways for handling errors and special conditions in a program. When you think that you have a code which can produce an error then you can use exception handling.

The following are common exception errors in Python:
* IOError - If the file cannot be opened.
* ImportError - If python cannot find the module
* ValueError - Raised when a built-in operation or function receives an argument that has the right type but an inappropriate value.
* KeyboardInterrupt - Raised when the user hits the interrupt key (normally Control-C or Delete)
* EOFError - Raised when one of the built-in functions (input() or raw_input()) hits an end-of-file condition (EOF) without reading any data

### Examples:
<pre>
try:
    print 1/0

except ZeroDivisionError:
    print "You cannot divide by zero."
</pre>

####  class Error(Exception):
####   """Base class for other exceptions"""
####   pass

</a>

<a href="#top">Return</a>
<br>
<br>
___________________________________________________________________________________________________________________________________

<a name="path"> 
  
## Unit Test
- Unit Testing is the first level of software testing where the smallest testable parts of a software are tested.

A unit is the smallest testable part of any software. It usually has one or a few inputs and usually a single output. In procedural programming, a unit may be an individual program, function, procedure, etc. The purpose is to validate that each unit of the software performs as designed.

### Examples:
#### import unittest 
#### class SimpleTest(unittest.TestCase): 

#### In Python:
<pre>
>>> assert sum([1, 2, 3]) == 6, "Should be 6"
</pre>
The above python code will not output anything because the values are correct.

However, in the code below a raised AssertionError will appear because the result of sum() does not match 6.
<pre>
>>> assert sum([1, 1, 1]) == 6, "Should be 6"
Traceback (most recent call last):
  File "<stdin>", line 1, in <module>
AssertionError: Should be 6
</pre>

</a>

<a href="#top">Return</a>
<br>
<br>
___________________________________________________________________________________________________________________________________

<a name="arrow"> 
  
## Constructor
- A constructor is a special kind of method that Python calls when it instantiates an object using the definitions found in your class
Python relies on the constructor to perform tasks such as initializing (assigning values to) any instance variables that the object will need when it starts.

The name of a constructor is always the same, __init__(). The constructor can accept arguments when necessary to create the object. When you create a class without a constructor, Python automatically creates a default constructor for you that doesn’t do anything. Every class must have a constructor, even if it simply relies on the default constructor.

### Example:
#### Type MyInstance = MyClass() and press Enter
#### def __init__(self):
</a>

<a href="#top">Return</a>
<br>
<br>
___________________________________________________________________________________________________________________________________

<a name="vi"> 
  
## Factory
- Factory method is a creational design pattern which solves the problem of creating product objects without specifying their concrete classes. 

In class-based programming, a factory is an abstraction of a constructor of a class, while in prototype-based programming a factory is an abstraction of a prototype object. A constructor is concrete in that it creates objects as instances of a single class, and by a specified process (class instantiation), while a factory can create objects by instantiating various classes, or by using other allocation schemes such as an object pool. A prototype object is concrete in that it is used to create objects by being cloned, while a factory can create objects by cloning various prototypes, or by other allocation schemes.

Factories may be invoked in various ways, most often a method call (a factory method), sometimes by being called as a function if the factory is a function object (a factory function). 

The simplest example of a factory is a simple factory function, which just invokes a constructor and returns the result. In Python, a factory function f that instantiates a class A can be implemented as:
<pre>
def f():
    return A()
</pre>

### Another Example:
####   def __init__(self):
####  self.product = self._factory_method()
</a>

<a href="#top">Return</a>
<br>
<br>
___________________________________________________________________________________________________________________________________

<a name="Decorator"> 
  
## Decorator
- A decorator is a design pattern in Python that allows a user to add new functionality to an existing object without modifying its structure. More specifically, a decorator in Python is any callable Python object that is used to modify a function or a class.

There are two different kinds of decorators in Python, however they have the same underlying concept:
* Function decorators - When a user needs to create an object that acts as a function then function decorator needs to return an object that acts like a function, so __call__ can be useful.
* Class decorators - To define a decorator as a class we have to use a __call__ method of classes.

### Example:
Defining Functions Inside other Functions
<pre>
 def plus_one(number):
      def add_one(number):
           return number + 1
           
      result = add_one(number)
      return result
plus_one(4)   

OUTPUT:  5
</pre>

#### Creating Decorators
Define a wrapper inside an enclosed function.
<pre>
def uppercase_decorator(function):
    def wrapper():
        func = function()
        make_uppercase = func.upper()
        return make_uppercase

    return wrapper

</pre>

</a>

<a href="#top">Return</a>
<br>
<br>
___________________________________________________________________________________________________________________________________

<a name="class"> 
  
## Extend Class
- Meaning, add new methods, not change existing ones classes, even built-in ones.

Extends means that you are creating a subclass of the base class you are extending. You can only extend one class in your child class, but you can implement as many interfaces as you would like.

When you extend a class, you have a parent-child relation between the original one and the new, extending one. The child class, the one extending the parent class, will have each and every member of the parent class, without the need to declare them again.

### Example:
#### import Color
####  class Color:
####  def getcolor(self):
####  return self.color + " extended!"
</a>

<a href="#top">Return</a>
<br>
<br>
___________________________________________________________________________________________________________________________________

<a name="csv"> 
  
## CSV Files
- Comma Separated Values or Comma Delimited files. 
CSV is the most common import and export format for spreadsheets and databases. These files are often used for exchanging data between different applications. They mostly use the comma character to separate (or delimit) data, but sometimes use other characters, like semicolons. The idea is that you can export complex data from one application to a CSV file, and then import the data in that CSV file into another application. CSV format was used for many years prior to attempts to describe the format in a standardized way in RFC 4180.

RFC 4180 formalized CSV. It defines the MIME type "text/csv", and CSV files that follow its rules should be very widely portable. Among its requirements: 

* MS-DOS-style lines that end with (CR/LF) characters (optional for the last line).
* An optional header record (there is no sure way to detect whether it is present, so care is required when importing).
* Each record "should" contain the same number of comma-separated fields.
* Any field may be quoted (with double quotes).
* Fields containing a line-break, double-quote or commas should be quoted. (If they are not, the file will likely be impossible to      process correctly).
* A (double) quote character in a field must be represented by two (double) quote characters.

The format can be processed by most programs that claim to read CSV files. The exceptions are (a) programs may not support line-breaks within quoted fields, (b) programs may confuse the optional header with data or interpret the first data line as an optional header and (c) double quotes in a field may not be parsed correctly automatically.


### Example of code use in an application:
#### import csv
####  with open('eggs.csv', newline='') as csvfile:

### Example of .csv data :
<pre>
Name,Email,Phone Number,Address

Bob Smith,bob@example.com,123-456-7890,123 Fake Street

Mike Jones,mike@example.com,098-765-4321,321 Fake Avenue
</pre>

A CSV file has a fairly simple structure. Itcan be a list of data separated by commas, as shown above. 
</a>

<a href="#top">Return</a>
<br>
<br>
___________________________________________________________________________________________________________________________________

<a name="reading"> 
  
## Reading Files
- In Python, there is no need for importing external library to read and write files. Python provides an inbuilt function for creating, writing and reading files. 

The following list the steps to reading a Python file.
How to Read a File:
1.  Open the file in Read mode
<pre>
f=open("guru99.txt", "r")
</pre>
2.   Use the mode function in the code to check that the file is in open mode. If yes, we proceed ahead
<pre>
if f.mode == 'r':
</pre>
Finally....
3.  Use f.read to read file data and store it in variable content
<pre>
contents =f.read()
</pre>
You also have the ability to rad a File line by line, by typing the following command: (f1=f.readlines()) 
When you run the code (f1=f.readlines()) for reading the file or document line by line, it will separate each line and present the file in a readable format. 

#### File Modes in Python for reading or writing 
|Mode|Description|
|----|-----------|
|'r'|This is the default mode. It Opens file for reading.|
|'w'|	This Mode Opens file for writing. If file does not exist, it creates a new file. If file exists it truncates the file.|
|'+'|	This will open a file for reading and writing (updating)|

### Example:
####  f= open("guru99.txt","w+")
</a>

<a href="#top">Return</a>
<br>
<br>
___________________________________________________________________________________________________________________________________

Readme Page [Click Here](/README.md)



