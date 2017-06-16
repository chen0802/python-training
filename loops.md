# Loops

Loops allow us to execute a block of code many times while certain conditions are met.

## While Loops

There are two types of loops in Python: `while` loops and `for` loops. Here is the structure of a `while` loop:

```python
x = 0
while x < 5:
    print x
    x += 1
```

The code block inside the while loop executes as long as the condition, in this case `x < 5`, is `True`. The example above prints the integers 0 through 4.

Beware of infinite loops:

```python
x = 0
while x < 5:
    print x
```

This loop never exits because `x` remains less than 5 throughout.

**Exercise**: Write a `while` loop that prints integers ascending from 1 to 5 (inclusive).

**Exercise**: Write a `while` loop that prints integers descending from 7 to 0 (inclusive).

**Exercise**: What does the following loop do?

```python
x = 0
while x < 5:
    if x % 2 == 0:
        print x
    x += 1
```

## For Loops

-   [Python tutorial: `for` statements](https://docs.python.org/2/tutorial/controlflow.html#for-statements)
-   [Python tutorial: The `range` function](https://docs.python.org/2/tutorial/controlflow.html#the-range-function)
-   [Python tutorial: Looping Techniques](https://docs.python.org/2/tutorial/datastructures.html#looping-techniques)

First, let's look at the `range` function:

```python
In [11]: range(4)
Out[11]: [0, 1, 2, 3]

In [12]: range(1, 7)
Out[12]: [1, 2, 3, 4, 5, 6]

In [13]: range(1, 7, 2)
Out[13]: [1, 3, 5]
```

`range(N)` returns a `list` of integers from 0 until `N`, not including N.

`range(start, end)` returns a `list` of integers from `start` until `end`, not including `end`.

`range(start, end, step)` returns a `list` of integers from `start` advancing by `step` and ending at `end`, not including `end`.

Now consider the following `for` loop:

```python
for x in range(5):
    print x
```

Equivalently, we could have written:

```python
for x in [0, 1, 2, 3, 4]:
    print x
```

`enumerate` allows us to obtain both the list item and its index at each iteration of the loop:

```python
In [14]: for i, value in enumerate([20, 30, 40]):
    ...:     print i, value
0 20
1 30
2 40
```

**Exercise**: Write a `for` loop that prints integers ascending from 1 to 5 (inclusive).

**Exercise**: Write a `for` loop that prints integers descending from 7 to 0 (inclusive).

[**Back to Index**](README.md)
