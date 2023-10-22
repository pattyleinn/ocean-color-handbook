<!-- @format -->

**Authors:** Mathabo Malange, Phangoxolo Sishuba

# Language Structures and Syntax

Now a working Python environment has been set we can move into learning the
basics of the Python programming language.

## Basic Data Types

Python has several built-in data types which are used to represent different
types of data. With different data types, different operations can be performed.
The following are the built-in data types in Python.

```{table} Standard or built-in data types in Python.
:name: basic-dtypes-ref

| Data Type     | Class               |
| :------------ | :------------------ |
| Numeric Types | int, float, complex |
| Text Type     | str                 |
| Boolean Type  | bool                |
| None Type     | NoneType            |
```

### Numeric type: integer

Integers are numbers with no decimal parts, such as `-5, -4, -1, 0, 7, 10, 100`,
etc. To declare an integer in Python, simply write: `variable_name = value`

Example:

```python
user_age = 48
```

### Numeric type: float

The float type in Python refers to floating-point numbers, those with decimal
parts, such as `1.234, -3.654, 12.01`, etc. Like an integer, to declare a float
in Python, simply write: `variable_name = value`.

Example:

```python
user_height = 1.75
user_weight = 80.2
```

The above is same as:

```python
user_height, user_weight = 1.75, 80.2
```

The latter involves two operations. On the right hand we pack the values and on
the left we unpack and each variable is assigned to the corresponding value on
the right.

### Numeric type: complex

Most general-purpose programming languages have limited or no support for
complex numbers. Python is special in this regard as it has complex numbers
built-in. In mathematical jargon, complex numbers are specified as
`"real" + "imaginary-j"`. To define a complex number we write:

```{python echo=TRUE}
2 + 3j
```

We are not going to work with complex numbers in this handbook but we just
included them for completeness.

### Text type: string

Strings represent a text surrounded by either single, double or triple quote
marks. Triple quoted strings may span multiple lines. To declare a string, we
can write

- variable_name = 'value' (single quotes)
- variable_name = "value" (double quotes)
- variable_name = '''value''' (triple quotes)

Example:

```python
user_first_name = 'Michael'
user_second_name = "Gary"
user_surname = '''Scott'''
```

Strings include a number of built-in methods to manipulate them. An example of a
method available in Python is the _.upper()_ which turns the string characters
to capital letters.

```python
'Michael'.upper()
MICHAEL
```

### Boolean type: logical

Boolean values consist of only the values `True` and `False` of the class bool.
These values are used to check truthness or falsehood. In Python, the bool class
is a subclass of the int class. When we compare two values, the expression is
evaluated and returns as either `True` or `False`, for instance:

```python
print(21 > 2, 1 == 3)
True, False
```

## Composite Data Type or Data Structures

```{table} Standard or built-in composite data types or data structures in Python.
:name: comp-dtypes-ref

| Data Type             | Class                        |
| :-------------------- | :--------------------------- |
| Sequence Types        | list, tuple, range           |
| Mapping Type          | dict                         |
| Set Types             | set, frozenset               |
| Binary Sequence Types | bytes, bytearray, memoryview |
```

### Sequence type: list

Lists are mutable sequences, meaning they **can** be modified after creation,
typically used to store collections of homogeneous items (where the precise
degree of similarity will vary by application). Lists may be constructed in
several ways:

- Using a pair of square brackets to denote the empty list: `[]`
- Using square brackets, separating items with commas: `[a], [a, b, c]`
- Using a list comprehension: `[x for x in iterable]`
- Using the type constructor: `list()` or `list(iterable)`

```python
empty_list = []
empty_list
[]
```

### Sequence type: tuple

