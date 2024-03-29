Que 1.  What is the purpose of Python's OOP?

Ans. 
1) Object-oriented programming is an approach for modeling concrete, real-world things, like cars, as well as relations between things, like companies and employees, students and teachers, and so on. OOP models real-world entities as software objects that have some data associated with them and can perform certain functions.

2) Object could represent a person with properties like a name, age, and address and behaviors such as walking, talking, breathing, and running. Or it could represent an email with properties like a recipient list, subject, and body and behaviors like adding attachments and sending.

Provides a clear program structure and a clean code
Facilitates easy maintenance and modification of existing code
Since the class is sharable, the code can be reused
Since the class is sharable, the code can be reused.
--------------------------------------------------------------------------------------------------
Que 2. Where does an inheritance search look for an attribute?

Ans. 
An inheritance search looks for an attribute first in the instance object, then in the class the instance was created from, then in all higher superclasses, progressing from left to right (by default). The search stops at the first place the attribute is found.
--------------------------------------------------------------------------------------------------
Que 3. How do you distinguish between a class object and an instance object?

Ans. Class object are access through class name. A class can have only one class object. The variable are static which access through class object. 
Instnce object are created by applying infront of class name then we assign this object to reference variable. We can create multiple instance object. If you define init function in our class then it will be called automatically after creating an instance object.
--------------------------------------------------------------------------------------------------
Que 4. What makes the first argument in a class’s method function special?

Ans. It always receives the instance object that is the implied subject of the method call. It’s usually called 'self' by convention.
--------------------------------------------------------------------------------------------------
Que 5. What is the purpose of the init method?

Ans. If the __init__ method is coded or inherited in a class, Python calls it automatically each time an instance of that class is created.
class New():
def __init__(self, arg1, arg2):
self.first_var = arg1
self.second_var = arg2
--------------------------------------------------------------------------------------------------
Que 6.  What is the process for creating a class instance?

Ans. You create a class instance by calling the class name as though it were a function; any arguments passed into the class name show up as arguments two and beyond in the __init__ constructor method.

x = ClassName()
y = AnotherClass(arg1, arg2)
--------------------------------------------------------------------------------------------------
Que 7. What is the process for creating a class?

Ans.
class Monkey:
    Pass
 
# instantiate the class Monkey and assign it to a variable Monkey
Monkey = Monkey()
print(Monkey)

Output:
<__main__.Pokemon object at 0x0000027B56ADD730>

Our Python custom class is empty, it simply returns the address where the object is stored.
--------------------------------------------------------------------------------------------------
Que 8. How would you define the superclasses of a class?

Ans. They are classes which are used to inherit from.
class Siblings(Girl, Boy): ...
In this case Girl and Boy are superclasses for Siblings subclass.
--------------------------------------------------------------------------------------------------
Que 9. What is the relationship between classes and modules?

Ans. 
Modules are collections of methods and constants. They cannot generate instances. Classes may generate instances (objects), and have per-instance state (instance variables).
Modules may be mixed in to classes and other modules. The mixed in module’s constants and methods blend into that class’s own, augmenting the class’s functionality. Classes, however, cannot be mixed in to anything.

A class may inherit from another class, but not from a module.

A module may not inherit from anything.
--------------------------------------------------------------------------------------------------
Que 10. How do you make instances and classes?

Ans. 
To create instances of a class, you call the class using class name and pass in whatever arguments its __init__ method accepts.

"This would create first object of Employee class"
emp1 = Employee("Zara", 2000)
"This would create second object of Employee class"
emp2 = Employee("Manni", 5000)
You access the object's attributes using the dot operator with object. Class variable would be accessed using class name as follows −

emp1.displayEmployee()
emp2.displayEmployee()
print "Total Employee %d" % Employee.empCount
--------------------------------------------------------------------------------------------------
Que 11.  Where and how should be class attributes created?

Ans.
To define a class attribute, you place it outside of the __init__() method. For example, the following defines pi as a class attribute:
class Circle:
    pi = 3.14159

    def __init__(self, radius):
        self.radius = radius

    def area(self):
        return self.pi * self.radius**2

    def circumference(self):
        return 2 * self.pi * self.radius
