<!-- @format -->

**Authors:** Eligio Maure, Patricia Simwa

**Reviewers:**

(chapter5)=

# Data Processing and Analysis in Python

## Overview

In this section we introduce ocean colour data retrieval methods, mostly
focusing on NASA and JAXA provided products. We then proceed to discuss how to
read and visualise the obtained products. Since the book focuses on the use of
ocean colour level-2 data, which are in the satellite view geometry, a
discussion on how to project these swath images into an Earth map projection is
given. Once the data is map projected then spatial and temporal analysis can be
done with ease. In the subsequent parts we introduce how to do the temporal and
spatial analysis. We close by discussing how the results can be saved to either
text file (e.g., csv) or netCDF files.

## Learning Outcomes

- Gain the ability to retrieve and map project a swath imagery
- Gain the ability to extract a pixel values from a swath
- Gain the ability to composite a series of swath imagery
- Perform time series analysis

## How to Proceed

This chapter assumes familiarity with materials of:

- {ref}`chapter2`
- {ref}`chapter3`
- {ref}`chapter4`

This chapter will start with swath reprojection. Data retrieval, reading and
visualisation have been introduced and discussed in {numref}`chapter3`. For the
swath reprojection, the following modules are used.

| Module Name                                                | Description                                                                         |
| :--------------------------------------------------------- | :---------------------------------------------------------------------------------- |
| [Pyresample](https://pyresample.readthedocs.io/en/latest/) | Resampling geospatial image data in Python                                          |
| [pyproj](https://pyproj4.github.io/pyproj/stable/)         | Python interface to cartographic projections and coordinate transformations library |

Once the data has been reasample, we can either visualise the resampled data or
the swath image using [`matplotlib`](https://matplotlib.org/).
[`Cartopy`](https://scitools.org.uk/cartopy/docs/latest/) helps in plotting
projected swath imagery on a map. Some of the possible map projections to use
with Cartopy were introduced in {numref}`chapter4`. Additional information can
be obtained directly from the Cartopy homepage.
