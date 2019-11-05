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
#### Behavioural Patterns involve communication between objects, how objects interact and fulfil a given task. According to GOF principles, there are a total of 11 behavioral patterns in Python: Chain of responsibility, Command, Interpreter, Iterator, Mediator, Memento, Observer, State, Strategy, Template, Visitor.

The Gang of Four are the four authors of the book, "Design Patterns: Elements of Reusable Object-Oriented Software". There are twenty-three design patterns described by the Gang of Four.

Design patterns provide solutions to common software design problems. In the case of object-oriented programming, design patterns are generally aimed at solving the problems of object generation and interaction, rather than the larger scale problems of overall software architecture. They give generalised solutions in the form of templates that may be applied to real-world problems.

The three pattern types are: 	Creational, Structural, Behavioral
Which are further broken down by their characteristics: 

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
- Object is simply a collection of data (variables) and methods (functions) that act on those data

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

</a>

<a href="#top">Return</a>
<br>
<br>
___________________________________________________________________________________________________________________________________


<a name="file"> 
  
## Exception
- Python has many built-in exceptions which forces your program to output an error when something in it goes wrong.

### Example:
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

### Example:
#### import unittest 
#### class SimpleTest(unittest.TestCase): 

</a>

<a href="#top">Return</a>
<br>
<br>
___________________________________________________________________________________________________________________________________

<a name="arrow"> 
  
## Constructor
- A constructor is a special kind of method that Python calls when it instantiates an object using the definitions found in your class

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

### Example:
####   def __init__(self):
####  self.product = self._factory_method()
</a>

<a href="#top">Return</a>
<br>
<br>
___________________________________________________________________________________________________________________________________

<a name="Decorator"> 
  
## Decorator
- A decorator is a design pattern in Python that allows a user to add new functionality to an existing object without modifying its structure. 

### Example:
#### def plus_one(number):
####  def add_one(number):
####  return number + 1
</a>

<a href="#top">Return</a>
<br>
<br>
___________________________________________________________________________________________________________________________________

<a name="class"> 
  
## Extend Class
- Meaning, add new methods, not change existing ones classes, even built-in ones.

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
- Comma Separated Values. CSV is the most common import and export format for spreadsheets and databases. CSV format was used for many years prior to attempts to describe the format in a standardized way in RFC 4180

### Example:
#### import csv
####  with open('eggs.csv', newline='') as csvfile:
</a>

<a href="#top">Return</a>
<br>
<br>
___________________________________________________________________________________________________________________________________

<a name="reading"> 
  
## Reading Files
- In Python, there is no need for importing external library to read and write files. Python provides an inbuilt function for creating, writing and reading files. 

### Example:
####  f= open("guru99.txt","w+")
</a>

<a href="#top">Return</a>
<br>
<br>
___________________________________________________________________________________________________________________________________

Readme Page [Click Here](/README.md)



