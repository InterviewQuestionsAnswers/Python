# Python Key Points

## Data Type
- A **data type** is classification that specifies which type of value a variable can hold, how it's stored in memory, and what operations can be performed on it.  
- **Python Data Types:**
  - **Numeric Types**  
    - **int** → Whole numbers → `x = 5`  
    - **float** → Decimal numbers → `y = 3.14`  
    - **complex** → Complex numbers → `z = 2 + 3j`  
  - **Sequence Types**  
    - **str** → Text → `text = "Hello"`  
    - **list** → Ordered, mutable → `my_list = [1, 2, 3]`  
    - **tuple** → Ordered, immutable → `my_tuple = (1, 2, 3)`  
  - **Mapping Type**  
    - **dict** → Key-value pairs → `my_dict = {'name': 'John', 'age': 30}`  
  - **Set Types**  
    - **set** → Unique, unordered → `my_set = {1, 2, 3}`  
    - **frozenset** → Immutable set → `my_frozenset = frozenset([1, 2, 3])`  
  - **Boolean Type**  
    - **bool** → `True` or `False` → `is_valid = True`  
  - **Binary Types**  
    - **bytes** → Immutable byte sequence → `data = b'Hello'`  
    - **bytearray** → Mutable byte sequence → `data = bytearray(b'Hello')`  
  - **None Type**  
    - **NoneType** → Represents `None` (no value) → `x = None`  
  - **Custom Data Types**  
    - Created using **classes & objects**  
        ```python
        class Person:  
            def __init__(self, name):  
                self.name = name  

        p = Person("John")  
        ```
### Strings in Python
- A **string** is a sequence of characters enclosed in `' '`, `" "`, `''' '''`, or `""" """`.  
- **Immutable**: Cannot be changed after creation.
- **String Operations:**  
    - **Indexing:** `my_string[0]` → First character  
    - **Concatenation:** `"Hello" + " World"` → `"Hello World"`  
    - **Slicing:** `my_string[2:5]` → Extracts characters from index `2` to `4`  
    - **Escape Sequences:** `\n` (new line), `\t` (tab)  
- **String Formatting:**  
  ```python
  name = "Alice"
  age = 25
  print(f"My name is {name} and I am {age} years old.")  # f-string
  print("My name is {} and I am {} years old.".format(name, age))  # str.format()
  print("My name is %s and I am %d years old." % (name, age))  # %-formatting
  ```
- **Common String Methods:**  
  ```python
  s = " Hello, World! "
  print(s.upper())      # " HELLO, WORLD! "
  print(s.lower())      # " hello, world! "
  print(s.strip())      # "Hello, World!" (removes spaces)
  print(s.replace("Hello", "Hi"))  # " Hi, World! "
  print(s.split(","))   # [' Hello', ' World! ']
  ```
### Numeric Data Types (int, float)
- Python supports two primary numeric data types:
  - **int** → Whole numbers → `x = 10`  
  - **float** → Decimal numbers → `y = 3.14`  
- **Arithmetic Operations:**  
    ```python
    a, b = 10, 3
    print(a + b)  # Addition → 13
    print(a - b)  # Subtraction → 7
    print(a * b)  # Multiplication → 30
    print(a / b)  # Division → 3.3333
    print(a // b) # Floor division → 3
    print(a % b)  # Modulus → 1
    print(a ** b) # Exponentiation → 1000
    ```
- **Built-in Numeric Functions:**  
    ```python
    print(abs(-10))   # 10
    print(round(3.75))  # 4
    import math
    print(math.sqrt(16))  # 4.0
    print(math.pi)  # 3.141592653589793
    ```
### Regular Expressions (Regex)
- **Regex**
  - **Regular Expressions (regex)** are used for **pattern matching and text processing**.  
  - The `re` module in Python provides functions for working with regex.  
