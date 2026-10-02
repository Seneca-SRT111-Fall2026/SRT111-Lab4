<h1 align="center">SRT111 Lab 4 - Fall 2026</h1>

<p align="center">
<b>Prepared by:</b> Tiayyba Riaz<br>
<b>Total Marks:</b> 10<br>
<b>Percentage Towards Final Grade:</b> 2%
</p>

In this lab, you will explore three important Python data structures: **lists**, **sets**, and **dictionaries**. These structures are widely used to organize, store, and manage data efficiently. You will begin by working with lists to understand ordered collections and practice modifying their contents. Next, you will learn how sets store unique, unordered elements and how set operations can be applied in problem-solving. Finally, you will work with dictionaries to see how key–value pairs allow fast and efficient data access. You will continue to use functions and a `main()` function to organize your programs, as practised in Lab 3.

The lab is divided into two components:

- **Part A: In-Class Lab** (must be completed during the scheduled lab period and demonstrated to the professor for grading).
- **Part B: Take-Home Lab** (can be completed independently after the scheduled class).

## Academic Integrity and Use of AI

This lab is intended to assess your individual understanding of Python programming. You may use AI tools (e.g., ChatGPT, Copilot, Gemini) to help explain concepts, syntax, or error messages. However, all submitted code must be your own work, and you must be able to explain your solution if asked by the professor.

Submitting copied, shared, or AI-generated solutions as your own work may result in a grade of zero and may be handled according to the College Academic Integrity Policy.

## Lab Objectives

By the end of this lab, you should be able to:

- Create and manipulate Python lists, including adding, removing, and modifying elements.
- Apply built-in functions and list methods to perform common list operations.
- Construct sets and use them to store unique, unordered items.
- Compare lists and sets, highlighting differences in ordering and duplication.
- Perform set operations such as union, intersection, difference, and symmetric difference.
- Create dictionaries with key–value pairs for efficient data storage.
- Access, update, and traverse dictionary values using keys.
- Differentiate between index-based access in lists and key-based access in dictionaries.
- Use functions and a `main()` function to organize programs that work with data structures.

## Required Comment Header

For every script created in this lab include the following comment block at the top of the file/cell.

```python
# Author: Your Name
# Date: YYYY-MM-DD
# Purpose: Brief description of what the program does.
```

---

# Part A - In-Class Lab [40% of Lab Marks]

Complete all assigned in-class tasks during your scheduled lab.

- This part can be completed in **Jupyter Lab** or **VS Code**. You have a choice. I recommend using **Jupyter Lab**.
  - If you are using Jupyter Lab, then please create a single notebook file called `Lab4.ipynb` and complete each task in a unique cell.
  - If you are using VS Code, then just follow the instructions for each task and create `.py` files.
- Demonstrate your completed work to the professor before leaving the lab.
- The professor may ask you to explain portions of your code.
- No PDF submission is required for Part A unless otherwise instructed.

## Using Lists

A list in Python is an ordered collection of items. Lists are **mutable**, meaning you can change their contents after creation. Lists usually contain similar kinds of data, but Python does not restrict you from storing values of different data types in the same list.

Lists are constructed with square brackets `[]`, with commas separating each element. For example:

```python
numbers = [1, 2, 3, 4]
mixed_list = [1, "two", 4.5, True]
```

### Task 1 - Creating Lists and List Concatenation

**Objective:** Practice creating Python lists, storing values in them, and concatenating multiple lists using the `+` operator.

**Instructions:**

- Create a file named `task1.py` and add the required comment header.
- Create a variable called `mylist1` that stores the first three odd numbers: 1, 3, 5.
- Create a second list called `mylist2` that stores the first three even numbers: 0, 2, 4.
- Create a third list called `mylist` that combines all elements from `mylist1` and `mylist2`.
  - *Hint:* You can use `+` to concatenate lists. For example, `[1, 2] + [3, 4]` results in `[1, 2, 3, 4]`.
- Print the variable `mylist` and check that it contains all six numbers in order.
- Run your script to test it.

**Expected Output:**

```text
[1, 3, 5, 0, 2, 4]
```

### Task 2 - Using List Methods to Add and Remove Elements

**Objective:** Practice using common list methods (`append()`, `insert()`, `pop()`, and `index()`) to modify and access list elements.

**Instructions:**

- Create a file named `task2.py` and add the required comment header.
- Create a variable `mylist` that contains the first 6 natural numbers: `[1, 2, 3, 4, 5, 6]`.
- Use the `append()` method to add the number 7 to the end of the list.
- Use the `insert()` method to insert the number 0 at index 0.
- Use the `pop()` method to remove the element at index 2.
- Print the variable `mylist`.
- Use the `index()` method to find the index of the element `6`, store it in a variable, and print the message shown in the expected output.
- Run your script to test it.

