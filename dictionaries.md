# Dictionaries

-   [Python tutorial: Dictionaries](https://docs.python.org/2/tutorial/datastructures.html#dictionaries)

The collections we've seen so far -- strings, lists, and tuples -- are ordered, i.e. their contents have a sequential ordering. But sometimes, we don't care about ordering.

A *dictionary* is an unordered collection of key/value pairs. (For those familiar with other programming languages, dictionaries are like associative arrays.)

To construct a dictionary, we use curly braces to surround the key/value pairs, each key/value pair is separated by commas, and keys and values are separated by colons.

```python
In [1]: states_caps_dict = {'Georgia': 'Atlanta', 'Colorado': 'Denver', 'Indiana': 'Indianapolis'}

In [2]: states_caps_dict
Out[2]: {'Colorado': 'Denver', 'Georgia': 'Atlanta', 'Indiana': 'Indianapolis'}
```

To initialize an empty dictionary, either use `dict()` or simply `{}`:

```python
In [1]: dict()
Out[1]: {}

In [2]: {}
Out[2]: {}
```

## Accessing Elements

As with strings, lists, and tuples, we use square brackets to index a dictionary. However, the index is the key of the key/value pair. The dictionary then returns the associated value. 

```python
In [1]: states_caps_dict = {'Georgia': 'Atlanta', 'Colorado': 'Denver', 'Indiana': 'Indianapolis'}

In [2]: states_caps_dict['Indiana']
Out[2]: 'Indianapolis'
```

If we tried to find a key that wasn't already in the dictionary, we get a `KeyError` telling us that that key is not stored in the dictionary.

```python
In [3]: states_caps_dict['Washington']
___________________________________________________________________________
KeyError                                  Traceback (most recent call last)
<ipython-input-3-fac88f6748> in <module>()
    > 1 states_caps_dict['Washington']

KeyError: 'Washington'
```

The `get` method also returns a value associated with a key but instead returns a default value if the key doesn't exist.

```python
In [4]: states_caps_dict.get('Washington', 'State not found')
Out[4]: 'State not found'
```

We can use the `get` method to update a key that might not yet exist:

```python
In [1]: tweet_count = dict() # empty dictionary

In [2]: tweet_count['Trump'] = tweet_count.get('Trump', 0) + 1 # 0 + 1

In [3]: tweet_count
Out[3]: {'Trump': 1}

In [4]: tweet_count['Trump'] = tweet_count.get('Trump', 0) + 1 # 1 + 1

In [5]: tweet_count
Out[5]: {'Trump': 2}
```

## Mutability

Dictionaries are mutable, i.e. after it is created, its contents can be changed.

```python
In [1]: my_dict = {'thing': 1, 'other': 2}

In [2]: my_dict['thing']
Out[2]: 1

In [3]: my_dict['thing'] = 3

In [4]: my_dict['thing']
Out[4]: 3

In [5]: my_dict['thingy'] = 4

In [6]: my_dict['thingy']
Out[6]: 4

In [7]: my_dict
Out[7]: {'other': 2, 'thing': 3, 'thingy': 4}
```

## Iterating

As with strings and lists and tuples, dictionaries are iterables. This means that Python knows how to traverse every element in the collection. The way we did this with list was with a `for` loop. We will again use the `for` loop with dictionaries, but there are a few changes in how it's implemented, since dictionaries are unordered key-value pairs.

If we traverse a dictionary with a `for` loop, we only retrieve the keys:

```python
In [1]: states_caps_dict = {'Georgia': 'Atlanta', 'Colorado': 'Denver', 'Indiana': 'Indianapolis'}

In [2]: for key in states_caps_dict:
   ...:     print key

Georgia
Indiana
Colorado
```

To retrieve both the keys and values, use the `items` (or `iteritems`) method:

```python
In [1]: states_caps_dict = {'Georgia': 'Atlanta', 'Colorado': 'Denver', 'Indiana': 'Indianapolis'}

In [2]: for key, value in states_caps_dict.items():
   ...:     print key, value

Colorado Denver
Indiana Indianapolis
Georgia Atlanta
```

[**Back to Index**](README.md)
