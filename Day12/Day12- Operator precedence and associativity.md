
# Day12- Operator Precedence and Associativity

## **Precedence**
The method/process via which compiler decide which operator should be computed first if more than one operator are present in an expression.  
In an expression, Python interpreter evaluates operators with higher precedence first.   
For Example: if Multiplication(*) and Addtion(+) both appear on one expression. Then precedence will be checked, here, * has greater precedence. Hence * will be evaluated first.
>### Below lists the operators with the highest precedence at the top and lowest at the bottom.

| Precedence |               Operators               |               Usage               |
|:----------:|:-------------------------------------:|:---------------------------------:|
|      1     |                  { }                  |       Parentheses (grouping)      |
|      2     |                f(args…)               |           Function call           |
|      3     |             x[index:index]            |              Slicing              |
|      4     |                x[index]               |            Subscription           |
|      5     |              x.attribute              |        Attribute reference        |
|      6     |                   **                  |              Exponent             |
|      7     |                   ~x                  |            Bitwise not            |
|      8     |                 +x, -x                |         Positive, negative        |
|      9     |                *, /, %                |    Product, division, remainder   |
|     10     |                  +, –                 |       Addition, subtraction       |
|     11     |                 <<, >>                |         Shifts left/right         |
|     12     |                   &                   |            Bitwise AND            |
|     13     |                   ^                   |            Bitwise XOR            |
|     14     |                   \|                  |             Bitwise OR            |
|     15     | in, not in, is, is not, <, <=, >, >=, |                                   |
|     16     |               <>, !=, ==              | Comparisons, membership, identity |
|     17     |                 not x                 |            Boolean NOT            |
|     18     |                  and                  |            Boolean AND            |
|     19     |                   or                  |             Boolean OR            |
|     20     |                 lambda                |         Lambda expression         |
|            |                                       |                                   |


## **Associativity**
Associativity, simply means whether to evaluate left or right operator when two or more operators of same precedence are present in an expression.
Whenever two or more operators have the same precedence, then associativity defines the order of operations.
And, except the exponent operator (\**) all other operators get evaluated from **left to right.**


# Python Namespaces and Scope

If we want to do serious programming, then it is vital for you to know how scopes and namespaces work in Python. With this knowledge, you can even develop a scalable package ecosystem to be used by a large group working on a massive project.

## **Namespaces**
A namespace is a simple system to control the names in a program. It ensures that names are unique and won’t lead to any conflict.   
Simply, namespaces are those user-defined names in programming like name of variables, name of funcitons, name of user-defined module, etc.  
Namespaces means while programming, programmer should keep those namespaces as distinct as possible so it is human readable for later.


## **Scope**
Scope means upto which it is recognizable. For example: if an variable is initialized within function, it is has local scope whereas if a variable is initialized outside all functions, it has global scope.


>These terminologies will get their real meaning when we will start to work in big real-world project.
>    >Keep Learning🙂