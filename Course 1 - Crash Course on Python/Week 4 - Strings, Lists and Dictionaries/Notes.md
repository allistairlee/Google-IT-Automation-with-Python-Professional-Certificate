# Crash Course of Python - Week 4 - Strings, Lists and Dictionaries

## Learning Objectives
* Create and use strings
* Create and use lists
* Create and use dictionaries
* Understand the difference between strings, lists, and dictionaries

---

## String
### What is a string?
* A **string** is a data type in Python that's used to represent a piece of text.
* Strings can be concatenated to build longer strings by using the plus sign or multiplied by a number, which multiplies the content of the string that many times.

### The Parts of a String
* The **string indexing** operation accesses the character in a given position or index using square brackets and the number of the position specified (ex. string[0]).
* To access the last character of a string, use negative indexes (ex. string[-1]).
* A **slice** is the portion of a string that can contain more than one character (ex. string[1:4]).

### Creating New Strings
* Strings in Python are immutable, meaning _they can't be modified_.
* We can locate the index that contains the letter g using animals.index("g"), which will return the index; in "lions tigers and bears", it's 8. 
* We can also use substrings to locate the index where the substring begins. animals.index("bears") would return 17, since that’s the start of the substring. 
* If there’s more than one match for a substring, the index method will return the first match. 
* If we try to locate a substring that doesn't exist in the string, we’ll receive a ValueError explaining that the substring was not found.

### String Reference Cheat Sheet
* [String Reference Cheat Sheet](https://github.com/allistairlee/Google-IT-Automation-with-Python-Professional-Certificate/blob/master/Course%201%20-%20Crash%20Course%20on%20Python/Week%204%20-%20Strings%2C%20Lists%20and%20Dictionaries/String%20Reference%20Cheat%20Sheet.md)

### Formatting String Cheat Sheet
* [Formatting String Cheat Sheet](https://github.com/allistairlee/Google-IT-Automation-with-Python-Professional-Certificate/blob/master/Course%201%20-%20Crash%20Course%20on%20Python/Week%204%20-%20Strings%2C%20Lists%20and%20Dictionaries/Formatting%20String%20Cheat%20Sheet.md)

---

## Lists
### What is a list?
* Square brackets are used to indicate where the list starts and ends in Python.
* In Python, strings and lists are both examples of **sequences**. There are other sequences too, and they all share operations like:-
 * Iterating over them using for loops.
 * Indexing using the len function to know the length of the sequence.
 * Using plus to concatenate two sequences.
 * Using in to verify if the sequence contains an element.

### Modifying the Contents of a List
* One of the ways that lists and strings are different is that lists are mutable. Which is another fancy word to say that they can change. This means we can add, remove, or modify elements in a list.
 * The append method adds a new element at the end of the list. 
 * The insert method inserts an element in a different position, instead of at the end, by taking an index as the first parameter and an element as the second parameter.
 * The remove method removes an element.
 * The pop method can also remove an element and receives an index.

### Lists and Tuples
* **Strings** are sequences of characters and are **immutable**.
* **Lists** are sequences of elements of any type and are **mutable**.
* **Tuples** are sequences of elements of any type that are **immutable**.
  * When using tuples the position of the elements inside the tuple have meaning.
  * Tuples can be **unpacked** whichwe can turn a tuple of elements into separate variables. 
  * Examples of tuples include:-
    * When a function returns more than one value, it's returning a tuple.
    * Store a filename and it's size.
    * Store the name and email address of a person.
    * Store a date and time and the general health of the system at any point in time.

### Iterating over Lists and Tuples
* Use **enumerate** method when iterate over lists or tuples.
* Using range method works BUT it's more idiomatic in Python to iterate through the elements of the list directly or using enumerate when we need the indexes.

### List Comprehension
* Since creating lists based on sequences is such a common task, Python provides a technique called **list comprehension**, which allows it to be done in just one line.
* List comprehensions let us create new lists based on sequences or ranges.

### Lists and Tuples Operations Cheat Sheet
* [Lists and Tuples Operations Cheat Sheet](https://github.com/allistairlee/Google-IT-Automation-with-Python-Professional-Certificate/blob/master/Course%201%20-%20Crash%20Course%20on%20Python/Week%204%20-%20Strings%2C%20Lists%20and%20Dictionaries/Lists%20and%20Tuples%20Operations%20Cheat%20Sheet.md)

---

## Dictionaries
### What is a dictionary?
* **Dictionaries** take the form of pairs of keys and values to store data.
 * Dictionaries are mutable.
 * Unlike lists, elements cannot be accessed using their position.
 
### Iterating Over Dictionaries
* Iterate over dictionaries using a for loop, just like with strings, lists, and tuples.
 * This will iterate over the sequence of keys in the dictionary. 
* If you want to access the corresponding values associated with the keys, you could use the keys as indexes. 
 * x = {key1:value1, key2:value2}
* If we only wanted to access the keys in a dictionary, we could use the keys() method on the dictionary: dictionary.keys(). 
* If you only wanted the values, you could use the values() method: dictionary.values().

---

## Credit
* [Coursera - Crash Course on Python - Week 4 - Strings, Lists and Dictionaries](https://www.coursera.org/learn/python-crash-course/home/week/4)
