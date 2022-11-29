### Assignment Part-1
Q1. Why do we call Python as a general purpose and high-level programming language?

Ans:- Python is a high-level programming language that is known for its ease of readability.When we write programs in python, we do not need to remember the system architecture, nor do we need to manage the memory.
********************************************************************************************************************
Q2. Why is Python called a dynamically typed language?

Ans:- Python is a dynamically-typed language. That means the type (for example- int, double, long, etc.) for a variable is decided at run time not in advance because of this feature we don’t need to specify the type of variable.
********************************************************************************************************************
Q3. List some pros and cons of Python programming language?
Ans:- Pros of Python:-
1. Python is easy to learn and read
2. Python has a vast collection of libraries
3. Python is free, open-source, and has a vibrant community
4. Python is a portable programming language
5. Python is an interpreted language

The cons of python programming language
1. Python has speed limitations
2. Python is not so strong with mobile computing
- Python was built to be used in the server-side programming, so the client-side is rarely used — and that’s if it is ever used at all. Because of this, Python does not do well with the making of mobile applications.
3. Python can have runtime errors
4. Python consumes a lot of memory space
5. Python is not easy to test
********************************************************************************************************************
Q4. In what all domains can we use Python?
Ans:-
1 Machine learning / Artificial intelligence
2 Desktop GUI
3 Data analytics and data visualization 
4 Web development
5 Game development
6 Mobile app development
7 Embedded systems
********************************************************************************************************************
Q5. What are variable and how can we declare them?
Ans:- Variable is a name given to memory location. Variables are containers for storing data values.
# Single variable declaration
a=10
# Multiple variable declaration and initialization
a=10
b=10
c=10
# instead of writing multiple statement you can write above 3 statement in single statement as below.
a=b=c=10
# Multiple variable declaration and initialization
a=10
b=10.23
c="Ravan"
d='Ram'
# instead of writing multiple statement you can write above 3 statement in single statement as below.
a, b, c, d = 10, 10.23, "Ravan", 'Ram'
********************************************************************************************************************
Q6. How can we take an input from the user in Python?
Ans:- input( ) – This function is used to accept input from keyboard. 
This function will stop the program flow until the user gives an input and end the input with the return key. 
Whatever user gives as input, input function convert it into a string. If user enters an integer value still input() function convert it into a string. 
So if you need an integer you have to use type conversion. 
Syntax:- input([prompt])
prompt is a string or message, representing a default message before input. It is optional
Ex:- 
name = input( )
name = input(“Your Name: ”)
mobile = input(“Enter Your Mobile Number: ”)

Whatever user gives as input, input function convert it into a string. If user enters an integer value still input() function convert it into a string. 
So if you need an integer you have to use type conversion. 
Ex:- 
mobile = input(“Enter Your Mobile Number: ”)
mb = int(mobile)
mobile = int ( input (“Enter Your Mobile Number: ”) )
price = float ( input (“Total Price: ”) )
mobile = complex ( input (“Enter Complex Number: ”) )
********************************************************************************************************************
Q7. What is the default datatype of the value that has been taken as an input using input() function?
:- In python, STRING is the default datatype of the value that has been taken as an input using input() function.
********************************************************************************************************************
Q8. What is type casting?
Ans:-
Converting one data type into another data type is called type casting.
Type of Type Conversion:-
1. Implicit Type Conversion 
2. Explicit Type Conversion

1. Implicit Type Conversion 
In the Implicit type conversion, python automatically converts one data type into another data type.
Ex:- 
a = 5
b = 2
value = a / b
print(value)
print(type(value))

2. Explicit Type Conversion
In the Cast/Explicit Type Conversion, Programmer converts one data type into another data type.
int (n)
float (n)
complex (n) 
complex (x, y) where x is real part and y is imaginary part
str (n)
list(n)
tuple(n)
bin (n)
oct (n)
hex (n )

********************************************************************************************************************
Q9. Can we take more than one input from the user using single input() function? If yes, how? If no, why?
********************************************************************************************************************
Q10. What are keywords?
Ans:- Keywords are reserved words in python. Each keywords have their own specific meaning. All the keywords except True , False and None are in lowercase and they must be written as they are.
********************************************************************************************************************
Q11. Can we use keywords as a variable? Support your answer with reason.
Ans:- We can't use keywords as a variable or function name in python. Keywords are used to define structure and syntax of python.
********************************************************************************************************************
Q12. What is indentation? What's the use of indentaion in Python?
Ans:- Indentation refers to the spaces at the beginning of a code line. Python uses indentation to indicate a block of code.
********************************************************************************************************************
Q13. How can we throw some output in Python?
Ans:-  We can display output on the screen using the print statement.The message can be a string, or any other object, the object will be converted into a string before written to the screen.
Basic syntax of print statement.
print(object(s), sep=separator, end=end, file=file, flush=flush)

sep - Separate the objects by given character. Character can be any string. Default is ‘ ’ or can write none.
end – It indicates ending character for the line. Default is ‘\n’ or can write none.
file - An object with a write method. Default is sys.stdout or can write none. sys.stdout means whatever the output will print on python console. If we change the value of file parameter then it will print all the output in that file.
Example:
newfile=open('abc.txt','w')   # w means write operation. It first search abc.txt. If it is present then clear the content of that file and if file is not created then it will create the file
print("Hi, file parameter",file=newfile)
newfile.close()

