# Automate-the-Boring-Stuff-Writeup

<h3>Chapter 6 - Manipulating Strings</h3>

<h4>Practice Questions </h4><br></br>

1. What are escape characters?

```
an escape character is used to create and alternate displey or interpretation of characters in a code
example:print('qwerty') and print('qwer\nty') creates a new type of output
This why we use escape characters
```
![image](https://user-images.githubusercontent.com/113903135/217636185-11caff46-f873-4951-a310-38ec7232fb2d.png)

2. What do the \n and \t escape characters represent?

```
\n or newline character is same as clicking enter in your keyboard as it takes the cursor to the newline
\t or tab character is same as clicking tab in your keyboard as it moves the cursor a tab space
```

3. How can you put a \ backslash character in a string?
```
we can put it simply by typing '\\'
```
![image](https://user-images.githubusercontent.com/113903135/217637368-2abbe24c-51cb-4beb-a89a-2f7ae92f5dc9.png)

4. The string value "Howl's Moving Castle" is a valid string. Why isn’t it a problem that the single quote character in the word Howl's isn’t escaped?

```
The reason is simply because we have used double quote to create the string rather than single quote.
therefore we don't have to escape the single quote in "Howl's Moving Castle"
```

5. If you don’t want to put \n in your string, how can you write a string with newlines in it?

```
u can use """ triple quotes to include newline without using '\n'
print("""qwerty
qwerty""")
```

![image](https://user-images.githubusercontent.com/113903135/217640641-b5fa2482-ad22-426a-9f91-102aacb4c9e5.png)

6. What do the following expressions evaluate to?

- 'Hello, world!'[1]
- 'Hello, world!'[0:5]
- 'Hello, world!'[:5]
- 'Hello, world!'[3:]

```
'Hello, world!'[1] => 'e' (output character at index 1)
'Hello, world!'[0:5] => 'Hello' (slice string from index 0 to 4)
'Hello, world!'[:5] => 'Hello' (slice string from start to index 4)
'Hello, world!'[3:] => 'lo, world!' (slice string from index 3 to end of string)
```
![image](https://user-images.githubusercontent.com/113903135/217641065-46fecd9a-ff49-4464-be1b-975883383fd7.png)

7. What do the following expressions evaluate to?

- 'Hello'.upper()
- 'Hello'.upper().isupper()
- 'Hello'.upper().lower()

```
'Hello'.upper() => 'HELLO' (turns all characters in string into uppercase)
'Hello'.upper().isupper() => True (turns all characters in string into uppercase then check if every character is in uppercase)
'Hello'.upper().lower() => 'hello' (turns all characters in string into uppercase, then turn all characters to lowercase)
```

![image](https://user-images.githubusercontent.com/113903135/217648818-4dcf73ea-d5c9-46b5-8a07-e1c5967bd9c6.png)

8. What do the following expressions evaluate to?

- 'Remember, remember, the fifth of November.'.split()
- '-'.join('There can be only one.'.split())

```
'Remember, remember, the fifth of November.'.split()
=> ['Remember,', 'remember,', 'the', 'fifth', 'of', 'November.']

'-'.join('There can be only one.'.split())
=>  'There-can-be-only-one.'
```
![image](https://user-images.githubusercontent.com/113903135/217649334-87c186a5-1826-4f3d-8d8d-5cdd0665b338.png)

9. What string methods can you use to right-justify, left-justify, and center a string?
```
right-justify => rjust()
left-justify => ljust()
center => center()
```

10. How can you trim whitespace characters from the beginning or end of a string?
```
we make use of strip() function to trim of blank spaces on both sides of the string
lstrip() is used to trim only at the beginning
rstrip() is used to trim only at the end
```
![image](https://user-images.githubusercontent.com/113903135/217650757-79271e5a-3904-41f7-929d-3c350bd7b995.png)

<h3>Practice Projects </h3><br></br>

<h4>Table Printer</h4>

Write a function named printTable() that takes a list of lists of strings and displays it in a well-organized table with each column right-justified. Assume that all the inner lists will contain the same number of strings. For example, the value could look like this:

```
tableData = [['apples', 'oranges', 'cherries', 'banana'],
             ['Alice', 'Bob', 'Carol', 'David'],
             ['dogs', 'cats', 'moose', 'goose']]
```
Your printTable() function would print the following:

```
   apples Alice  dogs
  oranges   Bob  cats
 cherries Carol moose
   banana David goose
```
Hint: your code will first have to find the longest string in each of the inner lists so that the whole column can be wide enough to fit all the strings. You can store the maximum width of each column as a list of integers. The printTable() function can begin with colWidths = [0] * len(tableData), which will create a list containing the same number of 0 values as the number of inner lists in tableData. That way, colWidths[0] can store the width of the longest string in tableData[0], colWidths[1] can store the width of the longest string in tableData[1], and so on. You can then find the largest value in the colWidths list to find out what integer width to pass to the rjust() string method.

> ANSWER

```
def printTable(t):
   for i in range(len(t[0])):
       for j in range(len(t)):
                      print(t[j][i],end=' ')
       print()
tableData = [['apples', 'oranges', 'cherries', 'banana'],
             ['Alice', 'Bob', 'Carol', 'David'],
             ['dogs', 'cats', 'moose', 'goose']]
printTable(tableData)
```
