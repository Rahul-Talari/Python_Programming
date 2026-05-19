**Core Python**

==================================================

1\. Procedural Programming

&#x20;      **Basics**                – Data types, variables, I/O, operators

&#x20;      **Control Flow**          – Conditionals, loops, break, continue, pass

&#x20;      **Data Structures**       – Strings, lists, tuples, sets, dictionaries



2\. Functional Programming

&#x20;      **Functions**	     – Functions, lambda, generators, decorators



3\. Object-Oriented Programming

&#x20;      **OOPS**                  – Access Modifiers, Classes, objects, inheritance, polymorphism, encapsulation, abstraction

&#x20;      **Modules \& Packages**    – Imports, code organization, reusability



4\. **Python Utilities**         – File handling, exception handling, logging

5\. **Parallel Programming**     – Multithreading, multiprocessing





**========================================================================================================================================================================================**

**Exceptions :** Exceptions are events that occur during execution, disrupting the normal flow of a program.





&#x09;     Types of Exceptions:

&#x09;	1. Built-in Exceptions (ex: SyntaxError, ValueError, TypeError)

&#x09;	2. User-defined Exceptions (custom classes)



Handling Exceptions:

&#x09;1. Try: Enclose code that may raise an exception.

&#x09;2. Except: Handle the exception (specific or general).

&#x09;3. Else: Execute if no exception occurs.

&#x09;4. Finally: Execute regardless of exception.



**Basic Syntax:**

try:

&#x20;   # code that may raise exception

except ExceptionType:

&#x20;   # handle exception

except Exception as e:

&#x20;      print(e)

else:

&#x20;   # code if no exception

finally:

&#x20;   # code always executed



**Ex:**

try:

&#x20;   # code block where exception can occur

&#x20;   a = int(input("Enter the number 1: "))

&#x20;   b = int(input("Enter the number 2: "))

&#x20;   c = a / b



except NameError:

&#x20;   print("The user has not defined the variable.")

&#x20;

except ZeroDivisionError:

&#x20;   print("Please provide a number greater than 0.")



except TypeError:

&#x20;   print("Try to make the datatype similar.")

&#x20;

except Exception as ex:

&#x20;   print("An error occurred:", ex)

&#x20;

else:

&#x20;   # Executes if no exception occurs

&#x20;   print("Result:", c)



finally:

&#x20;   # Always executes

&#x20;   print("The execution is done.")



Raising Exceptions:



1\. Raise a built-in exception: raise ValueError("Invalid input")

2\. Raise a custom exception: raise MyCustomError("Something went wrong")





Custom Exceptions:



Create a class inheriting from Exception:



























































Python OOPS

&#x20;  - Classes \& Objects, self, Constructors (\_\_init\_\_)

&#x20;  - Access Modifiers (public, protected, private), Encapsulation

&#x20;  - Inheritance (single, multiple, multilevel, hierarchical), Method Overriding

&#x20;  - Polymorphism (method overloading concept, overriding)

&#x20;  - Abstraction (ABC module, abstract methods)

&#x20;  - Static methods, Class methods



Modules \& Packages

&#x20;  - Modules, Built-in modules (math, random, os, sys, datetime)

&#x20;  - Packages

&#x20;  - Code reusability, pip \& external libraries





**========================================================================================================================================================================================**

**📦 Module vs Package (Python Imports)**

**========================================================================================================================================================================================**



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



