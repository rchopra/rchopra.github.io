---
layout: page
title: Expressions, Variables, and Data Types
parent: Study Guides
use_math: true
---
# Expressions, Variables, and Data Types
{:.no_toc}

## Table of Contents
{: .no_toc .text-delta }

1. TOC
{:toc}
---

## **Expressions**
An **expression** in Python is a combination of values, variables, operators, and function calls. When evaluated, an expression produces a value. 

### **Examples**
- `3 + 5` → `8`
- `x - 2` (assuming `x = 10`) → `8`
- `"Hello" + " World"` → `"Hello World"`

### **Key Operators in Python**:
- **Arithmetic Operators**:
  - `+` (Addition): `5 + 3` → `8`
  - `-` (Subtraction): `10 - 2` → `8`
  - `*` (Multiplication): `4 * 2` → `8`
  - `/` (Division): `16 / 2` → `8.0`
  - `//` (Floor Division): `16 // 3` → `5` gives **only** the whole number part (quotient) of a division
  - `%` (Modulus): `16 % 3` → `1` gives **only** the remainder of a division
  - `**` (Exponentiation): `2 ** 3` → `8`

- **String Operators**:
  - `+` (Concatenation): `"hello" + "world"` → `helloworld` combines two strings into one.
  - `*` (Repetition): `"hi" * 4` → `hihihihi` repeats the string an integer number of times.

### **Evaluating Expressions**
Python follows a specific order of operations when evaluating expressions, often called "PEMDAS":

1. Parentheses `()`: Highest precedence, anything in parentheses gets evaluated first.
1. Exponents `**`: Exponentiation happens next.
1. Multiplication `*`, Division `/` and `//`, Modulo `%`: These are processed left to right.
1. Addition `+` and Subtraction `-`: These are also processed left to right.

When evluating a complicated expression, work from the **innermost parentheses out**. Example:
```python
(2 + (3 * 4)) ** 2
(2 + 12) ** 2
14 ** 2
196
```
---

## **Variables**
A **variable** is a name that refers to a value stored in memory. Variables allow us to store and manipulate data. You can assign values to variables using the `=` operator.

### **Declaring and Assigning Variables**:
```python
x = 10
y = 20
name = "Alice"
```

- Variable names should be descriptive and follow these rules:
  - Must begin with a letter or underscore (`_`)
  - Can only contain letters, numbers, and underscores
  - Cannot be a Python **keyword** (e.g., `if`, `else`, `while`)

---

## **Data Types**
Python has several **built-in data types**. Each data type determines what kind of value can be stored and what operations can be performed on that value. In this class, we are concerned with the following four data types.

### **Numbers**
1. **Integers (int)**: Whole numbers (positive or negative).
   - Example: `x = 5`
2. **Floats (float)**: Numbers with decimal points.
   - Example: `pi = 3.14`

### **Strings (str)**
3. A string is a sequence of characters enclosed in quotes (single, double, or triple).
- Example: `greeting = "Hello"`
- You can access individual characters with indexing (`greeting[0]` gives `"H"`) and slice strings with `greeting[1:4]`.

### **Booleans (bool)**
4. Booleans represent **True** or **False** values.
- Example: `is_student = True`

---

## **Type Conversion**
Sometimes you need to convert between data types.
- **int()**: Convert to an integer.
- **float()**: Convert to a float.
- **str()**: Convert to a string.
- **bool()**: Convert to a bool.

### **Examples**
```python
int("5")  # Converts the string "5" to the integer 5
float(10) # Converts the integer 10 to the float 10.0
str(123)  # Converts the integer 123 to the string "123"
```

---

## **Input and Output**
- Use `input()` to get user input (returns a string).
  - `input()` **prompts** the user with instructions you provide, and then **waits** for the user to type in a result.
  - `input()` always returns a string! If you are trying to work with numbers, you may need to convert the result (see [Type Conversion](#type-conversion) above).
- Use `print()` to output data to the console.

### **Example**
```python
name = input("Enter your name: ")
print("Hello, " + name + "!")
```

---

## **Common Errors**
- **SyntaxError**: Occurs when the code violates Python's grammar rules.
  - Example: Missing a closing parenthesis `)` at the end of a `print` statement.
- **TypeError**: Occurs when an operation is applied to an object of inappropriate type.
  - Example: Adding a string to an integer (`"3" + 3`).

---

## **Practice Problems**:
1. Write a Python program to calculate the area of a rectangle. Prompt the user for length and width.
2. Write a program that converts a temperature in Celsius to Fahrenheit using the formula $$F = C  \times 1.8 + 32$$. Have the user input a temperature in Celsius.
3. Write a program that prompst the user for a number of minutes and displays that duration in hours and minutes. For example, 135 minutes would be 2 hours and 15 minutes.

---
