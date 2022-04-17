
# Python Data-types

- In Python, we don’t need to declare a variable with explicitly mentioning the data type. This feature is famously known as **dynamic typing**. Python determines the type of a literal directly from the syntax at runtime.
    
    ```python
    var1 = 4.9	#python determines the data-type of var1 as float at runtime.
    var2 = 'Suneel'	#python determines the data-type of var2 as string.
    var3 = [2, 3, 'Suneel']	#determines the data-type of var3 as list at runtime
    var4= {2, 3, 'Leapfrog'} #determines the data-type of var4 as dictionary..
    var5 = 2022 #determines the data-type of var5 as integer at runtime.
    ```
    
- Everything including variables, functions, modules in Python is an object. Another interesting fact is that same variable, the label can refer values of different Python data types. 
    ```python
    var1 = 19
    var1 = "Suneel"
    print(var1)	'''suneel is printed without error. Same variable can refers to different python data types '''
    ``` 
- List of important data types that are commonly used in Python
     1. Booleans   
     2. Numbers  
     3. Strings  
     4. Bytes
     5. Lists
     6. Tuples
     7. Sets
     8. Dictionaries    

- Python Data-types Brief
    1. Booleans ↓ 
        - Boolean in Python can have two values – **True or False**. These values are constants and can be used to assign or compare boolean values. 
        ```python
        condition = False
        if condition == True:
            print("You can continue with the prpgram.")
        else:
            print("The program will end here.")
        ```
        
        Same as above
        ```python
        condition = False
        if condition:
            print("You can continue with the prpgram if condition is True.")
        else:
            print("The program will end here.")
        ```
        - The above code shows: 
        ```python
        if condition:
        ```
        is equivalent to
        ```python
        if condition == True:
        ```
        - False is 0 and True is 1 in Python. 
        ```python
        a = True
        print(type(a))
        a = True + 0
        print(type(a))
        b = False + 0
        print("The Value of a and b are", a ,b )
        ``` 
        ```python
        #Output
        <class 'bool'>
        <class 'int'>
        The value of a and b are 1 0
        ```
        The above example prove the statement. 
          
             
    2. Numbers 
        - Unlike many languages which have only integers and floats, Python introduces **complex** as a new type of numbers.
        - The numbers in Python are classified using the following keywords.
        **int, float, and complex**.
        - Python has a built-in function **type()** to determine the data type of a variable or the value. 
        - Another built-in function **isinstance()** is there for testing the type of an object.
        - In Python, we can add a **“j”** or **“J”** after a number to make it imaginary or complex.
        ```python
        num = 2
        print("The number (", num, ") is of type", type(num))

        num = 3.0
        print("The number (", num, ") is of type", type(num))

        num = 3+5j
        print("The number ", num, " is of type", type(num))
        print("The number ", num, " is complex number?", isinstance(3+5j, complex))

        ``` 
        Output:
        ``` -- None -- 
        The number ( 2 ) is of type <class 'int'>
        The number ( 3.0 ) is of type <class 'float'>
        The number (3+5j) is of type <class 'complex'>
        The number (3+5j) is complex number? True
        ``` 
        - To form a complex number, we can even use the type as a constructor.
        ```python
        >>> complex(1.2,5)
        (1.2+5j)
        ```
        - Integers in Python don’t have any size limitation as long as the required memory is available.
        ```python
        >>> num = 1234567890123456789
        >>> num.bit_length()
        61
        ```
        - A float type number can have precision up to 15 decimal places.
        ```python
        >>> import sys
        >>> sys.float_info.dig
        15
        ```
        Here, dig is the maximum number of decimal digits in a float.
    3. Strings
        - A sequence of one or more characters enclosed within either single quotes ‘ or double quotes ” is considered as a String in Python. Any letter, a number or a symbol could be a part of the string. 
        - The strings in Python are{{ immutable}}. It means the memory will be allocated once and re-used thereafter.  
        - Python also supports multi-line strings which require a triple quotation mark at the start and one at end. 
        ```python
        str1 = 'A string wrapped in single quotes'

        str2 = "A string enclosed within double quotes"

        str3 = """A multiline string
        starts and ends with
        a triple quotation mark."""

        print(str1)
        print(str2)
        print(str3)
        ```
        Output:
        ``` -- None -- 
        A string wrapped in single quotes
        A string enclosed within double quotes
        A multiline string
        starts and ends with
        a triple quotation mark.
        ```
    4. Bytes ↓ 
        - It can store a sequence of bytes (each 8-bits) ranging from 0 to 255. Similar to an array, we can fetch the value of a single byte by using the index. But we can not modify the value.
        - The byte is {{an immutable}} type in Python.
        - Since the byte is machine-readable, so they can be directly stored to the disk.
        ```python
        #Make var1 an bytes object
        var1 = bytes(16)
        print(type(var1)
        print(var1)
        ```
        output: 
        ``` -- None -- 
        <class 'bytes'>
        '\x00\x00\x00\x00\x00\x00\x00\x00\x00\x00\x00\x00\x00\x00\x00\x00'
        ```
        - One scenario, where bytes matter is when carrying out I/O operations with buffering enabled. For example, we have a program which is continuously receiving the data over the network. It parses the date after waiting for the message headers and terminators to appear in the stream. It keeps appending the incoming bytes to a buffer.
        - With Python byte object, it is easy to program the above scenario using the below pseudo code. 
        ```python
        buf = b''
        while message_not_complete(buf):
            buf += read_from_socket()
        ```
    5. Lists
        - Python list is heterogeneous which stores arbitrarily typed objects in an ordered sequence. 
        - It is very flexible and does not have a fixed size.
        - List objects are mutable. i.e. Python allows modifying a list or its elements via assignments as well as through the built-in list methods.
        - Lists in Python can be declared by placing elements inside **square brackets separated by commas**.   
        - Index in a list begins with zero in python. 
        ```python
        #python list syntax
        #Defining list without element
        my_list = []
        print(my_list)
        #Initalization of list
        my_list1 = ["Suneel", 2022, "Leapforg", True, 21.6]
        print(my_list1[0])  #print first object of list
        print(my_list1)	#print whole list
        ```
        Output: 
        ``` -- None -- 
        []
        Suneel
        ['Suneel', 2022, 'Leapforg', True, 21.6]
        ```
    
    6. Tuples
        - Python tuple is a heterogeneous collection of Python objects separated by commas. The tuple and a list are somewhat similar as they share the following traits. 
        - Python Tuple syntax: 
        ```python
        #Defining a tuple without any element
        my_tuple = ()
        print(my_tuple)
        ``` 
        Output: 
        ```python
        ()
        ```
        - Python Tuple Initialization: 
        ```python
        my_tuple = ("Partnership", 2022, 14.5, 'IOE')
        print(my_tuple)
        ```
        Output: 
        ```python
        ('Partnership', 2022, 14.5, 'IOE')
        ```
    7. Sets 
        - A set is an unordered collection of unique and immutable objects. Its definition starts with enclosing braces { } having its items separated by commas inside.
        - Amongst all the Python data types, the set is one which supports mathematical operations like union, intersection, symmetric difference etc.
        - Creating a set. 
        ```python
        sample_set = {'Welcome', 2, 'sample set', 19.6}
        print(sample_set)
        explicit_set = set(Welcome to Google) #chaning into set explicitly
        print(explicit_set)
        print(type(explicit_set))
        ```
        Output: 
        ``` -- None -- 
        {2, 'sample set', 'Welcome', 19.6}
        {'t', 'e', 'g', 'W', 'l', ' ', 'o', 'm', 'G', 'c'}
        <class 'set'>
        ```

        ### Frozen set

        - A frozen set is a processed form of the traditional set. It is immutable and only supports methods and operators that executes without altering the frozen set used in the context. 
        ```python 
        depart = {'computer', 'mechanical', 'information', 'electrical'}
        fset = frozenset(depart)
        print(type(fset))
        ```
        Output:        
        ``` -- None -- 
        #output-
        <class 'frozenset'>
        ```
        - Example to  highlight difference between normal and frozen set:
        ```python
            # A standard set
            std_set = {'Nokia', 'Sony', 'Samsung', 'Apple'}
            print(std_set)
            print(type(std_set)

            std_set.add('Huawei')
            print(std_set)

            # A forzen set
            frozen_set = frozenset(std_set)
            print(frozen_set)
            print(type(frozen_set))

            # you cannot add new element into frozenset.
            # frozen_set.add('Huawei')
            # Above statement is pop up syntax error.
        ```

            Output: 
            ``` -- None -- 
            #Output-
            {'Apple', 'Nokia', 'Sony', 'Samsung'}
            <class 'set'>
            {'Apple', 'Sony', 'Huawei', 'Nokia', 'Samsung'}
            frozenset({'Nokia', 'Huawei', 'Apple', 'Sony', 'Samsung'})
            <class 'frozenset'>
            ```
    8. Dictionaries ↓ 
        - A dictionary in Python is an unordered collection of key-value pairs. It’s a built-in mapping type in Python where keys map to values. These key-value pairs provide an intuitive way to store data.
        - The dictionary solves the problem of efficiently storing a large data set. Python has made the dictionary object highly optimized for retrieving data.
        - Creating Dictionary:
        ``` -- None -- 
        sample_dict = {'key':'value', 'apr': 20, 'name':'suneel'}
        print(type(sample_dict))
        print(sample_dict)
        ```
        Output: 
        ``` -- None -- 
        <class 'dict'>
        {'key': 'value', 'apr': 20, 'name': 'suneel'}
        ```
        - Accessing dictionaries element with keys: 
        ```python
        print(sample_dict['name'])
        ```
        Output: 
        ``` -- None -- 
        suneel
        ```
    
- How does a tuple differ from the list?
    - Tuples do differ a bit from the list as they are immutable. Python does not allow to modify a tuple after it is created. We can not add or remove any element later. Instead, Python expects us to create a new one with the updated sequence of elements.  
    - 
- Why need a Tuple as one of the Python data types? ↓ 
    - Python uses tuples to return multiple values from a function.
    - Tuples are more lightweight than lists.
    - It works as a single container to stuff multiple things.
    - We can use them as a key in a dictionary.
