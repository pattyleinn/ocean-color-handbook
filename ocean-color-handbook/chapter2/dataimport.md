<!-- @format -->

**Authors:** Mathabo Malange, Phangoxolo Sishuba

# Data Input/Output

Python has several functions for creating, reading, updating, and deleting
files. In this section we will look at input/output to and from `text` and `CSV`
files to netCDF files. A built-in function for working with files in Python is
the `open()` function. The `open()` function takes two arguments: `filename` and
`mode`. There are four different modes (methods) for opening a file:

- "r": Read - Opens a file for reading, error if the file does not exist
- "a": Append - Opens a file for appending, creates if file does not exist
- "w": Write - Opens a file for writing, creates if file does not exist
- "x": Create - Creates a file, returns an error if the file exists

Besides the above file opening operations, the file can be opened in either text
or binary mode.

- "t" - Text - Default value. Text mode
- "b" - Binary - Binary mode (e.g. images)

## Text File Read

To open a text file for reading it suffice to pass the filename to the `open()`
function:

```python
>>> fid = open("filename.txt")
```

By default the file is open in read and text mode so that the "r" and "t"
options can be omitted. The above is equivalent to

```python
>>> fid = open("filename.txt", "rt")
```

It is important to note that the "filename.txt" is visible to the Python
interpreter from where the operation `open()` is being performed. What does this
mean? It means, the "filename.txt" indicates a full path to where the file is
located in the disk. Suppose the file is in the Windows documents folder. In
that case we can specify the full path as follows:

```python
>>> fid = open(r"C:\Users\username\Documents\filename.txt", "rt")
```

Note the "r" before the file path. This is to tell Python to treat the file path
as a raw string. What does this imply? Under ordinary circumstances, the Windows
file path separator is treated as an escape character in Python meaning that we
would get a syntax error after 'C:\'. In this case we used the "r" at the
beginning of the string or we could add a second escape character '\' to the
path so that only one is treated as a path separator as follows.

```python
>>> fid = open(r"C:\\Users\\username\\Documents\\filename.txt", "rt")
```

Escape characters are used for special operations such as specifying a newline
`\n`, a tab `\t`, a single quote `\'`, a carriage return `\r`, etc.

The `open()` operation returns an object 'fid' which we name file id, and which
has a `.read()` method for reading the content of the file.

```python
>>> fid = open("filename.txt", "rt")
>>> print(fid.read())
```

While the `.read()` method returns the whole text, we can pass an integer to
this method to read only a given number of text characters in the file such as
`.read(10)`. Besides the read() method, there is a `.readline()` method which
returns one line of text per call `print(fid.readline())`. By calling the same
method twice, two lines of text are returned. Finally, we can loop through the
contents of the file and process each line at the time.

```python
>>> fid = open("filename.txt", "rt")
>>> for line in fid:
>>>     print(line)
```

Once we are done processing the contents of the file, we should always close the
opened file with the `.close()` method. Python has a context manager (`with`)
which guarantees the file is properly closed even in the case when an error that
interrupts the normal process occurs.

```python
>>> fid = open("filename.txt", "rt")
>>> print(fid.read())
>>> fid.close()
```

or

```python
>>> with open("filename.txt", "rt") as fid:
>>>     print(fid.read())
```

## Text File Write

To write a text file in Python, the file needs to be opened in write mode using
the `open()` function, which in this case will take: the file name and `"w"` for
write mode:

```python
>>> fid = open("filename.txt", "w")
```

Once the file is open, the `.write()` method can be used to write content to the
file. By passing a string as an argument to the `.write()` method, the content
will be written to the file. Remember, to write multiple lines, the newline
character `\n` can be used as a separator.

```python
>>> fid.write("Hello, world!\n")
>>> fid.write("This is an example file.")
```

After writing the text to be included in the file, it is important to close the
file using the `.close()` method or use the context manager introduced above.
This step ensures that any buffered data is written to the file and frees up
system resources.

## netCDF File Read

NetCDF files are commonly used in various scientific domains, including
meteorology, climate science, oceanography, atmospheric sciences, and
geophysics. They are used to store complex multidimensional data. In Python, you
can use libraries such as `netCDF4` or `xarray`, which provide convenient
interfaces for reading, writing, and manipulating `netCDF` data.

To use the `netCDF4` library to read files in Python, the first step is to
import the library:

```python
>>> import netCDF4 as nc
```

`nc` here serves as alias to the `netCDF4` library. Remember to ensure that you
have the `netCDF4` library installed. You can install it using the pip package
manager by running `pip install netCDF4`. The `netCDF4` library contains a
function called `Dataset()` which is used to open `netCDF` files. To open a
`netCDF` file, we pass the file path to `Dataset()`.

```python
>>> filepath = "C:\\Users\\username\\Documents\\Data\\file.nc"
>>> dataset = nc.Dataset(filepath)
```

The netCDF4 library also has functions that allow you to access the variables
and attributes within the file once the NetCDF file is open. The variables
attribute provides a dictionary-like object that contains all the variables, and
the `ncattrs()` method returns a list of attributes associated with the NetCDF
file. You can use these variables and attributes to retrieve information and
data from the NetCDF file:

```python
>>> variables = dataset.variables
>>> attributes = dataset.ncattrs()
```

Once the data has been retrieved from the variable, you can perform any
necessary operations or analysis on it using Python's array manipulation and
data processing libraries such as `NumPy`, `pandas` or `SciPy`.

Similar to working with a text file, it is good practice to close the netCDF
file once you have finished reading or modifying its contents. Use the
`.close()` method of the dataset object created above:

```python
>>> dataset.close()
```
