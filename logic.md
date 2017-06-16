# Boolean Logic

## If Statements

Consider the following `if` statement:

```python
x = 1
if x > 0:
    print "x is greater than zero"
```

If the condition, in this case `x > 0`, evaluates to `True`, then the subsequent *conditional* code block is executed. 

All code that has the same indentation level belongs to the same code block. This introduces the concept of *significant whitespace*: whitespace such as tabs and spaces, especially indentation, is a meaningful element of Python syntax. In many other languages, such whitespace is ignored and instead relies upon, e.g., curly braces.

The `if` statement ends in a colon.  Don't forget the colon.

## Comparison Operators

```python
In [1]: 1 == 2
Out[1]: False

In [2]: 1 != 2
Out[2]: True

In [3]: 1 < 2
Out[3]: True

In [4]: 1 > 2
Out[4]: False

In [5]: 1 <= 1
Out[5]: True

In [6]: 1 >= 1
Out[6]: True
```

Now that we understand conditionals, let's talk about how we can use them with variables to make our programs dynamic.

**Exercise**: What does the following code do? (The `print` function simply prints the following value to the screen.)

```python
x = 6
if x > 5:
    x += 10
print x
```

## Elif and Else

In addition to the `if` statement, Python provides us with `elif` ("else if") and `else`. 

```python
x = 5
if x > 20:
    print "x is greater than 20"
elif x > 10:
    print "x is greater than 10 and less than or equal to 20"
else:
    print "x is less than or equal to 10"
```

There can be any number of `elif` statements after the `if`. The `else` statement is optional.

```python
x = 5
if x > 20:
    print "x is greater than 20"
elif x > 10:
    print "x is greater than 10 and less than or equal to 20"
elif x > 0:
    print "x is greater than 0 and less than or equal to 10"
```

### Boolean Operators

`and`:

```python
In [17]: True and True
Out[17]: True

In [18]: True and False
Out[18]: False

In [19]: False and True
Out[19]: False

In [20]: False and False
Out[20]: False
```

`or`:

```python
In [21]: True or True
Out[21]: True

In [22]: True or False
Out[22]: True

In [23]: False or True
Out[23]: True

In [24]: False or False
Out[24]: False
```

`not`:

```python
In [25]: not True
Out[25]: False

In [26]: not False
Out[26]: True
```

[This page](http://www.mathcs.emory.edu/~valerie/courses/fall10/155/resources/op_precedence.html) lists Python operators by precedence. For comparison operators, `not` is highest, then `and`, and finally `or`.

**Exercise**: What does the following code do?

```python
x = 7
if x > 0 and x < 10:
    print "A"
    if x < 5 or x > 8:
        print "B"
    else:
        print "C"
else:
    print "D"
```

### Pass

`pass` is a Python statement that does nothing. `pass` is frequently used as a place holder, since Python will complain about empty code blocks.

```python
if x < 0:
    pass
elif x > 0:
    pass
else:
    pass
```

In the above example, without `pass`, that is incorrect Python syntax because the code block would be missing (since whitespace is significant).

[**Back to Index**](README.md)
