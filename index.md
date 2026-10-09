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
- Use list methods to perform common list operations.
- Construct sets to store unique, unordered items.
- Compare lists and sets, highlighting differences in ordering and duplication.
- Apply set operations to compare sets.
- Create dictionaries with key–value pairs and access values using keys.
- Differentiate between index-based access in lists and key-based access in dictionaries.
- Traverse dictionaries using loops and use them to solve a counting problem.
- Use functions and a `main()` function to organize programs that work with data structures.

## Required Comment Header

For every script created in this lab include the following comment block at the top of the file/cell.

```python
# Author: Your Name
# Date: YYYY-MM-DD
# Purpose: Brief description of what the program does.
```

---

# Part A - In-Class Lab [30% of Lab Marks]

Complete all assigned in-class tasks during your scheduled lab.

**Part A Marking (3 marks):**

| Task | Marks |
|---|---|
| Task 1 - Creating Lists and List Concatenation | 1.0 |
| Task 2 - Using List Methods to Add and Remove Elements | 1.0 |
| Task 3 - Modifying a List, Looping, and Removing Duplicates | 1.0 |
| **Total** | **3** |

> Marks are awarded only when the required functions and methods are used as instructed. Correct output alone is not enough.

- This part can be completed in **Jupyter Lab** or **VS Code**. You have a choice. I recommend using **Jupyter Lab**.
  - If you are using Jupyter Lab, then please create a single notebook file called `Lab4.ipynb` and complete each task in a unique cell.
  - If you are using VS Code, then just follow the instructions for each task and create `.py` files.
- Demonstrate your completed work to the professor before leaving the lab.
- The professor may ask you to explain portions of your code.
- No PDF submission is required for Part A unless otherwise instructed.

<details>
  
<summary><b>Quick Reference: Lists</b></summary>

A list is an ordered collection of items, created with square brackets `[]` and commas between elements. Lists are mutable, so their contents can be changed after creation.

```python
numbers = [1, 2, 3, 4]
mixed_list = [1, "two", 4.5, True]

print(numbers[0])    # Output: 1  (indices start at 0)
numbers[1] = 20      # change the element at index 1
print(numbers)       # Output: [1, 20, 3, 4]
```

**Lists are changed in place.** When you pass a list to a function, the function receives the *same* list, not a new one. Any change the function makes (such as `append()`, `insert()`, or `pop()`) also changes the original list.

```python
def add_item(items):
    items.append(99)

values = [1, 2, 3]
add_item(values)
print(values)        # Output: [1, 2, 3, 99]  (the original list changed)
```

To keep the original list unchanged, work on a **copy** using the `copy()` method:

```python
def add_item(items):
    new_items = items.copy()   # a separate list with the same elements
    new_items.append(99)
    return new_items

values = [1, 2, 3]
result = add_item(values)
print(values)        # Output: [1, 2, 3]       (original unchanged)
print(result)        # Output: [1, 2, 3, 99]
```

</details>

### Task 1 - Creating Lists and List Concatenation

**Objective:** Practice creating Python lists, storing values in them, and concatenating lists inside a function using the `+` operator.

**Instructions:**

- Create a file named `task1.py` and add the required comment header.
- Write a function named `combine_lists` that:
  - Takes two lists, `list1` and `list2`, as parameters.
  - Combines them using the `+` operator.
  - Returns the combined list.
  - *Hint:* `[1, 2] + [3, 4]` results in `[1, 2, 3, 4]`.
- Write a `main()` function that:
  - Creates a list called `mylist1` that stores the first three odd numbers: 1, 3, 5.
  - Creates a list called `mylist2` that stores the first three even numbers: 0, 2, 4.
  - Calls `combine_lists()`, passing `mylist1` and `mylist2` as arguments.
  - Stores the returned list in a variable called `mylist`.
  - Prints `mylist`.
- Add a call to the `main()` function.
- Run your script to test it.

**Expected Output:**

```text
[1, 3, 5, 0, 2, 4]
```

### Task 2 - Using List Methods to Add and Remove Elements

**Objective:** Practice using common list methods (`append()`, `insert()`, `pop()`, and `index()`) inside a function, and use `copy()` so the original list is not changed in place.

**Instructions:**

