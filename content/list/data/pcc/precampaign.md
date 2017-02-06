+++
date = "2016-08-01"
title = "PRECAMPAIGN (Data: campaign.pcc)"
original_url = "/list/data/pcc.html#precampaign"
categories = [ "all-tag", "pcc-tag" ]
[menu.main]
    name = "PRECAMPAIGN (Data: campaign.pcc)"
    parent = "pcc"
+++

## Status

Updated 6.01.02

## Syntax

`PRECAMPAIGN:x,y,y`

## Parameters

-   x: Number (Number of items required to pass)
-   y: Text (Data set name as set by the CAMPAIGN tag).
-   y: BOOKTYPE=Text (Matches data set BOOKTYPE tag).
-   y: INCLUDES=Text (Data set name as set by the
    CAMPAIGN tag that is included in any selected campaign or one of its
    included sources).
-   y: INCLUDESBOOKTYPE=Text (Data set BOOKTYPE of any
    selected campaign or one of its included sources).



What it does
------------

-   This tag is used as a stand alone tag in .pcc files as well as an
    appended tag on [Main Body Tags](/list/data/pcc.html#mainbodytags) .
-   `PRECAMPAIGN` sets specific data sets as required or prohibited for
    the associated data set to be loaded. In the Source tab a data set
    which requires another data set will appear in red until that set is
    added to the right load pane.
-   When the tag is used inversely (i.e. !PRECAMPAIGN) a data set which
    prohibits itself from being used with another data set will appear
    in red when that data set is added to the right load pane.
-   Incompatible data sets will not load together. When incompatible
    data sets are selected in the right hand pane (i.e. one or more
    appears in red) an error message will be displayed if you click the
    load button.
-   Enclosing the data set name or `BOOKTYPE` sub-tag and text in
    square-brackets (\[\]) will exclude the relevant data sets from the
    prerequisite evaluation.
-   This tag is a global tag and so may be used in any LST file to set
    prerequisites for specific data sets. For more information see the
    [Global PRExxx](/list/global/pre/precampaign.html) page.

Example
-------

`PRECAMPAIGN:1,3.5 RSRD,3.5 RSRD Basics`

Will cause a data set to be loaded only if the "3.5 RSRD" or the "3.5
RSRD Basics" data set is loaded.

`!PRECAMPAIGN:1,3.5 RSRD`

Will prohibit the loading of the associated data set if the "3.5 RSRD"
data set is loaded.

`PRECAMPAIGN:1,3.5 RSRD Basics`

Will cause the associated data set to be loaded only if the "3.5 RSRD
Basics" data set is loaded.

`PRECAMPAIGN:1,BOOKTYPE=Core,[3.5 RSRD Basics]`

Will cause the associated data set to be loaded only if the a "Core"
data set is loaded but does not include the "3.5 RSRD Basics" data set
in the evaluation.

`!PRECAMPAIGN:1,BOOKTYPE=Core,[3.5 RSRD Basics]`

Will cause the associated data set to be loaded only if the a "Core"
data set other than the "3.5 RSRD Basics" data set is loaded.

`PRECAMPAIGN:1,INCLUDES=3.5 RSRD Basics`

Will cause a data set to be loaded only if the "3.5 RSRD Basics" data
set is loaded or a data set that includes the "3.5 RSRD Basics" set is
loaded.

`PRECAMPAIGN:1,INCLUDESBOOKTYPE=Core`

Will cause the associated data set to be loaded only if the a "Core"
data set is loaded or a set that includes a "Core" data set is loaded.

