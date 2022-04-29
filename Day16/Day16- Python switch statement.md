
# Day16- Python Switch Statement

Switch case give a cleaner wayt to implement control flow in program when we don’t want a conditional block cluttered with multiple if conditions.

> **Unlike other programming languages, Python doesn’t provide a switch case instrument over the self.**  
> [Here is why?](https://bit.ly/pep3103)

However, it has many other constructs like a dictionary, lambda function, and classes to write a custom implementation of the Python switch case statement.

### Switch statement in C
- The expression under the switch gets evaluated once.
- It should result in a constant integer value. [Note: In Python, we can alter this behavior.]
- A case with a duplicate value should not appear.
- If no case matches, then the default case gets executed.

```c
    switch (dayOfWeek) {
    case 1:
        printf("%s", Monday);
        break;
    case 2:
        printf("%s", Tuesday);
        break;
    case 3:
        printf("%s", Wednesday);
        break;
    case 4:
        printf("%s", Thursday);
        break;
    case 5:
        printf("%s", Friday);
        break;
    case 6:
        printf("%s", Saturday);
        break;
    case 7:
        printf("%s", Sunday);
        break;
    default:
        printf("Incorrect day");
        break;
    }
```

## Implement Python Switch Case Statement

1. Switch Case using a Dictionary
    1. First, define individual functions for every case.
    2. Make sure there is a function/method to handle the default case.
    3. Next, make a dictionary object and store each of the function beginning with the 0th index.
    4. After that, write a switch() function accepting the day of the week as an argument.
    4. The switch() calls the get() method on the dictionary object which returns the function matching the argument and invokes it simultaneously.

    ```python 
    # Implement Python Switch Case Statement using Dictionary

    def monday():
        return "monday"
    def tuesday():
        return "tuesday"
    def wednesday():
        return "wednesday"
    def thursday():
        return "thursday"
    def friday():
        return "friday"
    def saturday():
        return "saturday"
    def sunday():
        return "sunday"
    def default():
        return "Incorrect day"

    switcher = {
        1: monday,
        2: tuesday,
        3: wednesday,
        4: thursday,
        5: friday,
        6: saturday,
        7: sunday
        }

    def switch(dayOfWeek):
        return switcher.get(dayOfWeek, default)()

    print(switch(1))
    print(switch(0))
    ```
    Output:
    ```
    monday
    Incorrect day
    ```

2. Switch Case using a Class
    ```python
    # Implement Python Switch Case Statement using Class

    class PythonSwitch:

        def switch(self, dayOfWeek):
            default = "Incorrect day"
            return getattr(self, 'case_' + str(dayOfWeek), lambda: default)()

        def case_1(self):
            return "Monday"
    
        def case_2(self):
            return "Tuesday"
    
        def case_3(self):
            return "Wednesday"

    s = PythonSwitch()

    print(s.switch(1))
    print(s.switch(0))
    ```
    It takes the day of the week as an argument, converts it to string and appends to the ‘case_’ literal. After that, the resultant string gets passed to the getattr() method.
    The getattr() method returns a matching function available in the class.
    If the string doesn’t find a match, then the getattr() returns the lambda function as default.
    The class also have the definition for functions specific to different cases.

    Output:
    ```
    Monday
    Incorrect day
    ```