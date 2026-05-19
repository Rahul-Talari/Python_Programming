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

**Data Types, Variables, Input \& Outputs**

**========================================================================================================================================================================================**

**Datatypes :**

&#x09;Primitive datatypes     :  int, str, float, bool

&#x09;Collection datatypes    :  list, tuple, dictionary, set



**Variables:**

&#x20;   - Name used to store data that can change during program execution

&#x20;   - No datatype declaration required, can hold any data type



&#x20;     **Global Variable:** Use "global" keyword to access and modify a variable inside a function



&#x09;Ex:

&#x20;   	x = 10                          # Global variable



&#x09;def update\_global():

&#x09;        global x                    # Declare x as global

&#x20;       	x = 20                      # Update global variable



&#x09;update\_global()

&#x20;   	print(x)                        # Output: 20



&#x20;     **Naming Rules:**

&#x20;   		1. Allowed: letters (a-z, A-Z), numbers (0-9), underscore (\_); cannot start with a number

&#x20;   		2. Case-sensitive and cannot use Python keywords

&#x20;   		3. Multi-word naming styles:

&#x20;       		- camelCase  : first word lowercase, next words capitalized

&#x20;       		- PascalCase : each word starts with capital letter

&#x20;       		- snake\_case : words separated by underscores (preferred in Python)



**Input:**

&#x20;   Static:

&#x20;       ⮚ Multiple Values to Multiple variables : a, b, c = 1, "hero", "Ram charan"

&#x20;       ⮚ Single value to Multiple variables    : a = b = c = 1



&#x20;   Dynamic:

&#x20;       name   = input("Enter your name: ")              # String input (default); type(name)=<class 'str'>

&#x20;       age    = int(input("Enter your age: "))          # Integer input; type(age)=<class 'int'>

&#x20;       height = float(input("Enter your height: "))     # Float input; type(height)=<class 'float'>



**Output:**

&#x20;      print(f"Name: {name}\\nAge: {age}\\nHeight: {height}") # Display Output



**========================================================================================================================================================================================**

**Operators, Conditional Statements, Iterative Statements**

**========================================================================================================================================================================================**

**Operators:**

&#x09;Numerical Functions:

&#x20;   		Arithmetic     : +   -   \*   /   //   %   \*\* (exponential)

&#x20;   		Bitwise        : \&   |   ^   \~   <<   >>



&#x09;Single Value Check:

&#x20;   		Comparison     : ==  !=  >   <   >=   <=

&#x20;   		Logical        : and or  not



&#x09;Multi Value Check:

&#x20;   		Membership     : in  not in



**Quantifiers:**

&#x09;all(n == 1 for n in nums)   # True only if all elements are 1

&#x09;any(n == 1 for n in nums)   # True if at least one element is 1



**Conditional Statements in Python**



&#x20;1. Standard Format

&#x09;if condition1:

&#x20;   		print("Statement")

&#x09;elif condition2:

&#x20;   		print("Statement")

&#x09;elif condition3:

&#x20;   		print("Statement")

&#x09;else:

&#x20;   		print("Statement")





&#x20;2. Single-line Format

&#x09;if condition1: 	 print("Statement")

&#x09;elif condition2: print("Statement")

&#x09;elif condition3: print("Statement")

&#x09;else: print("Statement")





&#x20; 3. Short Hand If-Else (Ternary Operator)

&#x09;result = "Positive" if number > 0 else "Non-positive"



**Iterative Statements in Python: for(known iterations)/while**(condition-based iterations)



&#x09;**1. Index-Based Iteration**

&#x09;for i in range(len(numbers)):

&#x20;   		print(i, numbers\[i])



&#x09;**2. Element-Based Iteration**

&#x09;for value in numbers:

&#x20;   		print(value)



&#x09;**3. Index + Element Iteration using enumerate()**

&#x09;for i, value in enumerate(numbers):

&#x20;   		print(i, value)