- **`re` Module Functions & Examples**
  - **`re.match()`** → Checks if the pattern matches at the start of the string
  - **`re.search()`** → Finds a match anywhere in the string
  - **`re.findall()`** → Returns all occurrences of a pattern in a list
  - **`re.split()`** → Splits a string based on a pattern
  - **`re.sub()`** → Replaces matches with new text 
    ```python
    import re

    text = "I am learning Python for DevOps"

    # Search for a pattern
    pattern = r"Python"
    search = re.search(pattern, text)
    if search:
        print("Pattern Found:", search.group())  # "Python"

    # Match (only at the beginning of the string)
    match = re.match(pattern, text)
    print("Match Found:", match.group() if match else "Match not Found")

    # Replace text using regex
    new_text = re.sub(r"DevOps", "Cloud Computing", text)
    print("Modified Text:", new_text)  # "I am learning Python for Cloud Computing"

    # Split using regex
    split_result = re.split(r",", "Git,Jenkins,Terraform,Docker,Kubernetes,Python")
    print(split_result)  # ['Git', 'Jenkins', 'Terraform', 'Docker', 'Kubernetes', 'Python']
    ```

## Python Keywords
- Python **keywords** are reserved words with predefined meanings that **cannot** be used as variable names. They define the **structure and logic** of a Python program.
  - **Logical Operators**
    - `and` → Returns `True` only if both conditions are `True`.
    - `or` → Returns `True` if at least one condition is `True`.
    - `not` → Negates the condition (`True` → `False` and vice versa).
  - **Conditional Statements**
    - `if` → Starts a conditional block. Executes code if the condition is `True`.
    - `else` → Runs a block of code if the `if` condition is `False`.
    - `elif` → "Else if" condition, used for multiple condition checks.
  - **Looping Constructs**
    - `while` → Loops as long as a condition is `True`.
    - `for` → Iterates over a sequence (list, tuple, string, etc.).
    - `in` → Checks if a value is present in a sequence.
  - **Exception Handling**
    - `try` → Starts an exception handling block.
    - `except` → Handles exceptions raised in `try`.
    - `finally` → Always executes, whether an exception occurs or not.
  - **Function & Class Definitions**
    - `def` → Defines a function.
    - `return` → Specifies the value a function should return.
    - `class` → Defines a class in object-oriented programming.
  - **Module Handling**
    - `import` → Imports a module.
    - `from` → Imports specific components from a module.
    - `as` → Creates an alias for a module.
  - **Boolean & Null Values**
    - `True` → Boolean `True` value.
    - `False` → Boolean `False` value.
    - `None` → Represents a null or undefined value.
  - **Object Identity & Memory Management**
    - `is` → Checks if two objects refer to the same memory location.
    - `lambda` → Creates an anonymous function.
    - `with` → Manages resources (e.g., file handling).
    - `global` → Declares a global variable inside a function.
    - `nonlocal` → Modifies a variable in an enclosing (non-global) scope.

## Variables
- A **variable** is a named storage location used to store data.
- **Example:** Assigning & Accessing a Variable
    ```python
    # Assign a value to a variable
    my_variable = 24

    # Print the variable's value
    print(my_variable)  # Output: 24
    ```
- **Variable Scope**
  - **Local Scope:** A variable defined inside a function **cannot** be accessed outside of it.
    ```python
    def my_function():
        s = 22  # Local variable
        print(s)

    my_function()
    print(s)  # Error: 's' is not defined outside the function
    ```
  - **Global Scope:** A variable defined outside a function **can** be accessed anywhere in the program.
    ```python
    k = 44  # Global variable

    def my_function():
        print(k)  # Accessible inside the function

    my_function()
    print(k)  # Accessible outside the function
    ```
### Variable Lifetime
- **Local variables** exist **only while** the function is executing.
- **Global variables** exist **for the entire duration** of the program.
### Variable Naming Conventions & Best Practices
- Use descriptive names
- Use lowercase with underscores (`snake_case`)
- Use meaningful names
    ```python
    user_name = "Suresh"
    num_of_students = 10  # More descriptive
    ```
### Updating Variable Values
- When a variable is **reassigned**, the new value replaces the old one.
    ```python
    port = 80
    print(f"Port: {port}")  # Output: Port: 80

    port = 443  # Variable updated
    print(f"Updated Port: {port}")  # Output: Updated Port: 443
    ```

