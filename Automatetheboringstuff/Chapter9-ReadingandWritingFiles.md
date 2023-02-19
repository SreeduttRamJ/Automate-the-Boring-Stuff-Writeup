# Automate-the-Boring-Stuff-Writeup

<h3>Chapter 9 - Reading and Writing Files</h3>

<h4>Practice Questions </h4><br></br>

1. What is a relative path relative to?

```
A relative path is related to the programs current working directory

Here we use 2 notations 

dot(.) which is used to specify current directory
dot-dot(..) which is used to specify the parent folder
```

2. What does an absolute path start with?

```
Absolute path always start with the root folder
```

3. What does Path('C:/Users') / 'Al' evaluate to on Windows?

```
Path function in pathlib is used to return a file path using correct separators when we pass string values into it
```
![image](https://user-images.githubusercontent.com/113903135/219950065-1a22bdd2-8128-46e9-8542-a6c035575985.png)

4. What does 'C:/Users' / 'Al' evaluate to on Windows?

```
Gives a TypeError saying operand types are not supported
```
![image](https://user-images.githubusercontent.com/113903135/219950499-7c89ee5d-3a90-4849-a39c-217ff5c7e411.png)

5. What do the os.getcwd() and os.chdir() functions do?

```
os.getcwd() is used to obtain the current working directory same as Path.cwd()

os.chdir() is used to change the current working directory
```

6. What are the . and .. folders?

```
dot(.) which is used to specify current directory
dot-dot(..) which is used to specify the parent folder
```

7. In C:\bacon\eggs\spam.txt, which part is the dir name, and which part is the base name?

```
dir name => C:\bacon\eggs
base name => spam.txt
```

![image](https://user-images.githubusercontent.com/113903135/219951255-29b197f0-ac4c-4b44-8ffe-ae9b21d87467.png)


8. What are the three “mode” arguments that can be passed to the open() function?

```
r => read mode 
To read the contents of the file that exists

w => write mode
creates a new file if file does not exist and contents are overwritten from beginning 

a => append mode
appends data at the end of the existing file contents in the file are not overwritten
```

9. What happens if an existing file is opened in write mode?

```
Its existing contents get removed and becomes a new empty file
```

10. What is the difference between the read() and readlines() methods?

```
read funtion outputs a single string containing all the data in the file 
readlines function outputs a list containg strings were each string represent one line
```

11. What data structure does a shelf value resemble?

```
shelf resemble the dictionary data structure
```