- Create a file named `task2.py` and add the required comment header.
- Write a function named `modify_list` that:
  - Takes a list, `numbers`, as a parameter.
  - Creates a copy of the list using the `copy()` method and stores it in a new variable.
  - Uses the `append()` method to add the number 7 to the end of the **copy**.
  - Uses the `insert()` method to insert the number 0 at index 0 of the **copy**.
  - Uses the `pop()` method to remove the element at index 2 of the **copy**.
  - Returns the modified copy.
- Write a `main()` function that:
  - Creates a variable `mylist` that contains the first 6 natural numbers: `[1, 2, 3, 4, 5, 6]`.
  - Calls `modify_list()`, passing `mylist` as an argument, and stores the returned list in a variable called `new_list`.
  - Prints `mylist` and `new_list` with labels, as shown in the expected output.
  - Uses the `index()` method to find the index of the element `6` in `new_list`, stores it in a variable, and prints the message shown in the expected output.
- Add a call to the `main()` function.
- Run your script to test it.

**Expected Output:**

```text
Original list: [1, 2, 3, 4, 5, 6]
Modified list: [0, 1, 3, 4, 5, 6, 7]
The element 6 is present at index 5
```

> **Think about it:** Temporarily remove the `copy()` step so the function changes `numbers` directly, then run your script again. What happens to `mylist`? Be ready to explain why. Put the `copy()` step back before you demonstrate your work.

### Task 3 - Modifying a List, Looping, and Removing Duplicates

**Objective:** Practice updating a list element by its index, using a `for` loop inside a function to iterate over a list, and comparing how lists and sets handle duplicates and order.

**Instructions:**

- Create a file named `task3.py` and add the required comment header.
- Write a function named `print_names` that:
  - Takes a list of names as a parameter.
  - Uses a `for` loop to print each name on a separate line.
- Write a function named `remove_duplicates` that:
  - Takes a list of names as a parameter.
  - Converts the list to a set and returns the set.
  - *Hint:* `set(my_list)` creates a set from a list.
- Write a `main()` function that:
  - Creates a list variable called `students` with the following names: Ama, Eden, Maija, Daniel, Ibrahim.
  - Updates the element at index 1 to `"Maggy"`. *Hint:* Remember that list indices start at 0.
  - Calls `print_names()`, passing `students` as an argument.
  - Some students signed the attendance sheet twice. Creates a list called `attendance` with the following names: Ama, Eden, Ama, Daniel, Eden.
  - Prints `attendance`.
  - Calls `remove_duplicates()`, passing `attendance` as an argument, stores the returned set in a variable called `unique_attendance`, and prints it.
- Add a call to the `main()` function.
- Run your script to test it.

**Expected Output:**

```text
Ama
Maggy
Maija
Daniel
Ibrahim
['Ama', 'Eden', 'Ama', 'Daniel', 'Eden']
{'Ama', 'Eden', 'Daniel'}
```

> **Note:** The list keeps every name in its original order, including duplicates. The set keeps only unique names and does not preserve order, so your set may print in a different order.

---

# Part B - Take-Home Lab [70% of Lab Marks]

Complete the following tasks independently after the scheduled lab using VS Code.

**Part B Marking (7 marks):**

| Task | Marks |
|---|---|
| Task 4 - Creating Sets with a Function | 1.0 |
| Task 5 - Set Operations | 1.0 |
| Task 6 - Creating Dictionaries with a Function | 1.0 |
| Task 7 - Traversing a Dictionary | 2.0 |
| Task 8 - Using a Dictionary for Problem Solving | 2.0 |
| Submission requirements (comment headers, Git push, PDF named correctly, readable screenshots) | upto 100% deduction may apply |
| **Total** | **7** |

> Marks are awarded only when the required functions and methods are used as instructed. Correct output alone is not enough.

**Before You Begin:**

- Open your local Git repository `SRT111F2026` on your computer.
- Create a new folder named `Lab04` inside the repository.
- Open the `Lab04` folder in VS Code.
- Create all Python files for this lab (`task4.py`, `task5.py`, `task6.py`, `task7.py`, `task8.py`) inside the `Lab04` folder.

**For each task:**

- Run the script using the VS Code terminal.
- Take a screenshot that clearly shows:
  - Your code in the editor.
  - The terminal output, including your username visible in the terminal.
- Insert the screenshots into a Word document under a heading that matches the task name (e.g., **Task 5**, **Task 6**). You will export this Word document to PDF and submit it on Blackboard.


