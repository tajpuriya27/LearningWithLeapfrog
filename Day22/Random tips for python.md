## TIP1 - In-place swapping of two numbers.
Python provides an intuitive way to do assignments and swapping in one line.
```oython
x, y = 10, 20
print(x, y)
 
x, y = y, x
print(x, y)
 
#1 (10, 20)
#2 (20, 10)
```

The assignment on the right seeds a new tuple. While the left one instantly unpacks that (unreferenced) tuple to the names \<a> and \<b>.  
Once the assignment is through, the new tuple gets unreferenced and flagged for garbage collection. The swapping of variables also occurs at eventually.



## TIP2 - Chaining of comparison operators.

Aggregation of comparison operators is another trick that can come handy at times.
```python
n = 10
result = 1 < n < 20
print(result)

# True

result = 1 > n <= 9
print(result)

# False
```

## TIP3 - Use of Ternary operator for conditional assignment.
- Ternary operators are a shortcut for an if-else statement and also known as conditional operators.
    ```python
    [on_true] if [expression] else [on_false]
    ```

>The below statement is doing the same what it is meant to i.e. “assign 10 to x if y is 9, otherwise assign 20 to x“.
>```python
>x = 10 if (y == 9) else 20
>```

Likewise, we can do the same for class objects.
```python
x = (classA if y == 1 else classB)(param1, param2)
```
In the above example, classA and classB are two classes and one of the class constructors would get called.

Below is one more example with a no. of conditions joining to evaluate the smallest number.
```python
def small(a, b, c):
	return a if a <= b and a <= c else (b if b <= a and b <= c else c)
	
print(small(1, 0, 1))
print(small(1, 2, 2))
print(small(2, 2, 3))
print(small(5, 4, 3))

#Output
#0 #1 #2 #3
```
We can even use a ternary operator with the list comprehension.

## TIP4 - Storing elements of a list into new variables.
We can use a list to initialize a no. of variables. While unpacking the list, the count of variables shouldn’t exceed the no. of elements in the list.
```python
testList = [1,2,3]
x, y, z = testList

print(x, y, z)

#-> 1 2 3
```

## TIP5 - Use the Interactive “_” operator.
In the Python console, whenever we test an expression or call a function, the result dispatches to a temporary name, _ (an underscore).
```python
>>> 2 + 1
3
>>> _
3
>>> print _
3
```
The “_” references to the output of the last executed expression.