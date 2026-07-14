
<h1 align='center'>Variables & Data Types</h1>

- [Variables](#variables)
    - [Variable Declaration](#variable-declaration)
- [Data Types](#data-types)
    - [Typecasting](#typecasting)

## Variables
Variables are named containers used to store data (like numbers, text, etc.) in a computer memory. It’s a name given to a memory location to store a value.
Naming Convention:
- A variable name can only contain *alphanumeric characters* and *underscore* (`A-Z`, `a-z`, `0-9`, `_`). But it cannot start with a number.
- Variable names cannot contain spaces or special symbols like -, @, #, %, !, etc.
- A variable can have a short name (like x, y, z), but a more descriptive name (firstname, lastname, age, country) is highly recommended.
- Variable names are case-sensitive (firstname, Firstname, FirstName and FIRSTNAME) are different variables.
- Python developers use `snake_case` (eg. capital_city) for variable names.
- A variable name cannot be same as reserved Python keywords (words that are pre-defined in Python).

**List of Python keywords**

![python_keywords](/images/python_keywords.png)

**Examples of variable names**

```python
# ✅ VALID variable names
name            # simple lowercase word
_age            # starts with underscore
student1        # letters + number, but doesn't START with a number
_               # a lone underscore is a valid (if unusual) variable name
_while          # start with '_' to use keywords as variable name
capital_city    # descriptive snake_case name
PI              # all caps often used for constants


# ❌ INVALID variable names
1name            # starts with a number
first-name       # hyphen not allowed (Python reads it as subtraction)
first name       # contains a space
class            # 'class' is a reserved Python keyword
$salary          # special character '$' not allowed
first.name       # dot '.' not allowed (used for object attributes)
```

### Variable Declaration  
When we assign a certain value to a variable, it is called variable declaration. Assigning means storing data in the variable. **Assignment Operator (`=`)** is used to declare a new variable or update an existing one. The equal sign in Python is not equality as in Mathematics.

```python
# Variable Declaration
<variable_name> = <value>

#Examples
age = 45
salary = 2317.5
name = "John"
print(name, age, salary)   # John 45 2317.5

x,y = 1,2
print(x + y)  # 3

a = b = c = 1
print(a, b, c)  # 1 1 1

# To delete the variable
del a
print(a)     # NameError: name 'a' is not defined

# Update an existing variable
age = 17  
print(age)    # 17
age = age + 12 
print(age)    # 29

# Compound assignment operator
age -= 20     # Subtract and Assign (age = age-20)
age *= 5      # Multiply and Assign (age = age*5)
print(age)    # 45

"""
This is called compound assignment operator or shorthand operator. If '=' is used right after arithmetic
operator, arithmetic operation is performed first and then it is assigned to the variable.
"""
```

## Data Types
Data types define the type of value a variable can store. It decides the memory size and operations allowed.

| **Data Type** | **Description**                          | **Example**              |
| -------------- | ----------------------------------------- | ------------------------- |
| **`int`**      | Integer                                   | `10`, `-5`, `0`            |
| **`float`**    | Floating Point (Decimal number)           | `3.14`, `-2.5`             |
| **`complex`**  | Complex number (real + imaginary)         | `2+3j`, `5-4j`             |
| **`bool`**     | Boolean (Truth values, case-sensitive)    | `True`, `False`            |
| **`str`**      | String (Sequence of Unicode characters)   | `"Hello"`, `'Python'`      |
| **`list`**     | Ordered, mutable collection               | `[1, 2, 3]`, `["a", "b"]`  |
| **`tuple`**    | Ordered, immutable collection             | `(1, 2, 3)`                |
| **`set`**      | Unordered collection of unique elements   | `{1, 2, 3}`                |
| **`dict`**     | Key-value pair collection                 | `{"name": "Tom", "age": 21}` |
| **`NoneType`** | Represents the absence of a value         | `None`                     |
 


**`type()` Function:**

- It is used to find the data type of a given variable in python.
- **Data types are classes and variables are instances (objects) of these classes.**

```python
print(type(10))         # <class 'int'>
print(type(3.14))       # <class 'float'>
print(type("Hello"))    # <class 'str'>
print(type("True"))     # <class 'str'>
print(type(True))       # <class 'bool'>
print(type([1, 2]))     # <class 'list'>
print(type((1, 2)))     # <class 'tuple'>
print(type({1, 2}))     # <class 'set'>
print(type({"a": 1}))   # <class 'dict'>
print(type(None))       # <class 'NoneType'>
 
age = 10          # age is an object (instance of class 'int')
print(isinstance(age, int))    # True
 
is_logged_in = False   # is_logged_in is an object (instance of class 'bool')
print(isinstance(is_logged_in, bool))   # True
```

### Typecasting

Typecasting (or Type Conversion) is the process of converting one data type into another. Sometimes programs require changing the type of a variable so that operations can be performed correctly.

```python
a = "10"       # String
b = 5          # Integer
print(a + b)   # TypeError: can only concatenate str (not "int") to str
```

1. **Explicit Typecasting**  
Done manually by the programmer, using functions like `int()`, `float()`, `str()`, `bool()`, `list()`, etc.

```python
# int → float
marks = 10
marks_float = float(marks)  
print(marks_float)   # 10.0

# float → int
price = 3.8
price_int = int(price)  
print(price_int)   # 3

negative_price = -3.8
print(int(negative_price))   # -3  (int() truncates toward zero)
print(round(negative_price)) # -4  (use round() if you actually want rounding)

# int → str
score = 100
score_str = str(score)  
print(score_str)   # "100"

# str → float
pi_str = "3.14"
pi_float = float(pi_str)
print(pi_float)   # 3.14

# str → int
age_str = "50"
age_int = int(age_str)  
print(age_int)   # 50


'''
All int/float values can be converted to str, but a string can only be 
converted to int/float if it is a VALID LITERAL for that target type.
'''
print(int('2.5'))   # ValueError: invalid literal for int()
print(int(float('2.5')))  # 2 (convert to float first)

# str → list
greet = "Hello"
char_list = list(greet)
print(char_list)   # ['H', 'e', 'l', 'l', 'o']

# Can't convert list to str directly
print(str(char_list))   # "['H', 'e', 'l', 'l', 'o']"

# list → set (also removes duplicates)
numbers_with_duplicates = [1, 2, 2, 3, 3, 3]
unique_numbers = set(numbers_with_duplicates)
print(unique_numbers)   # {1, 2, 3}

# str → bool
flag_str = "False"
flag_bool = bool(flag_str)
print(flag_bool)   # True ... Huh? Why?

'''
Only falsy values return False in boolean i.e. 0 , 0.0 , 0j , "" , () , {} , [] , False , None. 
bool(0)   # False
bool('0') # True
'''
```

2. **Implicit Typecasting (Type Promotion)**  
Done automatically by Python to avoid data loss.

```python
# int → float
total = 5 + 2.5     # 5 → 5.0
print(total)        # 7.5
print(type(total))  # <class 'float'>

# bool → int
is_active = True
credits = 5
print(is_active + credits)   # 6 

'''
In Python, True behaves like 1, False behaves like 0
`bool` behaves like `int` in arithmetic because `bool` is actually a subclass of `int` in Python.
'''
print(issubclass(bool, int))   # True
print(isinstance(True, int))   # True
print(True + True)    # 2
```
---
<p align="right">
    <a href="https://github.com/xerohit/Xero-to-Python/blob/main/01_Variables_&_Data_Types/01_Variables_&_Data_Types.md"><i>Variables & Data Types >></i></a>
</p>

