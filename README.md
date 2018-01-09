# Using Qgrid with Binder. Also have Seaborn, VPython, and other useful dependencies

[![Binder](https://mybinder.org/badge.svg)](https://beta.mybinder.org/v2/gh/fomightez/qgrid-notebooks/master?filepath=index.ipynb)

This repository allows use of Qgrid with Binder. 

Qgrid is an interactive grid for sorting, filtering, and editing DataFrames in Jupyter notebooks, and is described [here](https://github.com/quantopian/qgrid). This is my fork demonstrating use in Binder and came from [here](https://github.com/quantopian/qgrid-notebooks).


----

### Post-Fork Differences
- After forking the the base `qgrid-notebooks` example, I added my other favorite dependencies using the `environment.yml`. 


### Issues

-  I found a better solution than I used in my appmode repo for adding the dependencies that conda cannot handle and needs `pip install`. Learned from http://repo2docker.readthedocs.io/en/latest/samples.html#conda-mixed-requirements I can add sub-group for pip to the `environment.yml` and that fixes my issue with vpnotebook, vpython, and matplotlib_venn without need of another file.

