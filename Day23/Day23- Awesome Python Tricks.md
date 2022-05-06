
# Day23- Awesome Python Tricks

## Tips1 - Create a dictionary from two related sequences.
```python
t1 = (1, 2, 3)
t2 = (10, 20, 30)

print(dict (zip(t1,t2)))

#-> {1: 10, 2: 20, 3: 30}
```

## Tips2 - Implement a true switch-case statement in Python.
Here is the code that uses a dictionary to imitate a switch-case construct.

```python
def xswitch(x): 
	return xswitch._system_dict.get(x, None) 

xswitch._system_dict = {'files': 10, 'folders': 5, 'devices': 2}

print(xswitch('default'))
print(xswitch('devices'))

#1-> None
#2-> 2
```

## Tips3 - In line search for multiple prefixes in a string.
```python
print("http://www.google.com".startswith(("http://", "https://")))
print("http://www.google.co.uk".endswith((".com", ".co.uk")))

#1-> True
#2-> True
```

## Tips4 - Check the memory usage of an object.
In Python 2.7, a 32-bit integer consumes 24-bytes whereas it utilizes 28-bytes in Python 3.5. To verify the memory usage, we can call the <getsizeof> method.

In Python 2.7.
```python
import sys
x=1
print(sys.getsizeof(x))

#-> 24
```

In Python 3.5.
```python
import sys
x=1
print(sys.getsizeof(x))

#-> 28
```

## Tips5 - Find the most frequent value in a list.
```python
test = [1,2,3,4,2,2,3,1,4,4,4]
print(max(set(test), key=test.count))

#-> 4
```

## Tips6 - Return multiple values from functions.
Not many programming languages support this feature. However, functions in Python do return multiple values.

```python
# function returning multiple values.
def x():
	return 1, 2, 3, 4

# Calling the above function.
a, b, c, d = x()

print(a, b, c, d)

#-> 1 2 3 4
```

## Tips7 - Four ways to reverse string/list.
#### Reverse the list itself.
```python
testList = [1, 3, 5]
testList.reverse()
print(testList)

#-> [5, 3, 1]
```

### Reverse while iterating in a loop.
```python
for element in reversed([1,3,5]): print(element)

#1-> 5
#2-> 3
#3-> 1
```

### Reverse a string in line.
```python
"Test Python"[::-1]
```
This gives the output as ”nohtyP tseT”

### Reverse a list using slicing.
```python
[1, 3, 5][::-1]
```
The above command will give the output as [5, 3, 1].

## Tips8 - Combining multiple strings.
If we want to concatenate all the tokens available in a list, then:
```python
>>> test = ['I', 'Like', 'Python', 'automation']
Now, let’s create a single string from the elements in the list given above.

>>> print ''.join(test)
```

## Tips9 - Simplify if statement.
To verify multiple values, we can do in the following manner.
>if m in [1,3,5,7]:  
instead of:   
if m==1 or m==3 or m==5 or m==7:   
Alternatively, we can use   
‘{1,3,5,7}’   
instead of   
‘[1,3,5,7]’ for ‘in’ operator because ‘set’ can access each element by O(1).


## Tips10 -  Concatenating strings.
We can use ‘+’ to concatenate strings in the following manner.
```python
# See how to use '+' to concatenate strings.

    >>> print('Python' + ' Coding' + ' Tips')

# Output:

    Python Coding Tips
```