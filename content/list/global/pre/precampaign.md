+++
date = "2016-08-01"
title = "PRECAMPAIGN (Global: PRErequisite)"
original_url = "list/global/pre.html#precampaign"
categories = [ "all-tag", "pre-tag" ]
+++

## Status

New 5.15.2

## Syntax

`PRECAMPAIGN:x,y,y`

## Parameters

-   x: Number (Number of items required to pass)
-   y: Text (Data set name as set by the CAMPAIGN tag).
-   y: BOOKTYPE=Text (Matches data set BOOKTYPE tag).
-   y: INCLUDES=Text (Data set name as set by the
    CAMPAIGN tag that is included in any selected campaign or one of its
    included sources). \*\*\* New 6.1.2
-   y: INCLUDESBOOKTYPE=Text (Data set BOOKTYPE of any
    selected campaign or one of its included sources). \*\*\* New 6.1.2



What it does
------------

-   Sets prerequisites for LST objects based upon the data sets loaded
    into PCGen. If the set is loaded it passes, if not it doesn't.
-   See PCC [PRECAMPAIGN](/list/data/pcc/precampaign.html) docs for full
    information on this tag.


