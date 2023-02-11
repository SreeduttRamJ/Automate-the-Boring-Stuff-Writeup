# Automate-the-Boring-Stuff-Writeup

<h3>Chapter 7 - Pattern Matching With Regular Expressions</h3>

<h4>Practice Questions </h4><br></br>

1. What is the function that creates Regex objects?

```
Regex object inn python is a sequence of characters that form a pattern to be used for searchin
compile() function from re module is used to create regex objects.
```

2. Why are raw strings often used when creating Regex objects?

```
Raw strings are used so that backslash does not escape

r'sting' is how you create a raw string
```

3. What does the search() method return?

```
search method in regex returns the first occurance of the pattern in the input
```

4. How do you get the actual strings that match the pattern from a Match object?

```
We can make use of the group method to return the strings
```

5. In the regex created from r'(\d\d\d)-(\d\d\d-\d\d\d\d)', what does group 0 cover? Group 1? Group 2?

```
group 0  cover the whole string
group 1 cover the first parenthesis
group 2 cover the second parenthesis
```

6. Parentheses and periods have specific meanings in regular expression syntax. How would you specify that you want a regex to match actual parentheses and period characters?

```

```