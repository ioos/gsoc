# GSoC 2022 Results

U.S. IOOS is participating for the second time as a mentoring organization for Google’s Summer of Code.
For the 2022 GSoC edition there are four new projects ranging from data visualization, data accessibility, data pre-processing for cloud optimization, and code re-factorization.

Three projects are completed:

- [echoshader](https://github.com/OSOceanAcoustics/echoshader/wiki/Google-Summer-of-Code-2022): Interactive visualization of ocean sonar data.
- [kerchunk](https://github.com/fsspec/GSoC-kechunk-2022/blob/main/GSOC_monitor.md) - interfacing WRF forecast grib2 data to zarray.
- [pyobis](https://ayushanand18.github.io/GSoC_design_documents/): Making ocean biodiversity data easily accessible with python.

And one extended until November 2022 thanks to GSoC's new flexible project timeline policy:

- [erddapy](https://github.com/ioos/erddapy/issues?q=label%3AGSoC22+is%3Aclosed): Refactoring into separate core and object layers.

Important highlights:

- Before GSoC 2022 the `pyobis` project was abandoned and the last available version did not work with the new OBIS API. Thanks to GSoC contributor Ayush Anand, OBIS users can once again rely on is Python library to query to the OBIS database.
-  The `kerchunk` library is a middle ground between converting data to a cloud optimized format while still keeping its original form. Peter Marsh created a [working demo](https://nbviewer.org/gist/peterm790/a977137f5335bb74a8038a27841317b0) for the [LiveOcean model](https://faculty.washington.edu/pmacc/LO/LiveOcean.html) within the [NANOOS region](http://www.nanoos.org/). In his work Peter improved documentation, optimized the code for compatibility with both grib2 and netcdf formats, and tested a complete end-to-end workflow to obtain cloud optimzed data based on the kerchunk approach.
-  `echoshader` is part of the `echopype` ecosystem and aims to be a visualization library for ocean sonar sound data. Dingrui Lei's GSoC project started that effort and implemented the first visualization and data exploration tools for these kind of data.
-  `erddapy` is a Python client for the [ERDDAP server](https://coastwatch.pfeg.noaa.gov/erddap/index.html) RESTful API. The library was showing signs of age and was built on top of functions and builders that no longer fitted most user's needs. Vini Salazar is working re-factoring `erddapy` and modernizing the codebase in order to make it both more user friendly and easier to maintain in the long term.


You can find out more about each project's results on the participants' blog posts:

1. https://medium.com/pangeo/accessing-netcdf-and-grib-file-collections-as-cloud-native-virtual-datasets-using-kerchunk-625a2d0a9191
1. https://ayushanand18.github.io/GSoC_design_documents/
1. https://medium.com/@viniws/my-experience-as-a-google-summer-of-code-intern-mid-project-update-cd9ea9a40130

# Project Details
More information about each project is also available on the [IOOS organization page](https://summerofcode.withgoogle.com/programs/2022/organizations/ioos) on the Google Summer of Code Website.


## Echoshader

Echoshader, an open source project, aims to enhance the ability to interactively visualize large amounts of cloud-based data to accelerate the data exploration and discovery process. Ocean sonar data is generated from echopype, which handles the normalization, preprocessing and organization of echo data. Echoshader will be developed in parallel with the ongoing development of echopype. As a participant of GSoC, I will develop the main APIs of echoshader based on the HoloViz suite of tools, test configuration for using echoshader widgets in Panel dashboards, and create Jupyter notebooks to demo use of the combination of tools. The main technology stacks used are Hvplot, Panel, fogrib2 data to zarraylium and PyVista.

Contributor: Dingrui Lei
Mentors: Valentina Staneva, Wu-Jung Lee, Brandon Reyes, Don Setiawan, and Emilio Mayorga

## Kerchunk

The Kerchunk package provides a means to access legacy geospatial datasets, such as GRIB2, in a cloud performant manor by creating a reference file which maps to variables within the datasets, this allows direct access to many data chunks within various files in one go, reducing overall latency and allowing easy parallel access. At present the scan_grib module within Kerchunk does not work when considering GFS operational data as GRIB data from different institutions can differ. I propose adapting the existing module to successfully access operational GFS forecast data before providing an example of the utility of Kerchunk to create a dictionary of lazy dimensional arrays containing all GFS variables.

Contributor: Peter Marsh
Mentors: Rich Signell and Martin Durant

## Pyobis

The goal of the project is to modify the pyobis python package to support the new OBIS API v3. This project also aims to improve tests coverage, diversify example usage, analyze and visualize fetched data from the updated package, and push the new version to PyPI. The pyobis package is really powerful and can fetch huge ocean biodiversity data through the OBIS API. It is interesting to note that OBIS also holds data for species even dating back to around 1078 AD, which makes pyobis even more essential to be maintained. As an extended objective, I will also create a high-level module inside pyobis package that can allow users to visualize data directly.

Contributor: Ayush Anand
Mentors: Tylar Murray, Mathew Biddle, and Filipe Fernandes

## Erddapy

The erddapy package provides a Python interface to the ERDDAP data server API. Currently, most of erddapy's functionality is concentrated into a single class, and the URL building features are implemented in that class along with the data transformation methods that process server responses into Python objects, such as Pandas DataFrames. This project proposes to separate erddapy into core and object (or opinionated) layers. The former will hold the URL building and data transformation functionality, which will be reused by the rest of the library. The latter layer will provide high-level objects that will support a functional API that does not depend on the state of the underlying object (which is the case for the current version of erddapy). This functional API will provide cleaner iterative usage when querying multiple servers and datasets, and new classes implemented in the object layer will support serialization so that they can be pickled and passed on to other processes or machines. To execute this project, I delineate two separate aims: refactoring the URL building and data transformation functionality into a new module containing minimal, standalone functions and reusing those functions in the existing primary class; and implementing an additional layer containing the high-level objects that will provide the basis for the functional API. Overall, this will greatly improve the flexibility and scalability of the package, and will help support its wide spectrum of users.

Contributor: Vini Salazar
Mentors: Filipe Fernandes, Alex Kerney, Mathew Biddle, and Callum Rollo