<details>
<summary><b>Quick Reference: Sets</b></summary>

A set stores unique, unordered items. Sets are created with curly brackets, and duplicate values are automatically ignored.

```python
myset = {"apples", "oranges", "kiwi", "oranges"}
print(myset)    # Output (order may vary): {'kiwi', 'apples', 'oranges'}
```

To create an **empty** set, use `set()`. Do **not** use `{}`, because that creates an empty dictionary. Use the `add()` method to add an element to a set.

```python
numbers = set()
numbers.add(10)
numbers.add(20)
numbers.add(10)   # duplicate, ignored
print(numbers)    # Output: {10, 20}
```

</details>

### Task 4 - Creating Sets with a Function

**Objective:** Practice creating sets in Python by completing a function that uses a loop and conditional logic to filter numbers by divisibility.

**Instructions:**

- Create a file named `task4.py` and add the required comment header.
- Copy the following starter code into your file, below the comment header:

```python
def build_the_set(divisor):
    # Complete this function
def main():

    s3 = build_the_set(3)
    print("s3: ", s3)
    print("----------------------------------------")

    # create s5 by calling build_the_set(), then print it and a separator line, following the s3 example above

    # create s7 by calling build_the_set(), then print it and a separator line, following the s3 example above

    # create s11 by calling build_the_set(), then print it, following the s3 example above

main()
```

> **Note:** The starter code will not run as-is, because a function cannot contain only a comment. It will run once you complete `build_the_set()`.

- Complete the `build_the_set()` function so that it:
  - Creates an empty set.
  - Uses a `for` loop to iterate over the numbers from 0 to 50 (inclusive).
  - Uses an `if` statement to check whether each number is divisible by `divisor`.
  - Adds each divisible number to the set using the `add()` method.
  - Returns the set.
- In `main()`, complete each comment by following the `s3` example:
  - Create `s5`, `s7`, and `s11` (numbers from 0 to 50 divisible by 5, 7, and 11) by calling `build_the_set()`.
  - Print each set and a separator line, in the same format as `s3`.
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


<details>
<summary><b>Quick Reference: Set Operations</b></summary>

Python sets support mathematical set operations directly, using either an operator or a method.

```python
set1 = {1, 2, 3}
set2 = {3, 4, 5}

# Union: all elements from both sets
print(set1 | set2)                        # Output: {1, 2, 3, 4, 5}
print(set1.union(set2))                   # Output: {1, 2, 3, 4, 5}

# Intersection: elements common to both sets
print(set1 & set2)                        # Output: {3}
print(set1.intersection(set2))            # Output: {3}

# Difference: elements in set1 but not in set2
print(set1 - set2)                        # Output: {1, 2}
print(set1.difference(set2))              # Output: {1, 2}

# Symmetric difference: elements in either set, but not in both
print(set1 ^ set2)                        # Output: {1, 2, 4, 5}
print(set1.symmetric_difference(set2))    # Output: {1, 2, 4, 5}
```

</details>

### Task 5 - Set Operations

**Objective:** Practice applying a set operation to existing sets and passing sets as function arguments.

**Instructions:**

- Create the file `task5.py` and add the required comment header.
- Copy your completed `build_the_set()` function and `main()` function from Task 4 (from `task4.py` or your `Lab4.ipynb` cell).
- Write a new function named `s3_or_s5` that:
  - Takes two sets, `s3` and `s5`, as parameters.
  - Returns a set containing all elements that are in `s3` or `s5`, but **not in both**.
  - *Hint:* Use the symmetric difference operator `^` or the `symmetric_difference()` method.
- In `main()`, remove the code for `s7` and `s11`. Then call `s3_or_s5()`, passing `s3` and `s5` as arguments, store the returned set in a variable, and print it with a label.
- Run your script to test it.

**Expected Output:**

```text
s3:  {0, 3, 6, 9, 12, 15, 18, 21, 24, 27, 30, 33, 36, 39, 42, 45, 48}
----------------------------------------
s5:  {0, 5, 10, 15, 20, 25, 30, 35, 40, 45, 50}
----------------------------------------
s3_or_s5:  {3, 5, 6, 9, 10, 12, 18, 20, 21, 24, 25, 27, 33, 35, 36, 39, 40, 42, 48, 50}
```

