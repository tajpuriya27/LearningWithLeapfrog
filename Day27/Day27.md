
# Day27 - Python NumPy

- NumPy stands for Numerical Python.
- NumPy is a Python library used for working with arrays.
- It also has functions for working in domain of linear algebra, fourier transform, and matrices.
- NumPy was created in 2005 by Travis Oliphant. It is an open source project and you can [use it freely](https://github.com/numpy/numpy).


### Why?
- In Python we have lists that serve the purpose of arrays, but they are slow to process.

- NumPy aims to provide an array object that is up to 50x faster than traditional Python lists.

- The array object in NumPy is called ndarray, it provides a lot of supporting functions that make working with ndarray very easy.

- Arrays are very frequently used in data science, where speed and resources are very important.


## Why is NumPy Faster Than Lists?
NumPy arrays are stored in locality of reference manner i.e. NumPy arrays are stored at one continuous place in memory unlike lists, so processes can access and manipulate them very efficiently.

Also it is optimized to work with latest CPU architectures.

## Which Language is NumPy written in?
NumPy is a Python library and is written partially in Python, but most of the parts that require fast computation are written in C or C++.


# Installation of NumPy

You must have Python and PIP already installed on a system, then installation of NumPy is very easy following below steps.

### Install it using this command:
```
C:\Users\Your Name>pip install numpy 
```

> If this command fails, then use a python distribution that already has NumPy installed like, Anaconda, Spyder etc.

## Import NumPy
Once NumPy is installed, import it in your applications by adding the import keyword:
```python
import numpy
```
Now NumPy is imported and ready to use.

Example
```python
import numpy

arr = numpy.array([1, 2, 3, 4, 5])

print(arr)
```

```python
NumPy as np
```

NumPy is usually imported under the np alias.

alias: In Python alias are an alternate name for referring to the same thing.

## Create an alias with the as keyword while importing:
```python
import numpy as np
```
Now the NumPy package can be referred to as np instead of numpy.

Example
```python
import numpy as np

arr = np.array([1, 2, 3, 4, 5])

print(arr)
```

## Checking NumPy Version
The version string is stored under __version__ attribute.

Example
```python
import numpy as np

print(np.__version__)
```

## Create a NumPy ndarray Object
- NumPy is used to work with arrays.
- The array object in NumPy is called ndarray.

We can create a NumPy ndarray object by using the array() function.
```python
import numpy as np
arr = np.array([1, 2, 3, 4, 5])
print(arr)
print(type(arr))
```

To create an ndarray, we can pass a list, tuple or any array-like object into the array() method, and it will be converted into an ndarray:

Use a tuple to create a NumPy array:
```python
import numpy as np
arr = np.array((1, 2, 3, 4, 5))
print(arr)
```

## Dimensions in Arrays
### 0-D Arrays
0-D arrays, or Scalars, are the elements in an array. Each value in an array is a 0-D array.

EX: Create a 0-D array with value 42
```python
import numpy as np

arr = np.array(42)

print(arr)
```

### 1-D Arrays
An array that has 0-D arrays as its elements is called uni-dimensional or 1-D array.

These are the most common and basic arrays.

EX: Create a 1-D array containing the values 1,2,3,4,5:
```python
import numpy as np
arr = np.array([1, 2, 3, 4, 5])
print(arr)
```

### 2-D Arrays
An array that has 1-D arrays as its elements is called a 2-D array.

These are often used to represent matrix or 2nd order tensors.

NumPy has a whole sub module dedicated towards matrix operations called numpy.mat

EX: Create a 2-D array containing two arrays with the values 1,2,3 and 4,5,6:
```python
import numpy as np

arr = np.array([[1, 2, 3], [4, 5, 6]])

print(arr)
```

### 3-D arrays
An array that has 2-D arrays (matrices) as its elements is called 3-D array.

These are often used to represent a 3rd order tensor.

EX: Create a 3-D array with two 2-D arrays, both containing two arrays with the values 1,2,3 and 4,5,6:
```python
import numpy as np

arr = np.array([[[1, 2, 3], [4, 5, 6]], [[1, 2, 3], [4, 5, 6]]])

print(arr)
```

## Check Number of Dimensions?
NumPy Arrays provides the ndim attribute that returns an integer that tells us how many dimensions the array have.

EX: Check how many dimensions the arrays have:
```python
import numpy as np

a = np.array(42)
b = np.array([1, 2, 3, 4, 5])
c = np.array([[1, 2, 3], [4, 5, 6]])
d = np.array([[[1, 2, 3], [4, 5, 6]], [[1, 2, 3], [4, 5, 6]]])

print(a.ndim)
print(b.ndim)
print(c.ndim)
print(d.ndim)
```

### Higher Dimensional Arrays
An array can have any number of dimensions.

When the array is created, you can define the number of dimensions by using the ndmin argument.

EX: Create an array with 5 dimensions and verify that it has 5 dimensions:
```python
import numpy as np

arr = np.array([1, 2, 3, 4], ndmin=5)

print(arr)
print('number of dimensions :', arr.ndim)
```

In this array the innermost dimension (5th dim) has 4 elements, the 4th dim has 1 element that is the vector, the 3rd dim has 1 element that is the matrix with the vector, the 2nd dim has 1 element that is 3D array and 1st dim has 1 element that is a 4D array.
