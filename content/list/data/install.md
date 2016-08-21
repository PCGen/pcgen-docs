+++
date = "2016-08-01"
title = "Out-of-Cycle (OOC) Data Set Install Files"
original_url = "/list/data/install.html"

[menu.main]
    identifier = "data_install"
    name = "Out-of-Cycle (OOC) Data Set Install Files"
    parent = "data"
    
+++
The OOC data set installation capability has been added to PCGen to
allow for the distribution of those data sets released between stable
releases. This page presents instructions for the creation of the OOC
data set installation archive. You will also find the explanation of the
tags required to create the *install.lst* file as well as an example
install file. To accomplish this, this page is divided into three
sections:

[OOC Data Set Preparation](/list/data/install.html#preparation)

[Data Set Installation Tags](/list/data/install.html#installfiletags)

[Example *install.lst* File](/list/data/install.html#example)

For information on installing OOC data sets in PCGen go to the [Install
Data Set Tool](/menu/tools/install-dataset.html) page.

------------------------------------------------------------------------

<span id="preparation"></span>

Data Set Preparation
--------------------

The following are the steps required to prepare a data set for OOC
release:

1.  Create a data set as per PCGen's standard process, including all
    required reviews. (e.g. OGL, QC, and publisher.)
2.  Create the *install.lst* file. (See
    [example](/list/data/install.html#example) and [Tag
    Descriptions](/list/data/install.html#installfiletags) below.)
3.  Create an installation folder, recreating a nested folder structure
    identical to that of the final PCGen installation location. The
    following are a few examples:
    -   TestDataSet/data/d20ogl/pcgen/testooc/
    -   FooDataSet/data/alpha/foopublishing/foosetting/
    -   BarDataSet/data/permissioned/bargames/barsupplement/
    -   MyCampaignDataSet/data/homebrew/mycampaign/

4.  Place the OOC data set at the lowest folder level in the
    installation folder. (ie. in the *testdoc* folder for the first
    example above.)
5.  Place the *install.lst* file in the top level folder. (i.e. in the
    *TestDataSet* folder in the first example above.)
6.  Create a "ZIP" archive of the installation folder.
7.  Change the name of the zip-file from *\*.zip* to *\*.pcz* .

The OOC data set is now ready for release.

------------------------------------------------------------------------

<span id="installfiletags"></span>

Data Set Installation Tags
--------------------------

The tags used in the *install.lst* file consist of three
[Exclusive](/list/data/install.html#exclusivetags) tags and a handful of
[PCC tags](/list/data/install.html#pcctags) .

------------------------------------------------------------------------

<span id="exclusivetags"></span>

### Exclusive Data Set Installation Tags

The following three tags are used exclusively in the *install.lst* file.

-   [MINVER](/list/data/install/minver.html)
-   [MINDEVVER](/list/data/install/mindevver.html)
-   [DEST](/list/data/install/dest.html)

------------------------------------------------------------------------

------------------------------------------------------------------------

<span id="pcctags"></span>

### Additional Source and Header Information Tags

The following tags are used in the *\*.pcc* file and are therefore
documented as part of the PCC file documentation.

------------------------------------------------------------------------

**Tag Name:** [CAMPAIGN:x](/list/data/pcc/campaign.html)

**Example:**

`CAMPAIGN:FGI - FooB Core Rulebook I - FHB`

------------------------------------------------------------------------

**Tag Name:** [COPYRIGHT:x](/list/data/pcc/copyright.html)

**Example:**

`COPYRIGHT:PCGen OGC dataset Copyright 2006, PCGen Data team (Including, but not limited to Eddy Anthony (MoSaT), Andrew McDougall (Tir Gwaith)).`

------------------------------------------------------------------------

**Tag Name:** [INFOTEXT:x](/list/data/pcc/infotext.html)

**Example:**

`INFOTEXT:PCGen Open Gaming Content objects are detailed in the PCGen documentation under the Source Help section`

------------------------------------------------------------------------

**Tag Name:** [PUBNAMELONG:x](/list/data/pcc/pubnamelong.html)

**Example:**

`PUBNAMELONG:PCGen Open Source Team`

------------------------------------------------------------------------

**Tag Name:** [PUBNAMESHORT:x](/list/data/pcc/pubnameshort.html)

**Example:**

`PUBNAMESHORT:PCGen`

------------------------------------------------------------------------

**Tag Name:** [PUBNAMEWEB:x](/list/data/pcc/pubnameweb.html)

**Example:**

`PUBNAMEWEB:http://pcgen.org/`

------------------------------------------------------------------------

**Tag Name:** [SOURCELONG:x](/list/data/pcc/sourcelong.html)

**Example:**

`SOURCELONG:PCGen Test Out of Cycle Releases`

------------------------------------------------------------------------

**Tag Name:** [SOURCESHORT:x](/list/data/pcc/sourceshort.html)

**Example:**

`SOURCESHORT:PCGen TOCC`

------------------------------------------------------------------------

**Tag Name:** [SOURCEWEB:x](/list/data/pcc/sourceweb.html)

**Example:**

`SOURCEWEB:http://pcgen.org/`

------------------------------------------------------------------------

**Tag Name:** [SOURCEDATE:x](/list/data/pcc/sourcedate.html)

**Example:**

`SOURCEDATE:2007-12`

------------------------------------------------------------------------

<span id="example"></span>

Example Install File
--------------------

The following is an example of an *install.lst* file.

> `CAMPAIGN:PCGen Test OCC`
>
> `MINVER:5.14.1`
>
> `MINDEVVER: 5.15.2`
>
> `DEST:VENDORDATA`
>
> `COPYRIGHT:Open Game License v 1.0a Copyright 2000, Wizards of the Coast, Inc.`
>
> `COPYRIGHT:System Reference Document Copyright 2000-2003, Wizards of the Coast, Inc.; Authors Jonathan Tweet, Monte Cook, Skip Williams, Rich Baker, Andy Collins, David Noonan, Rich Redman, Bruce R. Cordell, John D. Rateliff, Thomas Reid, James Wyatt, based on original material by E. Gary Gygax and Dave Arneson.`
>
> `COPYRIGHT:PCGen OGC dataset Copyright 2006, PCGen Data team (Including, but not limited to Eddy Anthony (MoSaT), Andrew McDougall (Tir Gwaith)).`
>
> `INFOTEXT:PCGen Open Gaming Content objects are detailed in the PCGen documentation under the Source Help section`
>
> `SOURCELONG:PCGen Test Out of Cycle Releases`
>
> `SOURCESHORT:PCGen TOCC`
>
> `SOURCEWEB:http://pcgen.org/`
>
> `SOURCEDATE:2007-12`
>
> `PUBNAMELONG:PCGen Open Source Team`
>
> `PUBNAMESHORT:PCGen`
>
> `PUBNAMEWEB:http://pcgen.org/`

------------------------------------------------------------------------