**Expected Output:**

```text
[0, 1, 3, 4, 5, 6, 7]
The element 6 is present at index 5
```

### Task 3 - Modifying a List and Using It in a Loop

**Objective:** Practice updating a list element by its index and using a `for` loop to iterate over a list.

**Instructions:**

- Create a file named `task3.py` and add the required comment header.
- Create a list variable called `students` and add the following names: Ama, Eden, Maija, Daniel, Ibrahim.
- Update the element at index 1 to `"Maggy"`.
  - *Hint:* Remember that list indices start at 0.
- Use a `for` loop to iterate over the `students` list and print each name on a separate line.
- Run your script to test it.

**Expected Output:**

```text
Ama
Maggy
Maija
Daniel
Ibrahim
```

## Working with Sets

Sets are used to store multiple items in a single variable. A set is one of 4 built-in data types in Python used to store collections of data; the other 3 are list, tuple, and dictionary, all with different qualities and usage.

A set has similar characteristics to a list, but there are two major differences:

- Sets are **unordered**.
- Sets **cannot contain duplicate values**. Duplicate entries are automatically ignored.

Set variables are created with curly brackets:

```python
myset = {"apples", "oranges", "kiwi", "oranges"}
print(myset)
```

Output (order may vary):

```text
{'kiwi', 'apples', 'oranges'}
```

To create an **empty** set, use `set()`. Do **not** use `{}`, because that creates an empty dictionary. Use the `add()` method to add an element to a set:

```python
numbers = set()
numbers.add(10)
numbers.add(20)
numbers.add(10)   # duplicate, ignored
print(numbers)    # Output: {10, 20}
```

Because duplicates are ignored, sets are very useful for comparisons, such as finding similarities or differences between groups of data.

### Task 4 - Creating Sets with a Function

**Objective:** Practice creating sets in Python by completing a function that uses a loop and conditional logic to filter numbers by divisibility.

**Instructions:**

- Create a file named `task4.py` and add the required comment header.
- Copy the following starter code into your file, below the comment header:

```python
def buildtheSet(divisor):
    # Complete this function
def main():

    s3 = buildtheSet(3)
    print("s3: ", s3)
    print("----------------------------------------")

    #create s5
    s7 = buildtheSet(7)
    print("s7: ", s7)
    print("----------------------------------------")

    s11 = buildtheSet(11)
    print("s11: ", s11)

main()
```

> **Note:** The starter code will not run as-is, because a function cannot contain only a comment. It will run once you complete `buildtheSet()`.

- Complete the `buildtheSet()` function so that it:
  - Creates an empty set.
  - Uses a `for` loop to iterate over the numbers from 0 to 50 (inclusive).
  - Uses an `if` statement to check whether each number is divisible by `divisor`.
  - Adds each divisible number to the set using the `add()` method.
  - Returns the set.
- In `main()`, replace the `#create s5` comment with code that:
  - Creates `s5` (numbers from 0 to 50 divisible by 5) by calling `buildtheSet()`.
  - Prints `s5` and a separator line, in the same format as the other sets.
- Run your script to test it.

**Expected Output:**

```text
s3:  {0, 3, 6, 9, 12, 15, 18, 21, 24, 27, 30, 33, 36, 39, 42, 45, 48}
----------------------------------------
s5:  {0, 5, 10, 15, 20, 25, 30, 35, 40, 45, 50}
----------------------------------------
s7:  {0, 7, 14, 21, 28, 35, 42, 49}
----------------------------------------
s11:  {0, 11, 22, 33, 44}
```

> **Note:** Sets are unordered, so your printed output may not appear in numerical order. The set contents must match.

---

# Part B - Take-Home Lab [60% of Lab Marks]

Complete the following tasks independently after the scheduled lab using VS Code.

**Before You Begin:**

- Open your local Git repository `SRT111F2026` on your computer.
- Create a new folder named `Lab04` inside the repository.
- Open the `Lab04` folder in VS Code.
- Create all Python files for this lab (`task5.py`, `task6.py`, `task7.py`, `task8.py`) inside the `Lab04` folder.

**For each task:**

- Run the script using the VS Code terminal.
- Take a screenshot that clearly shows:
  - Your code in the editor.
  - The terminal output, including your username visible in the terminal.
