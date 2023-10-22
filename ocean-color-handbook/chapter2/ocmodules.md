<!-- @format -->

**Authors:** Mathabo Malange, Phangoxolo Sishuba

# Modules Relevant to Ocean Colour Data Analysis

The following table introduces a list of modules relevant to the discussion of
this manual. This list is not exhausting but enough for the data analysis that
will follow in latter parts of the book.

```{table} Modules for data manipulation and analysis in Python.
:name: oc-modules-ref

| Module Name                                             | Short Description                                                                                                  |
| :------------------------------------------------------ | :----------------------------------------------------------------------------------------------------------------- |
| [Cartopy](https://scitools.org.uk/cartopy/docs/latest/) | Python package designed for geospatial data processing in order to produce maps and other geospatial data analyses |
| [h5py](https://www.h5py.org/)                           | Python interface to the HDF5 (Hierarchical Data Format) binary data                                                |
| [Matplotlib](https://matplotlib.org/)                   | Python library for creating static, animated, and interactive visualisations                                       |
| [netCDF4](https://unidata.github.io/netcdf4-python/)    | Python interface to the NetCDF (Network Common Data Form) C library                                                |
| [Numpy](https://numpy.org/)                             | The fundamental package for scientific computing with Python                                                       |
| [Pandas](https://unidata.github.io/netcdf4-python/)     | Python based data analysis and manipulation tool                                                                   |
| [Pyresample](https://unidata.github.io/netcdf4-python/) | Resampling of geospatial image data in Python                                                                      |
| [pyproj](https://unidata.github.io/netcdf4-python/)     | Python interface to the library for cartographic projections and coordinate transformations (PROJ)                 |
| [Requests](https://unidata.github.io/netcdf4-python/)   | Library for making HTTP/1.1 requests in Python                                                                     |
```

## Importing Modules into Python

To use packages or libraries in Python, you will need to import them at the
start of your Python code:

```python
import matplotlib.pytplot as plt
import numpy as np
import pandas as pd
import h5py
```

Note that for the `matplotlib` library we can also import it using the following
synthax `from … import` as exemplified below.

```python
from matplotlib import pyplot as plt
```
