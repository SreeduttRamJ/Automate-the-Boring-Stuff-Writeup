# Automate-the-Boring-Stuff-Writeup

<h3>Chapter 2 - Flow Control</h3>

Practice Questions

1. What are the two values of the Boolean data type? How do you write them?
```
The two boolean values are true and false.
They are written with their first letter in capital True and False.
```
2. What are the three Boolean operators?
```
Boolean operators are
AND
NOT
OR 
```
3. Write out the truth tables of each Boolean operator (that is, every possible combination of Boolean values for the operator and what they evaluate to).
```
AND Operator Truth Table

T AND T => T
T AND F => F
F AND T => F
F AND F => F

OR Operator Truth Table

T OR T => T
T OR F => T
F OR T => T
F OR F => F

NOT Operator Truth Table

NOT T => F
NOT F => T
```
4. What do the following expressions evaluate to?

      a) (5 > 4) and (3 == 5)<br>
  b) not (5 > 4)<br> 
  c) (5 > 4) or (3 == 5)<br>
  d) not ((5 > 4) or (3 == 5))<br>
  e) (True and True) and (True == False)<br>
  f)(not False) or (not True)

```
a) False
b) False
c) True
d) False
e) False
f) True
```
![image](https://user-images.githubusercontent.com/113903135/216751326-13268af4-5367-4359-b3b1-497c48b27834.png)

5. What are the six comparison operators?
```
less than <
greater than >
less than or equal to <=
greater than or equal to >=
equal to ==
not equal to !=
```

6. What is the difference between the equal to operator and the assignment operator?

| Equal to operator | Assignment Operator |
|:----------------------------:|:-----------------------------:|
|==|=|
|comparison operator|assignment operator|
|compare two values|assign a value to a variable|
|![image](https://user-images.githubusercontent.com/113903135/216752209-69b0ba5e-d125-4f0d-ac0a-dcb335984809.png)|![image](https://user-images.githubusercontent.com/113903135/216752239-9a51d6f4-9328-40c8-b909-8ffe4b06792e.png)|

7. Explain what a condition is and where you would use one.
```
A conditional statement is a statement that help you make a decision according to a certain scenario. 
They are specified using boolean expressions whic are evaluated as true or false.
We use it when we need a specific process to happen during a specific scenario.
```
![image](https://user-images.githubusercontent.com/113903135/216752722-52da15be-5335-4ffd-8277-db0f9c2b1a06.png)

8. Identify the three blocks in this code:

![image](https://user-images.githubusercontent.com/113903135/216752760-f96197d5-b469-4f78-bcdc-d1de3578b644.png)

```
1st block is everything inside "if spam==10"

    print('eggs')
    if spam > 5:
        print('bacon')
    else:
        print('ham')
    print('spam')
    
2nd block is everything inside "if spam > 5"

    print('bacon')
    
3rd block is everything inside "else"

    print('ham')
 ```
 9. Write code that prints Hello if 1 is stored in spam, prints Howdy if 2 is stored in spam, and prints Greetings! if anything else is stored in spam.
 ```
spam=1
if spam==1 : print("Hello")
elif spam==2 : print("Howdy")
else : print("Greetings")
```
![image](https://user-images.githubusercontent.com/113903135/216753264-8502a329-7c36-4b46-a2f1-a2fce002a759.png)

10. What keys can you press if your program is stuck in an infinite loop?

```
You stop the infinite loop by clicking CTRL + C
```

11. What is the difference between break and continue?

| break statement | continue statement |
|:----------------|:---------------|
|immediatly terminate the loop|terminate the current iteration and resume control to the next iteration of the loop|
|![image](https://user-images.githubusercontent.com/113903135/216753988-9d82bef7-5dbe-459e-b555-70cf565b5bea.png)|![image](https://user-images.githubusercontent.com/113903135/216754027-1e69804f-037d-4c75-a495-6753d1176a6d.png)|
|Above snippet you can see that loop is terminated as soon as it entered if statement|Above snippet you can see that only iterations were loop enters the if statement is terminated but loop still resume control|

12. What is the difference between range(10), range(0, 10), and range(0, 10, 1) in a for loop?

![image](https://user-images.githubusercontent.com/113903135/216755480-7361eef7-9abc-4cb1-ba43-ec3c944be463.png)
```
from the snippet above it might seem like there is not much difference but the three
for loops given are actually different ways to implement for loop using range

See the below snippet
```
![image](https://user-images.githubusercontent.com/113903135/216755677-6ccff9a1-22f7-4efe-b6c7-5a2952507db1.png)

```
see the difference 

range function has 3 parts range(start_value,stop_value,step_value)

range(10) is same as range(stop_value) which gives values from 0 to stop_value - 1

range(0,10) is same as range(start_value,stop_value) which gives values from 
start_value to stop_value - 1

range function usually increment values by one that is start_value,start_value + 1,start_value + 2,....
this is were step value come to play default step value is 1 as the default startvalue is 0

raange(0,10,n) changes the step value that difference between 2 immediate values are n
```

13. Write a short program that prints the numbers 1 to 10 using a for loop. Then write an equivalent program that prints the numbers 1 to 10 using a while loop.

```
for i in range(1,11):print(i,end=' ')

i=1
while i<11:
    print(i,end=' ')
    i=i+1
```
![image](https://user-images.githubusercontent.com/113903135/216756288-595f92e9-9745-4fc8-8490-9a6b661d511d.png)

14. If you had a function named bacon() inside a module named spam, how would you call it after importing spam?

```
import spam
spam.bacon()
```