Tuples are immutable sequences, meaning they **cannot** be modified after
creation, typically used to store collections of heterogeneous data (such as the
2-tuples produced by the
[`enumerate()`](https://docs.python.org/3/library/functions.html#enumerate)
built-in). Tuples are also used for cases where an immutable sequence of
homogeneous data is needed (such as allowing storage in a
[`set`](https://docs.python.org/3/library/stdtypes.html#set) or
[`dict`](https://docs.python.org/3/library/stdtypes.html#dict) instance). Tuples
may be constructed in a number of ways:

- Using a pair of parentheses to denote the empty tuple: `()`
- Using a trailing comma for a singleton tuple: `a,` or `(a,)`
- Separating items with commas: `a, b, c` or `(a, b, c)`
- Using the [`tuple()`](https://docs.python.org/3/library/stdtypes.html#tuple)
  built-in: `tuple()` or `tuple(iterable)`

```python
tuple('abc')
('a', 'b', 'c')
```

<!-- {glue:} abc_tuple -->

### Sequence type: range

The [`range`](https://docs.python.org/3/library/stdtypes.html#range) type
represents an immutable sequence of numbers and is commonly used for looping a
specific number of times in
[`for`](https://docs.python.org/3/reference/compound_stmts.html#for) loops. The
advantage of the `range` type over a regular `list` or `tuple` is that a `range`
object will always take the same (small) amount of memory, no matter the size of
the `range` it represents (as it only stores the start, stop and step values,
calculating individual items and subranges as needed). If a single value is
passed to `range`, it represents the value of the `stop` parameter, as in

```python
range(2)
range(0, 2)
```

<!-- {glue:} stop_only -->

If two values are passed to `range`, they represents the value of the `start`
and `stop` parameters. When the value of the `start` parameter is omitted it
defaults to `0`.

```python
range(1, 3)
range(1, 3)
```

<!-- {glue:} start_stop -->

The last case is when we also supply the `step`. The value of the `step`
parameter defaults to `1` if not supplied.

```python
range(1, 3, 2)
range(1, 3, 2)
```

```{warning}
TypeError is raised if 'float' step is supplied as only integer is expected.
```

### Mapping type: dict

A [`mapping`](https://docs.python.org/3/glossary.html#term-mapping) object maps
[`hashable`](https://docs.python.org/3/glossary.html#term-hashable) values to
arbitrary objects. Mappings are mutable objects. `dictionary` is currently the
only one standard mapping type. Dictionaries can be created by several means:

- Use a comma-separated list of `key: value` pairs within braces:
  `{'jack': 4098, 'sjoerd': 4127}` or `{4098: 'jack', 4127: 'sjoerd'}`
- Use a `dict` comprehension: `{}`, `{x: x \*\* 2 for x in range(10)}`
- Use the type constructor: `dict()`, `dict([('foo', 100), ('bar', 200)])`,
  `dict(foo=100, bar=200)`

```python
dict(one=1, two=2, three=3)
{'one': 1, 'two': 2, 'three': 3}
```

### Set type: set

A set object is an unordered collection of distinct
[hashable](https://docs.python.org/3/glossary.html#term-hashable) objects.
Common uses include membership testing, removing duplicates from a sequence, and
computing mathematical operations such as intersection, union, difference, and
symmetric difference. Sets can be created by several means:

- Use a comma-separated list of elements within braces: `{'jack', 'sjoerd'}`
- Use a set comprehension: `{c for c in 'abracadabra' if c not in 'abc'}`
- Use the type constructor: `set()`, `set('foobar')`, `set(['a', 'b', 'foo'])`

```python
set('foobar')
{'a', 'b', 'f', 'o', 'r'}
```

### Binary sequence type: bytes

Bytes objects are immutable sequences of single bytes. Since many major binary
protocols are based on the ASCII text encoding, bytes objects offer several
methods that are only valid when working with ASCII compatible data and are
closely related to string objects in a variety of other ways.

In-depth discussion about the above different data types, {numref} Table %s
`comp-dtypes-ref` can be found
[here](https://docs.python.org/3/library/stdtypes.html#).

## Type Casting in Python

Sometimes it is necessary to convert a variable from one type to another, such
as from a string (`str`) to an integer (`int`) or vice-versa. Here, we discuss
three built-in functions in Python that allow us to do type casting. These are
the `int()`, `float()`, and `str()` functions. The round brackets indicate that
these are functions.

The `int()` function takes in a `float` or a string and converts it to an
integer. To change a `float` to an integer, we can write

```python
int(5.71234)
5
```

The result of the above operation is 5. Anything after the decimal point is
removed. To change a string to an integer, we can type

```python
int("4")
4
```

Again, the result of the above operation is 4. However, we cannot do
`int("Hello")` or `int('4.258746')`. We will get an error in both cases. To be
able to convert decimal numbers into an integer we need to use a specialised
built-in module decimal.

```python
from decimal import Decimal

int(Decimal('4.258746'))
4
```

The decimal package is a rich library with methods that can also directly
convert the string number to either `int` or `float`.
