<!-- @format -->

**Authors:** Eligio Maure, Blessing Kamwi

(chapter4)=

# Working with Map Projections in Python

## Overview

The representation of a portion of the Earth on a two dimensional planar surface
leads to distortion of one form or another that often requires some
transformation of the round surface to a plane denoted projection
{cite}`Snyder1987,Snyder1989,Usery2009`. Simply put, a map projection is a
systematic representation of all or part of the surface of a round body, like
the Earth, on a plane. This representation often includes lines that delineate
meridians and parallels, depending on the definitions of a map projection
{cite}`Snyder1989`. To perform operations with geographic data, such as overlays
or accurate spatial/temporal analysis, a common coordinate framework is
required; map projections introduce transformations that allow the creation of
such common frameworks. The techniques involved in these transformations use
some kind of a coordinate system. Geodesy is the mathematical treatment of these
transformations. Together with geodesy, map projections allow the representation
and visualisation of the transformed spherical or ellipsoidal form of the
Earth’s surface to a two dimensional representation.

This chapter gives a brief outlook of map projections, the associated
transformations between different projections and the advantages and limitations
of working with different projections. We will briefly discuss a few important
concepts associated with geodesy and coordinate systems prior to the discussion
of map projections. As discussed in {numref}`chapter2`, Cartopy is the common
package used in Python to work with imagery that requires a map projection.
Matplotlib provides the visualisation capability.

## Learning Outcomes

- Gain familiarity with cartographic transformations
- Gain ability to visualise satellite scenes on a map
- Gain ability to convert a given map projection to another based on the use
  case

## How to Proceed

This chapter assumes familiarity with materials of {ref}`chapter2`.