## Functions, Modules, and Packages
### Python Functions
- A function is a **block of reusable code** that performs a specific task.
- Functions take inputs (**arguments**), process them, and return an output.
- **Defining a Function**
    ```python
    def greet(name):
        return f"Hello, {name}!"
    ```
- **Calling a Function**
    ```python
    message = greet("Suresh")
    print(message)  # Output: Hello, Suresh!
    ```
- **Function with Return Statement**
    ```python
    def add(a, b):
        return a + b

    result = add(10, 5)
    print(result)  # Output: 15
    ```
### Python Modules
- A **module** is a Python file (`.py`) that contains reusable functions, variables, and classes.
- **Types of Modules**
    1. **Built-in Modules** – Included in Python (e.g., `os`, `sys`, `math`)
    2. **Third-Party Modules** – Installed using `pip` (e.g., `requests`, `numpy`)
    3. **Custom Modules** – Created by users in `.py` files
- **Using Built-in Modules**
    ```python
    import math
    print(math.sqrt(16))  # Output: 4.0
    ```
- **Creating a Custom Module**
  - **File: `mymodule.py`**
    ```python
    def square(x):
        return x ** 2

    pi = 3.14
    ```
  - **Using the Module (`main.py`)**
    ```python
    import mymodule

    print(mymodule.square(3))  # Output: 9
    print(mymodule.pi)  # Output: 3.14
    ```
### Python Packages
- A **package** is a collection of Python **modules** grouped in a directory with an `__init__.py` file.
- **Package Structure**
    ```
    my_package/
    │── __init__.py
    │── module_1.py
    │── module_2.py
    ```
- **Creating a Package**
  - **File: `my_package/module_1.py`**
    ```python
    def greet(name):
        return f"Hello, {name}!"
    ```
  - **File: `my_package/module_2.py`**
    ```python
    def add(a, b):
        return a + b
    ```
- **Using a Package**
    ```python
    from my_package import module_1, module_2

    print(module_1.greet("Suresh"))  # Output: Hello, Suresh!
    print(module_2.add(5, 10))  # Output: 15
    ```
### Importing Modules and Packages
- **Import Methods:**
  - **Entire Module** → `import math`
  - **Specific Function** → `from math import sqrt`
  - **Multiple Functions** → `from math import pow, ceil`
  - **Using Alias** → `import numpy as np`
- **Example**
    ```python
    from math import sqrt as square_root
    print(square_root(16))  # Output: 4.0
    ```

## Python Workspaces
- A **Python workspace** is the environment where Python code is developed and executed. It includes:
  - **Python Interpreter**: The Python version used for execution.
  - **Installed Libraries**: Modules and packages available in the environment.
  - **Current Working Directory (CWD)**: The directory where scripts and files reside.
- Understanding Python workspaces is crucial for managing projects, dependencies, and code organization.
- **Types of Python Workspaces**
  - **Local Environment**
    - Uses a system-wide Python installation.
    - Shared across users on the same machine.
    - **Not recommended** for projects needing different dependency versions.
  - **Virtual Environment**
    - **Isolated** Python environment for a project.
    - **Own Python interpreter and libraries**.
    - **Prevents conflicts** between project dependencies.
    - Created using `venv` or `virtualenv`.
- **Creating a Virtual Environment** → `python -m venv myenv`
  - **Activating the Virtual Environment**
    - **Linux/macOS** → `source myenv/bin/activate`
    - **Windows** → `myenv\Scripts\activate`
  - **Deactivating the Virtual Environment** → `deactivate`

## Command Line Arguments
- Command line arguments allow passing input values when executing a script.
- **Example:** Calculator Using Command Line Arguments
  - **File:** `calculator_cla.py`
    ```python
    import sys

    def add(a, b): return a + b
    def sub(a, b): return a - b
    def mul(a, b): return a * b
    def div(a, b): return a / b

    if len(sys.argv) != 4:
        print("Usage: python calculator_cla.py <num1> <operation> <num2>")
        sys.exit(1)

    num1 = float(sys.argv[1])
    operation = sys.argv[2]
    num2 = float(sys.argv[3])

    operations = {"add": add, "sub": sub, "mul": mul, "div": div}

    if operation in operations:
        print(f"Result: {operations[operation](num1, num2)}")
    else:
        print("Invalid operation. Use add, sub, mul, or div.")
    ```
  - **Running the Script** → `python calculator_cla.py 10 add 5`
  - **Output:** `Result: 15.0`