&#x09;**4. while loop Iteration**

&#x09;i = 0

&#x09;while i < len(numbers):

&#x20;   		print(i, numbers\[i])

&#x20;   	i += 1





&#x09;for i in range(5):



&#x09;    if i == 1:

&#x20;       	print("break executed")

&#x20;       	**break**				    # **break**: Stops the entire loop immediately \& Control comes outside the loop

&#x09;    if i == 2:

&#x20;       	print("continue executed")

&#x20;       	**continue**			    # **continue**: Skips only the current iteration; Loop continues with the next iteration

&#x09;    if i == 3:

&#x20;       	print("pass executed")

&#x20;       	**pass**				    # **pass:** Does nothing, Used as a placeholder for future code



&#x09;    print(i)





**========================================================================================================================================================================================**

















































**Data Structures**:  Strings | List | Set | Tuple | Dictionary



&#x09;  🔸String     → Ordered          + **Immutable**, Sequence of characters       + Allows duplicates

&#x09;  🔸List       → Ordered   	  + Mutable Collection of elements          + Allows duplicates

&#x09;  🔸Tuple      → Ordered   	  + **Immutable** Collection of elements        + Allows duplicates

&#x09;  🔸Set        → **Unordered** 	  + Mutable Collection of unique elements   + **No duplicates**

&#x09;  🔸Dictionary → Inserted Order   + Mutable collection of key-value pairs   + where keys are unique \&  Values allow duplicates



**Operations**:



&#x20; 	🔸**Creation**	    → Initialization

&#x20; 	**🔸Modification**

&#x09;    Insert          → Add elements

&#x09;    Delete          → Remove elements

&#x09;    Update          → Modify elements

&#x20; 	**🔸Ordering**

&#x09;    Sorting         → Arrange elements

&#x09;    Reverse         → Reverse order

&#x20; 	**🔸Access**

&#x09;    Accessing       → Indexing / slicing / traversal

&#x09;    Search          → Find element / existence check

===========================================================================================================================================================

**List:\[]**

&#x09;**Initialization 		    :** list1=\[] , list1=\[0]\*n

&#x09;=================================================================================================

&#x09;**Insert**

&#x09;	l.insert(i, x)        : Insert item at given index

&#x09;	l.append(x)           : Add item to the end of the list

&#x09;	l.extend(iterable)    : Extend list by appending elements from iterable (or) list1 + list2

&#x09;**Delete**

&#x09;	\[x for x in lst if x != v] : Remove all occurrences of v

&#x09;	l.pop(i)     		   : Remove \& return item at index i (default last)

&#x09;	l.clear()    		   : Remove all elements from the list

&#x09;**Update**

&#x09;    	list\[i] = value    	   : Replace the element at index i with new value

&#x09;=================================================================================================

&#x09;**Sorting**

&#x09;	🔸l.sort(reverse=False)      : Sort list (Default: ascending)

&#x20; 		🔸sorted(lst)                : Returns new sorted list

&#x09;**Reverse**

&#x09;	🔸l.reverse()                : In-place reverse

&#x20; 		🔸l\[::-1]                    : Returns reversed copy

&#x09;=================================================================================================

&#x09;**Accessing**

&#x09;	**Indices:**

&#x09;		list\[start:stop:step]        → Slicing (stop is exclusive): Default: start = 0, stop=end of sequence, step=1

&#x20;       		list\[0:n:1]                  → Traverse left → right: +ve indexing

&#x09;	        list\[-1:-n:-1]               → Traverse right → left: -ve indexing



&#x09;	**Looping:**

&#x09;		🔸for item in lst:              → Iterate elements using value

&#x09;		🔸for i in range(len(lst)):     → Iterate elements using index

&#x20;   			🔸for i, val in enumerate(lst): → Iterate elements using index + value

&#x09;	**List comprehension:**

&#x09;			newlist = \[expression for item in list if condition]

