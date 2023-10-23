<!-- @format -->

**Authors:** Brishan Kalyan, Levis Sirikwa, Eligio Maure

**Reviewers:**

# Overview of data products in ocean colour

Ocean colour data is gathered by the various satellites
({numref}`Figure {number} <fig39>`) and stored as raw data (volts) that are
processed (Level 0 - 4) to produce products that can aid in sustainable
management by answering scientific and societal questions
({numref}`Figure {number} <fig34>` and {numref}`Figure {number} <fig39>`).

```{figure} ./figure39.png
---
align: left
name: fig39
---
Ocean colour satellites. A few active ocean colour satellites that are orbiting the Earth and gathering information.
```

## File formats

Data types and formats have changed over the years. However, standardisations
and conventions have been used across the various data providers (space agencies
/ private entities) to produce harmonised data and metadata outputs. A summary
of NASA’s Earth Science Data and Information System Standards Office standards
and conventions can be found
[here](https://www.earthdata.nasa.gov/esdis/esco/standards-and-practices). The
main file format used across ocean data is netCDF4.

NetCDF (Network Common Data Form) is a set of software libraries and
machine-independent data formats that support the creation, access, and sharing
of array-oriented scientific data
([NetCDF](https://docs.unidata.ucar.edu/netcdf-c/current/index.html)) . HDF
(Hierarchical Data Format) is a physical file format for storing scientific data
and a collection of utilities and applications for manipulating, viewing, and
analysing data in HDF files
([HDF](https://support.hdfgroup.org/products/hdf4/whatishdf.html)).

NetCDF is the combination of netCDF4 and HDF5 providing interoperability among
scientific data representations and integration of observations and numerical
model outputs. The goal of netCDF4 is to make netCDF more suitable for
high-performance computing and large datasets, and to provide a simple
high-level application programming interface (API) for HDF. The main reasons as
to why space agencies like NASA use the netCDF4/HDF5 file format can be found
[here](https://www.earthdata.nasa.gov/esdis/esco/standards-and-practices/netcdf-4hdf5-file-format).

## Data processing levels

Remote sensed data is computationally processed across various levels (0 - 4) to
allow for the creation of different products for end-user utilisation.
{numref}`Figure {number} <fig310>` simplifies the levels of processing across
ocean colour remote sensed data.

```{figure} ./figure310.png
---
align: left
name: fig310
---
Processing levels of satellite data to provide end-user products for various applications.
```

## Data Providers

There are many free and open data providers (space agencies/ private entities)
from where ocean colour data can be retrieved. The National Aeronautics and
Space Administration (NASA) provides different ways to browse, order and
download ocean colour data. NASA’s
[Worldview](https://worldview.earthdata.nasa.gov/) allows an interactive
visualisation and download capability for both historic and recent imagery
layers that are updated daily and made available within hours of observation.
The Worldview platform, however, is not a dedicated ocean colour dissemination
portal. The Ocean Biology Processing Group (OBPG) serves as the Distributed
Active Archive Center (DAAC) for all Ocean Biology (OB) data. The OB.DAAC
provides interfaces for (i)
[searching](https://oceandata.sci.gsfc.nasa.gov/api/file_search), (ii)
[browsing](https://oceancolor.gsfc.nasa.gov/cgi/browse.pl?sen=amod), (iii)
ordering and (iv) downloading ocean colour data at different data levels.
OB.DAAC data are free and open to the public, but downloading of any products
requires [registration](https://oceancolor.gsfc.nasa.gov/registration/). New
users should obtain an account on the
[Earthdata](https://urs.earthdata.nasa.gov/) user registration page prior to
being able to download the data. OB.DAAC data are also hosted in NASA's Earth
Observing System Data and Information System (EOSDIS). NASA's Common Metadata
Repository (CMR) provides a unified repository for Earth science metadata to
facilitate access to Earth Observation data through programmatic interfaces.
Examples on how to search data using CMR will be introduced below.

In this e-manual we focus the examples on data by NASA and JAXA (Japan Aerospace
eXploration Agency). We briefly cover the Globe Portal System (G-Portal), a
portal with similar capabilities of NASA’s OceanColor Web. Similarly, users
should obtain credentials prior to being able to download JAXA’s EO data. Like
the CMR, JAXA also provides a way for metadata search denoted CSW (G-Portal
User's manual, accessed 11 October 2022).

### Why NASA’s OB.DAAC and JAXA’s G-Portal?

We will extensively explain how to obtain ocean colour data from the OB.DAAC and
G-Portal since they are the main data providers used during the training that
inspired the creation of this e-manual. NASA’s OB.DAAC provides most of the
ocean colour data that extends beyond NASA’s sensors, such as GOCI, MERIS,
Sentinel 3A and 3B, etc. JAXA’s G-portal provides high spatial resolution data
that enables one to obtain detailed information on coastal areas.

However, there are many other ocean colour data providers worth of mention. The
[GlobColour Project](https://www.globcolour.info/) is a web portal serving as
the European Node for Global Ocean Colour. It provides scientists with a long
time series of consistently calibrated global ocean colour information. The
[Copernicus Marine Service](https://marine.copernicus.eu/) provides free and
open ocean data across the global ocean and across many ocean disciplines. The
[OceanColour - CCI](https://www.oceancolour.org/) is an ocean colour web portal
that provides satellite observations of ocean colour, focusing on the Ocean
Colour Climate Change Initiative project, it has browsing, downloading, and
analysis capabilities.