## Environment Variables
- Environment variables store configuration settings like **API keys**, **database credentials**, etc.
- **Setting Environment Variables**
  - **Linux/macOS**:
    ```bash
    export USERNAME="myuser"
    export PASSWORD="mypassword"
    ```
  - **Windows**:
    ```cmd
    set USERNAME=myuser
    set PASSWORD=mypassword
    ```
- **Accessing Environment Variables in Python**
  - **File: `env.py`**
    ```python
    import os

    user_name = os.getenv("USERNAME")
    password = os.getenv("PASSWORD")

    print(f"Username: {user_name}")
    print("Password:", password)
    ```
  - **Running the Script** → `python env.py`

## User Input in Python
- Python allows taking user input dynamically using `input()`.
- **Basic User Input**
    ```python
    name = input("Enter your name: ")
    print("Hello, " + name + "!")
    ```
- **Taking Integer Input**
    ```python
    age = int(input("Enter your age: "))
    print(f"You are {age} years old.")
    ```
- **Handling Multiple Inputs**
    ```python
    num1, num2 = map(int, input("Enter two numbers: ").split())
    print("Sum:", num1 + num2)
    ```

## Python Operators
- Python **operators** are symbols that perform operations on variables and values.
### Arithmetic Operators
- Used to perform mathematical calculations.  
  | Operator | Definition | Example | Output |
  |----------|------------|---------|--------|
  | `+` (Addition) | Adds two numbers | `5 + 2` | `7` |
  | `-` (Subtraction) | Subtracts the second number from the first | `5 - 2` | `3` |
  | `*` (Multiplication) | Multiplies two numbers | `5 * 2` | `10` |
  | `/` (Division) | Divides first number by the second, returns float | `5 / 2` | `2.5` |
  | `//` (Floor Division) | Divides and returns only the whole number part | `5 // 2` | `2` |
  | `%` (Modulus) | Returns the remainder of division | `5 % 2` | `1` |
  | `**` (Exponentiation) | Raises first number to the power of second | `5 ** 2` | `25` |
### Assignment Operators
- Used to assign values to variables and modify them.
  | Operator | Definition | Example | Equivalent To |
  |----------|------------|---------|---------------|
  | `=`  | Assigns value to a variable | `x = 5` | `x = 5` |
  | `+=` | Adds and assigns result | `x += 3` | `x = x + 3` |
  | `-=` | Subtracts and assigns result | `x -= 2` | `x = x - 2` |
  | `*=` | Multiplies and assigns result | `x *= 3` | `x = x * 3` |
  | `/=` | Divides and assigns result | `x /= 2` | `x = x / 2` |
  | `//=` | Floor divides and assigns result | `x //= 2` | `x = x // 2` |
  | `%=` | Modulus and assigns result | `x %= 3` | `x = x % 3` |
  | `**=` | Exponentiation and assigns result | `x **= 2` | `x = x ** 2` |
### Comparison (Relational) Operators
- Used to compare two values, returning `True` or `False`.
  | Operator | Definition | Example | Output |
  |----------|------------|---------|--------|
  | `==` (Equal) | Checks if values are equal | `5 == 5` | `True` |
  | `!=` (Not Equal) | Checks if values are different | `5 != 2` | `True` |
  | `>` (Greater Than) | Checks if first value is greater | `5 > 2` | `True` |
  | `<` (Less Than) | Checks if first value is smaller | `5 < 2` | `False` |
  | `>=` (Greater or Equal) | Checks if first is greater or equal | `5 >= 5` | `True` |
  | `<=` (Less or Equal) | Checks if first is smaller or equal | `5 <= 2` | `False` |
### Logical Operators
- Used to combine conditional statements.
  | Operator | Definition | Example | Output |
  |----------|------------|---------|--------|
  | `and` | Returns `True` if both conditions are `True` | `True and False` | `False` |
  | `or` | Returns `True` if at least one condition is `True` | `True or False` | `True` |
  | `not` | Reverses the Boolean value | `not True` | `False` |
