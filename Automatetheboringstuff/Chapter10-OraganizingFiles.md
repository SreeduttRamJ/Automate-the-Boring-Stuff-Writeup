# Automate-the-Boring-Stuff-Writeup

<h3>Chapter 10 - Organizing Files</h3>

<h4>Practice Questions </h4><br></br>

1. What is the difference between shutil.copy() and shutil.copytree()?

```
Both are functions from the module shutil and are used to copy files
shutil.copy() copy file to a given file path and also can be renamed if specified
shutil.copytree() can be used to copy the whole folder with all the data contained to a different location

shutil.copy(source,destination)
shutil.copytree(source,destination)
```

2. What function is used to rename files?

```
We can rename a file using move function by giving the destination path the same as the source path and changing the filename
```

3. What is the difference between the delete functions in the send2trash and shutil modules?

