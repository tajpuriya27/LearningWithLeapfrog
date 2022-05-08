
# Day25- Python DateTimeModule && Python string replace

Python Datetime module and its functions could come quite handy for recording the events and logs with the timestamp value.

### Pre-requisites
1. Introduction to Datetime in Python
2. Implementation
3. Datetime Examples
4. Usages of Datetime Module

>

### 1. Introduction to Datetime Module
Although we can use the time module to find out the current date and time, it lacks features such as the ability to create Date objects for a particular manipulation.
> To remedy this, Python has the built-in datetime module. Hence, to do any object manipulation regarding date and time, we need to import datetime module.

The datetime module is used to modify date and time objects in various ways.

### It contains five classes to manipulate date and time:
1. Date: deals with date objects.
2. Time: deals with time objects.
3. datetime: deals with date and time object combinations.
4. timedelta: deals with intervals of time. Used in calculations of past and future date and time objects.
5. Info: deals with time zone info of local time.
We are going to deal with date and time classes.

### 2. Implementation
To create and modify new date and time objects, we need to import the module. 
```python
import datetime
Or if you want only one of the modules-

from datetime import date

from datetime import time

from datetime import datetime
```

We could create new objects that have different date and time stored for manipulation using the datetime module.

The following syntax would do the needful.
```python
import datetime

datetime.datetime(year_number, month_number, date_number, hours_number, minutes_number, seconds_number)
```

- To format the dates into human readable strings, we use strftime() in the datetime module.

- The timedelta() function allows performing calculations on the date and time objects. It can be useful for time planning and management.

Syntax used in invoking timedelta() is:
```python
from datetime import timedelta

timedelta(days, hours, minutes, seconds, year,...)
```

### 3. Python Datetime Examples
You can use the commands either in python interpreter or by writing the code in a file and executing it.

To display today’s date we use the following code:
```python
import datetime

print (datetime.date.today())
```
Or
```python
from datetime import date

print (date.today())
```

To view the individual date components, we need:
```python
from datetime import date

print (datetime.date.today().day)

print (datetime.date.today().month)

print (datetime.date.today().year)

#If you prefer to write in one sentence, write it as 

print (datetime.date.today().day,datetime.date.today().month,datetime.date.today().year)
```

Since the above code is long, we can rewrite as:

```pyhton
from datetime import date

now = date.today()

print (now.day)

print (now.month)

print (now.year)

#You can also display the previous 3 sentences in one sentence 

#print (now.day, now.month, now.year)
```

>This code is cleaner and compact. Try to write the code in shortest way possible without affecting readability.


Example:

We could also use the date class to find out the weekday of the current date:

```python
from datetime import date

now = date.today()

print (now.weekday())
```

Example-2
- To format the date and time into human readable strings, we use strftime() in the datetime module.

The following example clarifies how to use this function and prints the date/time in a styled manner:

```python
Today = datetime.now()

print (Today.strftime(“%a, %B, %d, %y”))
```

- In the above the %a stands for the day, %B stands for the month, %d stands for date and %y stands for the year. These are the most common format types use.

If we wanted to print local date and time using strftime(), we could use
```python
import datetime

Today = datetime.now()

print (“Today’s date is “ ,Today.strftime(“%c”))
```

To display only local date, local time separately, we can replace %c with %x and %X, respectively.

Programs using timedelta
```python
from datetime import date,time,datetime,timedelta

Time_gap = timedelta(hours = 23, minutes = 34) 
#Time_gap is the timedelta object where we can do different calculations on it.

print (“Future time is ”, str(datetime.now() + Time_gap))
```


### Usages of Datetime Module
It is a powerful feature that allows us to manipulate system date and time without risking any system changes. We can define a new date object and modify its representation.

Arithmetic calculations can be done on the date and time objects for several purposes such as finding the future date, the present year, formatting of date into strings, creating a time management solution, etc.