### Identity Operators
- Used to compare memory locations of two objects.  
  | Operator | Definition | Example | Output |
  |----------|------------|---------|--------|
  | `is` | Returns `True` if objects are the same | `x is y` | `True/False` |
  | `is not` | Returns `True` if objects are different | `x is not y` | `True/False` |
### Membership Operators
- Used to check if a value exists in a sequence.  
  | Operator | Definition | Example | Output |
  |----------|------------|---------|--------|
  | `in` | Returns `True` if value is in sequence | `"a" in "apple"` | `True` |
  | `not in` | Returns `True` if value is not in sequence | `"x" not in "apple"` | `True` |
### Bitwise Operators
- Used to perform bit-level operations.  
  | Operator | Definition | Example | Output |
  |----------|------------|---------|--------|
  | `&` (AND) | Sets bit to 1 if both bits are 1 | `5 & 3` | `1` |
  | (OR) | Sets bit to 1 if at least one bit is 1 | `5 OR 3` | `7` |
  | `^` (XOR) | Sets bit to 1 if bits are different | `5 ^ 3` | `6` |
  | `~` (NOT) | Inverts bits | `~5` | `-6` |
  | `<<` (Left Shift) | Shifts bits left (multiplies by `2^n`) | `5 << 1` | `10` |
  | `>>` (Right Shift) | Shifts bits right (divides by `2^n`) | `5 >> 1` | `2` |
  - **Note:** Symbol of `OR` is `|`.
### Operator Precedence (Execution Order)
- Determines which operations execute first.  
  1. `()` → Parentheses  
  2. `**` → Exponentiation  
  3. `+x, -x, ~x` → Unary operators  
  4. `*, /, //, %` → Multiplication, Division, Floor Division, Modulus  
  5. `+, -` → Addition, Subtraction  
  6. `<<, >>` → Bitwise shift  
  7. `&` → Bitwise AND  
  8. `^` → Bitwise XOR  
  9. `|` → Bitwise OR  
  10. `==, !=, >, <, >=, <=` → Comparisons  
  11. `not` → Logical NOT  
  12. `and` → Logical AND  
  13. `or` → Logical OR

## Conditional Statements in Python
- Conditional statements are a fundamental part of programming that allow you to make decisions and execute different blocks of code based on certain conditions.
  - **if Statement:** Executes a block of code if a condition is `True`.  
    ```python
    x = 10
    if x > 5:
        print("x is greater than 5")
    ```
    - **Output:**  `x is greater than 5`  
  - **elif Statement:** Checks multiple conditions if the previous ones are `False`.  
    ```python
    x = 10
    if x > 15:
        print("x is greater than 15")
    elif x > 5:
        print("x is greater than 5 but not greater than 15")
    else:
        print("x is not greater than 5")
    ```
    - **Output:**  `x is greater than 5 but not greater than 15`  

  - **else Statement:** Executes a block of code if none of the conditions are `True`.  
    ```python
    x = 3
    if x > 5:
        print("x is greater than 5")
    else:
        print("x is not greater than 5")
    ```
    - **Output:**  `x is not greater than 5`

## Lists & Tuples
### Lists
- Lists are **ordered**, **mutable**, and can hold elements of different data types.
- Lists are **mutable**, meaning their content can be changed (We can add or remove items in the list)
- **Creating a List:** List are created using **square brackets `[]`** in Python.
  ```python
  my_list = [1, 2, 3, 'apple']
  ```
- **Common List Operations:**  
  - **Indexing:** `my_list[0]` → Access first element  
  - **Appending:** `my_list.append(4)` → Adds `4` to the end  
  - **Removing:** `my_list.remove('apple')` → Removes `'apple'`  
  - **Slicing:** `my_list[1:3]` → Gets a sublist `[2, 3]`  
  - **Concatenation:** `new_list = my_list + [5, 6]` → Combine two or more lists 
  - **Sorting:** `my_list.sort()` (in-place) or `sorted(my_list)` → Modifies the original list 
  - **Checking Membership:** `'banana' in my_list` → `True` (Check if a value exists in a list)
  - **Finding Length:** `len(my_list)` → Gets number of elements 
