<!-- @format -->

**Authors:** Brishan Kalyan, Levis Sirikwa, Eligio Maure

**Reviewers:**

(chapter3)=

# Introduction to Ocean Colour

## Overview

Colour is a physical quantity related to light. This means that in order to see
colour there has to be light. In the absence of light, such as in the dark, we
see no colour. However, the colour we see is a result of the interaction between
the light field and the matter. Therefore, when we talk about ocean colour, we
should think about the interaction of sunlight and ocean water. Using our naked
eyes, we might say that the colour of the ocean is one of the different shades
of blue as shown in {numref}`Figure {number} <fig31>`. In most cases this may be
true and the colour we see is the least absorbed or the most reflected or
scattered by the material or medium. This chapter will introduce the basics of
ocean colour remote sensing. For a thorough and a more complete discussion on
the topic the reader is referenced to the Ocean Optics Web Book
([OOWB](https://www.oceanopticsbook.info/)) and the International Ocean-Colour
Coordinating Group ([IOCCG](https://ioccg.org/)) report series.

```{figure} ./figure31.webp
---
align: left
name: fig31
---

Ocean colour through the interaction of light and ocean water. The image depicts the shades of blue that can be seen by the naked eye when light interacts with ocean water. Source: Jennifer Levine [2017](https://crosstalk.cell.com/blog/why-is-the-ocean-different-colors-in-different-places).
```

## Learning Outcomes

- Understand the basic principles of ocean colour remote sensing;
- Understand the benefits and limitations of ocean colour remote sensing;
- Get familiar with the different ocean colour data products and a few
  providers;
- Understand the different levels of ocean colour remote sensed data processing;
  and
- Gain the ability to retrieve data using various data retrieval methods.

## How to Proceed

The chapter provides an introductory background to ocean colour and remote
sensing. Therefore, it is assumed that knowledge on the basic biology, physics
and chemistry would be enough for you to understand this chapter.

## Definition of Terms

| Terms           | Description                                                                                                                                                                                                                                                                         |
| :-------------- | :---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| API             | Application programming interface                                                                                                                                                                                                                                                   |
| CDOM            | Colored Dissolved Organic Matter (Chromophoric organic matter)                                                                                                                                                                                                                      |
| JAXA            | Japan Aerospace eXploration Agency                                                                                                                                                                                                                                                  |
| HDF             | Hierarchical Data Format                                                                                                                                                                                                                                                            |
| IR              | Infrared                                                                                                                                                                                                                                                                            |
| netCDF          | Network Common Data Form                                                                                                                                                                                                                                                            |
| NIR             | Near Infrared Radiation                                                                                                                                                                                                                                                             |
| Reflectance     | A form of reflection that light undergoes upon interacting with matter (water), and is dependent on the nature of the surface of matter. For instance, light can either be reflected back to the sky at an angle, or get reflected in different directions in the water environment |
| Spectrum        | A band in the form of intensity of light which is differentiated in terms of wavelengths and frequencies                                                                                                                                                                            |
| Solar radiation | A radiant (electromagnetic) energy from the sun which has been known to support important life functions like photosynthesis, and other metabolic processes on earth                                                                                                                |
| SST             | Sea surface temperature                                                                                                                                                                                                                                                             |
| Wavelength      | The distance between identical points (successive crests) in cycles of a wave form propagating in space such as electromagnetic waveform                                                                                                                                            |
| nanometers (nm) | The units used to measure wavelengths                                                                                                                                                                                                                                               |
| NASA            | National Aeronautics and Space Administration, USA                                                                                                                                                                                                                                  |
