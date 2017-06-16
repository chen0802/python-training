# File Input/Output

-   [Python tutorial: Reading and Writing Files](https://docs.python.org/2/tutorial/inputoutput.html#reading-and-writing-files)

To open a (text) file, we use the `with .. as` keywords and the `open` function:

```python
with open(file_path) as txt_file:
    pass
```

The `open` function opens a file at the specified path and returns a *file object* which we store to the variable `txt_file`. In the enclosed code block, we process the file object, e.g. read or write the file. At the end of the enclosed code block, the file is automatically closed for us.

In the case of a text file, we use a `for` loop to read the lines of text:

```python
In [2]: with open('test_text.txt') as txt_file:
   ...:     for line in txt_file:
   ...:         print line
   ...:         
This is a test

text file.

The quick red fox

jumped over the

lazy brown dog.
```

To write to a file, we add the `w` argument:

```python
In [3]: with open('test_text.txt', 'w') as f:
   ...:     f.write("hello world")
   ...:         
```

[**Back to Index**](README.md)
