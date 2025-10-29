functions 
a  function is a reusable block of code that performs a specific task.
def keyword

def keyword

basic structure of function

def function_name(parameters):
    #block of code
    return result

Types of arguments

positional arguments
it is passed in the exact order as defined in the function

Keyword arguments
arguments passed with parameter names, order doesn't matter.

Variable length arguments
Accept any number of positional argument

Variable keyword arguments
Accept any number of keyword argument

Lambda 

Lambda functions are anonymous, single-line functions for simple operations
Lambda are not reuseable function but we can convert in reuseable one

syntax

lambda arguments : expression

lambda is the keyword

Ex: res = (lambda a,b: a+b)(65,64)
    print(res)

simple write whole function in single line

Recursive function
a function that calls itself 

Modules 

1. code reuseability
2. code maintaines
3. easy to debug

To import

1. module.variable name ()
2. module.funtion name ()
3. from module variable_name or function()

Practice program
String slicing can also work like this 
s1 = 'Abc' # AzbycX
s2 = 'Xyz'
s3 = s1[0] + s2[-1] + s1[1] + s2[1] + s1[-1] + s2[0]
print(s3)


append.left to add elements from the left side

append.extend 
                    can add both sides of lists
append.extendleft

dictionary is an unordered collection of data and as well as sets

object is a real world entity 

orientation means perception

class means blueprint 

to create class in python is class is the keyword

syntax: class classname :

self is just a variable name

type of variables

1. local variable
    The variable that defined inside the function but cannot access the outside of it
2. global variable
    The variable that is defined outside the function that can be accessble any where  
3. static variable

4. instance variable
5. class variable

changing local variable to gobal variable? *IMP
you gobal keyword for it inside the funtion

if child class is inherited to parent class then we should create object for child class
because it is a adavantage and it has access to both classes.

polymorphism

poly means many 
morphism means forms

method overloading -> overriding methods inside the class
creating many methods with same name in class
it excutes the latest method in the class before that all are ignored (overlapping)

method overriding -> overriding classes
creating many methods with same name in class
changing the implementation of methods in the child class

Encapsulation
1. hiding the important data
2. help of access modifiers 
    a. public    -> a = 10      -> access everywhere
    b. protected -> _a = 10     -> access within the class and current module
    c. private   -> __a = 10    -> access only within the class

Abstraction
1. hiding the internal functionilities
2. all the abstract must be overriding
3. @abstractmethod
4. import abstractmethod 

PDBC Python Database Connection
Databases 
1. RDBMS

Python default database 
1. sqlite3

* CRUD operations in every database you do
1. C -> create
2. R -> read
3. U -> update
4. D -> Delete

to connect sql in python 
1. install this -> pip install mysql-connector-python

Exception handling 
termination types:
1. gracefull termination    -> without error 
2. non gracefull termination-> with error 
    a. compile time / syntax error 
    ex: a = 10
        if a >= 10
        print(hello)
    b. runtime / exception error 
    ex: a = 10
        b = 0
        print(a/b)
        output it cant divide with zero number

standard way to 
try:
    # Code that may raise an exception
    risky_operation()
except ExceptionType:
    # Code to handle the exception
    print("An error occurred!")
else:
    # Code to execute if no exception occurs
    print("Operation successful!")
finally:
    # Code that always executes
    print("Cleanup actions.")

Exception types 
1. ZeroDivisionError-> any number divide by zero
2. ValueError       -> in place int giving string
3. FileNotFoundError-> if we try to access non existing file



For reading a text file (it is just like for loop*)
# Open the file in read mode ('r')
with open('filename.txt', 'r') as file:
    content = file.read()  # Reads the entire file
    print(content)

