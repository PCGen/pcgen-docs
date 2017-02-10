+++
date = "2016-08-01"
title = "SIZENUM (System: sizeAdjustment.lst)"
original_url = "/list/system/sizeadjustment.html#sizenum"
categories = [ "all-tag", "sizeadjustment-tag" ]
[menu.main]
    name = "SIZENUM"
    parent = "system_sizeadjustment"
    identifier = "system_sizeadjustment_SIZENUM"
+++

## Status

None

## Syntax

`None`

## Parameters




<span id="sizenum"></span>

### SIZENUM

**Mandatory:** Defines the sorting order for the size categories.

#### Status {#status-1}

New in 6.05.04.

Before 6.05.04, the size order was inferred from the order of the
`SIZENAME` tags in the `sizeAdjustment.lst` file. As of 6.05.04, the
order is explicitly indicated using the `SIZENUM` tag.

-   [JIRA NEWTAG-480](https://pcgenorg.atlassian.net/browse/NEWTAG-480)
    / [GitHub PR \#397](https://github.com/PCGen/pcgen/pull/397) - token
    parser changes.
-   [JIRA DATA-2507](https://pcgenorg.atlassian.net/browse/DATA-2507) /
    [GitHub PR \#410](https://github.com/PCGen/pcgen/pull/410) - added
    `SIZENUM` tags to all the default game modes.

#### Syntax: {#syntax-3}

`SIZENAME:size_name  →  SIZENUM:size_number`

`size_number` is an integer. Bigger numbers correspond to larger size
categories.

#### Example: {#example-2}

The following code, included in the `35e` version of
`sizeAdjustment.lst` , defines the ordering of the `35e` size
categories:

    SIZENAME:F  SIZENUM:010
    SIZENAME:D  SIZENUM:020
    SIZENAME:T  SIZENUM:030
    SIZENAME:S  SIZENUM:040
    SIZENAME:M  SIZENUM:050
    SIZENAME:L  SIZENUM:060
    SIZENAME:H  SIZENUM:070
    SIZENAME:G  SIZENUM:080
    SIZENAME:C  SIZENUM:090
    SIZENAME:P  SIZENUM:100

