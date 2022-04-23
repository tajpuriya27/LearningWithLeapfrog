
# Python Dictionay

A dictionary in Python is a scrambled collection of objects. Unlike other data types such as a list or a set which has a single value field, the dictionary type stores a key along with its value.  

The keys pair with values using a colon (:) while the commas work as a separator for the elements. Also, the entire dictionary object uses curly braces to enclose itself.  

Only keys inside a dictionary can’t have duplicates, but their values can repeat themselves.  

The combination of a key and its value, i.e. “key: value” represents a single element of a dictionary in Python.  

Only use immutable data types for the values while they can have duplicates.

```python
# Define a blank dictionary with no elements
blank_dict = {}
print(blank_dict)

# Define a dictionary with numeric keys
num_dict = {1: 'soccer', 2: 'baseball'}
print(num_dict)

# Define a dictionary with keys having different types
misc_dict = {'class': 'senior secondary', 1: [1, 2, 3,4,5]}
print(misc_dict)

# Create a dictionary with dict() method
get_dict_from_func = dict({1:'veg', 2:'non-veg'})
print(get_dict_from_func)

# Create a dictionary from a sequence of tuples
make_dict_from_seq = dict([(1,'jake'), (2,'john')])
print(make_dict_from_seq)
```
Output:
```
{}
{1: 'soccer', 2: 'baseball'}
{'class': 'senior secondary', 1: [1, 2, 3, 4, 5]}
{1: 'veg', 2: 'non-veg'}
{1: 'jake', 2: 'john'}
```

## Access Elements

Python dictionary has the key as an additional parameter. We can access the elements of a dictionary with the help of keys by using them as Index to the array operator ([]) or passing as Argument to the get() method.

Both methods will work the same, but the former will return a KeyError while the latter returns None if the element is not available.

```python
dict = {'Student Name': 'Suneel', 'Roll No.': 88, 'Subject': 'Python'}
print("dict['Student Name']: ", dict['Student Name'])
print("dict['Roll No.']: ", dict['Roll No.'])
print("dict['Subject']: ", dict['Subject'])
```
Output:
```
dict['Student Name']:  Suneel
dict['Roll No.']:  88
dict['Subject']:  Python
```
> Accessing an element with a non-existent key will return an error.

### Get method
```python
dict = {'Student Name': 'Suneel', 'Roll No.': 88, 'Subject': 'Python'}
print(dict.get('Student Name'))
print(dict.get('Roll No.'))
print(dict.get('Subject'))
```
Output:
```
Suneel
88
Python
```
## Append in Dictionary
- We can append a new item to an existing dict object with elements in the following two ways.   

1. ### Assignment to Append Elements
    ```python
    dict_append = {"1" : "Python", "2" : "Java"}
    print(dict_append)
    dict_append["3"] = "CSharp"
    print(dict_append)
    ```
    Output:
    ```
    {'1': 'Python', '2': 'Java'}
    {'1': 'Python', '2': 'Java', '3': 'CSharp'}
    ```
2. ### Update Method to Append Elements
    We can call the dictionary’s update method to append a new element to it.
    ```python
    dict_append = {"1" : "Python", "2" : "Java"}
    dict_append.update({"4" : "JavaScript"})
    print(dict_append)
    ```
    Output:
    ```
    {'1': 'Python', '2': 'Java', '4': 'JavaScript'}
    ```
## Update a Dictionary
Python allowed the dictionary object to be mutable. Hence, the add or update operations are permissible. We can push a new item or modify any existing with the help of the assignment operator.

Whenever we add an element whose key already exists, it’s value will get changed to the new value. On adding a fresh “key: value” pair, a new element will get added to the dictionary.   
    
1. ### Use Assignment
    ```python
    dict = {'Student Name': 'Suneel', 'Roll No.': 88, 'Subject': 'Python'}
    print("The student who left:", dict.get('Student Name'))
    dict['Student Name'] = 'Larry'
    print("The student who replaced: [Update]", dict.get('Student Name'))
    dict['Student Name'] = 'Jarry'
    print("The student who joined: [Addition]", dict.get('Student Name'))
    ```
    Output:
    
    ```
    The student who left: Suneel
    The student who replaced: [Update] Larry
    The student who joined: [Addition] Jarry
    ```

## Remove Element  
##### _4 different ways_
1. pop()
    - Most used.
    - It takes the key as the nput and deletes the corresponding element from the Python dictionary. It returns the value associated with the input key.

2. popitem()  
    - It removes and returns a random element (key, value) from the dictionary.
3. clear()
    - Used to flush everything.
4. del keyword  
    - It can help you delete individual items and consequently the whole dictionary object.
    ```python
    # Create a Python dictionary
    weekdays = {1:'sunday',2:'monday', 3:'Tuesday', 4:'Wednesday', 5: 'Thursday', 6:'Friday', 7:'Saturday'}

    # Delete a specific element using pop() method
    print(weekdays.pop(2)) 
    print(weekdays)

    # Delete an last element
    print(weekdays.popitem())
    print(weekdays)

    # Remove a specific element using del keyword
    del weekdays[4]
    print(weekdays)

    # Delete all elements from the dictionary, dictionary is still there.
    weekdays.clear()
    print(weekdays)

    # Finally, eliminate the dictionary object
    del weekdays
    # print(weekdays)
    # printing weekdays after elimination will show errors.
    ```
    Output:
    ```
    monday
    {1: 'sunday', 3: 'Tuesday', 4: 'Wednesday', 5: 'Thursday', 6: 'Friday', 7: 'Saturday'}
    (7, 'Saturday')
    {1: 'sunday', 3: 'Tuesday', 4: 'Wednesday', 5: 'Thursday', 6: 'Friday'}
    {1: 'sunday', 3: 'Tuesday', 5: 'Thursday', 6: 'Friday'}
    {}
    ```

## Iterate in Dictionary
We use for loop here.
```python
weekdays = {1:'sunday',2:'monday', 3:'Tuesday', 4:'Wednesday', 5: 'Thursday', 6:'Friday', 7:'Saturday'}
# iterate for keys only
for key in weekdays:
    print(key)
    
# iterate for keys and values
for key, value in weekdays.items():
    print(key, ':', value)

# iterate for keys and values
for key, value in weekdays.items():
    print({key},':',{value})

# Here 'key' and 'value' are variable and can be named as per the need.
```
Output:
```
1
2
3
4
5
6
7
1 : sunday
2 : monday
3 : Tuesday
4 : Wednesday
5 : Thursday
6 : Friday
7 : Saturday
{1} : {'sunday'}
{2} : {'monday'}
{3} : {'Tuesday'}
{4} : {'Wednesday'}
{5} : {'Thursday'}
{6} : {'Friday'}
{7} : {'Saturday'}
```

## Initializing List, Tuple, set & dictionary
```python
# initializing list:
# initializing list:
my_list = ['dharan', 'beautiful', 'city']
print(type(my_list), my_list)
print('\n')

# initializing tuple:
my_tuple = ('dharan', 'beutiful', 'city')
print(type(my_tuple), my_tuple)
print('\n')

# initializing set:
my_set = {'dharan', 'beautiful', 'city'}
print(type(my_set), my_set)
print('\n')

# initializing dictonay:
my_dict = {"city": "Dharan", "Adjective" : "Beautiful"}
print(type(my_dict), my_dict)
```
**Output:**
```
<class 'list'> ['dharan', 'beautiful', 'city']

<class 'tuple'> ('dharan', 'beutiful', 'city')

<class 'set'> {'dharan', 'city', 'beautiful'}

<class 'dict'> {'city': 'Dharan', 'Adjective': 'Beautiful'}
```
