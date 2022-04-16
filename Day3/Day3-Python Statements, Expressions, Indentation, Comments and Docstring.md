
# Day3- Python Statements, Expressions, Indentation, Comments and Docstring

## Python Statement ↓ 
- A statement is a logical instruction that a python interpreter can interpret and execute.

## Python Expression ↓
- A statement with operator in it.

## Python Indentation ↓ 
- Many of the high-level programming languages like C, C++, C# use braces { } to mark a block of code. Python does it via indentation.
- A code block that represents the body of a function or a loop begins with the indentation and ends with the first unindented line.
- Python style guidelines (PEP 8) states that you should keep an indent size of four. However, Google has its unique style guideline which limits indenting up to two spaces. So you too can choose a different style, but it is recommended to follow the PEP8.

    ```cpp
    for(i=0; i<5; i++)
    {
    print("Hello World");
    }
    ``` 

    ```python
    for(i=0; i<5; i++)
    ^^^^print("Hello world")  #Here ^^^^ represents 4 space indentation.
    ``` 

## Python Comment  ↓ 
1. Single line Comment
    - \# is used for single line comment.

    ```python
    # This is single line comment in python
    ```

2. Multiline Comment 
    - To add multiline comments, the programmer should begin each line with the pound (#) symbol followed by a single space.   You can divide a comment into paragraphs. Just add an empty line with a hash mark between each para.

    ```python
    # To learn any language we must following points:
    # Learn from the basics
    # Don't get frustrated. Every programming language is tough at the
    # begining.
    # Code everyday
    ```

## Python Docstring ↓ 
- Python has the documentation strings (or docstrings) feature. It gives programmers an easy way of adding quick notes with every Python module, function, class, and method.
- You can define a docstring with the help of a triple-quotation mark.

    ~~~
    ```
    This is a documentation string of python. We can write a paragraph here for our future reference.
    ```
    ~~~

## Differences between Python Comment and Docstring?  ↓ 
- The strings beginning with triple quotes are still regular strings except the fact that they could spread to multiple lines. It means they are executable statements. And if they are not labeled, then they will be garbage collected as soon as the code executes.
- The Python interpreter won’t ignore them as it does with the comments. However, if such a string is placed immediately after a function or class definition or on top of a module, then they turn into docstrings. You can access them using the following special variable.

    ```python
    myobj.__doc__
    ```

    Example
    ~~~python
    def theFunction():
        '''
    This function demonstrates the use of docstring in Python.
        '''
    print("Python docstrings are not comments.")
    print("\nJust printing the docstring value...")
    print(theFunction.__doc__)
    ~~~