&#x09;			Example: squares = \[x\*\*2 for x in numbers if x % 2 == 0]



&#x09;**Search**

&#x09;		  in operator                    → Check existence

&#x20; 			  \[x for x in lst if x==2]       → Get all index's of 2

===========================================================================================================================================================

**String:""**

&#x09;**Initialization** 		    : str="" Empty String / str="Hello World !!"

&#x09;=================================================================================================

&#x09;**Insert**		❌ Not possible (Strings are immutable)

&#x09;**Delete**		❌ Not possible (Cannot delete characters directly)

&#x09;**Update**		❌ Not possible (Cannot modify existing characters)

&#x09;	        ✔ Workaround: Convert to list → modify → join back

&#x09;=================================================================================================

&#x09;**Sorting**		🔸sorted(string)   : Returns new sorted list of characters;

&#x09;				     "separator".join(list)  						# Joins elements of list into a single string using 'separator'



&#x09;**Reverse**		🔸string\[::-1]     : Returns reversed string (copy)

&#x09;=================================================================================================

&#x09;**Accessing**

&#x09;	**Indices:**

&#x09;		string\[start:stop:step]        → Slicing (stop is exclusive)				Default: start = 0, stop = end, step = 1

&#x09;		string\[0:n:1]                  → Traverse left → right (+ve indexing)

&#x09;		string\[-1:-n:-1]               → Traverse right → left (-ve indexing)

&#x09;	**Looping:**

&#x09;		🔸for item in string:              → Iterate characters (value)

&#x09;		🔸for i in range(len(string)):     → Iterate using index

&#x09;		🔸for i, val in enumerate(string): → Iterate index + value

&#x09;	**List comprehension (on string):**

&#x09;		newlist = \[expression for item in string if condition]

&#x09;		Example: \[ch for ch in string if ch != ' ']



&#x09;**Search**

&#x09;		🔸in operator                   					     → Check existence

&#x09;		🔸\[i for i, ch in enumerate(string) if ch == 'a']                           → Get all index positions of 'a'

===========================================================================================================================================================

**SET: {}**



&#x09;**Initialization** 		  : set()

&#x09;=================================================================================================

&#x09;**Insert**

&#x09;	s.add(x)		: Add element x to the set

&#x09;	s.update(iterable)      : Add multiple elements from iterable



&#x09;**Delete**

&#x09;	new\_set = s-{x}	: Remove all occurrences of v

&#x09;	s.pop()     	: Remove \& return last item (No index support)

&#x09;	s.clear()    	: Remove all elements in the set

&#x09;**Update**

&#x09;    	Set elements can’t be updated directly, you must remove \& add new value.

&#x09;=================================================================================================

&#x09;**Sorting**	sorted(lst)              : Returns new sorted list

&#x09;**Reverse**	rev\_list = list(s)\[::-1]  # convert set to list (since set is unordered) and reverse the list using slicing

&#x09;=================================================================================================

&#x09;**Accessing**

&#x09;	**Looping:**

&#x09;		🔸for item in lst:              → Iterate elements using value

&#x09;

&#x09;	**Set comprehension:**

&#x09;			newlist = {expression for item in list if condition}

&#x09;			Example: squares = {x\*\*2 for x in numbers if x % 2 == 0}



&#x09;**Search**

&#x09;		🔸in operator                    → Check existence

&#x09;=================================================================================================

&#x09;**Set Operations:**                                           	   **Set Checks:**

&#x09;	A | B → A.union(B)                                      	    A.issubset(B)    : A ⊆ B

&#x09;	A \& B → A.intersection(B)                                 	    A.issuperset(B)  : A ⊇ B

&#x09;	A - B → A.difference(B)                                     	    A.isdisjoint(B)  : no common elements

&#x09;	A ^ B → A.symmetric\_difference(B)   A ^ B = (A ∪ B) - (A ∩ B)

===========================================================================================================================================================

**Tuple:**