Code language: Python (python)
After that, you can access the class attribute via instances of the class or via the class name:

object_name.class_attribute
class_name.class_attribute
Code language: Oracle Rules Language (ruleslanguage)
In the area() and circumference() methods, we access the pi class attribute via the self variable.

Outside the Circle class, you can access the pi class attribute via an instance of the Circle class or directly via the Circle class. For example:

c = Circle(10)
print(c.pi)
print(Circle.pi)
Code language: Python (python)
Output:

3.14159
3.14159
--------------------------------------------------------------------------------------------------
Que 12. Where and how are instance attributes created?

Ans. Attributes are just the properties that specify the information associated with each class object.
To add instance attributes to our class, first of all, we create the class itself and give it a name ClassName.

Next, we add some instance attributes which are usually defined inside a method called the constructor method. This method is defined using the keyword def like any function in Python, and this method name should be __init__. The first parameter for this method should be (self) which is a reference to the object itself 
Then we can list all of our instance attributes using the dot operator.

class ClassName:
def __init__(self):
        self.instance_atrr1 = None
        self.instance_atrr2 = None
new_object = ClassName()

In the previous code snippet, we have two instance attributes: instance_atrr1, and instance_atrr2 and their initial value is None.

In the last line, we are creating an object from the class. This is done by writing the class name and then () like if I am calling function. What happens beyond the scene is that the constructor method is auto-called and the object is auto-passed to this method with the name “self”. Inside the constructor, the two attributes will be attached to the object with their initial value.
--------------------------------------------------------------------------------------------------
Que 13. What does the term "self" in a Python class mean?

Ans. self will be a reference for that object and using the dot operator the instance attributes are attached to the object itself.
Within __init__ we pass the first parameters self which represents an object from a class that is currently being defined, and usually, we attach instance attributes to these objects using the dot operator.
--------------------------------------------------------------------------------------------------
Que 14. How does a Python class handle operator overloading?

Ans. Python operators work for built-in classes. But the same operator behaves differently with different types. For example, the + operator will perform arithmetic addition on two numbers, merge two lists, or concatenate two strings.

This feature in Python that allows the same operator to have different meaning according to the context is called operator overloading.
Example:
class Point:
    def __init__(self, x=0, y=0):
        self.x = x
        self.y = y


p1 = Point(1, 2)
p2 = Point(2, 3)
print(p1+p2)

Output:

Traceback (most recent call last):
  File "<string>", line 9, in <module>
    print(p1+p2)
TypeError: unsupported operand type(s) for +: 'Point' and 'Point'

To overload the + operator, we will need to implement __add__() function in the class. With great power comes great responsibility. We can do whatever we like, inside this function. But it is more sensible to return a Point object of the coordinate sum.

class Point:
    def __init__(self, x=0, y=0):
        self.x = x
        self.y = y

    def __str__(self):
        return "({0},{1})".format(self.x, self.y)

    def __add__(self, other):
        x = self.x + other.x
        y = self.y + other.y
        return Point(x, y)
Now let's try the addition operation again:

class Point:
    def __init__(self, x=0, y=0):
        self.x = x
        self.y = y

    def __str__(self):
        return "({0},{1})".format(self.x, self.y)

    def __add__(self, other):
        x = self.x + other.x
        y = self.y + other.y
        return Point(x, y)


p1 = Point(1, 2)
p2 = Point(2, 3)

print(p1+p2)
Run Code
Output

(3,5)
What actually happens is that, when you use p1 + p2, Python calls p1.__add__(p2) which in turn is Point.__add__(p1,p2). After this, the addition operation is carried out the way we specified.

Similarly, we can overload other operators as well.
--------------------------------------------------------------------------------------------------
Que 15. When do you consider allowing operator overloading of your classes?

Ans. Its giving extended meaning beyond their predefined operational meaning. For example operator + is used to add two integers as well as join two strings and merge two lists. It is achievable because ‘+’ operator is overloaded by int class and str class.
Operators in Python work for built-in classes, like int, str, list, etc. But you can extend their operability such that they work on objects of user-defined classes
too.
Operators in Python work for built-in classes, like int, str, list, etc. But you can extend their operability such that they work on objects of user-defined classes too.
--------------------------------------------------------------------------------------------------

