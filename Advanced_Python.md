**Core Python**

==========================================================================================================================

1\. Procedural Programming      – **Basics** (data types, variables, I/O, operators),
**Control Flow** (if-else, loops, break, continue, pass)
**Data Structures** (strings, lists, tuples, sets, dicts)



2\. **Function**al Programming      – Functions, lambda, generators, decorators

3\. **Object-Oriented** Programming – OOPs (classes, objects, access modifiers, inheritance, polymorphism, encapsulation, abstraction), exception handling, Multithreading/processing

4\. **Modules \& Packages**          – Built-in modules (random, os, shutil, json, datetime), file handling, logging



**🧠 Python OOPS**



&#x09;- 🧱 Classes \& Objects, Constructors (`\\\_\\\_init\\\_\\\_`), `self`

&#x09;- 🔒 Encapsulation, Access Modifiers (public, protected, private)

&#x09;- 🎭 Abstraction (ABC module, abstract methods)

&#x09;- 🔁 Inheritance (single, multiple, multilevel, hierarchical)

&#x09;- 🔄 Polymorphism (method overriding, concept of overloading)

&#x09;- ⚙️ Class methods, Static methods



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