&#x09;**Initialization 		    :** t = (1,2,3,4)

&#x09;=================================================================================================

&#x09;**Insert, Delete, Update	    :** NA

&#x09;			      **Insert** : Tuples are immutable, so new elements cannot be added after creation.

&#x20;   				      **Delete** : Individual elements cannot be removed because tuple size cannot change.

&#x20;   				      **Update** : Existing values cannot be modified once the tuple is created.

&#x09;=================================================================================================

&#x09;**Sorting**	🔸sorted(lst)      : Returns new sorted list ; sort method wont work since tuples are immutable \& inplace not possible

&#x09;**Reverse**	🔸l\[::-1]          : Returns reversed copy; ; reverse method wont work since tuples are immutable \& inplace not possible

&#x09;=================================================================================================

&#x09;**Accessing**

&#x09;

&#x09;	**Indexing:**

&#x09;		tup\[index]		    → Access random element based on index

&#x09;		a, b, c, d, e = tup         → Unpacking

&#x09;

&#x09;	**Slicing:**

&#x09;		tup\[start:stop:step]        → Slicing (stop is exclusive): Default: start = 0, stop=end of sequence, step=1

&#x20;       		tup\[0:n:1]                  → Traverse left → right: +ve indexing

&#x09;	        tup\[-1:-n:-1]               → Traverse right → left: -ve indexing



&#x09;	**Looping:**

&#x09;		🔸for item in tup:              → Iterate elements using value

&#x09;		🔸for i in range(len(tup)):     → Iterate elements using index

&#x20;   			🔸for i, val in enumerate(tup): → Iterate elements using index + value

&#x09;

&#x09;**Search**

&#x09;		  in operator                    → Check existence

&#x20; 			  \[x for x in tup if x==2]       → Get all index's of 2

&#x09;=================================================================================================

&#x09;**Packing \& Unpacking:**

&#x09;	t = 1,2,3	# Packing

&#x09;	a,b,c = t	# UnPacking

&#x09;

===========================================================================================================================================================

**Dictionary:{}**



&#x09;**Initialization**

&#x09;	dict\_var={}

&#x09;	defaultdict(int)   : int()   → If key not exists return 0

&#x09;	defaultdict(float) : float() → If key not exists return 0.0

&#x09;	defaultdict(str)   : str()   → If key not exists return ""

&#x09;	defaultdict(\[])    : \[]      → If key not exists return \[]

&#x09;	defaultdict(set()) : {}      → If key not exists return {}

&#x09;=================================================================================================

&#x09;**Insert**

&#x09;	d\["a"] = 1                    # single insert

&#x09;	d.update({"b": 2, "c": 3})    # multiple inserts



&#x09;**Update**

&#x09;	d\["a"] = 1                    # single insert

&#x09;	d.update({"b": 2, "c": 3})    # multiple inserts



&#x09;**Delete**

&#x09;	pop(key)  : Remove key and return value			   d = {k:v for k, v in d.items() if k != "a"}

&#x09;	popitem() : Remove and return last inserted key-value pair

&#x09;	clear()   : Remove all items

&#x09;=================================================================================================

&#x09;**Accessing:**



&#x09;	1. d.keys()  : view all keys		for key in d.keys():    print(key)

&#x09;	2. d.values(): view all values  	for value in d.values():  print(value)

&#x09;	3. d.items() : view key-value pairs	for key, value in d.items(): print(f"Key{key} Value: {value}")





&#x09;**Searching:**

&#x09;	print("a" in d)           # Key search

&#x09;	print(2 in d.values())    # Value search

===========================================================================================================================================================











































=====================================================================================================================================================================================

**1. String Methods**

\----------------------------------------------------



├─ ASCII Functions

│     ├─ ord(c)        : ASCII value                    -> ord('a')        # 97

│     └─ chr(n)        : Character from ASCII           -> chr(97)         # 'a'

│

├─ Extraction

