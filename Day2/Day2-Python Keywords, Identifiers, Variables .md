
# Day1-Python Keywords, Identifiers, Variables.

## Python Overview
 
- Case-sensitive.
- Indentation is whitespace.
- Statements not ending with semicolons(;).
- Newline will declare the end of statements.
    
## Python Keywords

- Special words which are reserved by python and have specific meaning.
- A total of 33 Keywords are present in Python.
- Keywords are also case-sensitive.
    
> List all Keywords using Python-shell  
> ```python
>    help>keywords
> ```  
> ```python
>    import keyword
>    keyword.kwlist
> ``` 

> Test if a provided "word" is Python Keyword using python-shell   
> ```python
>    import keyword
>    keyword.iskeyword("Word")
> ```

> Access Python shell  
>    Open command prompt and type
> ```python
> python
> ```

> Check installed python version
> ```python
> version
> ```

## Python Identifiers

- Identifiers are user-defined names to represent a variable, function,class, module or any other object. 
> Best practices for Python Identifiers  
> - Use a sequence of lowercase(a to z) or uppercase(A to Z). Programmer can mix up digits(0 to 9) or an underscore(_) while writing an identifier. For example - **Shape_1, Upload_to_db, etc** 
> - According to Python Documentation, an identifier can have unlimited length. Using a large name(more than 79 chars) would lead to a violation of a rule set by the **PEP-8** standard. Therefore, in best practice, an identifier can have a maximum length of 79 characters. 

> Practices that lead to syntax error 
> - Using a digit or underscore(`_`) to begin an identifier name. For example - **0Shape, _string1** 
> - Using keyword as an identifier leads to syntax error.
 
> Worst practices for Python Identifiers  
> - Using special Characters **['.' , '!', '@', '#', ' $', '%']** is avoided. For example- @index, #count, etc

> Check if an identifier is valid or not  
> ```python
>    str.isidentifier()
> ```
 
## Python Variables

- Variables is an conceptual memory location which holds the actual value and may change when required.
- Python variables don`t require declaration. Variables in python are assigned as soon as they appear in the program.
> For example:  
>In C++
> ```cpp
> int sum;      //integer variable sum is declared
> sum = 10;     //sum is initialized with 10.
> ```
> In Python
> ```python
> sum = 10   #integer variable sum is initialized with 10.
> ``` 
> In python, variable declaration is not required. They are initialized as soon as they appear in the program.