### Tuples
- A **tuple** is a data structure that is similar to a list but with one key difference: tuples are **immutable**, meaning their contents cannot be changed after they are created.
- **Creating a Tuple:** Tuples are created using **parentheses `()`**. 
  ```python
  my_tuple = (1, 2, 'apple', 'banana')
  ```
- **Common Tuple Operations:**  
  - **Indexing:** `my_tuple[0]` → Access first element  
  - **Tuple Length:** `len(my_tuple)` → Gets number of elements  
  - **Packing & Unpacking:** Pack multiple values into a tuple and unpack them into separate variables
    ```python
    x, y = (3, 4)  # x = 3, y = 4
    ```
  - **Concatenation:** `new_tuple = my_tuple + (3.14, 'cherry')` → Combine two or more tuples 
  - **Checking Membership:** `'apple' in my_tuple` → `True`  (Check if a value exists in a tuple)
  - **Multiple Return Values:** Tuples are often used to return multiple values from a function
    ```python
    def get_coordinates():
        return (3, 4)

    x, y = get_coordinates()  # x = 3, y = 4
    ```
### Usage
- **Use Lists** when you need flexibility and modifications.  
- **Use Tuples** when you need fixed, efficient storage.

## Loops in Python
- Loops are a **fundamental programming concept** that allows executing a block of code **multiple times** until a specified condition is met.
- Loops help in **automating repetitive tasks**, reducing code duplication, and improving efficiency.
- Python provides **two primary types of loops**:
  1. **`for` loop** – Used to iterate over a sequence (list, tuple, dictionary, string, or range).
  2. **`while` loop** – Executes as long as a given condition remains `True`.
### `for` Loop (Definite Loop)
- Used when the number of iterations is **known**
- Iterates over a **sequence** (e.g., list, tuple, string, dictionary, or range)  
- A `for` loop **iterates over a sequence** and executes a block of code for each element in the sequence.
- **Syntax:**  
  ```python
  for variable in sequence:
      # Code block to execute
  ```
- **Examples:**
  - **Iterating through a list**
    ```python
    fruits = ['apple', 'banana', 'cherry']
    for fruit in fruits:
        print(fruit)
    # Output:
    # apple
    # banana
    # cherry
    ```
  - **Using `range()`**
    ```python
    for i in range(5):  # Loops from 0 to 4
        print(i)
    # Output: 0 1 2 3 4
    ```
  - **Using `enumerate()`**
    ```python
    fruits = ['apple', 'banana', 'cherry']
    for index, fruit in enumerate(fruits):
        print(f"Index: {index}, Fruit: {fruit}")
    # Output:
    # Index: 0, Fruit: apple
    # Index: 1, Fruit: banana
    # Index: 2, Fruit: cherry
    ```
### `while` Loop (Indefinite Loop)
- Used when the number of iterations is **unknown**  
- Executes **as long as** a given condition is `True`
- A `while` loop **executes a block of code repeatedly** until the given condition becomes `False`.
- **Syntax:**  
  ```python
  while condition:
      # Code block to execute
  ```
- **Example:** Basic `while` loop
    ```python
    count = 0
    while count < 5:
        print(count)
        count += 1
    # Output: 0 1 2 3 4
    ```
### Loop Control Statements
- Loop control statements are used to modify the behavior of loops. Python provides **three** main loop control statements:
#### `break` Statement
- **Terminates** the loop immediately  
- Works in both `for` and `while` loops  
- The `break` statement **exits the loop prematurely** when a certain condition is met.
- **Example:**  
  ```python
  numbers = [1, 2, 3, 4, 5]
  for number in numbers:
      if number == 3:
          break  # Stops loop at 3
      print(number)
  # Output: 1 2
  ```
#### `continue` Statement
- **Skips** the current iteration and moves to the next one  
- The `continue` statement **skips** the remaining code in the current iteration and moves to the **next iteration** of the loop.
- **Example:**  
  ```python
  numbers = [1, 2, 3, 4, 5]
  for number in numbers:
      if number == 3:
          continue  # Skips 3
      print(number)
  # Output: 1 2 4 5
  ```
