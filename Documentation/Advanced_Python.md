**Core Python**

==========================================================================================================================

1\. Procedural Programming      – **Basics** (data types, variables, I/O, operators),
**Control Flow** (if-else, loops, break, continue, pass)
**Data Structures** (strings, lists, tuples, sets, dicts)



2\. **Function**al Programming      – Functions, lambda, generators, decorators

3\. **Object-Oriented** Programming – OOPs (classes, objects, access modifiers, inheritance, polymorphism, encapsulation, abstraction), exception handling, Multithreading/processing

4\. **Modules \& Packages**          – Built-in modules (random, os, shutil, json, datetime), file handling, logging



**🧠 Python OOPS**



&#x09;- 🧱 Classes, Objects, attributes(class/Instance), methods(class/Instance), constructors,self

&#x09;- 🔁 Inheritance (single, multiple, multilevel, hierarchical)

&#x09;- 🔄 Polymorphism (method overriding, concept of overloading)

&#x09;- 🔒 Encapsulation, Access Modifiers (public, \_protected, \_\_private)

&#x09;- 🎭 Abstraction (ABC module, abstract methods)



========================================================================================================================================================================================

**📦 Module vs Package (Python Imports)**

========================================================================================================================================================================================



**📄 Module:** A module is a **single Python file (.py)** containing functions, classes, variables.



&#x09;**Syntax:**

&#x20;   		import module\_name              	# imports **entire module**

&#x20;   		import module\_name as alias     	# imports **module with alias** (a shortcut name)

&#x20;   		from module\_name import function\_name   # imports **only specific function** from module



&#x09;**Example**:

&#x20;   		import math                     	# imports math module

&#x20;   		from math import sqrt           	# imports only sqrt function from math module



&#x09;	print(math.sqrt(25))            	# uses sqrt via module name → returns 5.0

&#x20;   		print(sqrt(25))                 	# uses directly imported sqrt function → returns 5.0





**📦 Package:** A package is a **folder containing multiple modules**; Used to organize large projects.

&#x09;    **\_\_init\_\_.py** is a special file inside a package that tells Python the folder is a package and runs automatically when the package is imported.



&#x09;**Syntax:**

&#x20;   		import package.module                     # imports **module from package** using full path

&#x20;   		from package import module                # imports **module**  directly from package into current namespace

&#x20;   		from package.module import function       # imports **specific function** from module inside package



&#x09;**Example:**

&#x09;    from mypackage import math\_utils          	  # imports math\_utils module from mypackage

&#x20;   	    from mypackage.math\_utils import add     	  # imports add function from math\_utils module



&#x09;    print(add(2, 3))                          	  # calls add function → returns 5

========================================================================================================================================================================================

**Exceptions :** Exceptions are runtime events that disrupt the normal flow of a program.



&#x09;     **Types of Exceptions:**

&#x09;	1. Built-in Exceptions 	    : SyntaxError, ValueError, TypeError

&#x09;	2. User-defined Exceptions  : raise built-in/custom exceptions



&#x09;     **Exception Handling Flow:**

&#x09;	try     -> code that may raise exception

&#x09;	except  -> handles the exception

&#x09;	else    -> runs if no exception occurs

&#x09;	finally -> always runs (whether error occurs or not)



**Basic Syntax:**

======================

try:

&#x20;   # risky code

&#x20;   a = int(input("Enter number 1: "))

&#x20;   b = int(input("Enter number 2: "))

&#x20;   c = a / b



except ZeroDivisionError:

&#x20;   print("Denominator cannot be zero")



except Exception as e:

&#x20;   print("Unexpected error:", e)



else:

&#x20;   print("Result:", c)



finally:

&#x20;   print("Execution completed")



**Raise Built-in Exception**

========================

&#x09;raise ValueError("Age cannot be negative")            → Immediately raises an error and stops execution

&#x09;raise ZeroDivisionError("Denominator cannot be zero") → Immediately raises an error and stops execution



&#x09;If you want the program to continue execution after an error, wrap the risky code inside try-except block.



**Raise Custom exception**

========================

class MyError(Exception):

&#x20;   pass



x = -10

try:

&#x20;   if x < 0:

&#x20;       **raise** MyError("Negative number not allowed")

except MyError as e:

&#x20;   print("Error caught:", e)

===============================================================================================================================================================

















===============================================================================================================================================================

**Class**        : A blueprint/template for creating objects. Defines attributes (data) and methods (behavior).

**Object**       : An instance of a class (real entity created using a class).



**Attributes**   : Variables inside a class that store data.

&#x20;              ├─ Class Attributes    : Shared variables belonging to the class; accessed using ClassName.attribute.

