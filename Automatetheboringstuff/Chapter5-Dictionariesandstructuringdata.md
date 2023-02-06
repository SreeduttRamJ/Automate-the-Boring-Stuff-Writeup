# Automate-the-Boring-Stuff-Writeup

<h3>Chapter 5 - Dictionaries and structuring data</h3>

<h4>Practice Questions</h4><br></br>

1. What does the code for an empty dictionary look like?

```
d={}
```

2. What does a dictionary value with a key 'foo' and a value 42 look like?

```
d={"foo":42}
```

3. What is the main difference between a dictionary and a list?

|List|Dictionary|
|:------------:|:-----------:|
|collection of index values pairs|collection of key value pairs|
|place elements in [ ] separated by commas(,)|place elements in { } as “key”:”value”,separated by commas(,)|
|value accesed using indices starting from 0|values accesed using keys|
|element order is maintained|element order may not be maintained|


4. What happens if you try to access spam['foo'] if spam is {'bar': 100}?

```
It shows a keyerror
```
![image](https://user-images.githubusercontent.com/113903135/217070393-27a70e59-01e4-4051-98f5-77ca2a1c7c3a.png)

5. If a dictionary is stored in spam, what is the difference between the expressions 'cat' in spam and 'cat' in spam.keys()?

```
Both returns same value as both expressions check if a key named 'cat' is present in spam
```
![image](https://user-images.githubusercontent.com/113903135/217070952-2b2ef455-f516-4a68-bd63-ca215dc633f3.png)

6. If a dictionary is stored in spam, what is the difference between the expressions 'cat' in spam and 'cat' in spam.values()?

```
first expression check for a key named 'cat' while second expression check for value named 'cat'
```

![image](https://user-images.githubusercontent.com/113903135/217071743-0c1af3eb-4ad6-4c82-878e-ee6a85fb1288.png)

7. What is a shortcut for the following code?

if 'color' not in spam: spam['color'] = 'black'

```
spam.setdefault('color', 'black')
```
![image](https://user-images.githubusercontent.com/113903135/217072235-c39550f4-8c5f-495a-a118-21757e17a8a1.png)

8. What module and function can be used to “pretty print” dictionary values?

```
we use the module pprint and function pprint()
```