- Insert the screenshots into a Word document under a heading that matches the task name (e.g., **Task 5**, **Task 6**). You will export this Word document to PDF and submit it on Blackboard.

## Useful Set Operations

Python's set data type directly supports mathematical set operations such as union, intersection, difference, and symmetric difference.

The **union** of two sets is a set containing all the elements of both sets, without duplicates.

```python
set1 = {1, 2, 3}
set2 = {3, 4, 5}

print(set1 | set2)         # Output: {1, 2, 3, 4, 5}
print(set1.union(set2))    # Output: {1, 2, 3, 4, 5}
```

The **intersection** of two sets is a set containing only the elements that are common to both sets.

```python
print(set1 & set2)                # Output: {3}
print(set1.intersection(set2))    # Output: {3}
```

The **difference** of two sets is a set containing the elements that are in the first set but not in the second set.

```python
print(set1 - set2)              # Output: {1, 2}
print(set1.difference(set2))    # Output: {1, 2}
```

The **symmetric difference** of two sets is a set containing the elements that are in either set, but not in both.

```python
print(set1 ^ set2)                        # Output: {1, 2, 4, 5}
print(set1.symmetric_difference(set2))    # Output: {1, 2, 4, 5}
```

### Task 5 - Set Operations

**Objective:** Practice applying set operations to existing sets and passing sets as function arguments.

**Instructions:**

- Create the file `task5.py` and add the required comment header.
- Copy your completed `buildtheSet()` function and `main()` function from Task 4 (from `task4.py` or your `Lab4.ipynb` cell).
- Write a new function named `s3_or_s5` that:
  - Takes two sets, `s3` and `s5`, as parameters.
  - Returns a set containing all elements that are in `s3` or `s5`, but **not in both**.
  - *Hint:* Use the symmetric difference operator `^` or the `symmetric_difference()` method.
- Modify `main()` so that it:
  - Creates and prints only `s3` and `s5` (remove the code for `s7` and `s11`).
  - Calls `s3_or_s5()`, passing `s3` and `s5` as arguments.
  - Stores the returned set in a variable and prints it with a label.
  - Prints the union, intersection, and difference (`s3 - s5`) of `s3` and `s5`, each with a label.
- Run your script to test it.

**Expected Output:**

```text
s3: {0, 3, 6, 9, 12, 15, 18, 21, 24, 27, 30, 33, 36, 39, 42, 45, 48}
s5: {0, 5, 10, 15, 20, 25, 30, 35, 40, 45, 50}
s3_or_s5: {3, 5, 6, 9, 10, 12, 18, 20, 21, 24, 25, 27, 33, 35, 36, 39, 40, 42, 48, 50}
union: {0, 3, 5, 6, 9, 10, 12, 15, 18, 20, 21, 24, 25, 27, 30, 33, 35, 36, 39, 40, 42, 45, 48, 50}
intersection: {0, 15, 30, 45}
difference: {3, 6, 9, 12, 18, 21, 24, 27, 33, 36, 39, 42, 48}
```

> **Note:** Sets are unordered, so your printed output may not appear in numerical order. Spacing after the labels and separator lines may also differ from the sample. The set contents must match.

## Dictionaries

In Python, a dictionary is a collection of **key–value pairs**. Each value is associated with a key, and you can retrieve any value efficiently if you know its key. Since Python 3.7, dictionaries keep their items in the order they were inserted.

Think back to lists: list elements are accessed using numeric indexes (0, 1, 2, ...). If you want to find an element in a list, you either already know its index or you have to search through the list. In contrast, dictionaries let you use descriptive keys instead of numeric indexes. Each key maps directly to a value, and that value can be accessed or changed using the key.

**Example (try it yourself, not graded):**

```python
this_dictionary = {}
this_dictionary["Switzerland"] = "Alps"
this_dictionary["United States"] = "Alaska Range"
this_dictionary["Armenia"] = "Caucasus"
this_dictionary["Argentina"] = "Andes"
this_dictionary["Pakistan"] = "Karakoram"

print(len(this_dictionary))
print(this_dictionary)
print(this_dictionary["Argentina"])
```

Output:

```text
5
{'Switzerland': 'Alps', 'United States': 'Alaska Range', 'Armenia': 'Caucasus', 'Argentina': 'Andes', 'Pakistan': 'Karakoram'}
Andes
```

Here:

- `{}` creates an empty dictionary.
- Five key–value pairs are added: `"Switzerland"` maps to `"Alps"`, `"United States"` maps to `"Alaska Range"`, and so on.
- `len(this_dictionary)` returns the number of key–value pairs.
- Printing the dictionary shows all its contents.
- `this_dictionary["Argentina"]` retrieves the value `"Andes"`.

