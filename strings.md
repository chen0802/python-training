# Strings

-   [Python tutorial: Strings](https://docs.python.org/2/tutorial/introduction.html#strings)

Every bit of data we have seen so far -- `int`, `float`, `bool`, even functions themselves -- are known as *objects*. In Python, everything is an object.

Next, we will examine five more types of objects: strings, lists, dictionaries, tuples, and sets. These five data types also known as *collections* because they each can contain multiple values. These types are also known as *iterables* because we can iterate over their values.

A *string* is a sequence of characters. Strings have type `str`.

Strings are surrounded either by single quotes or double quotes.

```python
In [1]: 'This is a string.'
Out[1]: 'This is a string.'

In [2]: "This is another string, but this time with double quotation marks."
Out[2]: 'This is another string, but this time with double quotation marks.'

In [3]: 'They told me not to do this, but I didn't listen.'
SyntaxError: invalid syntax

In [4]: "Isn't this better?"
Out[4]: "Isn't this better?"
```

We can store strings in variables in the exact same way that we can store an `int`, `float`, or `bool`.

```python
In [1]: s = 'This is a string variable.'

In [2]: s
Out[2]: 'This is a string variable.'
```

## String Operations

Concatenation and repetition:

```python
In [1]: 'My first string' + 'My second string'
Out[1]: 'My first stringMy second string'

In [2]: 'My first string' + ' ' + 'My second string'
Out[2]: 'My first string My second string'

In [3]: 'Repeating string' * 3
Out[3]: 'Repeating stringRepeating stringRepeating string'

In [4]: 'Repeating string ' * 3
Out[4]: 'Repeating string Repeating string Repeating string '
```

One of the *methods* (a function attached to an object) that we can call on strings is the `strip` method. Methods are called on our objects through *dot notation*. We simply place a `.` at the end of our object (`str`, `int`, `float`, any variable, etc.), and then call the method like we would call a function.

Here's how the use of this *dot notation* looks in practice. Consider the `strip` method: 

```python
In [1]: ' hello world   '.strip()
Out[1]: 'hello world'
```

As we see, the `strip` method removes both the leading and trailing spaces from a string. 

Let's examine other string methods:

```python
In [1]: my_str_variable = 'this IS my STRING to PLAY around WITH.'

In [2]: my_str_variable.capitalize()
Out[2]: 'This is my string to play around with.'

In [3]: my_str_variable.upper()
Out[3]: 'THIS IS MY STRING TO PLAY AROUND WITH.'

In [4]: my_str_variable.lower()
Out[4]: 'this is my string to play around with.'

In [5]: my_str_variable.replace('STR', 'fl')
Out[5]: 'this IS my flING to PLAY around WITH.'

In [6]: my_str_variable.split()
Out[6]: ['this', 'IS', 'my', 'STRING', 'to', 'PLAY', 'around', 'WITH.']
```

In IPython, you can discover available string methods through *tab autocompletion*. Type the variable name followed by a period, and then press `<Tab>` to see all the methods available for strings.

```python
In [1]: my_str.  # Press <Tab> now!

my_str.capitalize  my_str.isalnum     my_str.lstrip      my_str.splitlines
my_str.center      my_str.isalpha     my_str.partition   my_str.startswith
my_str.count       my_str.isdigit     my_str.replace     my_str.strip
my_str.decode      my_str.islower     my_str.rfind       my_str.swapcase
my_str.encode      my_str.isspace     my_str.rindex      my_str.title
my_str.endswith    my_str.istitle     my_str.rjust       my_str.translate
my_str.expandtabs  my_str.isupper     my_str.rpartition  my_str.upper
my_str.find        my_str.join        my_str.rsplit      my_str.zfill
my_str.format      my_str.ljust       my_str.rstrip      
my_str.index       my_str.lower       my_str.split
```

(Tab autocompletion works for all variable types. We can also tab complete the names of the variables that were previously declared, i.e. those in the *namespace*).

## Accessing individual characters

To access individual elements, i.e. characters, in a string, use square brackets to surround the index of the element:

```python
In [1]: my_str_variable = 'Test String'

In [2]: my_str_variable[0]
Out[2]: 'T'

In [3]: my_str_variable[1]
Out[3]: 'e'

In [4]: my_str_variable[-1]
Out[4]: 'g'

In [5]: my_str_variable[-2]
Out[5]: 'n'
```

Like most programming languages, Python starts indexing strings and lists at 0.

Negative indices count back from the end of the string, i.e. the last character in the string can be accessed with the index `-1`. 

## Slicing

We can access a subset of the string by using the colon. This is known as *slicing*. The slice `start:end` starts at index `start` and ends at `end`, not including `end`.

```python
In [1]: my_str_variable = 'Test String'

In [2]: my_str_variable[1:4]
Out[2]: 'est'

In [4]: my_str_variable[-6:-1]
Out[4]: 'Strin'
```

By default, if you omit `start`, it starts the slice at the beginning. If you omit `end`, the slice ends at the end.

```python
In [5]: my_str_variable[1:]
Out[5]: 'est String'

In [6]: my_str_variable[:-1]
Out[6]: 'Test Strin'
```

You can also access elements at regular intervals by adding an optional third parameter, `start:end:step`.

```python
In [1] my_str_variable = 'Test String'

In [2]: my_str_variable[::2]
Out[2]: 'Ts tig'

In [3]: my_str_variable[2:10:3]
Out[3]: 'sSi'
```

## Iteration and Strings

We can iterate through the characters of a string in a few ways.

**Exercise**: what does the following code do?

```python
company = 'galvanize'
i = 0
while i < 9:
    print company[i]
    i += 1
```

---

The `len` function returns the number of items in a collection. For strings, it returns the length of the string.

```python
In [1]: my_str = 'hello'

In [2]: len(my_str)
Out[2]: 5
```

We can rewrite our `while` loop as follows:

```python
company = 'galvanize'
i = 0
while i < len(company):
    print company[i]
    i += 1
```

In general we try to stay away from `while` loops in Python.  We can also iterate over a string using a `for` loop.

**Exercise**: what does the following code do?

```python
company = 'galvanize'
for i in range(len(company)):
    print company[i]
```

---

In the case above, since `len(company)` is 9, `range(len(company))` returns a list of integers from 0 until 9.

With our `for` loop, the variable `i` is automatically changed, whereas in the `while` loop, we had to manually update `i`.

However, we can still make the `for` loop more concise:

```python
company = 'galvanize'
for char in company:
    print char
```

Instead of iterating over the integers in `range(len(company))`, then indexing the string `company`, we simply iterated over the characters directly. This is the preferred method for iterating over any collection, including strings.

## String Formatting 

String formatting allows us to insert variable contents into strings dynamically. Let's examine a few ways to do this.

```python
In [1]: my_name = 'Sean'

In [2]: print 'Hello %s' % my_name
Hello Sean

In [3]: print 'Hello {}'.format(my_name)
Hello Sean
```

In each case, we are completing our string with the value of the variable `my_name`. In the first case, we use a `%` sign to denote where the replacement should happen, followed by a letter to denote what type of variable will be passed in there (`s` is used for string, `d` is for a decimal, etc.). You can find what each letter denotes [here](https://docs.python.org/2/library/stdtypes.html#string-formatting). 

In the second case, we use brackets `{}` to denote where the replacement should take place in conjunction with the *format* method. We can also place numbers, or even variable names themselves inside these brackets and reference them in the `format` method:

```python
In [1]: print 'Hello {0}'.format(my_name)
Hello Sean 

In [2]: print 'Hello {name}'.format(name=my_name)
Hello Sean 
```

[**Back to Index**](README.md)
