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





