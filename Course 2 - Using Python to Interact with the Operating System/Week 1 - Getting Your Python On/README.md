# Using Python to Interact with the Operating System - Week 1 - Getting Your Python On

## Getting Ready for Python

### Getting Familiar with the Operating System
* The operating system (OS) manages everthing that goes on the in the computer.
* There are 2 main parts in OS:-
 * Kernel: Main core of an OS; talks directly to hardware and manages systems resources.
 * User space: Space that users interact with; basically everything outside of the kernel.
* Major OS:-
 * Windows: Developed by Microsoft.
 * Mac OS: Developed by Apple.
 * Linux: Named after the kernel developed by Linus Torvalds; open source software.
 * Unix: Developed by Bell Labs in the 70s; Linux based on Unix principle. 
* Python is a great tool because it's a cross-platform language.

### Getting Your Computer Ready for Python
* Check if Python is installed using command "python --version" or "python -V".
* Python Standard Library comes with standard Python installation but there are tons of other things that we might want to do in our scripts and are not in the standard library.
* We can browse Python modules through the Python Package Index, PyPI.
* External modules are managed with a command line tool called pip.

---

## Running Python Locally

### Interpreted vs. Compiled Languages
* Compiled language needs to feed source code into compiler, which translates the source code into machine level language. 
 * Compiled program is super fast to run, but the compilation process itself can take a bit of time.
 * Example of compiled language: C, C++, Go and Rust.
* Interpreted language rely on an intermediary program called an interpreter. 
 * Source code does not need to be compiled to execute.
 * Same source code can be read by interpreters running on different operating systems without needing to make any additional changes. 
 * Generally runs slower than compiled languages.
 * Example of interpreted language: Python, Ruby, JavaScript, Bash and PowerShell.
* Java and C# use a mixed approach, meaning source code needs to be compiled into intermediate code, which is supportable code that can be executed on different platforms.

### How to Run a Python Script
* Once you close the interpreter, the code you wrote isn't even saved.
 * To make our code more permanent, we can store it in files. Saved Python scripts usually end with a.py extension (ex. hello_world.py).
* To run a Python script saved on a Windows system, you can just type the name of your script and the operating system will recognize as the pipeline executable from the file extension. On Linux and Mac OS, you can execute the script by calling the pipeline interpreter followed by the name of the file.
* Inserting a shebang line (ex. #!/usr/bin/env python3) as the first line tells the operating system what command we want to use to execute the script.

### Your Own Python Modules
* In programming, we often reuse code that we've written or someone else has written. This is called code reuse and nearly all languages provide some way of doing it.
* As our scripts get bigger and more complicated, we want to be able to reuse more than a single function. We might even want to reuse entire scripts and other programs that we write.
* Duplicating code in this way has an ugly downsides. 
 * Every time you need to make a change to either script, you have to remember to do it to both places. That means you'd have to do any updates and bug fixes twice.
 * If your coworkers want to use the same e-mail code you wrote for their own projects, they'd probably have to go and create new copies.
* To avoid this, we can put the code we want to reuse into a separate module. 
* To use them in an interpreter or script, we can import a module by typing import (ex. import areas).

### What is an IDE?
* Integrated Development Environment (IDE) refers to a code editor with some handy extra capabilities that make writing scripts a lot easier. 
* Features in code editors:- 
 * Syntax highlighting.
  * Recognizes the language we are writing our code in, and highlights the pieces of code that make up the syntax of the language. 
 * Code completion.
  * Editor automatically complete the names of the variables and functions.
* Don't be completely tied to just one editor. It's possible you may need to debug a problem on the computer with a different editor installed, and you don't want to waste time installing your preferred editor.

---

## Credit
* [Coursera - Using Python to Interact with the Operating System - Week 1](https://www.coursera.org/learn/python-operating-system/home/week/1)
