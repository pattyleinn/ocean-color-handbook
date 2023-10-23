<!-- @format -->

**Authors:** Mathabo Malange, Phangoxolo Sishuba

**Reviewers:**

# Data Visualisation

There are many packages in Python that allow one to perform powerful data
analysis. [Matplotlib](https://matplotlib.org/) is a comprehensive library for
creating static, animated, and interactive visualizations in Python. Matplotlib
makes easy things easy and hard things possible. It is a 2D graphics package
used, across user interfaces and operating systems, for application development,
interactive scripting, publication-quality image generation, in IPython shells
and Jupyter notebook, web application servers, and in graphical user interface
toolkits {cite}`Hunter2007`. With Matplotlib, we are able to

Matplotlib is organised into a hierarchy. At the top of the hierarchy, there is
a library called pyplot (`import matplotlib.pyplot as plt`). We call `pyplot` to
create a figure. The figure keeps track of all the child Axes, artists (titles,
figure legends, etc), and the canvas.

```python
import matplotlib.pyplot as plt

plt.plot([0, 1], [0, 1])
```
