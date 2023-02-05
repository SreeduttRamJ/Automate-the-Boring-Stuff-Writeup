# Automate-the-Boring-Stuff-Writeup

<h3>Chapter 3 - Functions</h3>

Practice Questions<br></br>

1. Why are functions advantageous to have in your programs?

```
Functions help you reduce the need to write the same code again and again
```

2. When does the code in a function execute?

```
When function is called 
```

3. What statement creates a function?
```
we use "def" keyword to define(create) a function 

example: def function_name()

```

4. What is the difference between a function and a function call?

```
Function: A block of code that does a particular operation
Function call: It is a code used to pass control to the function
```

5. How many global scopes are there in a Python program? How many local scopes?

```
Global scope: The names that you define in this scope are available to all your code.
              A global scope is an entire program so 1.

Local scope: The names that you define in this scope are only available or visible to the code 
             within the scope.
             Local scope can be considered under every function therefore infinite in number
```

6. What happens to variables in a local scope when the function call returns?

```
Variables in the local scope of the function gets deleted right after the function returns the 
result.
```

7. What is a return value? Can a return value be part of an expression?

```
A return is a value that a function returns when it completes its task.
The datatype of your return value vary the expressions it can be used in.

```
![image](https://user-images.githubusercontent.com/113903135/216833663-045ef183-ee4b-423e-98f2-e2352073c27c.png)


8. If a function does not have a return statement, what is the return value of a call to that function?

```
It returns the value None
```
![image](https://user-images.githubusercontent.com/113903135/216833777-e33abb5c-5268-4757-96a1-54b9962632d9.png)

9. How can you force a variable in a function to refer to the global variable?

```
When creating a variable in a function it is a local variable.
But we can create a global variable inside the function if we use the global keyword.
```

10. What is the data type of None?

```
None can be defined as a Null value its data type is "NoneType".
```

11. What does the import areallyourpetsnamederic statement do?

```
The statement import a module of the name areallyourpetsnamederic
```

12. If you had a function named bacon() in a module named spam, how would you call it after importing spam?

```
spam.bacon()
```

13. How can you prevent a program from crashing when it gets an error?

```
We can use try and except clause to prevent program from crashing
```
![image](https://user-images.githubusercontent.com/113903135/216835531-8e2cdd05-e343-4df2-b863-b43de46112de.png)

14. What goes in the try clause? What goes in the except clause?

```
try clause contain the code to be executed

except clause is executed when there is an error in try block

Some of common errors are:

IOError: when the file is unable to be opened
KeyboardInterrupt: when a key that is not needed in the program is pressed by the user
ValueError: when built-in function receives a wrong value
EOFError: when End-Of-File is reached program completes execution
ImportError: if module is not found
ZeroDivisionError: if a number is divided by zero

```
