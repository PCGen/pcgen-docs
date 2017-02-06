+++
date = "2016-08-01"
title = "SEX (System: bio/biosettings.lst)"
original_url = "/list/system/biosettings.html#sex"
categories = [ "all-tag", "biosettings-tag" ]
[menu.main]
    name = "SEX (System: bio/biosettings.lst)"
    parent = "biosettings"
+++

## Status

None

## Syntax

`SEX:gender[BASEHT:v|HTDIEROLL:w|BASEWT:x|WTDIEROLL:y|TOTALWT:z]`

## Parameters

-   Variables Used (gender): Text (Male or Female)
-   v: Number (The base height for the
    associated race/gender)
-   w: Text (The die roll for randomizing height)
-   x: Number (The base weight for the
    associated race/gender)
-   y: Text (The die roll for randomizing weight)
-   z: Text (A formula used to get the total weight)



What it does
------------

-   Determines how the Description tab randomizer generates height and
    weight for the different genders.
-   Both sexes are usually given on one line, one following the other
    with the same format as shown.

Example
-------

`Male[BASEHT:58|HTDIEROLL:2d10|BASEWT:130|WTDIEROLL:2d4|TOTALWT:BASEWT+(HTDIEROLL*WTDIEROLL)]`

Male height is 58+2d10 and Weight is 130+(height\*2d4).

