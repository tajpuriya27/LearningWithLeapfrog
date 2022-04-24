
# Day11 - Python Operators

Like many programming languages, Python reserves some special characters for acting as operators. Every operator carries out some operation such as addition, multiplication to manipulate data and variables. The variables passed as input to an operator are known as operands.

**List of Python Operators:**
1. Arithmetic
2. Comparison
3. Logical
4. Bitwise
5. Assignment
6. Identity
7. Membership

## Brief
## 1. Arithmetic Operators
| Operator Symbol| Name - Purpose                                          | Usage  |
|----|-------------------------------------------------------------------------|------|
| +  | Addition – Sum of two operands                                          | a+b  |
| –  | Subtraction – Difference between the two operands                       | a-b  |
| *  | Multiplication – Product of the two operands                            | a*b  |
| /  | Float Division – Quotient of the two operands                           | a/b  |
| // | Floor Division – Quotient of the two operands (Without fractional part) | a//b |
| %  | Modulus – Integer remainder after division of ‘a’ by ‘b.’               | a%b  |
| ** | Exponent – Product of ‘a’ by itself ‘b’ times (a to the power of b)     | a**b |
|     |  |  |

```python
# Arithmetic operator
a = 42
b = 4
print('The first number is', a, '& the second number is', b)
# add+
print('The sum of two numbers:', a+b)
# sub-
print('substraction of b from a:', a-b)
#mul*
print('The multiplication of two number is', a*b)
#division with decimal
print('The division yields', a/b)
#division w/o decimal
print('The division yields', a//b)
#Modulus==Remainder
print('The remainder is', a%b)
#Exponent== power
print('The exponent** is equal to pow(a,b)', a**b)
```
Output:
```
The first number is 42 & the second number is 4
The sum of two numbers: 46
substraction of b from a: 38
The multiplication of two number is 168
The division yields 10.5
The division yields 10
The remainder is 2
The exponent** is equal to pow(a,b) 3111696
```

## 2. Comparator Operator
- Returns boolean value(True or False).    

| Operator-Symbol  | Name - Purpose        | Usage |
|------------------|----------------------------------------------|-------|
| >                | Greater than – if the left operand is greater than the right, then it returns true.                      | a>b   |
| <                | Less than – if the left operand is less than the right, then it returns true.                            | a<b   |
| ==               | Equal to – if two operands are equal, then it returns true.                                              | a==b  |
| !=               | Not equal to – if two operands are not equal, then it returns true.                                      | a!=b  |
| >=               | Greater than or equal – if the left operand is greater than or equal to the right, then it returns true. | a>=b  |
| <=               | Less than or equal – if the left operand is less than or equal to the right, then it returns true.       | a<=b  |
|     |  |  |


```python
# Comparator Operator
i =23
j = 17
# Greater then >
print('"i" is greater then "j":', i > j)
print('"i" is less then "j":', i < j)
print('"i" is equal to "j":', i == j)
print('"i" is not equal to "j":', i != j)
print('"i" is greater then or equal to "j":', i >= j)
print('"i" is less then or equal to "j":', i <= j)
```
Output:
```
"i" is greater then "j": True
"i" is less then "j": False
"i" is equal to "j": False
"i" is not equal to "j": True
"i" is greater then or equal to "j": True
"i" is less then or equal to "j": False
```

## 3. Logical operators

- Logical Python operators enable us to make decisions based on multiple conditions. The operands act as conditions that can result in a true or false value.
- The outcome of such an operation is either true or false (i.e., a Boolean value).
- The ‘and’ and ‘or’ operators do return one of their operands instead of pure boolean value. Whereas the ‘not’ operator always gives a real boolean outcome.


| Operator Symbol  | Name - Purpose                         | Usage   |
|------------------|----------------------------------------|---------|
| and              | if ‘a’ is false, then ‘a’, else ‘b’    | a and b |
| or               | if ‘a’ is false, then ‘b’, else ‘a’    | a or b  |
| not              | if ‘a’ is false, then True, else False | not a   |
|                  |                                        |         |

```python
# Logical Operator
a=7
b=4

# Result: a and b is 4
print('a and b is',a and b)

# Result: a or b is 7
print('a or b is',a or b)

# Result: not a is False
print('not a is',not a)
```
Output:
```
a and b is 4
a or b is 7
not a is False
```

## 4. Bitwise Operator

| Operator |                            Purpose         |  Usage |
|:--------:|:---------------------------------------------------------:|:------:|
|     &    |Bitwise AND – compares two operands on a bit level and returns 1 if both the corresponding bits are 1|  a & b |
|    \|    |Bitwise OR – compares two operands on a bit level and returns 1 if any of the corresponding bits is 1| a \| b |
|   \~    |        Bitwise NOT – inverts all of the bits in a single operand    |   ~a   |
|     ^    | Bitwise XOR – compares two operands on a bit level and returns 1 if any of the corresponding bits is 1, but not both |  a ^ b |
|    >>    |Right shift – shifts the bits of ‘a’ to the right by ‘b’ no. of times | a >> b |
|    <<    |Left shift – shifts the bits of ‘a’ to the left by ‘b’ no. of times | a << b |
|    **=   |    a**=4                                | a=a**4 |
|    &=    |                  a&=4                  |  a=a&4 |
|    \|=   |                 a\|=4                        | a=a\|4 |
|    ^=    |              |  a=a^4 |
|    >>=   |   a>>=4                       | a=a>>4 |
|    <<=   |        a<<=4                |  a=<<4 |
|          |                             |        |

## 5. Assignment Operators

| Operator | Example | Similar to |
|----------|---------|------------|
| =        | a=4     | a=4        |
| +=       | a+=4    | a=a+4      |
| -=       | a-=4    | a=a-4      |
| *=       | a*=4    | a=a*4      |
| /=       | a/=4    | a=a/4      |
| %=       | a%=4    | a=a%4      |
| \**=      | a**=4   | a=a**4     |
| &=       | a&=4    | a=a&4      |
| \|=      | a\|=4   | a=a\|4     |
| ^=       | a^=4    | a=a^4      |
| >>=      | a>>=4   | a=a>>4     |
| <<=      | a<<=4   | a=<<4      |
|          |         |            |