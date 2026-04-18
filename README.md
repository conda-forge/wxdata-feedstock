About wxdata-feedstock
======================

Feedstock license: [BSD-3-Clause](https://github.com/conda-forge/wxdata-feedstock/blob/main/LICENSE.txt)

Home: https://github.com/edrewitz/WxData

Package license: MIT

Summary: A Python package of end-to-end weather data clients & raw data clients with VPN/PROXY support, data processors that decode variable keys from GRIB format into a plain-language format & various tools for assisting Python automated workflows, querying meteorological datasets and filling gaps in meteorological data.

Development: https://github.com/edrewitz/WxData

Documentation: https://pypi.org/project/wxdata/


Project Description
-------------------
WxData is a Python package geared to help atmospheric scientists set up automated workflows that download,
pre-process and post-process various types of weather data (observational and forecast).

Data Clients
------------
There are two classes of clients: End-To-End and Raw. End-To-End clients download, pre-process and post process data
specific to a type of dataset (i.e. gfs0p25() for GFS (0.25x0.25) Data). Raw clients assist users in downloading different
types of data (i.e. get_gridded_data(), get_csv_data(), get_excel_data(), get_aws_open_data() and get_xmacis_data()).
These clients have built-in support for users working on VPN/PROXY connections. Users will need to define their own
PROXY settings and pass those settings into the client so the client knows the path from the HOST to the Data Server.

Post-Processors
---------------
WxData has post-processing modules for every type of dataset that has an end-to-end client. Users may also import these
post-processing modules if they wish to use their own downloading procedures.

Data Querying Tools
-------------------
WxData has tools to assist users with pixel and line querying for gridded datasets.

Data Transformation & Gap Filling Tools
---------------------------------------
WxData has tools to assist users with:

1) Shifting longitude in gridded datasets from a 0 to 360 into a -180 to 180 projection.
2) Adding cyclic points to resolve data gaps along the 180 or 0 degree meridian in gridded datasets.
3) Linearly interpolating between two data points.

Automated Python Workflow Tools
-------------------------------
WxData has a tool users can use to execute a series of Python scripts in the order the user lists them in.


Current build status
====================


<table><tr>
    <td>All platforms:</td>
    <td>
      <img src="https://img.shields.io/badge/noarch-disabled-lightgrey.svg" alt="noarch disabled">
    </td>
  </tr>
</table>

Current release info
====================

| Name | Downloads | Version | Platforms |
| --- | --- | --- | --- |
| [![Conda Recipe](https://img.shields.io/badge/recipe-wxdata-green.svg)](https://anaconda.org/conda-forge/wxdata) | [![Conda Downloads](https://img.shields.io/conda/dn/conda-forge/wxdata.svg)](https://anaconda.org/conda-forge/wxdata) | [![Conda Version](https://img.shields.io/conda/vn/conda-forge/wxdata.svg)](https://anaconda.org/conda-forge/wxdata) | [![Conda Platforms](https://img.shields.io/conda/pn/conda-forge/wxdata.svg)](https://anaconda.org/conda-forge/wxdata) |

Installing wxdata
=================

Installing `wxdata` from the `conda-forge` channel can be achieved by adding `conda-forge` to your channels with:

```
conda config --add channels conda-forge
conda config --set channel_priority strict
```

Once the `conda-forge` channel has been enabled, `wxdata` can be installed with `conda`:

```
conda install wxdata
```

or with `mamba`:

```
mamba install wxdata
```

It is possible to list all of the versions of `wxdata` available on your platform with `conda`:

```
conda search wxdata --channel conda-forge
```

or with `mamba`:

```
mamba search wxdata --channel conda-forge
```

Alternatively, `mamba repoquery` may provide more information:

```
# Search all versions available on your platform:
mamba repoquery search wxdata --channel conda-forge

# List packages depending on `wxdata`:
mamba repoquery whoneeds wxdata --channel conda-forge

# List dependencies of `wxdata`:
mamba repoquery depends wxdata --channel conda-forge
```


About conda-forge
=================

[![Powered by
NumFOCUS](https://img.shields.io/badge/powered%20by-NumFOCUS-orange.svg?style=flat&colorA=E1523D&colorB=007D8A)](https://numfocus.org)

conda-forge is a community-led conda channel of installable packages.
In order to provide high-quality builds, the process has been automated into the
conda-forge GitHub organization. The conda-forge organization contains one repository
for each of the installable packages. Such a repository is known as a *feedstock*.

A feedstock is made up of a conda recipe (the instructions on what and how to build
the package) and the necessary configurations for automatic building using freely
available continuous integration services. Thanks to the awesome service provided by
[Azure](https://azure.microsoft.com/en-us/services/devops/), [GitHub](https://github.com/),
[CircleCI](https://circleci.com/), [AppVeyor](https://www.appveyor.com/),
[Drone](https://cloud.drone.io/welcome), and [TravisCI](https://travis-ci.com/)
it is possible to build and upload installable packages to the
[conda-forge](https://anaconda.org/conda-forge) [anaconda.org](https://anaconda.org/)
channel for Linux, Windows and OSX respectively.

To manage the continuous integration and simplify feedstock maintenance,
[conda-smithy](https://github.com/conda-forge/conda-smithy) has been developed.
Using the ``conda-forge.yml`` within this repository, it is possible to re-render all of
this feedstock's supporting files (e.g. the CI configuration files) with ``conda smithy rerender``.

For more information, please check the [conda-forge documentation](https://conda-forge.org/docs/).

Terminology
===========

**feedstock** - the conda recipe (raw material), supporting scripts and CI configuration.

**conda-smithy** - the tool which helps orchestrate the feedstock.
                   Its primary use is in the construction of the CI ``.yml`` files
                   and simplify the management of *many* feedstocks.

**conda-forge** - the place where the feedstock and smithy live and work to
                  produce the finished article (built conda distributions)


Updating wxdata-feedstock
=========================

If you would like to improve the wxdata recipe or build a new
package version, please fork this repository and submit a PR. Upon submission,
your changes will be run on the appropriate platforms to give the reviewer an
opportunity to confirm that the changes result in a successful build. Once
merged, the recipe will be re-built and uploaded automatically to the
`conda-forge` channel, whereupon the built conda packages will be available for
everybody to install and use from the `conda-forge` channel.
Note that all branches in the conda-forge/wxdata-feedstock are
immediately built and any created packages are uploaded, so PRs should be based
on branches in forks, and branches in the main repository should only be used to
build distinct package versions.

In order to produce a uniquely identifiable distribution:
 * If the version of a package **is not** being increased, please add or increase
   the [``build/number``](https://docs.conda.io/projects/conda-build/en/latest/resources/define-metadata.html#build-number-and-string).
 * If the version of a package **is** being increased, please remember to return
   the [``build/number``](https://docs.conda.io/projects/conda-build/en/latest/resources/define-metadata.html#build-number-and-string)
   back to 0.

Feedstock Maintainers
=====================

* [@edrewitz](https://github.com/edrewitz/)

