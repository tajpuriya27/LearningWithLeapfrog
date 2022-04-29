
# Day17- Python Function

A function is an independent and reusable block of code which you can call any no. of times from any place in a program.  
It is an essential tool for programmers to split a big project into smaller modules.

## Syntax
```python
# Single line function
def single_line(): statement
```
  
Python Function with docstring:
```python
def fn(arg1, arg2,...):
    """docstring"""
    statement1
    statement2
```

Nested Python Function
```python
def fn(arg1, arg2,...):
    """docstring"""
    statement1
    statement2
    def fn_new(arg1, arg2,...):
        statement1
        statement2
        ...
    ...
```

## Few Points about Python Functions:
1. The “def” call creates the function object and assigns it to the name given.
2. We can further re-assign the same function object to other names.
3. We should give a unique name to your function and follow the same rules while naming the identifiers.
4. It is a professional pratice to add a meaningful docstring to explain what the function does.
5. start the function body by adding valid Python statements each indented with four spaces.
6. We can also add a statement to return a value at the end of a function. However, this step is optional.
7. Since def is a statement, so we can use it anywhere a statement can appear – such as nested in an if clause or within another function.

### Example:
```python
def typeOfNum(num): # Function header
    # Function body
    if num % 2 == 0:
        def message():
            print("You entered an even number.")
    else:
        def message():
            print("You entered an odd number.")
    message()
# End of function

typeOfNum(2)  # call the function
typeOfNum(3)  # call the function again
```

### Polymorphism in Python
In Python, functions polymorphism is possible as we don’t specify the argument types while creating functions.

Polymorphism means, the behavior of a function may vary depending upon the arguments passed to it. The same function can accept arguments of different object types.

#### Expample:
```python
#defining function 
def product(x, y) : return x * y

# calling function passing arguments 4, 9
print(product(4, 9)) # function returns 36

# calling same function passing string-'python' and number - 2
print(product('Python!', 2))  # function returns
                              # Python!Python!
```


### Parameters & Arguments:
We often use the terms parameters and arguments interchangeably. However, there is a slight difference between them.

Parameters are the variables used in the function definition whereas arguments are the values we pass to the function parameters.

#### Notes:
>The argument gets assigned to the local variable name once passed to the function.  
Changing the value of an argument inside a function doesn’t affect the caller.  
If the argument holds a mutable object, then changing it in a function impacts the caller.  
We call the passing of immutable arguments as Pass by Value because Python doesn’t allow them to change in place.  
The passing of mutable arguments happens to be Pass by Pointer in Python because they are likely to be affected by the changes inside a function.