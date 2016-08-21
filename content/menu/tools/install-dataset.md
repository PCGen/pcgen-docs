+++
date = "2016-08-01"
title = "Out-of-Cycle (OOC) Data Set Installation"
original_url = "/menu/tools/install-dataset.html"

[menu.main]
    identifier = "tools_install-dataset"
    name = "Out-of-Cycle (OOC) Data Set Installation"
    parent = "tools"
    
+++
The OOC data set installation capability has been added to PCGen to
allow for the distribution of those data sets released between stable
releases. This capability can also be used to install commercial data
sets released by game publishers. Such data sets must conform to PCGen's
guidlines for the preparation of data set archives. This page presents
instructions for the installation of an OOC data set installation
archive.

For more information on the preparation of an OOC dataset archive check
out the [Data Set Install Files](/list/data/install.html) page.

------------------------------------------------------------------------

<span id="installation"></span>

Data Set Installation
---------------------

The following are the steps required to install an OOC data set:

1.  PCGen team publishes OOC dataset archive to SourceForge
    downloads section.
2.  Download the OOC dataset archive from SourceForge.
3.  Launch PCGen and select **Tools** &gt; **Install Dataset** .
    <div align="center">

    \
    ![](../../images/windows/data_installer.png)

    </div>

    \
4.  Find and **Select** the archive file to install via the presented
    "File Selection" dialog.
5.  PCGen will verify that the selected dataset is compatible with the
    version of PCGen being used.
6.  Information on the selected archive is displayed and you will be
    given a choice of "DATA" or "VENDORDATA" folders with the default
    specified in *install.lst* .
7.  Select the destination and click **Install** .
8.  The dataset is saved to the selected location and is made available
    for use within PCGen.

If installing a data set archive provided by a commercial game publisher
you will obtain the archive file, i.e. steps 1 and 2 above, per the
publishers instructions.

------------------------------------------------------------------------



