
# Built-in String Function in Python

## Conversion Funcitons

1. Capitalize()  
Returns the string with the first character capitalized and rest of the characters in lower case. 
    ```python
    var_str = 'SUNEEL TAJPURIYA'
    print(var_str.capitalize())
    #Suneel tajpuriya
    ```
2. lower()  
Converts all the characters of the String to lowercase. 
    ```python
    var_str = 'SUNEEL TAJPURIYA'
    print(var_lower())
    #suneel tajpuriya
    ```
3. upper()   
Converts all the characters of the String to uppercase. 
    ```python
    var_str = 'Suneel Tajpuriya'
    print(var_str.upper())
    #SUNEEL TAJPURIYA
    ```
4. swapcase()    
Swaps the case of every character in the String means that lowercase characters got converted to uppercase and vice-versa.  
    ```python
    var_str = 'Suneel Tajpuriya'
    print(var_str.capitalize())
    #sUNEEL tAJPURIYA
    ```
5. title()   
Returns the ‘titlecased’ version of String, which means that all words start with uppercase and the rest of the characters in words are in lowercase. 
    ```python
    var_str = 'suneel tajpuriya'
    print(var_str.capitalize())
    #Suneel Tajpuriya
    ```
6. count(str[,beg[,end]])  
Returns the number of times substring ‘str’ occurs in the range [beg, end] if beg and end index are given else the search continues in full String Search is case-sensitive.  
    ```python
    var_str = 'LearningwithLeapfrog'
    print(var_str.count('e'))
    #2
    print(var_str.count('e', 0, 10))
    #1
    ``` 

## Comparison Functions

1. islower()  
Returns ‘True’ if all the characters in the String are in lowercase. If any of the char is in uppercase, it will return False.  
    ```python
    var_str = 'LearningwithLeapfrog'
    print(var_str.islower())
    #False
    ```
2. isupper()  
Returns ‘True’ if all the characters in the String are in uppercase. If any of the char is in lowercase, it will return False.  
    ```python
    var_str = 'LearningwithLeapfrog'
    print(var_str.upper())
    #False
    ```
3. isdecimal()
Returns ‘True’ if all the characters in String are decimal. If any character in the String is of other data-type, it will return False.

    ```python
    num = '1234'
    print(type(num))
    #<class 'str'>
    print(num.isdecimal())
    #True
    ``` 

4. isdigit()
5. isnumeric()
6. isalpha()  
Returns ‘True’ if string contains at least one character (non-empty String), and all the characters are alphabetic, ‘False’ otherwise.  
    ```python
    print('Learning'.isaplpha())
    #True
    ```
7. isalnum()  
Returns ‘True’ if String contains at least one character (non-empty String), and all the characters are either alphabetic or decimal digits, ‘False’ otherwise. 
    ```python
    print('Learning'.isalnum())
    #True
    print('Learning2022'.isalnum())
    #True
    ```

##Search Functions

1. find(str[, i[, i]])   
Searches for ‘str’ in a complete String (if i and j are not defined) or in a sub-string of String (if i and j are defined). This function returns the index if ‘str’ is found else returns ‘-1’. Here, i=search starts from this index, and j=search ends at this index. 
    ```python
    var_str = 'I am learning Python string in-built function.'
    print(var_str.find('g'))
    #12
    print(var_str.find('z'))
    #-1
    print(var_str.find('Python'))
    #14
    print(var_str.find('n'))
    #9
    print(var_str.find('n',10))
    #11
    ```
2. index(str[, i[, j]])  
This is same as ‘find’ method. The only difference is that it raises the ‘ValueError’ exception if ‘str’ doesn’t exist.
    ```python
    var_str = 'I am learning Python string in-built function.'
    print(var_str.index('g'))
    #12
    print(var_str.find('n'))
    #9
    print(var_str.index('z'))
    #ValueError: substring not found
    ```