&#x20;              └─ Instance Attributes : Object-specific variables initialized using self inside constructor.



**Methods**      : Functions defined inside a class that define behavior of objects.

&#x20;              ├─ Class Methods       : Methods working with class attributes using cls and @classmethod.

&#x20;              └─ Instance Methods    : Methods working with instance attributes using self.



**Constructor**  : A special method (\_\_init\_\_) automatically called when an object is created; used to initialize instance variables.



=========================================================================

class Employee:			 # **Class**



&#x20;   company = "TCS"              # Class Attribute/**Static Variable**



&#x20;   @classmethod

&#x20;   def get\_company(cls):        # Class Method/**Static Method**

&#x20;       return cls.company



print(Employee.company)		 # Accessing attribute using class name

print(Employee.get\_company())	 # Accessing method using class name

=========================================================================



class Employee:			 # **Class**



&#x20;   def \_\_init\_\_(self, name):    # **Default constructor** (Initializer)

&#x20;       self.name = name         # **Instance Attribute**



&#x20;   def get\_name(self):          # **Instance Method**

&#x20;       return self.name



obj = Employee("Rahul")		 # **Creating object**



print(obj.name)			 # Accessing attribute using object

print(obj.get\_name())		 # Accessing method using object

========================================================================================================================================================



**Inheritance:** Concept in OOP that allows a class to inherit the attributes, methods from another class.



&#x09;     **Supported**:      Single Inheritance       Multi-Level Inheritance                    Hierarchical Inheritance

&#x09;	      	    ---------------------     --------------------------                ---------------------------

&#x09;   		     Parent ───▶ Child       Grand\_Parent ───▶ Parent ───▶ Child      Parent ───▶ Child1

&#x20;                            		                                                                └──▶ Child2



&#x09;     **Not Supported**: Multiple Inheritance     Hybrid Inheritance

&#x09;       		    ---------------------    ------------------

&#x09;		    Parent1 ──┐

&#x09;   		               ├──▶ Child     Grand\_Parent

&#x09;   		    Parent2 ──┘                    │

&#x20;         		    		                    ▼

&#x20;                         				  Parent

&#x20;                            		    		 /      \\

&#x20;                           		  	        ▼       ▼

&#x20;                         		 	     Child1    Child2



&#x09;     **Concepts in Inheritance:**

&#x09;	✔ Inheritance: Parent Class, Child Class

&#x09;	✔ Constructor Inheritance (via super())

&#x09;	✔ Method Inheritance





class Employee:						**# Parent Class**



&#x20;   def \_\_init\_\_(self, name):				# Parent Constructor

&#x20;       self.name = name

&#x20;       print("Employee Constructor Called")



&#x20;   def employee\_details(self):				# Parent Method

&#x20;       print(f"{self.name} works in the company")





class Developer(Employee):				**# Child Class inheriting Parent Class**



&#x20;   def \_\_init\_\_(self, name, skill):			# Child Constructor

&#x20;        super().\_\_init\_\_(name)				**# Calling Parent Constructor using super()**

&#x20;       self.skill = skill

&#x20;       print("Developer Constructor Called")



&#x20;   def coding(self):					**# Child Method**

&#x20;       print(f"{self.name} writes {self.skill} code")





dev = Developer("Rahul", "Python")			# Creating Child Object

dev.employee\_details()					# Accessing Parent Method

dev.coding()						# Accessing Child Method

========================================================================================================================================================



**Polymorphism:**	Polymorphism means "many forms". It allows the same method/operator/function name to perform different behaviors depending on the object or data type.



&#x09;**EX:** Same method name -> Different behavior



&#x09;class Dog:

&#x09;    def sound(self): print("Dog barks")     # Dog behavior



&#x09;class Cat:

&#x09;    def sound(self): print("Cat meows")     # Cat behavior



&#x09;for obj in \[Dog(), Cat()]:		    # Different objects responding differently to same method

&#x20;   	obj.sound()



**Method overriding (Run-time Polymorphism)**:

&#x09;- It occurs when a child class provides its own implementation of a method i.e. already defined in the parent class using the same method name and parameters.



&#x09;class Animal:

&#x20;   		def sound(self): print("Animal sound")



&#x09;class Dog(Animal):

&#x20;   		def sound(self): print("Dog barks")   # Method Overriding



&#x09;Dog().sound()





**Method overloading:**

&#x09;**-** Using the same method name for different number/types of inputs.

&#x09;**-** Python does not support true method overloading directly. The latest method definition overrides the previous one.



&#x09;Alternative: Use default arguments (\*args / default parameters) to achieve similar behavior.

========================================================================================================================================================