Que 16. What is the most popular form of operator overloading?

Ans. A very popular and convenient example is the Addition (+) operator.

Just think how the ‘+’ operator operates on two numbers and the same operator operates on two strings. It performs “Addition” on numbers whereas it performs “Concatenation” on strings.
--------------------------------------------------------------------------------------------------
Que 17. What are the two most important concepts to grasp in order to comprehend Python OOP code?

Ans. Encapsulation, Abstraction, Inheritance, Polymorphism are most important concepts in Python OOP code.
--------------------------------------------------------------------------------------------------
Que 18. Describe three applications for exception processing.

Ans. 
Exceptions occur for numerous reasons, including invalid user input, code errors, device failure, the loss of a network connection, insufficient memory to run an application, a memory conflict with another program, a program attempting to divide by zero or a user attempting to open files that are unavailable.

When an exception occurs, specialized programming language constructs, interrupt hardware mechanisms or operating system interprocess communication facilities handle the exception.

Exception handling differs from error handling in that the former involves conditions an application might catch versus serious problems an application might want to avoid. In contrast, error handling helps maintain the normal flow of software program execution.

1) We can define our own exception types if we would like to have more control over what will happen in specific conditions.

class InvalidStudentAgeException(Exception):
    def __init__(self, student_age, error_message="Student age should be in 2-10 range"):
        self.student_age = student_age
        self.error_message = error_message
        super().__init__(self.error_message)
student_age = int(input("Enter Student age: "))
if not 1 < student_age < 11:
        raise InvalidStudentAgeException(student_age)
Output:
Enter Student age: 54
Traceback (most recent call last):
  File "ErrorsAndExceptions.py", line 68, in <module>
    raise InvalidStudentAgeException(student_age)
__main__.InvalidStudentAgeException: Student age should be in 2-10 range: 54 is not a valid age

Output:
Enter Student age: 56
Traceback (most recent call last):
  File "C:\Users\HP\PycharmProjects\MyProject\Demo2.py", line 8, in <module>
    raise InvalidStudentAgeException(student_age)
__main__.InvalidStudentAgeException: Student age should be in 2-10 range

2)
# Python code to catch an exception and handle it using try and except code blocks

a = ["Python", "Exceptions", "try and except"]
try:
    # looping through the elements of the array a, choosing a range that goes beyond the length of the array
    for i in range(4):
        print("The index and element from the array is", i, a[i])
    # if an error occurs in the try block, then except block will be executed by the Python interpreter
except:
    print("Index out of range") 
--------------------------------------------------------------------------------------------------
    Que 19. What happens if you don't do something extra to treat an exception?

    Ans. 

The reasons for using exceptions in Python as below:

1) Exception handling allows you to separate error-handling code from normal code.
2) An exception is a Python object which represents an error.
3) As with code comments, exceptions helps you to remind yourself of what the program expects.
4) It clarifies the code and enhances readability.
5) Allows you to stimulate consequences as the error-handling takes place at one place and in one manner.
6) An exception is a convenient method for handling error messages.
7) In Python, you can raise an exception in the program by using the raise exception method.
8) Raising an exception helps you to break the current code execution and returns the exception back to expection until it is handled.
9) Processing exceptions for components which can’t handle them directly.
Example:
while True:
    x = int(input("Please enter a number: "))
    print("%s squared is %s" % (x, x**2))
    When you enter a string or any other character that is not a number, like "one", the program will raise a "Value Error" exception:
 This is where handling exceptions comes in. You need to know how to properly handle exceptions, especially in production environments, because if they are not handled your program won't know what to do and will crash.
 
 With exception:
 while True:
    try:
        x = int(input("Please enter a number: "))
        print("%s squared is %s" % (x, x**2))
    except ValueError:
        print("Please enter a valid number!")
Output:
Please enter a number: 4
4 squared is 16
Please enter a number: four
Please enter a valid number
--------------------------------------------------------------------------------------------------
Que 20. What are your options for recovering from an exception in your script?

    Ans:- We will place the code into try and except block.
