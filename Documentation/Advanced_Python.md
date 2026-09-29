**Core Python**

==========================================================================================================================

1\. Procedural Programming      – **Basics** (data types, variables, I/O, operators),
**Control Flow** (if-else, loops, break, continue, pass)
**Data Structures** (strings, lists, tuples, sets, dicts)



2\. **Function**al Programming      – Functions, lambda, generators, decorators

3\. **Object-Oriented** Programming – OOPs (classes, objects, access modifiers, inheritance, polymorphism, encapsulation, abstraction), exception handling, Multithreading/processing

4\. **Modules \& Packages**          – Built-in modules (random, os, shutil, json, datetime), file handling, logging



**🧠 Python OOPS**



&#x09;- 🧱 Class, attributes(class/static, dynamic/Instance), methods(class/static, dynamic/Instance), self; Objects, constructors

&#x09;- 🔁 Inheritance (single, multiple, multilevel, hierarchical)

&#x09;- 🔄 Polymorphism (method overriding, concept of overloading)

&#x09;- 🔒 Encapsulation, Access Modifiers (public, \_protected, \_\_private)

&#x09;- 🎭 Abstraction (ABC module, abstract methods)



======================================================================================================================================================================================

**Class**        : A blueprint/template for creating objects. Defines attributes (data) and methods (behavior).



**Attributes**   : Variables defined inside a class that stores data/properties of an object.

&#x20;              ├─ Class Attributes    : shared by all objects; **accessed using ClassName.attribute**

&#x20;              └─ Instance Attributes : Object-specific; defined using self.



**Methods**      : Functions defined inside a class that define behavior of objects.

&#x20;              ├─ Class Methods       : Work with class data; using cls and @classmethod.

&#x20;              └─ Instance Methods    : Work with object data; using self.



**Object**       : An instance of a class (real world entity created using a class).

**Constructor**  : A special method (\_\_init\_\_) automatically called when an object is created; used to initialize instance variables.



\# =========================================================================

\# CLASS ATTRIBUTE + CLASS METHOD

\# =========================================================================

&#x09;class Employee:			



&#x09;    company = "TCS"              # **Class Attribute**

&#x09;

&#x09;    @classmethod

&#x09;    def get\_company(cls):        # **Class Method**

&#x09;        return cls.company



&#x09;print(Employee.company)		 # Access class attribute

&#x09;print(Employee.get\_company())	 # Access class method 



\# =========================================================================

\# INSTANCE ATTRIBUTE + INSTANCE METHOD

\# =========================================================================

&#x09;class Employee:



&#x09;    def \_\_init\_\_(self, name):    # **Default constructor**

&#x09;        self.name = name         # **Instance Attribute**



&#x09;    def get\_name(self):          # **Instance Method**

&#x09;        return self.name



&#x09;obj = Employee("Rahul")		 # Creating object



&#x09;print(obj.name)			 # Access Instance attribute

&#x09;print(obj.get\_name())		 # Access Instance method



\# =================================================================================================================

**Inheritance:** Concept in OOP that allows a class to inherit the attributes, methods from another class.

\# =================================================================================================================



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





&#x09;class Employee:						**# Parent Class**



&#x09;    def \_\_init\_\_(self, name):				# Parent Constructor

&#x09;        self.name = name

&#x09;        print("Employee Constructor Called")



&#x09;    def employee\_details(self):				# Parent Method

&#x09;        print(f"{self.name} works in the company")





&#x09;class Developer(Employee):				**# Child Class inheriting Parent Class**

&#x09;

&#x09;    def \_\_init\_\_(self, name, skill):			# Child Constructor

&#x09;         super().\_\_init\_\_(name)				**# Calling Parent Constructor using super()**

&#x09;        self.skill = skill

&#x09;        print("Developer Constructor Called")



&#x09;    def coding(self):					**# Child Method**

&#x09;        print(f"{self.name} writes {self.skill} code")





&#x09;dev = Developer("Rahul", "Python")			# Creating Child Object

&#x09;dev.employee\_details()					# Accessing Parent Method

&#x09;dev.coding()						# Accessing Child Method



\# ========================================================================================================================================================================

**Polymorphism:**	Polymorphism means "many forms". It allows the same method/operator/function name to perform different behaviors depending on the object or data type.

\# ========================================================================================================================================================================



&#x09;**Method overloading:**

&#x09;	**-** Using the same method name for different number/types of inputs.

&#x09;	**-** Python does not support true method overloading; use default arguments or \*args.



&#x09;    EX:

&#x09;    def add(\*args):

&#x09;        return sum(args)





&#x09;    print(add(1, 2))

&#x20;   	    print(add(1, 2, 3))



&#x09;**Method overriding (Run-time Polymorphism)**:

&#x09;	- It occurs when Child class provides its own implementation of a method already defined in the parent class.



&#x09;class Animal:

&#x20;   		def sound(self): print("Animal sound")



&#x09;class Dog(Animal):

&#x20;   		def sound(self): print("Dog barks")   # Method Overriding



&#x09;Dog().sound()



\# ========================================================================================================================================================================

**Abstraction** : 

\# ========================================================================================================================================================================

&#x09;- Hiding implementation details and showing only essential functionality. It can contain attributes, abstract methods, and concrete methods.

&#x20;       - In Python, an abstract class is created by extending the ABC base class and using @abstractmethod for functions.



&#x09;Example:



&#x09;from abc import ABC, abstractmethod



&#x09;class Employee(ABC):              # Abstract class



&#x09;    company = "TCS"               # Attribute

&#x09;    @abstractmethod

&#x09;    def work(self):               # Abstract Method

&#x09;        pass





&#x09;class Developer(Employee):



&#x09;    def work(self):               # Implementation

&#x20;       	print("Writing code")

&#x09;



&#x09;obj = Developer()

&#x09;obj.work()

======================================================================================================================================================================================









========================================================================================================================================================================================

**📦 Module vs Package (Python Imports)**

========================================================================================================================================================================================



**📄 Module:** A module is a **single Python file (.py)** containing classes, variables, functions.



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

======================================================================================================================================================================================









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

