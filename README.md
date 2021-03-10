# Google Summer of Code 

<img src="img/GSoC-logo-horizontal.svg" alt="Google Summer of Code logo" width="300" style="padding-right: 50px; vertical-align: middle">&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; <img src="img/IOOS_Emblem_Tertiary_A_RGB.jpg" alt="IOOS logo" width="300" style="vertical-align: middle">

### U.S. IOOS Mission
To produce, integrate, and communicate high quality ocean, coastal and Great Lakes information that meets the safety, economic, and stewardship needs of the Nation.

The Integrated Ocean Observing System (IOOS®) is a national-regional partnership working to provide new tools and forecasts to improve safety, enhance the economy, and protect our environment. Integrated ocean information is available in near real time, as well as retrospectively. Easier and better access to this information is improving our ability to understand and predict coastal events - such as storms, wave heights, and sea level change. Such knowledge is needed for everything from retail to development planning.

For more information visit: [https://ioos.noaa.gov](https://ioos.noaa.gov).

### Information about IOOS' activities for Google Summer of Code
The US IOOS Organization has submitted an application to GSoC 2021.  IOOS maintains several open source packages for oceanographic data management that are used both within the IOOS community as well as by ocean observation organizations worldwide.  

**View the 2021 IOOS GSoC project ideas list here: https://github.com/ioos/gsoc/blob/master/2021/ideas-list.md**

The [IOOS Data Management and Cyberinfrastructure](https://ioos.noaa.gov/project/dmac/) (DMAC) community is a coalition of scientific software developers focused on developing and supporting software used within our community and also by other NOAA and US Federal Government offices and international organizations to deliver earth science data to their users.  The DMAC community is an active coalition of both public and private participants contributing to this effort.  

We host annual DMAC [data management meetings](https://ioos.noaa.gov/project/dmac/), bi-annual [code sprints](https://www.glos.us/code-sprint/) (2019, 2021 - planned), monthly technical webinars, and maintain virtual communications through our ['ioos_tech'](https://groups.google.com/g/ioos_tech) mailing list and other platforms such as Slack and of course GitHub.  

### Project Descriptions

|**Project**|**Description**|
|--------|------------|
|[**ERDDAP**](https://github.com/BobSimons/erddap)| ERDDAP is a data server that gives you a simple, consistent way to download subsets of gridded and tabular scientific datasets in common file formats and make graphs and maps. ERDDAP's focus is on making it easier for you to get scientific data.  ERDDAP unifies the different types of data servers so you have a consistent way to get the data you want, in the format you want.  <br /><br />ERDDAP is widely used in the oceanographic data commmunity - a complete list of public ERDDAP instances throughout the world is maintained by the ['awesome-erddap'](https://github.com/IrishMarineInstitute/awesome-erddap) project of the Irish Marine Institute.  <br /><br />The primary ERDDAP CoastWatch server and ERDDAP documentation is available here: https://coastwatch.pfeg.noaa.gov/erddap/, and a highly-active ERDDAP mailing list is available at: https://groups.google.com/g/erddap. |
|[**erddapy**](https://github.com/ioos/erddapy)| erddapy is the Python client for ERDDAP.  erddapy takes advantage of ERDDAP’s RESTful web services to create the ERDDAP URLs. The users can create virtually any request like, searching for datasets, acquiring metadata, downloading data, etc.  <br /><br />Documentation for erddapy is available at: https://ioos.github.io/erddapy/v0.9.0/.|
|[**colocate**](https://github.com/ioos/colocate)| The colocate project is a utility built on top of both ERDDAP and erddapy to provice easy access to oceanographic data co-located in space and time via Python.  It queries the global collection of ERDDAP servers based on user-specified filter criteria and provides map visualization of dataset results via SciPy plotting tools, and will eventually allow download of datasets direct from the ERDDAP sources.  <br /><br />colocate grew out of a student project during the University of Washington's [OceanHackWeek 2019](https://oceanhackweek.github.io/ohw19/).|
|[**IOOS Notebook Gallery**](https://github.com/ioos/notebooks_demos)| The IOOS Notebook Gallery is a collection of Jupyter notebooks demonstrating use of IOOS' data and software for scientific analysis.  <br /><br />The gallery is regularly updated with new demonstration notebooks and is available via GitHub at: https://ioos.github.io/notebooks_demos/ |
|**Additional Projects**| IOOS also has some new efforts in the hopper for students looking to start on a fresh project with some experienced mentors.  These project ideas can be found in issues labeled 'GSoC' on this repository: [https://github.com/ioos/gsoc/labels/GSoC](https://github.com/ioos/gsoc/labels/GSoC)|