The try statement works as follows.
First, the try clause (the statement(s) between the try and except keywords) is executed.
If no exception occurs, the except clause is skipped and execution of the try statement is finished.
If an exception occurs during execution of the try clause, the rest of the clause is skipped. Then, if its type matches the exception named after the except keyword, the except clause is executed, and then execution continues after the try/except block. 
--------------------------------------------------------------------------------------------------
Q21. Describe two methods for triggering exceptions in your script.

    Ans:- SystemExit -->	Raised when the sys.exit() function is called
TypeError -->	Raised when two different types are combined
UnboundLocalError -->	Raised when a local variable is referenced before assignment
UnicodeError -->	Raised when a unicode problem occurs
--------------------------------------------------------------------------------------------------
Q22. Identify two methods for specifying actions to be executed at termination time, regardless of whether or not an exception exists.

    Ans:-
1) Try - except Method:
# Python code to catch an exception and handle it using try and except code blocks

a = ["Python", "Exceptions", "try and except"]
try:
    # looping through the elements of the array a, choosing a range that goes beyond the length of the array
    for i in range(4):
        print("The index and element from the array is", i, a[i])
    # if an error occurs in the try block, then except block will be executed by the Python interpreter
except:
    print("Index out of range") 
2) AssertionError Method:
import sys
assert ('linux' in sys.platform), "This code runs on Linux only."

Output:
  Traceback (most recent call last):
  File "<input>", line 2, in <module>
  AssertionError: This code runs on Linux only.
--------------------------------------------------------------------------------------------------

Q23. What is the purpose of the try statement?

    Ans. 
The try statement works as follows.

First, the try clause (the statement(s) between the try and except keywords) is executed.
If no exception occurs, the except clause is skipped and execution of the try statement is finished.
If an exception occurs during execution of the try clause, the rest of the clause is skipped. Then, if its type matches the exception named after the except keyword, the except clause is executed, and then execution continues after the try/except block.
If an exception occurs which does not match the exception named in the except clause, it is passed on to outer try statements; if no handler is found, it is an unhandled exception and execution stops with a message as shown above.

These exceptions can be handled using the try statement:
try:
  print(x)
except:
  print("An exception occurred")
--------------------------------------------------------------------------------------------------
    Q24. What are the two most popular try statement variations?

    Ans:- A try statement, often referred to as a try block, in fact consists of at least two parts: 1 try and except variations.
The code we want to safeguard goes inside the try portion of the block. Afterwards, we define what happens when something goes wrong within the except.

try:
   print(x)
except Exception:
   print("Something broke!")
# Something broke!

In the example above, we use the catch-all value Exception to route any exception to this portion of the block. 

2. Try with multiple except
You can define multiple except blocks within a try, specifying the exact type of exception that should be routed to each. Additionally, you can set the error message to a variable—e is common—so it can be used in your program.
try:
   print(int(x))
except NameError:
  print("The variable is undefined")   
except Exception as e:
   print(e)

3. Try/Except/Else
When attaching an else statement to the end of a try/except, this code will be executed after the try has been completed, but only if no exceptions occur.
while True:
  try:
    num = int(input("Enter an int: "))
  except Exception as e:
    print(e)
  else:
    print("Thank you for the integer!")
    break

4. Try/Except/Finally
When attaching a finally statement to the end of a try/except, this code will be executed after the try has been completed, regardless of exceptions.
count = 0
while True:
  try:
    num = int(input("Enter an int: "))
    break
  except Exception as e:
    print(e)
  finally:
    count += 1
    print("Attempt #:",count)
--------------------------------------------------------------------------------------------------
    Q25. What is the purpose of the raise statement?

    Ans:- Python raise Keyword is used to raise exceptions or errors. The raise keyword raises an error and stops the control flow of the program. It is used to bring up the current exception in an exception handler so that it can be handled further up the call stack.
--------------------------------------------------------------------------------------------------

    Q26. What does the assert statement do, and what other statement is it like?

    Ans. 
The assert keyword is used when debugging code.
The assert keyword lets you test if a condition in your code returns True, if not, the program will raise an AssertionError.
--------------------------------------------------------------------------------------------------
    Q27. What is the purpose of the with/as argument, and what other statement is it like?

    Ans. In Python, with statement is used in exception handling to make the code cleaner and much more readable. It simplifies the management of common resources like file streams. Observe the following code example on how the use of with statement makes code cleaner. 