│     ├─ strip()       : Remove spaces (both sides)     -> "  hello  ".strip()   # "hello"

│     ├─ lstrip()     : remove left spaces

│     ├─ rstrip()     : remove right spaces

│     └─ split()       : Split string                   -> "hello world".split()  # \['hello','world']

│

├─ Manipulations

│     ├─ replace()     : Replace substring              -> "hello world".replace("world","Python")

│     ├─ lower()       : Convert to lowercase           -> "HELLO".lower()       # "hello"

│     └─ upper()       : Convert to uppercase           -> "hello".upper()       # "HELLO"

│

├─ String Checks

│     ├─ isalpha()     : Only letters                   -> "abc".isalpha()       # True

│     ├─ isdigit()     : Only digits                    -> "123".isdigit()       # True

│     ├─ isnumeric()   : Numeric (incl unicode)         -> "123".isnumeric()     # True

│     ├─ isalnum()     : Letters + digits               -> "abc123".isalnum()    # True

│     ├─ islower()     : Check lowercase                -> "hello".islower()     # True

│     └─ isupper()     : Check uppercase                -> "HELLO".isupper()     # True

│

└─ Pattern Matching

&#x20;     ├─ startswith()  : Starts with prefix             -> "hello".startswith("he")  # True

&#x20;     └─ endswith()    : Ends with suffix               -> "hello".endswith("lo")    # True



**2. Numerical Functions**

\----------------------------------------------------



├─ Absolute \& Rounding

│     ├─ abs(n)         : Absolute value                -> abs(-7)           # 7

│     ├─ round(n,d)     : Round to d decimals           -> round(3.1415,2)   # 3.14

│     ├─ math.ceil(n)   : Round up                      -> math.ceil(5.1)    # 6

│     └─ math.floor(n)  : Round down                    -> math.floor(5.9)   # 5

│

├─ Power \& Logarithmic

│     ├─ math.sqrt(n)   : Square root                   -> math.sqrt(25)     # 5.0

│     ├─ math.pow(n,p)  : Power (float)                 -> math.pow(2,3)     # 8.0

│     ├─ pow(n,p,mod)   : Modular power (IMPORTANT)     -> pow(2,3,5)        # 3

│     ├─ math.exp(n)    : e^n                           -> math.exp(1)

│     ├─ math.log(x)    : Natural log                   -> math.log(10)

│     ├─ math.log2(x)   : Log base 2                    -> math.log2(8)      # 3.0

│     └─ math.log10(x)  : Log base 10                   -> math.log10(100)   # 2.0

│

├─ Aggregate Functions

│     ├─ min(iterable)  : Minimum value                 -> min(\[1,2,3])      # 1

│     ├─ max(iterable)  : Maximum value                 -> max(\[1,2,3])      # 3

│     ├─ len(iterable)  : Count elements                -> len(\[1,2,3])      # 3

│     ├─ sum(iterable)  : Sum                           -> sum(\[1,2,3])      # 6

│     ├─ statistics.mean(data)     : Average             -> mean(\[1,2,3])     # 2

│     ├─ statistics.variance(data) : Variance

│     └─ statistics.stdev(data)    : Standard deviation

│

└─ DSA Important Functions

&#x20;     ├─ divmod(a,b)    : (quotient, remainder)          -> divmod(7,3)       # (2,1)

&#x20;     ├─ math.gcd(a,b)  : Greatest common divisor         -> math.gcd(12,8)    # 4

&#x20;     └─ math.lcm(a,b)  : Least common multiple           -> math.lcm(4,6)     # 12



===========================================================================================================================================================

**Functions :**



&#x09;**# Syntax**

&#x09;def function\_name(var1:int, var2:str, var3:bool, var4:list)->list\[str]/None:

&#x20;   	    # code

&#x20;   	    return values



&#x09;**# Example**

&#x09;def add\_numbers(a: int, b: int) -> int:

&#x20;   	    """Adds two integers and returns the result."""

