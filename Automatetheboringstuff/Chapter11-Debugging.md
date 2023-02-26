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

|    Level    |   Logging function   | 
|:-----------:|:---------------------:|
|Debug|logging.debug()|
|Info|logging.info()|
|Warning|logging.warning()|
|Error|logging.error()|
|Critical|logging.critical()|

7. What line of code can you add to disable all logging messages in your program?

```
logging.disable()
```

8. Why is using logging messages better than using print() to display the same message?

```
After a person compelete the debugging removing the print() is a hassle while we can disable logging messages easily by using
logging.disable()
```

9. What are the differences between the Step Over, Step In, and Step Out buttons in the debugger?

```
Step In button execute next line of code and pause if its a function call it will goto the first line of function and stop

Step Over button is same as Step In but if the next line us a function call it execute code in normal speed and pause after function return

Step Out button is mostly used with step in function that is if step in enters a function and you need to get out of it You use step out which will execute the function and pause at return
```

10. After you click Continue, when will the debugger stop?

```
Debugger stop at the break point or compelete execution of the code
```

11. What is a breakpoint?

```
It is used to stop or pause the execution of a program
```

12. How do you set a breakpoint on a line of code in Mu?

```
You can just click on the left of code line were you want the break point

```




