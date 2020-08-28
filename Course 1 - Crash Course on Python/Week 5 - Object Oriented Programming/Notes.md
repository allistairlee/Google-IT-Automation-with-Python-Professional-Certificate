# Crash Course of Python - Week 5 - Object-oriented Programming

## Learning Objectives
* Understanding Object-oriented Programming
* Create classes and methods
* Reusing code

---

## Object-oriented Programming
### What is Object-oriented programming?
* Python uses a programming pattern called object-oriented programming, which models concepts using:-
  * Classes - Represent and define concepts.
  * Objects - Instances of classes.
* Almost everything in Python is an object, including strings, lists, dictionaries, and numbers.
* Classes also have attributes and methods associated with them:-
  * Attributes are the characteristics associated to a type (ex. A file has lots of attributes, it has a name, a size, the date it was created, permissions to access it, its contents, and a whole lot more).
  * Methods are the functions associated to a type (ex. The typical file object focuses on the file's contents, and so this object has a bunch of methods to read and modify what's inside the file).

### Classes and Objects in Python
* We can use the type() function to figure out what class a variable or value belongs to (ex. type(" ") tells us that this is a string class).
  * The only attribute in this case is the string value, but there are a bunch of methods associated with the class (ex. upper(), isnumeric(), etc.). 
* The dir() function to print all the attributes and methods of an object. 
* The help() function will return the documentation for the corresponding class, showing all the methods for the class, along with parameters the methods receive, types of return values, and a description of the methods.

### Defining New Classes
* Create and define classes is similar to defining functions. 
  * Start with the class keyword, followed by the name of class and a colon. 
  * Python style guidelines recommend class names to start with a capital letter.
  * After the class definition line is the class body, indented to the right. 
  * Inside the class body, attributes for the class can be defined.
* ```Python
  class Apple:
    color = ""
    flavor = ""
  jonagold = Apple()
  jonagold.color = "red"
  jonagold.flavor = "sweet"
  ```

---

## Classes and Methods
### Instance Methods
* We can define methods within a class by creating functions inside the class definition. 
  * Methods are functions that operate on the attributes of a specific instance of a class.
  * Example: When we call the lower method on the string, we're making the contents of that specific string lowercase.
* Variables that have different values for different instances of the same class are called instance variables.

### Constructors and Other Special Methods
* Instead of creating classes with empty or default values, we can set these values when we create the instance.
  * We use a special method called a constructor ```__init__```
  * ```Python
    class Apple:
      def __init__(self, color, flavor):
        self.color = color
        self.flavor = flavor
    ````
* In addition, there is also the ```__str__``` special method. 
  * This method allows us to define how an instance of an object will be printed when it’s passed to the print() function.
  * ```Python
    class Apple:
      def __init__(self, color, flavor):
        self.color = color
        self.flavor = flavor
      def __str__(self):
        return "This apple is {} and its flavor is {}".format(self.color, self.flavor)
    ```
    
### Documenting Functions, Classes, and Methods
* The Python help function can be super helpful for easily pulling up documentation for classes and methods.
  * We can add documentation to our own classes, methods, and functions using docstrings, ```"""Documentation""".
  * ```Python
    def to_seconds(hours, minutes, seconds):
      """Returns the amount of seconds in the given hours, minutes and seconds."""
      return hours*3600+minutes*60+seconds
    ```
---

## Credit
* [Coursera - Crash Course on Python - Week 5 - Object Oriented Programming](https://www.coursera.org/learn/python-crash-course/home/week/5)
