
# Python List

Python list is a container like an array that holds an ordered sequence of objects. The object can be anything from a string to a number or the data of any available type.  
A list can also be both homogenous as well as heterogeneous. It means we can store only integers or strings or both depending on the need. Index can be used later to locate a particular item. The first index begins at zero, next is one, and so forth.  
It is very flexible and does not have a fixed size.   
List objects are mutable. i.e. Python allows modifying a list or its elements via assignments as well as through the built-in list methods.  
Lists in Python can be declared by placing elements inside **square brackets separated by commas**.   

Creating Python List: 
```python
mylist = ['n0', 'n1', 'n2', 'n3']
print(mylist[0])
print(mylist)
#n0
#['n0', 'n1', 'n2', 'n3']
``` 

Using List() constructor:
 ```python
mylist = list(['n0', 'n1', 'n2', 'n3'])
print(mylist[0])
print(mylist)
#n0
#['n0', 'n1', 'n2', 'n3']
print(len(mylist))
#4
```

List Slicing
```python
mylist = ['n0', 'n1', 'n2', 'n3', 'n4', 'n5', 'n6']
print(mylist[2:5])
#['n2', 'n3', 'n4']
print(mylist[2:-1])
#['n2', 'n3', 'n4', 'n5']
print(mylist[:2])
#['n0', 'n1']
print(mylist[2:])
#['n2', 'n3', 'n4', 'n5', 'n6']
``` 

### Reverse a list   
It is effortless to achieve this by using a special slice syntax (::-1).     
Note that it is more memory intensive than an in-place reversal. 
```python
mylist = ['n0', 'n1', 'n2', 'n3', 'n4', 'n5', 'n6']
print(mylist[::-1])
#['n6', 'n5', 'n4', 'n3', 'n2', 'n1', 'n0']
print(mylist[::-2])
#['n6', 'n4', 'n2', 'n0'] #Skip every second memeber
```
### Copy a list  
Operator :: is used.
>```python
>mylist = ['n0', 'n1', 'n2', 'n3', 'n4', 'n5', 'n6']
>print(id(mylist))
>list1 = mylist[::]
>print(id(list1))
>print(list1)
>```
>Output:
>``` -- None -- 
>1977285752064
>1977285686208
>['n0', 'n1', 'n2', 'n3', 'n4', 'n5', 'n6']
>```

### Iterate Python List
Python provides a traditional for-in loop for iterating the element of a list one by one.
>```python
>mylist = ['n0', 'n1', 'n2', 'n3', 'n4', 'n5', 'n6'] 
>for element in mylist:
> 	print(element)
>```
>Output: 
>``` -- None -- 
>n0
>n1
>n2
>n3
>n4
>n5
>n6
>```

If we wish to use both the index and the element, then call the **enumerate()** function.

>```python
>mylist = ['n0', 'n1', 'n2', 'n3', 'n4', 'n5', 'n6'] 
>for index, element in enumerate(mylist):
> print(index, element)
>```
>Output: 
>``` -- None -- 
>0 n0
>1 n1
>2 n2
>3 n3
>4 n4
>5 n5
>6 n6
>```

### Add elements to a list
  
We can use assignment operator(=) to update an element or a range of items. 
>```python
>mylist = ['n0', 'n1', 'n2', 'n3', 'n4', 'n5', 'n6'] 
>mylist[4] = 'newItem'
>print(mylist)
>
>mylist[1:4] = ['Item1', 'Item2', 'Item3']
>print(mylist)
>```
>Output: 
>``` -- None -- 
>['n0', 'n1', 'n2', 'n3', 'newItem', 'n5', 'n6']
>['n0', 'Item1', 'Item2', 'Item3', 'newItem', 'n5', 'n6']
>```
 
