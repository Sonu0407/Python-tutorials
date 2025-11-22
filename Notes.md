range (start, stop, step)
loop 
1. for loop
2. while loop
Advanced datatypes
1. list []  .index for print the indexs
2. dict {key: value}
3. set does not allow duplicates {}
4. tuples ()
5. list comprehension
6. strings ' ' " " ''' '''




functions 
a  function is a reusable block of code that performs a specific task.
def keyword

types of function
1. Built in function
2. User defined function
3. lambda function
4. Recurssive function

def keyword

basic structure of function

def function_name(parameters):
    #block of code
    return result

function_name(parameters) # function calling

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

to create class in python class is the keyword

syntax: class class_name :

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
types of    
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

custom exception error 

* reverse is used only for list method

# Restart

Python virtual machine PVM

1. code loop to iterate byte code
2. Run time engine as car engine
3. also know as python interpreter (line by line)

Byte code is Not machine code

1. byte code is for python specific interpretation

h1 = [1, 2, 3]
h2 = h1
h2 = [1, 2, 3] # changed to another object and reference
print(h1)
[1, 2, 3]
print(h2)
[1, 2, 3]
h1[0] = 55
print(h1)
[55, 2, 3]
print(h2)
[1, 2, 3]

h1 = [1, 2, 3]
h2 = h1 # same refrence for both
print(h1)
[1, 2, 3]
print(h2)
[1, 2, 3]
h1[0] = 55
print(h1)
[55, 2, 3]
print(h2)
[55, 2, 3]

h1 = [1, 2, 3]
h2 = h1[:] # list slicing make a copy of it
print(h1)
[1, 2, 3]
print(h2)
[1, 2, 3]
h1[0] = 55
print(h1)
[55, 2, 3]
print(h2)
[1, 2, 3]

== checks for values
is keyword checks for memory reference 

import math
math.floor(3.5) # it goes towords bottom
3
math.floor(-3.5)
-4
math.floor(3.6)
3
math.trunc(2.8) # it goes towords 0
2
math.trunc(-2.8)
-2

Sets => {}
operations
1. & => intersection
2. |  => union
3. -  => differences
4. issuperset() => superset # A set A is a superset of set B if all elements of B are also present in A.

ex: 
# Example 1: A is a superset of B
A = {1, 2, 3, 4, 5}
B = {2, 3}
print(A.issuperset(B))  # Output: True

# Example 2: A is not a superset of B
C = {6, 7}
print(A.issuperset(C))  # Output: False

print(type({}))
dict

setone = {1, 2, 3, 4}
>>> setone
{1, 2, 3, 4}
>>> type(setone)
<class 'set'>
>>> setone - {1, 2, 3, 4}
set() # empty parentises is dict 

True + 4
output = 5

slice has three argument [start: end : hop]

method in strings
1. lower()
2. upper()
3. strip() removes extra spaces from begining and end
4. replace() ex: replace("sun", "moon") sun replaces to moon
5. split() to convert string into list ex: split(", ") based on comma ,
6. find()
7. count()
8. join() look for ex down
9. len()

Questioning with strings
print("sonu" in word) -> true or false

r for rw string ex: "home/nend" o/p home
end
r"home/nend" o/p home/nend prints as it is

I ordered {} cups of coffee
here {} is place holders with holds variables

how to convert list to string 
my_list = ["car", "bike", "plane"]
print(" ".join(my_list))

list

methods in list
1. slicing same as string
2. append()
3. pop() last value remove
4. remove() specific value removing purpose
5. insert() two arguments first position and "value"
6. copy() gives a different variable a copy of it ex: car_copy = car.copy()
                                                    here it is created another reference called car_copy and gave car properties
7. list comprehension first what ouput you want and loop or condition
    ex: sqaured_num = [x**2 for x in range(10)]
        print(sqaured_num)
        o/p [0, 1, 4, 9, 16, 25, 36, 49, 64, 81]

end in print is default set to /n if we give end="-" we get o/p black-green-red-blue

Dictionaries
EX:
car_types = {"Toyota": "supra", "bmw": "Rolls royces", "Porsche": "S911"}

Access
1. car_types["Toyota"]
2. car_types.get("bmw")

Change
1. car_types["Porsche"] = "GTRS"

To print key and values using forloop

for car in car_types:
    print(car, car_types[chai])

# in forloop we can add variables also in dict
ex:
for key, value in car_types.items():
    print(key, value)

can ask questions as well
if "bmw" in car_types:
    print("I have BMW cars")

len() can be used as well  

deleting
1. car_types.pop("Porsche") # provide key
2. car_types.popitem() #deletes last item in dict
3. del car_types["Porsche"]

copy
car_types_copy = chai_types.copy()

can contain nested dict means dict inside dict.....

readline() -> raw function is __next__()

*args is used to take n number of parameters in function

**kwargs is used to take n number positional arguments in the function

yield keyword saves the variable doesn't again in the loop

enumerate: when we use it we can  covert into list[] and giving index to it
ex
x = ('car','bike','bus','truck')
y = enumerate(x)
list(y)
o/p = [(0,'car'),(1,'bike'),(2,'bus'),(3,'truck')]

file = open('test.py', 'w') # this create a file in explorer write mode
