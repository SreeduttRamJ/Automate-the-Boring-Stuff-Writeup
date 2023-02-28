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
\d represent any numeric 1 t0 9
\w represent any letter, numeric digit, or the underscore character.(used for words)
\s represent any space, tab , newline
```
13. What do the \D, \W, and \S shorthand character classes signify in regular expressions?

```
\D represent any character that is not a numeric 1 to 9
\W represent any character that is not a letter, numeric digit, or the underscore character.
\S represent any character that is not a space, tab , newline
```

14. What is the difference between .* and .*? ?

```
. means any character other than newline and * means 0 or more characters

.* matches as much characters as possible to match
.*? matches the minimum characters required to match

CODE:
import re
date=re.compile(r'ice(.*)tea')
x=date.search('wwd aron qw ice tea')
y=date.search('wwd aron qw icetea tea tea')
date=re.compile(r'ice(.*?)tea')
z=date.search('wwd aron qw ice  tea')
q=date.search('wwd aron qw icetea tea tea')

OUTPUT:
ice tea
icetea tea tea
ice  tea
icetea
```
15. What is the character class syntax to match all numbers and lowercase letters?

```
we can use [a-z0-9] as the range

CODE:
import re
date=re.compile(r'[a-z0-9]')
x=date.findall('wwd aron qw ice 1231 tea 214323')

OUTPUT:
['w', 'w', 'd', 'a', 'r', 'o', 'n', 'q', 'w', 'i', 'c', 'e', '1', '2', '3', '1', 't', 'e', '
a', '2', '1', '4', '3', '2', '3']
```

16. How do you make a regular expression case-insensitive?

```
We can use re.I to make the expression case insensitive

CODE:
import re
date=re.compile(r'ICE')
x=date.findall('wwd aron qw ICE ice Ice')
date=re.compile(r'ICE',re.I)
y=date.findall('wwd aron qw ICE ice Ice')

OUTPUT:
['ICE']
['ICE', 'ice', 'Ice']
```

17. What does the . character normally match? What does it match if re.DOTALL is passed as the second argument to re.compile()?

```
. character match any character except mewline 
re.DOTALL is used to make . character read new line

CODE:
import re
date=re.compile(r'.*')
x=date.search('''wwd aron qw
 ICE ice Ice''')
date=re.compile(r'.*',re.DOTALL)
y=date.search('''wwd aron qw 
ICE ice Ice''')

OUTPUT:
wwd aron qw
wwd aron qw \nICE ice Ice
```

18. If numRegex = re.compile(r'\d+'), what will numRegex.sub('X', '12 drummers, 11 pipers, five rings, 3 hens') return?

```
CODE:

numRegex = re.compile(r'\d+')
x=numRegex.sub('X', '12 drummers, 11 pipers, five rings, 3 hens')

OUTPUT:
X drummers, X pipers, five rings, X hens

here we use \d+ to match one or more numeric characters until space
sub is used to substitute the matched characters with given character 
```

19. What does passing re.VERBOSE as the second argument to re.compile() allow you to do?

```
re.VERBOSE allow you to type your regular expression in multiline
```

20. How would you write a regex that matches a number with commas for every three digits? It must match the following:

- '42'
- '1,234'
- '6,368,745'

but not the following:

- '12,34,567' (which has only two digits between the commas)
- '1234' (which lacks commas)

```
CODE:
import re
date=re.compile(r'((^\d{1,3},)(\d\d\d(,)?)*$)')
x=date.search('23,123,123')
y=date.search('14,13,121')
z=date.search('1234')
q=date.search('123,12,111')

OUTPUT:
23,123,123
None
None
None

```

21. How would you write a regex that matches the full name of someone whose last name is Watanabe? You can assume that the first name that comes before it will always be one word that begins with a capital letter. The regex must match the following:

- 'Haruto Watanabe'
- 'Alice Watanabe'
- 'RoboCop Watanabe'

but not the following:

- 'haruto Watanabe' (where the first name is not capitalized)
- 'Mr. Watanabe' (where the preceding word has a nonletter character)
- 'Watanabe' (which has no first name)
- 'Haruto watanabe' (where Watanabe is not capitalized)

```
CODE:

import re
date=re.compile(r'^[A-Z]([A-Za-z])*\sWatanabe$')
x=date.search('Watanabe')
y=date.search('RoboCop Watanabe')
z=date.search('Mr. Watanabe')
q=date.search('Haruto watanabe')

OUTPUT:

None
RoboCop Watanabe
None
None
```

22. How would you write a regex that matches a sentence where the first word is either Alice, Bob, or Carol; the second word is either eats, pets, or throws; the third word is apples, cats, or baseballs; and the sentence ends with a period? This regex should be case-insensitive. It must match the following:

- 'Alice eats apples.'
- 'Bob pets cats.'
- 'Carol throws baseballs.'
- 'Alice throws Apples.'
- 'BOB EATS CATS.'

but not the following:

- 'RoboCop eats apples.'
- 'ALICE THROWS FOOTBALLS.'
- 'Carol eats 7 cats.'

```
CODE:

import re
date=re.compile(r'''^
(ALICE|BOB|CAROL)\s
(THROWS|EATS|PETS)\s
(CATS.|APPLES.|BASEBALLS.)
$''',re.VERBOSE|re.I)
x=date.search('BOB EATS CATS.')
y=date.search('Carol throws base')
z=date.search('Carol eats 7 cats.')
q=date.search('Alice eats apples.')

OUTPUT:
BOB EATS CATS.
None
None
Alice eats apples.
```
<br></br>

<h3>Practice Projects </h3><br></br>

Date Detection<br></br>

Write a regular expression that can detect dates in the DD/MM/YYYY format. Assume that the days range from 01 to 31, the months range from 01 to 12, and the years range from 1000 to 2999. Note that if the day or month is a single digit, it’ll have a leading zero.

The regular expression doesn’t have to detect correct days for each month or for leap years; it will accept nonexistent dates like 31/02/2020 or 31/04/2021. Then store these strings into variables named month, day, and year, and write additional code that can detect if it is a valid date. April, June, September, and November have 30 days, February has 28 days, and the rest of the months have 31 days. February has 29 days in leap years. Leap years are every year evenly divisible by 4, except for years evenly divisible by 100, unless the year is also evenly divisible by 400. Note how this calculation makes it impossible to make a reasonably sized regular expression that can detect a valid date.

```
import re
def check(day, month, year):

    monthday = {4: 30, 6: 30, 9: 30, 11: 30, 2: 28}
    days = monthday.get(month, 31)

    if days == 28:
        if year % 4 == 0:
            days = 29

    if day <= days:
        return True
    return False
        

date=input("date= ")
date_regex = re.compile(r"([0-2]\d|3[01])/(0\d|1[0-2])/([12]\d{3})")
x= date_regex.search(date)
if x:
    day = int(x.group(1))
    month = int(x.group(2))
    year = int(x.group(3))

if check(day, month, year):
    print("Day: ",day," \n Month: ",month," Year: ",year)
else:
    print('Invalid Date!')
```
