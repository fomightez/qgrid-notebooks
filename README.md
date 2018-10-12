# Using Qgrid with Binder. Also have Seaborn, VPython, BLAST, and other useful dependencies

[![Binder](https://mybinder.org/badge.svg)](https://mybinder.org/v2/gh/fomightez/qgrid-notebooks/master?filepath=index.ipynb)

This repository allows use of Qgrid with Binder. 

Qgrid is an interactive grid for sorting, filtering, and editing DataFrames in Jupyter notebooks, and is described [here](https://github.com/quantopian/qgrid). This is my fork demonstrating use in Binder and came from [here](https://github.com/quantopian/qgrid-notebooks).


----

### Post-Fork Differences
- After forking the the base `qgrid-notebooks` example, I added my other favorite dependencies using the `environment.yml`. (I just noticed even though I didn't list it there, it seems I can also use `import ipywidgets as widgets` to use widgets in notebooks launched from here. They were probably a depedency of qgrid since that is a widget.)


### Issues

-  At first I couldn't get commands to handle dependencies conda wouldn't handle, i.e., need `pip`, placed in `postBuild` to work even though I made executable and had copied the exact one from the appmode repo, probably because cannot use web interface to deal with an executable since I have since had it work elsewhere if I use git software only. Howver, I found a better solution than I used in my appmode repo for adding the dependencies that conda cannot handle and needs `pip install`. Learned from [here](http://repo2docker.readthedocs.io/en/latest/samples.html#conda-mixed-requirements) and [here](https://github.com/binder-examples/python-conda_pip) that I can add sub-group for pip to the `environment.yml` and that fixes my issue with vpnotebook, vpython, and matplotlib_venn without need of another file.

----

### Related

There is a repository that I made that allows use of Qgrid and appmode along with the dependencies I favor. It is [here](https://github.com/fomightez/qgridNappmode-notebooks). Unfortunately because of the way Github works, I cannot have two forks of the same repository and so it is a mirror of this one before I removed appmode. I removed appmode from this repository because it breaks the use of the technique described by harshil's answer [here](http://stackoverflow.com/questions/27934885/how-to-hide-code-from-cells-in-ipython-notebook-visualized-with-nbviewer) for hiding all code cells with a toggle button.