#### `pass` Statement
- **Does nothing** (used as a placeholder)  
- The `pass` statement is a **null operation** that **allows a syntactically required block** to be left empty.
- **Example:**  
  ```python
  for i in range(5):
      if i == 3:
          pass  # Placeholder for future logic
      else:
          print(i)
  # Output: 0 1 2 4
  ```
#### `else` with Loops
- Executes **after the loop completes naturally** (i.e., without encountering a `break`).  
- If `break` is encountered, the `else` block **does not execute**.
- The `else` block **executes when the loop finishes successfully**, but **not** when `break` is used.
- **Example:**  
  ```python
  for i in range(5):
      if i == 3:
          break
      print(i)
  else:
      print("Loop finished")  # This will NOT execute
  # Output: 0 1 2
  ```
#### Nested Loops
- A loop inside **another loop**  
- The **inner loop executes completely** for each iteration of the **outer loop**  
- A nested loop is **a loop inside another loop**, where the inner loop executes for each iteration of the outer loop.
- **Example:** Using `break` in nested loops  
  ```python
  for i in range(3):
      for j in range(3):
          if j == 2:
              break  # Stops inner loop when j == 2
          print(f"i={i}, j={j}")
  # Output:
  # i=0, j=0
  # i=0, j=1
  # i=1, j=0
  # i=1, j=1
  # i=2, j=0
  # i=2, j=1
  ```

## Python Dictionary
- A dictionary in Python is a data structure that stores data as key-value pairs.
- **Creating a Dictionary:**
  - Dictionary is created using curly braces `{}`
    ```python
    my_dict = {'name': 'Alice', 'age': 30}
    ```
  - Creating an empty dictionary and adding items later:  
    ```python
    my_dict = {}
    my_dict['color'] = 'blue'
    ```
- **Accessing Values:**  
  - Using a key:  
    ```python
    print(my_dict['name'])  # Output: Alice
    ```
  - Using `get()` to avoid errors:  
    ```python
    print(my_dict.get('name'))  # Output: Alice
    print(my_dict.get('salary'))  # Output: None
    ```
- **Adding or Updating Values:**  
  - Adding a new key-value pair:  
    ```python
    my_dict['job'] = 'Teacher'
    ```
  - Updating an existing key:  
    ```python
    my_dict['age'] = 31
    ```
- **Removing Items:**  
  - Using `del`:  
    ```python
    del my_dict['job']
    ```
  - Using `pop()` (returns the removed value):  
    ```python
    removed = my_dict.pop('age')
    print(removed)  # Output: 31
    ```
- **Checking if a Key Exists:**  
  ```python
  if 'age' in my_dict:
      print('Age is in the dictionary')
  ```
- **Looping Through a Dictionary:**  
  - Loop through keys and values:  
    ```python
    for key, value in my_dict.items():
        print(f"{key}: {value}")
    ```
    **Output:**  
    ```
    name: Alice
    age: 31
    ```
- **Nested Dictionaries:** A dictionary inside another dictionary.  
  ```python
  students = {
      'student1': {'name': 'Alice', 'age': 25},
      'student2': {'name': 'Bob', 'age': 22}
  }
  print(students['student2']['age'])  # Output: 22
  ```
- **List of Dictionaries:** A list where each element is a dictionary.  
  ```python
  my_list_of_dicts = [
      {'name': 'Alice', 'age': 30},
      {'name': 'Bob', 'age': 25}
  ]
  print(my_list_of_dicts[1]['name'])  # Output: Bob
  ```

## Sets and Set Operations
- A **set** in Python is an **unordered** collection of **unique** elements. It does not allow duplicates and is useful for mathematical operations like **union, intersection, and difference**.
- **Creating a Set:**
  - **Using curly braces `{}`**  
    ```python
    my_set = {1, 2, 3, 4, 5}
    ```
  - **Creating an empty set** (use `set()` instead of `{}` to avoid confusion with dictionaries)
    ```python
    empty_set = set()
    ```