&#x20;   	    return a + b



&#x20;       **Returning Multiple Values :** When multiple values are separated by commas in the return statement, Python automatically groups them into a tuple.



&#x09;def get\_person\_details():

&#x20;   	    name, age, city = "Alice" , 25, "NYC"

&#x20;   	    return name, age, city				# Python automatically groups them into a tuple.



&#x09;name, age, city = get\_person\_details()			# Tuple Unpacking



&#x09;# =========================================================

&#x09;# Types of Function Arguments

&#x09;# =========================================================



&#x09;**1. Required Arguments** :Must be passed in correct positional order



&#x09;	def add(a, b):

&#x20;   		    return a + b



&#x09;	print(add(3, 4))      # Output: 7



&#x09;**2. Keyword Arguments:** Passed using parameter names



&#x09;	def introduce(name, age):

&#x20;   		     print(f"My name is {name}, and I am {age} years old.")



&#x09;	introduce(age=25, name="Alice")





&#x09;**3.Default Arguments :** Uses default value if argument is not provided in the function call



&#x09;	def greet(name, message="Hello"):

&#x20;   		    print(f"{message}, {name}!")



&#x09;	greet("Alice")

&#x09;	greet("Bob", "Good Morning")





&#x09;**4. Variable-Length Arguments**



&#x09;a. \*args : Multiple positional arguments



&#x09;	def add\_all(\*args):			-- args is a tuple of values

&#x20;   		    return sum(args)



&#x09;	print(add\_all(1, 2, 3, 4))



&#x09;b. \*\*kwargs : Multiple keyword arguments



&#x09;	def print\_info(\*\*kwargs):		-- args is a dictionary value

&#x20;   		    for key, value in kwargs.items():

&#x20;      		    print(f"{key}: {value}")



&#x09;	print\_info(name="Charlie", age=30, city="New York")

==================================================================================================================================



**Lambda**   : A lambda function is an anonymous function used for short single-expression operations.

&#x09;   It can take multiple inputs, contains a single expression, and returns a single output.



&#x09;   **Syntax**  : var = lambda arguments:expression

&#x09;   **Example :** x = lambda a,b:a\*b

&#x09;	     print(x(5, 6)) 			    # Output: 30

==================================================================================================================================



**Generator:**



&#x09;⮚ Generators produce values **on-demand** instead of storing them in memory.

&#x09;⮚ They **remember their state** and continue execution from where they left off.

&#x09;⮚ They are **memory efficient**, especially for large datasets or streams.



&#x09;**EX:**

&#x09;def square\_numbers(n):

&#x20;   	    for i in range(1, n+1):

&#x20;       	yield i \* i  		# Similar to return, but produces values one by one



&#x09;squares = square\_numbers(5)

&#x09;for square in squares:

&#x20;   		print(square)



&#x09;⮚ Usage Scenario  : Ideal for replacing yield with return statements **{large datasets, file streams, or infinite sequences}**

==================================================================================================================================



**Decorator:** It wraps another function to extend or modify its behavior, then returns that wrapped version.



&#x20;  	   A decorator is a function that:

&#x09;	1. Accepts the original function as a parameter

&#x09;	2. Defines an inner wrapper that adds additional logic to original function

&#x09;	3. Calls the original function within the wrapper.

&#x09;	4. Returns the wrapper, allowing the original function to execute with the enhanced behavior when invoked.

&#x20;

&#x09;**Example :**



&#x09;import time



&#x09;def timer\_decorator(original\_function):

&#x20;   	    def wrapper():

&#x20;               start = time.time()

&#x20;       	original\_function()

&#x20;       	end = time.time()

&#x20;       	print("Execution Time:", end - start)

&#x20;   	    return wrapper



&#x09;@timer\_decorator

&#x09;def process():

&#x20;   	    time.sleep(2)

&#x20;   	    print("Processing...")



&#x09;process()

=====================================================================================================================================================================================

