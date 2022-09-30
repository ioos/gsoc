# GSoC 2021 Results

U.S. IOOS is participating for the first time as a mentoring organization for Google’s Summer of Code 2021.
Google granted IOOS three slots and the projects ranged from machine learning, new features in IOOS software, and documentation translation capabilities.

Completed projects:

- [erddapy](https://gist.github.com/callumrollo/ee28f7e1863d30162bdb041156314543): Implemented griddap and issued gliderpy first release.
- [ERDDAP](https://q1zeng.github.io/): Translated ERDDAP User Interface Into Different Languages
- [SeaFloor Sampling and IOOS Code Lab](https://lohithmunakala.medium.com/seafloor-sampling-and-data-demo-center-jupyter-book-migration-gsoc21-ioos-a9930abc4c42): Hybrid project that worked on identifying sea floor features with machine learning and implemented a jupyter-book for the IOOS Code Lab page examples.

Important highlights:

- `errdapy` long awaited feature, griddap, was implemented thanks to GSoC participant Callum Rollo. He also expanded his contribution to the `gliderpy` project, preparing it for a first stable release.
- Lohith Munakala tackled two separate problems. He created a machine learning framework to identify sea floor features in underwater imagery and converted the IOOS Data Demo Center project into a the Jupyter Book format.
- Last but not least, Qi Zeng tackled an extremely important problem to implement language translation support for the ERDDAP server. With this new feature released in [ERDDAP v2.15}(https://coastwatch.pfeg.noaa.gov/erddap/download/changes.html#changes2.15), for ERDDAP servers that enable translation, browsers will load the correct language based on selected locale.

You can find out more about some of the project's results on the participants' blog posts:

1. https://callumrollo.github.io/griddap.html
2. https://callumrollo.github.io/gliderpy.html

# Project Details

More information about each project is also available on the [IOOS organization page](https://summerofcode.withgoogle.com/archive/2021/organizations) on the Google Summer of Code Website.

## erdappy-griddap

This proposal will add griddap functionality to the erddapy package and simplify the API. Support for griddap will enable near real time access to gridded datasets such as climate models and weather forecasts via a simple Python API. This access will benefit oceanographers, search and rescue teams and the maritime industry at large. Additional tasks include enabling high level, simplified queries for easy access and improving the gliderpy package to make swathes of high resolution ocean glider data more readily available.

Contributor: Callum Rollo
Mentors: Mathew Biddle, Filipe Fernandes, Micah Wengren

## Machine Learning for Sea Floor Sampling and IOOS Demo Data Center migration to Jupyterbook

Sea Floor Sampling is a tedious job and requires a lot of manual work. This project intends to automate the process of labelling the videos using object detection and classification methods. This will reduce the amount of time taken drastically.

IOOS Data Demo Center Migration to Jupyterbook. JupyterBook is a simple yet elegant way to show the documentation of one's work. It can be used for scientific purposes as it builds publication-quality books. The aim of the project is to move the existing Demo Data Center to a jupyterbook style and automate the process.

Contributor: Lohith Munakala
Mentors: Dalton Kell, Benjamin Adams, Mathew Biddle


## Translate ERDDAP User Interface Into Different Languages

ERDDAP is a data server widely used in many organizations over the world to upload and gather data sets on the ocean environment, but currently it only supports English and not all users are proficient in English. This project will create an automated tool to translate the user interface of ERDDAP into any target language, and also modify ERDDAP’s structure to allow one ERDDAP setup to display messages in multiple languages to enhance the accessibility of the oceanographic data for the scientific community.

Contributor: Qi Zeng
Mentors: Bob Simons, Filipe Fernandes, Micah Wengren