--------------------------------------------------------------------------------------------------
    Q28.  What are *args, **kwargs?

    Ans. *args specifies the number of non-keyworded arguments that can be passed and the operations that can be performed on the function in Python whereas **kwargs is a variable number of keyworded arguments that can be passed to a function that can perform dictionary operations.
args enable us to pass the variable number of non-keyword arguments to functions, but we cannot use this to pass keyword arguments. Keyword arguments mean that they contain a key-value pair, like a Python dictionary.

**kwargs allows us to pass any number of keyword arguments.

In Python, these keyword arguments are passed to the program as a Python dictionary.

Python will consider any variable name with two asterisks(**) before it as a keyword argument.
--------------------------------------------------------------------------------------------------
    Q29. How can I pass optional or keyword parameters from one function to another?

    Ans. To pass, collect the arguments using the * and ** in the function’s parameter list. Through this, you will get the positional arguments as a tuple and the keyword arguments as a dictionary. Pass these arguments when calling another function by using * and ** −

def f(a, *args, **kwargs):
   ...
   kwargs['width'] = '14.3c'
   ...
   g(a, *args, **kwargs)
--------------------------------------------------------------------------------------------------
    Q 30.  What are Lambda Functions?

    Ans.
A lambda function is an anonymous function (i.e., defined without a name) that can take any number of arguments but, unlike normal functions, evaluates and returns only one expression.

A lambda function in Python has the following syntax:

lambda parameters: expression

The anatomy of a lambda function includes three elements:

The keyword lambda — an analog of def in normal functions
The parameters — support passing positional and keyword
arguments, just like normal functions
The body — the expression for given parameters being evaluated
with the lambda function
Note that, unlike a normal function, we don’t surround the parameters of a lambda function with parentheses. If a lambda function takes two or more parameters, we list them with a comma.

We use a lambda function to evaluate only one short expression (ideally, a single-line) and only once, meaning that we aren’t going to apply this function later. Usually, we pass a lambda function as an argument to a higher-order function (the one that takes in other functions as arguments), such as Python built-in functions like filter(), map(), or reduce().
--------------------------------------------------------------------------------------------------
Que 31. Explain Inheritance in Python with an example?

    Ans:- Inheritance is a powerful feature in object oriented programming.
It refers to defining a new class with little or no modification to an existing class. The new class is called derived (or child) class and the one from which it inherits is called the base (or parent) class.
--------------------------------------------------------------------------------------------------
Que 32. Suppose class C inherits from classes A and B as class C(A,B).Classes A and B both have their own versions of method func(). If we call func() from an object of class C, which version gets invoked?
--------------------------------------------------------------------------------------------------
Que 33. Which methods/functions do we use to determine the type of instance and inheritance?

    Ans:- The isinstance() method checks whether an object is an instance of a class whereas issubclass() method asks whether one class is a subclass of another class (or other classes).
1. isinstance(object, classinfo)
Return true if the object argument is an instance of the classinfo argument, or of a (direct, indirect or virtual) subclass thereof.

2. issubclass(class, classinfo)
Return true if class is a subclass (direct, indirect or virtual) of classinfo. A class is considered a subclass of itself.
--------------------------------------------------------------------------------------------------
Que 34.Explain the use of the 'nonlocal' keyword in Python.

    Ans. 

The nonlocal keyword is used to work with variables inside nested functions, where the variable should not belong to the inner function.
Use the keyword nonlocal to declare that the variable is not local.

def myfunc1():
  x = "John"
  def myfunc2():
    x = "hello"
  myfunc2()
  return x

print(myfunc1())
--------------------------------------------------------------------------------------------------
Que 35. What is the global keyword?

    Ans. 
A global keyword is a keyword that allows a user to modify a variable outside the current scope. It is used to create global variables in Python from a non-global scope, i.e. inside a function. Global keyword is used inside a function only when we want to do assignments or when we want to change a variable. Global is not needed for printing and accessing.
# global variable
a = 15
b = 10
 
# function to perform addition
def add():
    c = a + b
    print(c)
 
 
# calling a function
add()
--------------------------------------------------------------------------------------------------
