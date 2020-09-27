# Using Python to Interact with the Operating System - Week 5 - Testing in Python

## Simple Tests
### What is testing?
* Software testing is a process of evaluating computer code to determine whether or not it does what you expect it to do.
* Writing tests can help wth:-
  * Eliminate bugs
  * Improve the reliability and the quality of automation
  
### Manual Testing and Automated Testing
* The **manual testing** is the most basic way of testing a script by running the test with different parameters and see if it returns the expected values.
* The automatic testing is codifying tests into its own software and code that can be run to verify that the programs do what we expect them to do. The goal of automatic testing is to automate the process of checking *if the returned value matches the expectations*.

---

## Unit Tests
### Unit Tests
* **Unit tests** are used to verify that *small isolated parts of a program are correct*.
* An important characteristic of a unit test is **isolation**.
* Unit test should only test the unit of code they target, the function or method that's being tested. This ensures that any success or failure of the test is caused by the behavior of the unit in question and doesn't result from some external factor like the network being down or a database server being unresponsive.

### Writing Unit Tests in Python
* Use the **unittest module** which includes classes and methods for creating unit tests to write unit tests in Python.

### Edge Cases
* Edge cases are inputs that produce unexpected results, and are found at the extreme ends of the ranges of input that programs could work with.
* Some of the edge case examples for a function that expects a number include:-
  * Passing zero to 
  * Negative numbers
  * Extremely large numbers

---

## Credit
* [Coursera - Using Python to Interact with the Operating System - Week 5 - Testing in Python](https://www.coursera.org/learn/python-operating-system/home/week/5)
