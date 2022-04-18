
# Python Numbers

Python numbers are a group of four data types: plain integer, long integer, floating-point and complex numbers. They not only support simple arithmetic calculations but can also be used in quantum computation as complex numbers.  

Python numbers are immutable objects so any change in the value would lead to the creation of a new object. Usually, assigning a numeric value to a variable will get the number object created.

```python
num = 10+5j				#complex number is assigned to num
print(type(num))		
print(id(num))			#The initial address of 'num' in memory

num = 10				#'num' gets new integer value
print(type(num))
print(id(num))			#Change in value caused 'num' have a new memory address.

y = num + 20
print(y)
print(id(num))
print(id(y))
```
Output:
```--None--
2257150318544

2257149297168
30
2257149297168
2257149297808
```

- Interestingly, Python 2.x had four built-in data types (**int, long, float and complex**) to represent numbers. Later Python 3.x removed the long and extended the int type to have unlimited length.

## Types:
- Key Points - Python numbers
    - The number types are automatically upcast(converted) in the following order.
        - **Int **→** Long → Float → Complex**
    - While integers in Python 3.x can be of any length, a float type number is only precise to fifteen decimal places.
    - If we need to use number systems other than decimal number system, it can be done using proper prefixes.
    
     ```python
        x = 0b101
        print(x)
        print(type(x))

        print(0b101 + 5)
        print(0o123)
        print(type(0x10))
        ```
    Output:
    ```no
        5

        10
        83
    ```
    If you use mixed data types in an expression, then all operands will turn to behave as the most complex type used.

    ```python
    num = 2 + 3.8  
    print(type(num))   
    #prints  as int('2') is implicitly converted into float.
    ```

    In Python 2.x, the division (/) will return an integer quotient as the output. While, in Python 3.x, the division (/) will return a float quotient as the output.
    
    ```python
    print(7/2)
    # prints 3 in python 2.x
    # prints 3.5 in python 3.x
    ```
    - The floor operator (//) returns the integer quotient, and the mod (%) operator gives the remainder. However, you can get both these by using the divmod() function.
    
    ```python
    print(divmod(7,2))
    
    print(7%2)
    print(7/2)
    print(7//2)
    ```
    Output:
    ```
    (3,1)
    1
    3.5
    3
    ```

## Type Converstion(casting) in python
- In python, any numeric data type convert into another complex type. This process is called as coercion in pythonic term. Int → Long → Float → Complex
  
    ```python
        print(2+4.5)
        #Output will be 6.5
    ```

Here, first integer(2) turned into a float (2.0) for addition, and the output is also a floating point number.
- Explicit conversion  
    We can use buit-in-functions such as int(),  float() and complex() to convert between types explicitly. These functions can even convert strings to numbers.
    ```python
    print(int(3.7))
    print(int(-3.4))
    print(float(3))
    ```
    Output:
    ```python
    3
    -3
    3.0
    ```

### List of different Modules to manipulate Python Numbers:
    1. Python Decimal __(import decimal)__  
    2. Python Fractions __(import fractions)__  
    3. Python Mathematics( __import math__ ) 
