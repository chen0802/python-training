# Basic Variables and Types

## Variable Data Types

-   [Python tutorial: Numbers](https://docs.python.org/2/tutorial/introduction.html#numbers)

There are a number of data *types* built into Python. Among them include:

-   `int`, an integer.
-   `float`, a floating-point number, i.e. with a decimal.
-   `bool`, Boolean, which only takes values `True` or `False`.
-   `None`, a special value that roughly means "nothing".

Let's experiment with using these types in the IPython console. Type `7` and press Enter.

```python
In [1]: 7
Out[1]: 7
```

The IPython console will accept Python commands at the input prompt, execute them, and print the results of the computation.

```python
In [1]: 7.5
Out[1]: 7.5

In [1]: 7.
Out[1]: 7.0
```

To inspect the type of any Python object, use the `type` function.

```python
In [1]: type(7)
Out[1]: int

In [2]: type(7.5)
Out[2]: float

In [3]: type(True)
Out[3]: bool

In [4]: type(None)
Out[4]: NoneType
```

## Arithmetic Operations

```python
In [1]: 7 + 8
Out[1]: 15

In [2]: 7 - 8
Out[2]: -1

In [3]: 7 * 8
Out[3]: 56

In [4]: 7 / 8
Out[4]: 0

In [5]: 7 / 8.0
Out[5]: 0.875

In [6]: 7 / 8.
Out[6]: 0.875

In [7]: 8 % 3
Out[7]: 2

In [8]: 7 ** 2
Out[8]: 49
```

## Casting

*Casting* is the process of converting the data type of an object. Sometimes, some information is lost during casting, e.g. casting a `float` to an `int`.

```python
In [4]: int(8.9)
Out[4]: 8

In [4]: int(-8.9)
Out[4]: 8

In [4]: float(8)
Out[4]: 8.0

In [4]: float(0)
Out[4]: 0.0
```
## Variable Assignment

*Variable assignment* occurs with the `=` operator. The value on the right-hand side is assigned to the variable on the left-hand side.

```python
In [1]: x = 1

In [2]: x
Out[2]: 1

In [3]: x + 1
Out[3]: 2

In [4]: x
Out[4]: 1
```

Note that we saw no output from the first command above. This is because the return value that would have been printed to the console for output was assigned to the variable `x`. This is why we had to view it in the next line with a simple call to `x`.

For most variables, the common naming convention in Python is to use lower case with underscores, e.g. `first_name`. It is good practice to use descriptive variable names.

Let's add 5 to the current value of `x` and store the new value in `x`.

```python
In [1]: x = x + 5

In [2]: x
Out[2]: 6
```

Another way to do this is with the `+=` or *increment* operator:

```python
In [8]: y = 7

In [9]: y += 1

In [10]: y
Out[10]: 8
```

Similar operators exist, e.g. `-=`, `*=`, `/=`.

[**Back to Index**](README.md)
