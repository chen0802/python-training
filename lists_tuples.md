# Lists

-   [Python tutorial: Lists](https://docs.python.org/2/tutorial/introduction.html#lists)
-   [Python tutorial: More on Lists](https://docs.python.org/2/tutorial/datastructures.html#more-on-lists)

*Lists* are collections of ordered items, i.e. sequences. A list can contain items of different types. For those familiar with other programming languages, lists are like arrays.

You can construct a list by surrounding an arbitrary number of items, separated by commas, with square brackets.

```python
In [1]: my_first_lst = [1, 'hello', 3, 'goodbye']

In [2]: my_first_lst
Out[2]: [1, 'hello', 3, 'goodbye']
```

We are able to place different types of values into our lists.  We could even create a list of lists.  

```python
In [1]: my_lst_of_lsts = [[1, 2, 3], ['str1', 'str2', 'str3'], [1, 'mixed', 3]]

In [2]: my_lst_of_lsts
Out[2]: [[1, 2, 3], ['str1', 'str2', 'str3'], [1, 'mixed', 3]]

In [3]: my_lst_of_lsts[1][-1]
Out[3]: 'str3'
```

## Casting

Earlier, we used the `int` and `float` functions to convert between numeric types. We can use the `list` function to convert a string into a list of its characters:

```python
In [3]: my_second_lst = list('hello')

In [4]: my_second_lst
Out[4]: ['h', 'e', 'l', 'l', 'o']
```

## List Operations

Here are some common `list` methods.

`append` adds an element to the end of the list:

```python
In [1]: my_lst = [1, 2, 3, 4]

In [2]: my_lst.append(5)

In [3]: my_lst
Out[3]: [1, 2, 3, 4, 5]
```

`pop` removes the last element from the list and returns it:

```python
In [4]: my_lst.pop()
Out[4]: 5

In [5]: my_lst
Out[5]: [1, 2, 3, 4]
```

`remove(value)` removes the first occurrence of `value` from the list:

```python
In [5]: my_lst.remove(4)

In [6]: my_lst
Out[6]: [1, 2, 3]
```

`reverse` will reverse the elements of the list, in place:

```python
In [7]: my_lst.reverse()

In [8]: my_lst
Out[8]: [3, 2, 1]
```

`sort` sorts the elements of the list, in place:
```python
In [9]: my_lst.sort()

In [10]: my_lst
Out[10]: [1, 2, 3]
```

Just as we can use tab complete in IPython to see all the available methods for strings, we can also do this with lists!

```python
In [1]: my_lst. # Press <Tab> now!

my_lst.append   my_lst.index    my_lst.remove   
my_lst.count    my_lst.insert   my_lst.reverse  
my_lst.extend   my_lst.pop      my_lst.sort
```

## Accessing Individual Elements

Indexing individual elements in a list is the same as indexing strings.

```python
In [1]: my_lst = [1, 2, 'hello', 'goodbye']

In [2]: my_lst[1]
Out[2]: 2

In [3]: my_lst[2:3]
Out[3]: ['hello']

In [4]: my_lst[:]
Out[4]: [1, 2, 'hello', 'goodbye']

In [5]: my_lst[-1]
Out[5]: 'goodbye'
```

As with strings, we can also add an optional `step` parameter, `start:end:step`, to our slice:

```python
In [1]: my_lst = [1, 2, 3, 4, 5, 6, 7, 8, 9, 10]

In [2]: my_lst[::3]
Out[2]: [1, 4, 7, 10]

In [3]: my_lst[4::2]
Out[3]: [5, 7, 9]

In [4]: my_lst[::-1]
Out[4]: [10, 9, 8, 7, 6, 5, 4, 3, 2, 1]
```

## Iteration

We iterate through lists the same way we iterate through strings.

```python
In [1]: my_lst = [1, 2, 3, 4, 5]

In [2]: for num in my_lst:
   ...:     print num

1
2
3
4
5
```

If you need both the index and the item itself, `enumerate` allows us to obtain both the list item and its index at each iteration of the loop:

```python
In [1]: my_lst = ['a', 'b', 'c']

In [2]: for idx, item in enumerate(my_lst):
   ...:     print idx, item
   ...:
0 a
1 b
2 c
```

## List Comprehensions

-   [Python tutorial: List Comprehensions](https://docs.python.org/2/tutorial/datastructures.html#list-comprehensions)

*List comprehensions* provide a concise way to produce sequences of items:

```python
In [1]: [n**2 for n in range(5)]
Out[1]: [0, 1, 4, 9, 16]
```

You can even add a filter that only produces items if a condition is met:

```python
In [2]: [n**2 for n in range(5) if n % 2 == 0]
Out[2]: [0, 4, 16]
```

## Mutability

Lists are *mutable*, meaning that the object can be changed after it has been created/instantiated. With lists, we can change the contents at any arbitrary index and even grow the list dynamically.

```python
# Declare a simple list
l = range(10)  # [0, 1, 2, 3, 4, 5, 6, 7, 8 , 9]

# Change the element at the 4th index, the fifth in the list, to 0
l[4] = 0  # [0, 1, 2, 3, 0, 5, 6, 7, 8 , 9]

# Add the number 1 to the end of the list
l.append(1)  # [0, 1, 2, 3, 0, 5, 6, 7, 8 , 9, 1]
```

# Tuples

-   [Python tutorial: Tuples and Sequences](https://docs.python.org/2/tutorial/datastructures.html#tuples-and-sequences)

Tuples are immutable lists. Once a tuple is created, it cannot be changed.

To construct a tuple, you surround an arbitrary number of items, separated by commas, with parentheses:

```python
my_tuple = (1, 2)
```

You actually don't even need the parentheses:

```python
my_tuple = 1, 2
```

You can cast a `list` or `str` to a `tuple`:

```python
In [1]: tuple([1, 2])
Out[1]: (1, 2)

In [2]: tuple('hello')
Out[2]: ('h', 'e', 'l', 'l', 'o')
```

For safety, there are times when you do not want your data structure to be mutable. Depending upon your application, you may encounter collections of data that should remain constant for the duration of your application. In that case, a tuple is more appropriate than a list.

Even though tuples are immutable, if they are storing any mutable data types, those nested structures *can* be changed.

```python
In [1]: t = (1, [1, 2])

In [2]: t[1].append(3)

In [3]: t
Out[3]: (1, [1, 2, 3])
```

Since tuples are immutable, they have very few methods associated with them - only `count` and `index`. Therefore, tuples are lightweight; they don't take up much space in memory but also don't have much built-in functionality.

[**Back to Index**](README.md)