flush - A Boolean, specifying if the output is flushed (True) or buffered (False). Default is False
Ex:-
Buffered  output means that the computer spools the output somewhere in memory until a certain ammount ha accumulated. The it write the entire block at once. This is more efficient than using unbufferd output which writes the output as soon as you request for it to be written.
The downside is that your program will run a little slower depending on how much output you are writting. If they are short programs which dont do too much output, you're unlikely to notice a differnece.

Ex.
print ( ) – This function is used to display a blank line.
********************************************************************************************************************
Q14. What are operators in Python?
Ans:- List of various operators are used in python are:-
1 Arithmetic Operators:-
Arithmetic operators are used to performing mathematical operations like addition, subtraction, multiplication, and division.
Arithmetic operators are +,-,*, /, //, %

2. Comparison Operators
Comparison of Relational operators compares the values. It either returns True or False according to the condition.
Comparison Operators are >,<,==,!=, >=,<=, is , is not.

3. Logical Operators
Logical operators perform Logical AND, Logical OR, and Logical NOT operations. It is used to combine conditional statements.
Logical Operators are and, or ,not.

4. Bitwise Operators
Bitwise operators act on bits and perform the bit-by-bit operations. These are used to operate on binary numbers.
Bitwise Operators are & (bitwise and), | (bitwise or), ~ (bitwise not), ^ (bitwise xor), >> (bitwise right shift), << (bitwise left shift).

5. Assignment Operators 
Assignment operators are used to assign values to the variables.

6. Identity Operators
is and is not are the identity operators both are used to check if two values are located on the same part of the memory. Two variables that are equal do not imply that they are identical. 
is          True if the operands are identical 
is not      True if the operands are not identical 

7. Membership Operators
in and not in are the membership operators; used to test whether a value or variable is in a sequence.
in            True if value is found in the sequence
not in        True if value is not found in the sequence
********************************************************************************************************************
Q15. What is difference between / and // operators?
Ans: '/' is used for the normal division of two numbers.
'//' is used to obtain the smallest integer nearest to the quotient obtained by dividing two numbers.
If the quotient obtained by dividing two numbers is not an integer, then operators '/' and '//' will return different answers.
For eaxmple:-
x = 15
y = 3
print(x / y)   #This prints output as 5
print(x // y)  #This prints output as 5
a = 19
b = 4
print(a // b)  #This prints output as 4
print(a / b)  #This prints output as 4.75
********************************************************************************************************************
Q16. Write a code that gives following as an output.
```
iNeuroniNeuroniNeuroniNeuron
```
Ans:- print("iNeuroniNeuroniNeuroniNeuron")
********************************************************************************************************************
Q17. Write a code to take a number as an input from the user and check if the number is odd or even.
Ans: -
n= int(input('Enter your number'))
if n%2==0:
    print("Number is even")
else:
    print("Number is odd")
********************************************************************************************************************
Q18. What are boolean operator?
Ans:- There are 3 boolean operators in python. Boolean operators are also known as logical operator. Boolean operator are as follows:
1. or - It returns true if any one operand or expression is true otherwise it returns false.
2. and - All expression should be true else it will return false.
3. not - It will return negation of current expression. That means it will returns false for true expression and returns true for false expression.
********************************************************************************************************************
Q19. What will the output of the following?
```
1 or 0

0 and 0

True and False and True

1 or 0 or 0
```
Ans:- 
1 or 0
output :- 1

0 and 0
output :- 0

True and False and True
output :- False 

1 or 0 or 0
output :- 1
********************************************************************************************************************
Q20. What are conditional statements in Python?
Ans:- The conditional statements are as below:
1. if statement
2. if else statement
3. if elif else statement
4. switch statement
********************************************************************************************************************
Q21. What is use of 'if', 'elif' and 'else' keywords?
Ans:- 'if', 'elif' and 'else' are the conditional statement which is used to specify condition and decide the flow of statement and generate certain result according to the user need.
********************************************************************************************************************
Q22. Write a code to take the age of person as an input and if age >= 18 display "I can vote". If age is < 18 display "I can't vote".
Ans:-
age = int(input('Enter your age:'))
if age >= 18:
    print("I can vote")
else:
    print("I can't vote")
********************************************************************************************************************
Q23. Write a code that displays the sum of all the even numbers from the given list.
```
numbers = [12, 75, 150, 180, 145, 525, 50]
```
Ans:-
numbers = [12, 75, 150, 180, 145, 525, 50]
x= len(numbers)
sum=0
for i in range(x):
    if numbers[i]%2==0:
        sum=sum+numbers[i]
print("Sum of even number: ",sum)
********************************************************************************************************************

Q24. Write a code to take 3 numbers as an input from the user and display the greatest no as output.
Ans:- 
num1,num2,num3= input('Enter three number:').split()
if num1 > num2 and num1 > num3:
    print(num1,"is the greatest number")
elif num2 > num1 and num2 > num3:
    print(num2,"is the greatest number")
else:
    print(num3,"is the greatest number")
********************************************************************************************************************
Q25. Write a program to display only those numbers from a list that satisfy the following conditions

- The number must be divisible by five

- If the number is greater than 150, then skip it and move to the next number

- If the number is greater than 500, then stop the loop
```
numbers = [12, 75, 150, 180, 145, 525, 50]
```
Ans:-
numbers = [12, 75, 150, 180, 145, 525, 50]
x= len(numbers)
for i in range(x):
    if numbers[i]>500:
        break
    elif numbers[i]<150 and numbers[i] % 5==0:
        print(numbers[i])
    else:
        continue
********************************************************************************************************************