### Task 6 - Creating Dictionaries with a Function

**Objective:** Practice creating and returning a dictionary by generating key–value pairs from a range of numbers.

**Instructions:**

- Create the file `task6.py` and add the required comment header.
- Write a function named `times_ten` that:
  - Takes two parameters: `start_index` and `end_index`.
  - Creates an empty dictionary.
  - Uses a `for` loop to iterate over the numbers from `start_index` to `end_index` (inclusive).
  - Adds each number as a key, with the key multiplied by ten as its value.
  - Returns the dictionary.
- Write a `main()` function that:
  - Calls `times_ten(2, 6)`.
  - Stores the returned dictionary in a variable named `my_dictionary`.
  - Prints `my_dictionary`.
- Add a call to the `main()` function.
- Run your script to test it.

**Expected Output:**

```text
{2: 20, 3: 30, 4: 40, 5: 50, 6: 60}
```

### Task 7 - Traversing a Dictionary

**Objective:** Practice traversing dictionaries using keys, values, and key–value pairs, and formatting the output using the `.items()` method.

The familiar `for item in collection` loop can also be used with dictionaries. By default, looping through a dictionary goes through its **keys** one by one. Python provides different ways to traverse a dictionary, depending on whether you want to work with keys, values, or key–value pairs.

**Example 1 – Traversing keys:**

```python
student = {
    "name": "John Doe",
    "age": 21,
    "major": "Computer Science"
}

for key in student:
    print(key)
```

Output:

```text
name
age
major
```

**Example 2 – Traversing values:** To iterate through all the values in a dictionary, use the `values()` method.

```python
for value in student.values():
    print(value)
```

Output:

```text
John Doe
21
Computer Science
```

**Example 3 – Traversing key–value pairs:** To iterate through key–value pairs, use the `items()` method, which returns the dictionary's key–value pairs as tuples.

```python
for key, value in student.items():
    print(f"Key: {key}, Value: {value}")
```

Output:

```text
Key: name, Value: John Doe
Key: age, Value: 21
Key: major, Value: Computer Science
```

**Instructions:**

- Create the file `task7.py` and add the required comment header.
- Copy the following starter code into your file, below the comment header:

```python
my_dict = {"Switzerland" : "Alps", "United States" : "Alaska Range", "Armenia" : "Caucasus", "Argentina" : "Andes", "Pakistan" : "Karakoram"}
# TO DO 1: Create a for in loop as instructed in the lab instructions.
# TO DO 2: Run the script, and take the screenshot of code and output.
```

- **TO DO 1:** Use a `for ... in` loop with the `.items()` method to traverse `my_dict`. Inside the loop, print each key and value in the format `key : value`.
- **TO DO 2:** Run your script, and take a screenshot of your code and output.

**Expected Output:**

```text
Switzerland : Alps
United States : Alaska Range
Armenia : Caucasus
Argentina : Andes
Pakistan : Karakoram
```

### Task 8 - Using a Dictionary for Problem Solving

**Objective:** Use a dictionary to count and summarize data from a string by building a simple text-based histogram.

**Instructions:**

- Create the file `task8.py` and add the required comment header.
- Write a function named `histogram` that:
  - Takes a string as a parameter.
  - Creates an empty dictionary to store the letter counts.
  - Uses a `for` loop to go through each character in the string, skipping spaces.
  - Counts how many times each letter occurs, using the letter as the key and its count as the value.
  - Uses a second `for` loop to print each letter followed by stars (`*`) representing its count.
- Write a `main()` function that:
  - Calls `histogram("hello amma")`.
  - Calls `histogram()` a second time with a string of your choice.
- Add a call to the `main()` function.
- Run your script to test it.

**Expected Output** (for `histogram("hello amma")`):

```text
h *
e *
l **
o *
a **
m **
```

---

## Part B Sign-Off

- Commit and push your `Lab04` folder to your GitHub repo `SRT111F2026`.
- Submit a PDF named using your Seneca username (e.g., `yoursenecausername.pdf`) on Blackboard.
- Your PDF must include:
  - Task 5 screenshot(s)
  - Task 6 screenshot(s)
  - Task 7 screenshot(s)
  - Task 8 screenshot(s)
- Ensure the code and output are clearly readable. Screenshots should be high-resolution (minimum 800x600) and not blurry.
- Blurry or unreadable submissions will be returned for redo. Resubmissions will only be graded as **Satisfactory** with a grade of 0, provided the work is satisfactory.