> **Note:** Sets are unordered, so your printed output may not appear in numerical order. Spacing after the labels and separator lines may also differ from the sample. The set contents must match.

<details>
<summary><b>Quick Reference: Dictionaries</b></summary>

A dictionary is a collection of **key–value pairs**. Instead of numeric indexes, you use a key to access its value. Since Python 3.7, dictionaries keep items in the order they were added.

```python
capitals = {}                      # empty dictionary
capitals["Canada"] = "Ottawa"      # add a key-value pair
capitals["Japan"] = "Tokyo"

print(capitals)                    # Output: {'Canada': 'Ottawa', 'Japan': 'Tokyo'}
print(capitals["Japan"])           # Output: Tokyo
print(len(capitals))               # Output: 2
print("Canada" in capitals)        # Output: True  (checks whether a key exists)
```

Looping over a dictionary with `.items()` gives you each key and its value:

```python
for key, value in capitals.items():
    print(key, "->", value)

# Output:
# Canada -> Ottawa
# Japan -> Tokyo
```

</details>

### Task 6 - Creating Dictionaries with a Function

**Objective:** Practice creating and returning a dictionary by generating key–value pairs from a range of numbers, and accessing a value by its key.

**Instructions:**

- Create the file `task6.py` and add the required comment header.
- Write a function named `times_ten` that:
  - Takes two parameters: `start` and `end`.
  - Creates an empty dictionary.
  - Uses a `for` loop to iterate over the numbers from `start` to `end` (inclusive).
  - Adds each number as a key, with the key multiplied by ten as its value.
  - Returns the dictionary.
- Write a `main()` function that:
  - Calls `times_ten(2, 6)`.
  - Stores the returned dictionary in a variable named `my_dictionary`.
  - Prints `my_dictionary`.
  - Prints the value stored under the key `4` using `my_dictionary[4]`.
- Add a call to the `main()` function.
- Run your script to test it.

**Expected Output:**

```text
{2: 20, 3: 30, 4: 40, 5: 50, 6: 60}
40
```

> **Note:** In `my_dictionary[4]`, `4` is a **key**, not a position. If the same values were stored in a list, `[20, 30, 40, 50, 60]`, then index 4 would give `60`.

### Task 7 - Traversing a Dictionary

**Objective:** Practice traversing a dictionary inside a function and formatting the output using the `.items()` method.

**Instructions:**

- Create the file `task7.py` and add the required comment header.
- Copy the following starter code into your file, below the comment header:

```python
def print_dictionary(d):
    # TO DO 1: Create a for in loop as instructed in the lab instructions.

def main():
    my_dict = {"Switzerland" : "Alps", "United States" : "Alaska Range", "Armenia" : "Caucasus", "Argentina" : "Andes", "Pakistan" : "Karakoram"}
    print_dictionary(my_dict)

main()
# TO DO 2: Run the script, and take the screenshot of code and output.
```

> **Note:** The starter code will not run as-is, because a function cannot contain only a comment. It will run once you complete `print_dictionary()`.

- **TO DO 1:** Inside `print_dictionary()`, use a `for ... in` loop with the `.items()` method to traverse the dictionary `d`. Inside the loop, print each key and value in the format `key : value`.
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
  - Converts the string to lowercase using `lower()`, so that uppercase and lowercase letters are counted together.
  - Creates an empty dictionary to store the letter counts.
  - Uses a `for` loop to go through each character in the string, skipping spaces.
  - Counts how many times each letter occurs, using the letter as the key and its count as the value.
  - Uses a second `for` loop to print each letter followed by stars (`*`) representing its count.
- Write a `main()` function that:
  - Calls `histogram("hello amma")`.
  - Calls `histogram()` a second time, passing **your own full name** as a string (for example, `histogram("Jane Smith")`, using your real name).
- Add a call to the `main()` function.
- Run your script to test it.

**Expected Output** (for `histogram("hello amma")`; the output for your name will be unique to you):

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
  - Task 4 screenshot(s)
  - Task 5 screenshot(s)
  - Task 6 screenshot(s)
  - Task 7 screenshot(s)
  - Task 8 screenshot(s)
- Ensure the code and output are clearly readable. Screenshots should be high-resolution (minimum 800x600) and not blurry.
- Blurry or unreadable submissions will be returned for redo. A resubmission will be marked **Satisfactory** if the work is acceptable, but it will receive a grade of 0.
