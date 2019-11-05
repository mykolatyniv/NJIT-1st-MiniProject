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
- DRY principle is a software development practice aimed at reducing repetition of information. In this lesson, you learned how to apply DRY when making comparisons in your Python code

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
</a>

<a href="#top">Return</a>
<br>
<br>
___________________________________________________________________________________________________________________________________


<a name="pwd"> 
  
## Class 
- A class is a code template for creating objects. Objects have member variables and have behaviour associated with them. In python a class is created by the keyword class.

### Example:
#### Instance = class(arguments)

</a>

<a href="#top">Return</a>
<br>
<br>
___________________________________________________________________________________________________________________________________


<a name="mv"> 
  
## Object
- Object is simply a collection of data (variables) and methods (functions) that act on those data.

### Example:
#### ob = MyClass()

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
- The instance_attr is only accessible from the scope of an object. The class attribute (class_attr) is accessible as both a property of the class and as a property of objects, as it is shared between all of them.

### Example:
####  print (foo.istance_attr)
####  print (ExampleClass.instance_attr)

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