- **Adding and Removing Elements**
  - **Adding an element** → `my_set.add(6)`
  - **Removing an element:**
    - `remove()`: Raises an error if the element does not exist → `my_set.remove(3)`
    - `discard()`: Does not raise an error if the element does not exist  → `my_set.discard(3)`
### Set Operations
```python
set1 = {1, 2, 3, 4}
set2 = {3, 4, 5, 6}

union_set = set1.union(set2)  
intersection_set = set1.intersection(set2)  
difference_set = set1.difference(set2)  
```
- **Union:** All unique elements from both sets → `{1, 2, 3, 4, 5, 6}`
- **Intersection:** Common elements → `{3, 4}`
- **Difference:** Elements in first set but not in second → `{1, 2}`
### Subset and Superset
- **Subset (`issubset()`):** True if all elements of one set are in another.  
  ```python
  print(set1.issubset(set2))  # Output: False
  ```
- **Superset (`issuperset()`):** True if a set contains all elements of another set.  
  ```python
  print(set1.issuperset(set2))  # Output: False
  ```

## File Operations in Python
- File operations in Python allow you to **read, write, append, and manage files** efficiently. Python supports handling files in **text** and **binary** formats.
- **Opening a File:**
  - The `open()` function is used to open a file. It requires a **filename** and a **mode**.
    ```python
    file = open("example.txt", "r")  # Opens the file in read mode
    ```
  - **Modes:**
    - `"r"` → Read mode (default). Opens file for reading.
    - `"w"` → Write mode. Overwrites existing content or creates a new file.
    - `"a"` → Append mode. Adds content to the file without deleting previous data.
    - `"x"` → Create mode. Fails if the file already exists.
    - `"b"` → Binary mode (used for images, PDFs, etc.).
- **Reading from a File:**
  - `read()` → Reads the entire file content.
  - `readline()` → Reads a single line from the file.
  - `readlines()` → Reads all lines into a list.
- **Copying Content from One File to Another**
  - Reads the source file and writes content into the destination file.
    ```python
    with open("source.txt", "r") as source, open("destination.txt", "w") as dest:
        for line in source:
            dest.write(line)

    print("File copied successfully!")
    ```
- **Updating a Configuration File (`server.conf`)**
  - Modifying a **specific key-value** pair inside a configuration file.
  - **Example File:** `server.conf`
    ```
    # Network Settings
    PORT = 8080
    MAX_CONNECTIONS = 200
    TIMEOUT = 30
    ```
  - **Program to update `MAX_CONNECTIONS` to 1000**
    ```python
    def update_config_list(filepath, key, value):
        with open(filepath, "r") as file:
            file_lines = file.readlines()
        with open(filepath, "w") as file:
            for line in file_lines:
                if key in line:
                    file.write(key + " = " + value + "\n")
                else:
                    file.write(line)

    update_config_list("server.conf", "MAX_CONNECTIONS", "1000")
    ```

## Boto3
- Boto3 is the AWS SDK for Python, allowing developers to interact with AWS services using Python scripts.  
- **Uses of Boto3:**  
  - **Managing AWS Resources** – Automate EC2, S3, IAM, and other AWS services.  
  - **Interacting with AWS Services** – Read/write data in S3, invoke Lambda, query DynamoDB.  
  - **Automation & DevOps** – Used in CI/CD pipelines, backups, security monitoring.  
  - **Machine Learning & Data Processing** – Fetch training data from S3, use SageMaker, AWS Glue.  
- **Installation:**  
  - Install Boto3 using pip: `pip install boto3`
  - Ensure AWS CLI is installed and configured: `aws configure`
- **Use of Boto3 Documentation:**
  - Go to [Boto3 Official Docs](https://boto3.amazonaws.com/v1/documentation/api/latest/index.html).  
  - Click **Available Services** and select the required AWS service.  
  - Choose the resource (e.g., S3, EC2, Lambda).  
  - Use **Request Syntax & Response Syntax** to implement in Python scripts.  
- **Use of Boto3 with Lambda Function:**
  - Ensure Lambda has the necessary IAM permissions.
  - Define function `def lambda_handler(event, context):` and add Python script in that.