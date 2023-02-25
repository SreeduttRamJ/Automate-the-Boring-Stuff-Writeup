# Automate-the-Boring-Stuff-Writeup

<h3>Chapter 11 - Debugging</h3>

<h4>Practice Questions </h4><br></br>

1. Write an assert statement that triggers an AssertionError if the variable spam is an integer less than 10.

```
q=11
assert q<=10

here we get assertion error as the statement is false
```

2. Write an assert statement that triggers an AssertionError if the variables eggs and bacon contain strings that are the same as each other, even if their cases are different (that is, 'hello' and 'hello' are considered the same, and 'goodbye' and 'GOODbye' are also considered the same).

```
assert bacon.lower()!=eggs.lower()

you might think why I gave not equal to in the statement while my condition is equal to
that is because assert returns error when the statement is false

we use .lower() as we 'goodbye' and 'GOODbye' are considered the same

```
3. Write an assert statement that always triggers an AssertionError.

```
assert 1==2
```
4. What are the two lines that your program must have in order to be able to call logging.debug()?

```
import logging
logging.basicConfig(level=logging.DEBUG, format='%(asctime)s -  %(levelname)s -  %(message)s')

level=logging.DEBUG 
sets the logging level to DEBUG, which means that all log messages with severity level DEBUG 
and higher (INFO, WARNING, ERROR, and CRITICAL) will be returned as output.

format='%(asctime)s - %(levelname)s - %(message)s' 
specifies the format of each log message,
timestamp (in the format of year-month-day hour:minute:second,millisecond), the severity level, and message.
```
5. What are the two lines that your program must have in order to have logging.debug() send a logging message to a file named programLog.txt?

```
import logging
logging.basicConfig(filename='programLog.txt', level=logging.DEBUG,format=' %(asctime)s - %(levelname)s - %(message)s')

we can just add filename to basicConfig 
```
6. What are the five logging levels?

```


