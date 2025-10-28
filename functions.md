# Python Functions 📚

## Table of Contents
1. [Introduction to Functions](#introduction-to-functions)
2. [User Defined Functions (UDFs)](#user-defined-functions-udfs)
3. [Function Arguments](#function-arguments)
4. [Lambda Functions](#lambda-functions)
5. [Recursive Functions](#recursive-functions)
6. [Practice Examples](#practice-examples)

---

## Introduction to Functions

A **function** is a reusable block of code that performs a specific task. Functions help us:
- 📦 Organize code into manageable pieces
- 🔄 Reuse code without repetition
- 🐛 Debug and maintain code more easily
- 📊 Make programs more modular

### Basic Function Structure

```python
def function_name(parameters):
    """Function documentation"""
    # Function body
    # Code to execute
    return result  # Optional
```

---

## User Defined Functions (UDFs)

These are functions created by programmers to solve specific problems.

### Example 1: Basic Calculator Function

```python
def calculator(a, b, c):
    """
    A simple calculator that performs basic operations
    Parameters: a, b, c - numbers for calculations
    """
    add = a + b
    print(f"Addition: {a} + {b} = {add}")
    
    sub = a - b
    print(f"Subtraction: {a} - {b} = {sub}")
    
    div = a / c
    print(f"Division: {a} / {c} = {div}")

# Calling the function with different values
calculator(10, 20, 30)
print('*' * 10)
calculator(100, 200, 300)
print('*' * 10)
calculator(65, 947, 684)
```

**Output:**
```
Addition: 10 + 20 = 30
Subtraction: 10 - 20 = -10
Division: 10 / 30 = 0.333...
**********
Addition: 100 + 200 = 300
Subtraction: 100 - 200 = -100
Division: 100 / 300 = 0.333...
**********
Addition: 65 + 947 = 1012
Subtraction: 65 - 947 = -882
Division: 65 / 684 = 0.095...
```

### 📊 Function Flow Visualization

```
Input (a, b, c) → [Function Processing] → Output (Results)
     ↓                    ↓                     ↓
  (10, 20, 30)    Add, Subtract, Divide    30, -10, 0.33
```

---

## Function Arguments

### 1. Positional Arguments ➡️

Arguments passed in the exact order as defined in the function.

```python
def exp(a, b):
    """Calculate a raised to power b"""
    result = a ** b
    return result

# Order matters!
print(exp(10, 2))  # 10^2 = 100
print(exp(2, 10))  # 2^10 = 1024
```

**Key Point:** The position of arguments changes the result!

### 2. Keyword Arguments 🔑

Arguments passed with parameter names, order doesn't matter.

```python
def exp(a, b):
    """Calculate a raised to power b using keyword arguments"""
    result = a ** b
    return result

# Order doesn't matter with keywords!
print(exp(a=10, b=2))  # 10^2 = 100
print(exp(b=2, a=10))  # Still 10^2 = 100
```

### Comparison Table

| Type | Example | Order Matters? | Use Case |
|------|---------|---------------|----------|
| Positional | `exp(10, 2)` | ✅ Yes | When order is intuitive |
| Keyword | `exp(a=10, b=2)` | ❌ No | When clarity is needed |

### 3. Variable Length Arguments (*args) 📦

Accept any number of positional arguments.

```python
def addnum(*a):
    """Add any number of arguments"""
    print(f"Arguments received: {a}")
    print(f"Sum: {sum(a)}")

# Examples with different numbers of arguments
addnum(10, 20)        # Works with 2 args
addnum(10, 20, 30)    # Works with 3 args
addnum(10, 20, 30, 40)  # Works with 4 args
```

### 4. Variable Length Keyword Arguments (**kwargs) 🗂️

Accept any number of keyword arguments.

```python
def data(**a):
    """Accept any keyword arguments"""
    print(f"Data received: {a}")

# Examples
data()                    # Empty dictionary
data(a=10, b=20)         # {'a': 10, 'b': 20}
data(a=10, b=20, c=30)   # {'a': 10, 'b': 20, 'c': 30}
```

---
## Types of Functions

1. User Defined Functions (UDFs)
2. Builtin Functions 
3. Lambda Functions / Lambda Expressions
4. Recurssive Functions

---

## Lambda Functions

Lambda functions are **anonymous, single-line functions** for simple operations.

### Syntax
```python
lambda arguments: expression
```

### Traditional Function vs Lambda

#### Traditional Function:
```python
def calc(a, b):
    c = a + b
    return c

print(calc(65, 64))  # 129
```

#### Lambda Equivalent:
```python
res = (lambda a, b: a + b)(65, 64)
print(res)  # 129
```

### Lambda Examples

#### 1. Temperature Converter 🌡️
```python
# Convert Celsius to Fahrenheit
celsius_to_fahrenheit = lambda celsius: (celsius * (9/5)) + 32

print(celsius_to_fahrenheit(69))  # 156.2°F
print(celsius_to_fahrenheit(70))  # 158.0°F
```

#### 2. Find Largest Number 🔍
```python
# Find the larger of two numbers
largest = (lambda x, y: x if x > y else y)(9864, 6843)
print(largest)  # 9864
```

#### 3. Conditional Lambda
```python
# Print based on comparison
(lambda a, b: print(f"{a} is greater") if a > b else print(f"{b} is greater"))(10, 2)
```

---

## Recursive Functions

A function that **calls itself** to solve smaller instances of the same problem.

### Factorial Example - Two Approaches

#### Approach 1: Without Recursion (Iterative)
```python
def factorial_iterative(num):
    """Calculate factorial using iteration"""
    result = 1
    while num >= 1:
        result = result * num
        num = num - 1
    return result

num = 5
res = factorial_iterative(num)
print(f'The factorial of {num} is {res}')  # 120
```

#### Approach 2: With Recursion
```python
def factorial_recursive(n):
    """Calculate factorial using recursion"""
    if n == 0:
        result = 1
    else:
        result = n * factorial_recursive(n - 1)
    return result

n = 5
res = factorial_recursive(n)
print(f'The factorial of {n} is {res}')  # 120
```

### 📈 Recursion Visualization for factorial(5)

```
factorial(5)
    ├── 5 * factorial(4)
    │   ├── 4 * factorial(3)
    │   │   ├── 3 * factorial(2)
    │   │   │   ├── 2 * factorial(1)
    │   │   │   │   ├── 1 * factorial(0)
    │   │   │   │   │   └── 1
    │   │   │   │   └── 1 * 1 = 1
    │   │   │   └── 2 * 1 = 2
    │   │   └── 3 * 2 = 6
    │   └── 4 * 6 = 24
    └── 5 * 24 = 120
```

### Pattern Printing with Recursion
```python
def print_pattern(n):
    """Print star pattern using recursion"""
    if n > 1:
        print_pattern(n - 1)
    
    for i in range(n):
        print(" * ", end="")
    print()

print_pattern(5)
```

**Output:**
```
 * 
 *  * 
 *  *  * 
 *  *  *  * 
 *  *  *  *  * 
```

---

## Practice Examples

### Example 1: Welcome Message Function
```python
def welcome(name):
    """Print personalized welcome message"""
    print(f"Hi {name}, welcome to Python Programming!")

welcome("Suhas")
welcome("Sandesh")
```

### Example 2: Conditional Greetings
```python
def greetings(name):
    """Print different greetings based on name"""
    if name.lower() == "kumar":
        print("Hi, Good morning! ☀️")
    elif name.lower() == "suhas":
        print("Hi, Good afternoon! 🌤️")
    elif name.lower() == "kiran":
        print("Hi, Good night! 🌙")
    else:
        print(f"Hi {name}, welcome to Python class! 👋")

# Test the function
greetings("Kumar")
greetings("Suhas")
greetings("Kiran")
greetings("Dinesh")
```

### Example 3: Palindrome Checker
```python
def palindrome_check(word):
    """Check if a word is palindrome"""
    if word.lower() == word.lower()[::-1]:
        print(f"'{word}' is a palindrome! ✅")
    else:
        print(f"'{word}' is not a palindrome. ❌")

# Test cases
palindrome_check("MALAYALAM")  # Palindrome ✅
palindrome_check("python")     # Not palindrome ❌
palindrome_check("MOM")        # Palindrome ✅
```

---

## 📝 Summary

| Concept | Key Points | When to Use |
|---------|------------|-------------|
| **Functions** | Reusable code blocks | When you need to repeat code |
| **Positional Args** | Order matters | Simple, ordered parameters |
| **Keyword Args** | Order doesn't matter | Complex functions with many parameters |
| **Variable Args** | Accept any number | When parameter count varies |
| **Lambda** | One-line functions | Simple operations |
| **Recursion** | Function calls itself | Tree-like problems, mathematical sequences |

## 🎯 Quick Tips for Students

1. **Start Simple**: Begin with basic functions before moving to complex ones
2. **Practice Return vs Print**: Understand when to return values vs printing them
3. **Use Descriptive Names**: Name functions based on what they do
4. **Document Your Functions**: Always add comments explaining the purpose
5. **Test with Different Inputs**: Try edge cases and various input types
6. **Master One Concept at a Time**: Don't rush through all types of arguments

## 🚀 Challenge Yourself

Try creating functions that:
- Calculate compound interest
- Check if a number is prime
- Generate Fibonacci sequence
- Convert between different units
- Validate email addresses

---

*Happy Coding! Remember: The best way to learn functions is by writing lots of them!* 🐍✨