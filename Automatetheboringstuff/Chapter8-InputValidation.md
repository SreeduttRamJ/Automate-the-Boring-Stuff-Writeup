# Automate-the-Boring-Stuff-Writeup

<h3>Chapter 8- Input Validation</h3>

<h4>Practice Questions </h4><br></br>

1. Does PyInputPlus come with the Python Standard Library?

```
PyInputPlus does not come with the standard library
We can install it using pip

pip install --user pyinputplus
```

2. Why is PyInputPlus commonly imported with import pyinputplus as pyip?

```
It is just imported as pyip as we can use the shortername when calling function from the module
We can import it in any name you want
```

3. What is the difference between inputInt() and inputFloat()?

```
inputInt check whether the input data is an integer or not
It asks an input again and again until input becomes an integer

inputFloat check whether the input data is a float or not
It asks for input until input is a float

we use prompt to show the message we want the user to see

CODE:
import pyinputplus as pyip
x=pyip.inputInt(prompt= "input integer = ")
y=pyip.inputFloat(prompt= "input float = ")

print("\nint data = ",x)
print("float data = ",y)

OUTPUT:

input integer = qw
'qw' is not an integer.
input integer = q
'q' is not an integer.
input integer = 123
input float = ww
'ww' is not a float.
input float = 1

int data = 123
float data = 1.0
```

4. How can you ensure that the user enters a whole number between 0 and 99 using PyInputPlus?

```
we can use min, max, greaterThan, lessThan keyword arguments to ensure the input is between 0 & 99
 
CODE:
 
import pyinputplus as pyip
x=pyip.inputInt(prompt= "input integer ",min=0,max=99)

print("data = ",x)

OUTPUT:
 
Number must be at maximum 99.
input integer 12.1
'12.1' is not an integer.
input integer -32
Number must be at minimum 0.
input integer 13
data = 13
```

5. What is passed to the allowRegexes and blockRegexes keyword arguments?

```
Last chapter we learned how to match patterns using regular expression 

The given commands 
allowregex stores data if input matches the regular expression 
blockregex won't store data if input match the regular expression

CODE:
import pyinputplus as pyip
x=pyip.inputNum('input: ', allowRegexes=[r'[A|BAT|CAT]+$'])
print(x," is allowed as input because it is matched")

y=pyip.inputNum('input: ', blockRegexes=[r'^([0-4])*$'])
print(y," is allowed as input because it is not a match with regex")

OUTPUT:

input: QWERTY
'QWERTY' is not a number.
input: QW
'QW' is not a number.
input: A
A  is allowed as input because it is matched
input: 14
This response is invalid.
input: 12
This response is invalid.
input: 64
64  is allowed as input because it is not a match with regex

REASON:
Here A gets considered as a number as we are allowing it using regex
Next case we are blocking every combination of 0,1,2,3,4 
```

6. What does inputStr(limit=3) do if blank input is entered three times?

```
An exception called RetryLimitException occurs
```

7. What does inputStr(limit=3, default='hello') do if blank input is entered three times?

```
the given default value is returned

CODE:

import pyinputplus as pyip
x=pyip.inputStr(limit=3, default='hello')

print('\n',x)

OUTPUT:

Blank values are not allowed.

Blank values are not allowed.

Blank values are not allowed.

hello

 ```
