# Automate-the-Boring-Stuff-Writeup

<h3>Chapter 4 - Lists</h3>

<h4>Practice Questions</h4><br></br>

1. What is []?
```
It can seen as a list without values or an empty list
```

2. How would you assign the value 'hello' as the third value in a list stored in a variable named spam? (Assume spam contains [2, 4, 6, 8, 10].)

```
we can just write spam[2]='hello' as indexing start from 0
```
![image](https://user-images.githubusercontent.com/113903135/216836800-927d0d4a-08d3-4cbb-9030-40983ca4761b.png)

For the following three questions, let’s say spam contains the list ['a', 'b', 'c', 'd'].

3. What does spam[int(int('3' * 2) // 11)] evaluate to?

```
'3'* 2 gives you a string "33"
now its int("33")//11 = 33//11 = 3.0 (float type)
now its spam[int(3.0)] = spam[3] = 'd'
```
![image](https://user-images.githubusercontent.com/113903135/216837054-e4ffdf2f-c0df-46e7-ad89-42e4ef159902.png)

4. What does spam[-1] evaluate to?

```
It evaluates to 'd' as -1 is first index when start from the back of the list
```
![image](https://user-images.githubusercontent.com/113903135/216837153-06dc6909-9c5a-4d8f-8d28-21823122e32f.png)

5. What does spam[:2] evaluate to?

```
this command gives values from starting index zero to index 2
```
![image](https://user-images.githubusercontent.com/113903135/216837678-1e9a5e92-1dcb-4c79-b5aa-748a0b07a78f.png)

For the following three questions, let’s say bacon contains the list [3.14, 'cat', 11, 'cat', True].

6. What does bacon.index('cat') evaluate to?

```
This command returns index of the value cat from the list bacon
```
![image](https://user-images.githubusercontent.com/113903135/216837789-01654044-9bab-4e62-a14a-1776f7845e7d.png)

7. What does bacon.append(99) make the list value in bacon look like?

```
The code helps you insert the value 99 at the end of the list bacon
```
![image](https://user-images.githubusercontent.com/113903135/216837877-d942734f-79ea-4753-93d1-b8bc9c20d795.png)

8. What does bacon.remove('cat') make the list value in bacon look like?

```
Remove command helps you remove the first occurence of the input value from the list.
```
![image](https://user-images.githubusercontent.com/113903135/216837941-cf2f3937-7bd5-46e9-a263-0f28693d095c.png)

9. What are the operators for list concatenation and list replication?

```
concatination is '+'
replication is '*'
```
![image](https://user-images.githubusercontent.com/113903135/216838062-73cf704a-4d3d-48f5-ac9e-5e528eaf0286.png)

10. What is the difference between the append() and insert() list methods?

```
append() add a value to the end of the list
insert() add the element to the specified position in a list
```
![image](https://user-images.githubusercontent.com/113903135/216838256-b071355c-2a90-4c59-86c8-aa139e325259.png)

11. What are two ways to remove values from a list?

```
remove() and pop()
```

12. Name a few ways that list values are similar to string values.

```
both list and string can be
1. indexed
2. concatinated
3. replicated
4. used in loops
5. sliced
6. in and not in operators
7. used with len()
```

13. What is the difference between lists and tuples?

|       LIST      |       TUPLE      |
|:---------------:|:----------------:|
|mutable|immutable|
|Lists have several built-in methods|Tuple does not have many built-in methods|
| consume more memory|consumes less memory|


14. How do you type the tuple value that has just the integer value 42 in it?

```
t=(42)
```

15. How can you get the tuple form of a list value? How can you get the list form of a tuple value?

```
we can use built in function tuple() to convert list to tuple
we can use built in function list()  to convert tuple to list
```

16. Variables that “contain” list values don’t actually contain lists directly. What do they contain instead?

```
They actually acts as a reference to the location of the list almost like pointers
(Note pointers are variables that store memory address of another variable as its value
```

17. What is the difference between copy.copy() and copy.deepcopy()?

```
copy.copy() returns a shallow copy of the list 
copy.deepcopy() returns a deep copy of the list 
```

|     Shallow copy    |    Deep copy    |
|:-------------------:|:---------------:|
|only reference address is copied|epetitive copies are stored|
|fast|slow|
|changes reflects on the original object|changes are not reflected to the original|
|stores references in the main memory|stores copies of object value|

<br></br>

<h4>Practice Projects</h4>


For practice, write programs to do the following tasks.

<h4>Comma Code</h4>

Say you have a list value like this:

spam = ['apples', 'bananas', 'tofu', 'cats']

Write a function that takes a list value as an argument and returns a string with all the items separated by a comma and a space, with and inserted before the last item. For example, passing the previous spam list to the function would return 'apples, bananas, tofu, and cats'. But your function should be able to work with any list value passed to it. Be sure to test the case where an empty list [] is passed to your function.

> ANSWER

```
l=['apples', 'bananas', 'tofu', 'cats']
for i in range(len(l)):
    if i==len(l)-1:
        print("and ",l[i])
    else:
        print(l[i],end=", ")
```
![image](https://user-images.githubusercontent.com/113903135/216840146-4e548c7a-6d4b-442a-b13c-c3432ffbc1eb.png)



<h4>Coin Flip Streaks</h4>


For this exercise, we’ll try doing an experiment. If you flip a coin 100 times and write down an “H” for each heads and “T” for each tails, you’ll create a list that looks like “T T T T H H H H T T.” If you ask a human to make up 100 random coin flips, you’ll probably end up with alternating head-tail results like “H T H T H H T H T T,” which looks random (to humans), but isn’t mathematically random. A human will almost never write down a streak of six heads or six tails in a row, even though it is highly likely to happen in truly random coin flips. Humans are predictably bad at being random.

Write a program to find out how often a streak of six heads or a streak of six tails comes up in a randomly generated list of heads and tails. Your program breaks up the experiment into two parts: the first part generates a list of randomly selected 'heads' and 'tails' values, and the second part checks if there is a streak in it. Put all of this code in a loop that repeats the experiment 10,000 times so we can find out what percentage of the coin flips contains a streak of six heads or tails in a row. As a hint, the function call random.randint(0, 1) will return a 0 value 50% of the time and a 1 value the other 50% of the time.

You can start with the following template:

import random
numberOfStreaks = 0
for experimentNumber in range(10000):
    # Code that creates a list of 100 'heads' or 'tails' values.

    # Code that checks if there is a streak of 6 heads or tails in a row.
print('Chance of streak: %s%%' % (numberOfStreaks / 100))

Of course, this is only an estimate, but 10,000 is a decent sample size. Some knowledge of mathematics could give you the exact answer and save you the trouble of writing a program, but programmers are notoriously bad at math.

> ANSWER

```
import random
numberOfStreaks = 0
for i in range(10000):
    l=[]
    for i in range(100):
        l.append(random.randint(0,1))
    for i in range(0,95):
        if l[i:i+6] in [[1,1,1,1,1,1],[0,0,0,0,0,0]]:
            numberOfStreaks +=1
print('Chance of streak: %s%%' % (numberOfStreaks / 100))
```
![image](https://user-images.githubusercontent.com/113903135/216840874-d4b9eb0e-6600-48eb-b248-86ef9826dcea.png)


<h4>Character Picture Grid</h4>


Say you have a list of lists where each value in the inner lists is a one-character string, like this:
```
grid = [['.', '.', '.', '.', '.', '.'],
        ['.', 'O', 'O', '.', '.', '.'],
        ['O', 'O', 'O', 'O', '.', '.'],
        ['O', 'O', 'O', 'O', 'O', '.'],
        ['.', 'O', 'O', 'O', 'O', 'O'],
        ['O', 'O', 'O', 'O', 'O', '.'],
        ['O', 'O', 'O', 'O', '.', '.'],
        ['.', 'O', 'O', '.', '.', '.'],
        ['.', '.', '.', '.', '.', '.']]
```

Think of grid[x][y] as being the character at the x- and y-coordinates of a “picture” drawn with text characters. The (0, 0) origin is in the upper-left corner, the x-coordinates increase going right, and the y-coordinates increase going down.

Copy the previous grid value, and write code that uses it to print the image.
```
..OO.OO..
.OOOOOOO.
.OOOOOOO.
..OOOOO..
...OOO...
....O....
```

> ANSWER

```
grid = [['.', '.', '.', '.', '.', '.'],
        ['.', 'O', 'O', '.', '.', '.'],
        ['O', 'O', 'O', 'O', '.', '.'],
        ['O', 'O', 'O', 'O', 'O', '.'],
        ['.', 'O', 'O', 'O', 'O', 'O'],
        ['O', 'O', 'O', 'O', 'O', '.'],
        ['O', 'O', 'O', 'O', '.', '.'],
        ['.', 'O', 'O', '.', '.', '.'],
        ['.', '.', '.', '.', '.', '.']]
for i in range(len(grid[0])):
    x=0
    for j in range(len(grid)):
        if grid[j][i]=='.':
            if x==1:
                print('',grid[j][i],end=' ')
                x=0
            else:
                print(grid[j][i],end=' ')
        else:
            print(grid[j][i],end='')
            x=1
    print()
