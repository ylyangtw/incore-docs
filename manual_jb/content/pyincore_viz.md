# pyIncore viz

Visualization package associated with pyIncore is called **pyIncore-viz**. It contains advanced Python packages 
and methods required for visualizing and disseminating the IN-CORE results, mainly via Jupyter Notebooks. 
A library called [Matplotlib](https://matplotlib.org/) for creating static visualizations in Python is already 
part of pyIncore (as a dependency). We decided however to keep more interactive visualization in a separate package. 
An example would be for example geo-referenced mapping with [ipyleaflet](https://ipyleaflet.readthedocs.io/en/latest/).

## Features
1. Geospatial visualization such as tornado path or earthquake raster data, vector data (shapfile) and network data.
2. Data visualization, graphs of data such as statistical curves including pre-processing.
3. Creates map window from inventory of multiple csv files stored in a folder (in progress).
 
## Prerequisites

- **pyIncore**: A user must have pyIncore package installed. See [pyIncore section](pyincore) for details.

- **Virtual environment**: We recommend that users work with virtual environment managers called [Anaconda](https://www.anaconda.com/) 
or [Miniconda](https://docs.conda.io/en/latest/miniconda.html).

- Mac OS specific notes: There is a Mac specific `matplotlib` installation issue addressed 
  at StackOverflow [link 1](https://stackoverflow.com/questions/4130355/python-matplotlib-framework-under-macosx) and [link 2](https://stackoverflow.com/questions/21784641/installation-issue-with-matplotlib-python). In a nutshell, insert line:
    ```
        backend : Agg
    ```
    
    into `~/.matplotlib/matplotlibrc` file. You must create the file (`matplotlibrc`) if it does not exist.

## Installation

1. To install pyIncore-viz, navigate to the directory you want to use for running Jupyter Notebooks and run the following command:
    ```
    conda install -c in-core pyincore-viz
    ```
   
   For update replace `install` with `update`.
   
2. To check that the package is installed run 
    ```
    conda list
    ```
    It will again list all packages currently installed. You can check if **pyincore** and **pyincore-viz** exist in the list.

## Examples

Jupyter notebook showing a visualization of shape files and other geographic information. Web Map Service (WMS) layer 
generated by Geoserver is also used for mapping an infrastructure. The shapefile format is a geospatial vector data 
format for geographic information system (GIS) software developed by Esri for interoperability among GIS software products. 
WMS is protocol for geo-referenced images developed by the OG Consortium.

Examples: <br />
[pyincore-viz-example.ipynb](https://github.com/IN-CORE/incore-docs/blob/master/notebooks/pyincore-viz-example.ipynb) <br />
[pyincore-viz-analysis-example.ipynb](https://github.com/IN-CORE/incore-docs/blob/master/notebooks/pyincore-viz-analysis-example.ipynb)