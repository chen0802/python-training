# Imports

-   [Python tutorial: Modules](https://docs.python.org/2/tutorial/modules.html)

The `import` statement allows us to access code (generally functions and classes) from existing Python libraries. For example, the `math` module is part of the Python Standard Library:

```python
In [1]: import math

In [2]: math.sqrt(49)
Out[2]: 7.0
```

You can import individual functions from a library using the `from .. import` keyword:

```python
In [1]: from math import sqrt

In [2]: sqrt(49)
Out[2]: 7.0
```

To inspect the contents of a library, press `<Tab>` to autocomplete:

```python
In [3]: math. # Press <Tab> now
        math.acos      math.atanh     math.e         math.factorial math.hypot     math.log10     math.sin       
        math.acosh     math.ceil      math.erf       math.floor     math.isinf     math.log1p     math.sinh      
        math.asin      math.copysign  math.erfc      math.fmod      math.isnan     math.modf      math.sqrt      
        math.asinh     math.cos       math.exp       math.frexp     math.ldexp     math.pi        math.tan       
        math.atan      math.cosh      math.expm1     math.fsum      math.lgamma    math.pow       math.tanh      
        math.atan2     math.degrees   math.fabs      math.gamma     math.log       math.radians   math.trunc     
```

You can provide an alias to an imported library so that it is easier to type:

```python
In [1]: import matplotlib.pyplot as plt

In [2]: plt.plot(x)
```

You can import from your own Python files. For example, if you were in the same directory as `txt_file_processing.py`, and that file defined a function `create_report`, you could import that library and use its contents:

```python
In [1]: import txt_file_processing

In [2]: txt_file_processing.create_report('report.txt')
```

## Exercises

Inside the IPython shell, import the following modules, e.g. `import math`. Use tab autocompletion in the IPython shell to explore the contents of each module. Perhaps play around with some of the contents.

1.  [`math`](https://docs.python.org/2/library/math.html)
1.  [`random`](https://docs.python.org/2/library/random.html)
2.  [`string`](https://docs.python.org/2/library/string.html)
3.  [`datetime`](https://docs.python.org/2/library/datetime.html)
3.  [`os.path`](https://docs.python.org/2/library/os.path.html)
3.  [`os`](https://docs.python.org/2/library/os.html)
3.  [`sys`](https://docs.python.org/2/library/sys.html)

[**Back to Index**](README.md)
