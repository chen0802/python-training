# Functions

A *function* is a sequence of instructions that perform a specific task, packaged together as an independent, modular piece of code.

Functions are *reusable*. Functions prevent us from writing the same code over and over.

Functions offer *abstraction*. Consider some of the built-in functions we have encountered, e.g. `len`, `range`, `type`. For each of these functions, we didn't need to know how it was implemented, i.e. how it works inside. All we needed to know was the format of the input and the output, i.e. the interface.  Since the implementation is hidden from the caller, the implementation can change so long as the interface of the inputs and outputs remains the same.

## Calling Functions

To call a function, place the function arguments, if any, inside parentheses. Here are some examples of built-in functions which we have called before:

```python
In [1]: range(1, 5)
Out[1]: [1, 2, 3, 4]

In [2]: len("hello")
Out[2]: 5

In [3]: type(0.0)
Out[3]: float

In [4]: list()
Out[4]: []
```

[Here are all of the built-in functions for Python 2.](https://docs.python.org/2/library/functions.html) On your own, take a look at `any`, `all`, `min`, `max`, `sum`, and `isinstance`.

Let's take a look at the usage text for `range`:

    In [1]: range?
    Docstring:
    range(stop) -> list of integers
    range(start, stop[, step]) -> list of integers

    Return a list containing an arithmetic progression of integers.
    range(i, j) returns [i, i+1, i+2, ..., j-1]; start (!) defaults to 0.
    When step is given, it specifies the increment (or decrement).
    For example, range(4) returns [0, 1, 2, 3].  The end point is omitted!

The first usage of `range` accepts one input. The second usage of `range` accepts two inputs plus an optional third input. Both usages return a list.

## Defining Functions

-   [Python tutorial: Defining Functions](https://docs.python.org/2/tutorial/controlflow.html#defining-functions)

Functions are defined with a `def` statement followed by the function name, a set of parentheses (without or without function parameters in them), and finally a colon.

```python
def my_func():
    pass
```

This particular function doesn't do anything.

The following function uses the `return` keyword to return the value 5:

```python
def my_func():
    return 5
```

The moment `return` is executed, the function immediately exits.

```python
def my_func():
    return 5
    print "this line never executes"
```

The `return` statement returns `None` if no value is specified:

```python
def my_func():
    return # returns None
```

## Arguments and Parameters

-   [Python tutorial: Default Argument Values](https://docs.python.org/2/tutorial/controlflow.html#default-argument-values)

Values that are passed to a function are called *arguments*. The following function call has two arguments, `1` and `5`:

```python
In [1]: range(1, 5)
Out[1]: [1, 2, 3, 4]
```

When defining a function, *parameters* are the input variables to the function. In this function, there is one parameter, `n`:

```python
def my_func(n):
    return 5*n
```

Functions can have default parameter values:

```python
In [1]: def f(n=1):
   ...:     return 5*n
   ...: 

In [2]: f(3)
Out[2]: 15

In [3]: f()
Out[3]: 5
```

Parameters without default values must come before those parameters with default values:

```python
In [1]: def f(n=1, m):
   ...:     return 5*n
   ...: 
  File "<ipython-input-50-5ae46c26803d>", line 1
      def f(n=1, m):
SyntaxError: non-default argument follows default argument
```

## Docstrings

-   [Python tutorial: Document Strings](https://docs.python.org/2/tutorial/controlflow.html#documentation-strings)

A string placed immediately within a function definition is called a *docstring*. It is used to document what the function does.

```
In [1]: def f(n):
   ...:     """This function returns the input times five."""
   ...:     return 5*n

In [2]: f?
Signature: f(n)
Docstring: This function returns the input times five.
Type:      function
```

Docstrings can occupy multiple lines, if you need:

```python
In [1]: def g(n):
   ...:     """
   ...:     This function returns the input times six.
   ...:     You can use a multi-line string, if you want.
   ...:     """
   ...:     return 6*n
```

## Variable Scope

Variables defined within a function are only visible within the function.

```python
In [1]: my_global_var = 5

In [2]: def my_test_func():
   ...:     print "My global variable:",  my_global_var # Accessible and will print.
   ...:     my_local_var = 10 # Only accessible in my_test_func.
   ...:     print "My local variable:", my_local_var  
   ...:

In [3]: my_global_var # Remember it's accessible anywhere.
Out[3]: 5

In [4]: my_test_func()
My global variable: 5
My local variable: 10

In [5]: print my_local_var
NameError                                 Traceback (most recent call last)
<ipython-input-4-b0b2b2a41781> in <module>()
    > 1 print my_local_var

NameError: name 'my_local_var' is not defined
```

`my_global_var` is accessible anywhere, both inside and outside of our function. This is because it is in the *global scope*. `my_local_var`, on the other hand, was defined within `my_test_func`. As a result, it is enclosed within the scope of `my_test_func` and not accessible outside of it.   

## Exercises

1.  Write a function, `is_even(n)`, that returns `True` if `n` is even, and `False` otherwise.

    ```python
    In [1]: is_even(6)
    Out[1]: True

    In [2]: is_even(-6)
    Out[2]: True

    In [3]: is_even(7)
    Out[3]: False

    In [4]: is_even(6.1)
    Out[4]: False
    ```

2.  Write a function, `count_words(s)`, that returns a dictionary whose keys are words found in the string `s` and whose values are a count of the corresponding word:

    ```python
    In [1]: s = "the dog ate the cat"

    In [2]: count_words(s)
    Out[2]: {'ate': 1, 'cat': 1, 'dog': 1, 'the': 2}
    ```

    You may find the `split` string method and the `get` dictionary method useful.


[**Back to Index**](README.md)
