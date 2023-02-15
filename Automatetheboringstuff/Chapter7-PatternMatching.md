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
One can just use \ for escaping periods and parenthesis so you can use actual parentheses & period characters
```

7. The findall() method returns a list of strings or a list of tuples of strings. What makes it return one or the other?

```
list of groups if groups are present while gives a list of string if no group
```
![image](https://user-images.githubusercontent.com/113903135/218538571-9b7a92b8-663f-4062-8fe3-5be82645e2cf.png)

8. What does the | character signify in regular expressions?

```
It used as an or operator 
That is if you have to search for either a or b we use | 
It gives first occurance as the output

CODE:
import re
date=re.compile(r'aron|qw|ice')
x=date.search('wwd aron qw ice')

OUTPUT

ice
```
![image](https://user-images.githubusercontent.com/113903135/218544287-3ccb2760-e5fe-4ea8-bb77-f730a3f2a52c.png)


9. What two things does the ? character signify in regular expressions?

```
? is used as an if condition
that is we want to match a pattern optionally


CODE:

import re
date=re.compile(r'ice(tea)?')
x=date.search('wwd aron qw ice')
y=date.search('wwd aron qw icetea')

OUTPUT:

ice
icetea
```
10. What is the difference between the + and * characters in regular expressions?

```
* mean zero or more 
That is the term to be matched even if not there there is no issue

+ mean one or more 
That is the term to be matched should be present atleast once 

CODE:

import re
date=re.compile(r'ice(tea)*')
x=date.search('wwd aron qw ice')
y=date.search('wwd aron qw iceteateatea')
date=re.compile(r'ice(tea)+')
z=date.search('wwd aron qw ice')
q=date.search('wwd aron qw iceteateatea')

OUTPUT:

ice
iceteateatea
None
iceteateatea

```
11. What is the difference between {3} and {3,5} in regular expressions?

```
(ice){3} is the same as (ice)(ice)(ice)
That is it check for iceiceice

(ice){3,5} is the same as (ice)(ice)(ice)|(ice)(ice)(ice)(ice)|(ice)(ice)(ice)(ice)(ice)
That is it cahecks for either iceiceice or iceiceiceice or iceiceiceiceice
```

12. What do the \d, \w, and \s shorthand character classes signify in regular expressions?
```
```

