
# Python Tuples

A Python tuple is a collection type data structure which is immutable by design and holds a sequence of heterogeneous elements

### Tuples v/s List
- Tuples store a fixed set of elements and don’t allow changes whereas the list has the provision to update its content.
- The list uses square brackets for opening and closing whereas, and a tuple has got parentheses for the enclosure.

### Simple examples to create a tuple
> ```python
> # create an empty tuple
> py_tuple = ()
> print("A blank tuple:", py_tuple)
>
> # create a tuple without using round brackets
> py_tuple = 33, 55, 77
>print("A tuple set without parenthesis:", py_tuple, "type:", type(py_tuple))
>
> # create a tuple of numbers
>py_tuple = (33, 55, 77)
>print("A tuple of numbers:", py_tuple)
>
># create a tuple of mixed numbers
># such as integer, float, imaginary
>py_tuple = (33, 3.3, 3+3j)
>print("A tuple of mixed numbers:", py_tuple)
>
># create a tuple of mixed data types
># such as numbers, strings, lists
>py_tuple = (33, "33", [3, 3])
>print("A tuple of mixed data types:", py_tuple)
>
># create a tuple of tuples
># i.e. a nested tuple
>py_tuple = (('x', 'y', 'z'), ('X', 'Y', 'Z'))
>print("A tuple of tuples:", py_tuple)
>```
> Output:
>```
>A blank tuple: ()
>A tuple set without parenthesis: (33, 55, 77) type: <class 'tuple'>
>A tuple of numbers: (33, 55, 77)
>A tuple of mixed numbers: (33, 3.3, (3+3j))
>A tuple of mixed data types: (33, '33', [3, 3])
>A tuple of tuples: (('x', 'y', 'z'), ('X', 'Y', 'Z'))
>```

### Using Built-in function "tuple()" to create tuple
>```python
>py_tuple = tuple({33, 55 , 77})
>print(type(py_tuple))
>print(py_tuple)
># creating tuple from list
>my_tuple = tuple([33,44,77])
>print(type(my_tuple))
>```
>Output:
>```
><class 'tuple'>
>(33,35,77)
><class 'tuple'>
>```

### Creating a tuple of size one
>```python
># A single element surrounded by parenthesis will create a string instead of a tuple
>>>> py_tuple = ('single')
>>>> type(py_tuple)
><class 'str'>
># You need to place a comma after the first element to create a tuple of size "one"
>>>> py_tuple = ('single',)
>>>> type(py_tuple)
><class 'tuple'>
># You can use a list of one element and convert it to a tuple
>>>> py_tuple = tuple(['single'])
>>>> type(py_tuple)
><class 'tuple'>
># You can use a set of one element and convert it to a tuple
>>>> py_tuple = tuple({'single'})
>>>> type(py_tuple)
><class 'tuple'>

### Access a tuple in Python
#### 1. Via Indexing
The simplest is the direct access method where you use the index operator [] to pick an item from the tuple. You can start indexing from the 0th position.

>```python
>vowel_tuple = ('a','e','i','o','u')
>print("The tuple:", vowel_tuple, "Length:", len(vowel_tuple))
>
># Indexing the first element
>print("OP(vowel_tuple[0]):", vowel_tuple[0])
>
># Indexing the last element
>print("OP(vowel_tuple[length-1]):", vowel_tuple[len(vowel_tuple) - 1])
>
># Indexing a non-existent member
># will raise the IndexError
>try:
>print(vowel_tuple[len(vowel_tuple)+1])
>except Exception as ex:
>print("OP(vowel_tuple[length+1]) Error:", ex)
>
># Indexing with a non-integer index
># will raise the TypeError
>try:
>print(vowel_tuple[0.0])
>except Exception as ex:
>print("OP(vowel_tuple[0.0]) >Error:", ex)
>
># Indexing in a tuple of tuples
>t_o_t = (('jan', 'feb', 'mar'), ('sun', 'mon', 'wed'))
>
># Accessing elements from the >first sub tuple
>print("OP(t_o_t[0][2]):", t_o_t[0][2])
>
># Accessing elements from the second sub tuple
>print("OP(t_o_t[1][2]):", t_o_t[1][2])
>```
>Output:
>```
>The tuple: ('a', 'e', 'i', 'o', 'u') Length: 5
>OP(vowel_tuple[0]): a
>OP(vowel_tuple[length-1]): u
>OP(vowel_tuple[length+1]) >Error: tuple index out of range
>OP(vowel_tuple[0.0]) Error: tuple indices must be integers or slices, not float
>OP(t_o_t[0][2]): mar
>OP(t_o_t[1][2]): wed
>```

#### 2. Via Reverse Indexing
Python tuple supports reverse indexing, i.e., accessing elements using the (-ve) index values.

The reverse indexing works in the following manner.
- The index -1 represents the last item. An index with value -2 will refer to the second item from the rear end.
    ```python
    vowel_tuple = ('a','e','i','o','u')
    print("The last object of tuple is '", vowel_tuple[-1], "'")
    print('The second- last object of tuple is', vowel_tuple[-2])
    ```
    Output:
    ```
    The last object of tuple is ' u '
    The second- last object of tuple is o
    ```
#### 3. Via Slicing
- Slice opertor(:) is used for slicing.
    ```python
    weekdays = ('mon0', 'tue1', 'wed2' ,'thu3', 'fri4', 'sat5', 'sun6')
    print(weekdays)
    # accessing elements leaving the first one
    print(weekdays[1:])

    # accessing elements between the first and fifth positions
    print(weekdays[1:5])

    # accessing elements after the fifth position
    print(weekdays[5:])

    # accessing the first five elements 
    print(weekdays[:5])

    # accessing elements that appears after
    # counting five from the rear end
    print(weekdays[:-5])

    # accessing five elements from the rear
    print(weekdays[-5:])

    # accessing elements from the start to end
    print(weekdays[:])
    ```
    Output: 
    ```
    ('mon0', 'tue1', 'wed2', 'thu3', 'fri4', 'sat5', 'sun6')
    ('tue1', 'wed2', 'thu3', 'fri4', 'sat5', 'sun6')
    ('tue1', 'wed2', 'thu3', 'fri4')
    ('sat5', 'sun6')
    ('mon0', 'tue1', 'wed2', 'thu3', 'fri4')
    ('mon0', 'tue1')
    ('wed2', 'thu3', 'fri4', 'sat5', 'sun6')
    ('mon0', 'tue1', 'wed2', 'thu3', 'fri4', 'sat5', 'sun6')
    ```