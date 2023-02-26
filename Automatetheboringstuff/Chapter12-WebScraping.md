# Automate-the-Boring-Stuff-Writeup

<h3>Chapter 12 - Web Scraping</h3>

<h4>Practice Questions </h4><br></br>

1. Briefly describe the differences between the webbrowser, requests, bs4, and selenium modules.
```
webbrowser -> opens a browser to a specific page
requests -> Download files and webpages from internet
bs4 -> Parses HTML
selenium -> Launch and control web browser
```

2. What type of object is returned by requests.get()? How can you access the downloaded content as a string value?

```
requests.get() returns a response object which contain the response of the webserver
You can access the downloaded content using .text

res = requests.get(URL)
print(res.text)
```

3. What requests method checks that the download worked?

```
we can check it using

res = requests.get(URL)
res.status_code == requests.codes.ok

if the above code returns true its downloaded
```

4. How can you get the HTTP status code of a requests response?
```
we can use .status_code

some of them are 
404 -> not found
200 -> ok
```
5. How do you save a requests response to a file?

```
we can save the response by first opening a file in write mode
after which you can save content in it

.iter_content(size) and for loop

qwerty = open('hi.txt', 'w')
for ch in res.iter_content(100000):
        qwerty.write(chunk)

Here ch is in bytes as .iter_content() categorize contents in the form of bytes
hi.txt is placed in current working directory if you using any file not in the current working directory then give the path
```
6. What is the keyboard shortcut for opening a browser’s developer tools?

```
View ▸ Developer ▸ Developer Tools

or you can use shortcut 

Google Chrome: Ctrl + Shift + I (Windows) or Command + Option + I (Mac)
Mozilla Firefox: Ctrl + Shift + I (Windows) or Command + Option + I (Mac)
Microsoft Edge: Ctrl + Shift + I (Windows) or Command + Option + I (Mac)
Safari: Option + Command + C (Mac)
```

7. How can you view (in the developer tools) the HTML of a specific element on a web page?

```
You can use inspect element tool or select element tool
```

8. What is the CSS selector string that would find the element with an id attribute of main?

```
soup.select('#main')

here soup is the BeautifulSoup object
```

9. What is the CSS selector string that would find the elements with a CSS class of highlight?

```
soup.select('.highlight')

here soup is the BeautifulSoup object
```

10. What is the CSS selector string that would find all the `<div>` elements inside another `<div>` element?

```
soup.select('div div')

here soup is the BeautifulSoup object
```

11. What is the CSS selector string that would find the `<button>` element with a value attribute set to favorite?

```
soup.select('button[value="favorite"]')

here soup is the BeautifulSoup object
```

12. Say you have a Beautiful Soup Tag object stored in the variable spam for the element `<div>Hello, world!</div>`. How could you get a string 'Hello, world!' from the Tag object?
```
we can do that using spam.text
```
13. How would you store all the attributes of a Beautiful Soup Tag object in a variable named linkElem?

```
we can use linkElem.attrs
```
14. Running import selenium doesn’t work. How do you properly import the selenium module?

```
we import it using

from selenium import webdriver
```

15. What’s the difference between the find_element_* and find_elements_* methods?

```
find_element_* returns the first matching element as WebElement object.
find_elements_* methods return a list of all  matching elements as WebElement objects
```
16. What methods do Selenium’s WebElement objects have for simulating mouse clicks and keyboard keys?

```
It uses click() and send_keys() 
These are performed using advanced user interactions API in Selenium Webdriver
```

17. You could call send_keys(Keys.ENTER) on the Submit button’s WebElement object, but what is an easier way to submit a form with selenium?

```
It is better to use .submit() to submit the form with selenium.
```

18. How can you simulate clicking a browser’s Forward, Back, and Refresh buttons with selenium?

```
driver.navigate().forward() 
driver.navigate().back()
driver.navigate().refresh()

These work on the basis of your browser history