3. rindex(str[,i[,j]])  
This is same as 'index' method. The only difference is that it returns the last index where 'str' is found. If 'str' is not found, it returns 'valueError'. 
    ```python
    var_str = 'I am learning Python string in-built function.'
    print(var_str.index('g'))
    #26
    print(var_str.rindex('n'))
    #44
    print(var_str.index('z'))
    #ValueError: substring not found
    ```
4. rfind(str[, i[, j]])  
This is same as find() just that this function returns the last index where ‘str’ is found. If ‘str’ is not found, it returns ‘-1’.  
    ```python
    var_str = 'I am learning Python string in-built function.'
    print(var_str.rfind('z'))
    #-1
    print(var_str.rfind('Python'))
    #14
    print(var_str.rfind('n'))
    #44
    ```
5. count(str[, i[, j]])  
Returns the number of occurrences of substring ‘str’ in the String. Searches for ‘str’ in the complete String (if i and j not defined) or in a sub-string of String (if i and j are defined). Where: i=search starts from this index, j=search ends at this index. 
    ```python
    var_str = 'I am learning Python string in-built function.'
    print(var_str.count('n'))
    #7
    ```

## String Substitution functions

1. replace(old, new[, count])  
Replaces all the occurrences of substring ‘old’ with ‘new’ in the String.  
If the count is available, then only ‘count’ number of occurrences of ‘old’ will be replaced with the ‘new’ var. Where old =substring to replace, new =substring
    ```python
    var = 'This is amazing.'
    print(var.replace('is','was'))
    #Thwas was amazing.
    print(var.replace('is', 'was', 1))
    #Thwas is amazing.
    ```
2. split([sep[, maxsplit]])  
Returns a list of substring obtained after splitting the String with ‘sep’ as a delimiter. Where, sep= delimiter, the default is space, maxsplit= number of splits to be done. 
    ```python
    var = "This is a good example"
    print (var.split())
    # ['This', 'is', 'a', 'good', 'example']
    print (var.split(' ', 3))
    # ['This', 'is', 'a', 'good example']
    ```  
3. splitlines(num)  
Splits the String at line breaks and returns the list after removing the line breaks. Where num = if this is a positive value. It indicates that line breaks will appear in the returned list.
    ```python
    var='Print new line\nNextline\n\nMove again to new line'
    print (var.splitlines())
    # ['Print new line', 'Nextline', '', 'Move again to new line']
    print (var.splitlines(1))
    # ['Print new line\n', 'Nextline\n', '\n', 'Move again to new line']
    ```
4. join(seq)
Returns a String obtained after concatenating the sequence ‘seq’ with a delimiter string. Where: the seq= sequence of elements to join. 
    ```python
    seq=('ab','bc','cd')
    str='='
    print (str.join(seq))
    # ab=bc=cd
    ```

## Misc String Functions

1. Istrip([chars])  
Returns a string after removing the characters from the beginning of the String. Where: Chars=this is the character to be trimmed from the String. The default is whitespace character.
    ```python
    var_str = ' Learning Python is fun '
    print(var_str.lstrip())
    #Learning Python is fun
    var_str = '****Learning Python is fun****'
    print(var_str.lstrip('*'))
    #Learning Python is fun****
    ``` 
2. rstrip()   
Returns a string after removing the characters from the End of the String. Where: Chars=this is the character to be trimmed from the String. The default is whitespace character. 
    ```python
    var_str = ' Learning Python is fun '
    print(var_str.rstrip())
    # Learning Python is fun
    var_str = '****Learning Python is fun****'
    print(var_str.rstrip('*'))
    #****Learning Python is fun
    ```
3. len(string)  
Returns the length of given string. 
```python
var_str = 'Learning Python is fun'
print(len(var_str))
#22
```

## Padding Functions

    1. rjust(width[, fillchar])
    2. Ijust(width[, fillchar])
    3. center(width[, fillchar])
    4. zfill(width)
