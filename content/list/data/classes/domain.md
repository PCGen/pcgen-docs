+++
date = "2016-08-01"
title = "DOMAIN (Data: classes.lst)"
original_url = "/list/data/classes.html#domain"
categories = [ "all-tag", "classes-tag" ]
[menu.main]
    name = "DOMAIN"
    parent = "data_classes"
+++

## Status

Updated 6.3.0

## Syntax

`DOMAIN:x|x`

## Parameters

-   x: Text



What it does
------------

-   This grants additional domains, as listed, directly to
    the character.
-   It is a pipe-delimited (|) list of domain names.
-   If a domain is added on top of the character's other normal domains,
    it will need to be paired with a `BONUS:DOMAIN|NUMBER|x` .
-   This tag can use trailing PRExxx tags to provide prerequisites for
    the domains included in the associated `DOMAIN` tag.
-   Multiple `DOMAIN` tags may be used in a class object, allowing
    access to some domains without prerequisites and some with.

Example:s
---------

`7 <tab> DOMAIN:Sun`

At the seventh level class gets the Sun domain added.

`15 <tab> DOMAIN:Sun|Law`

At fifteenth level class gets the Sun or law domain added.

`11 <tab> DOMAIN:Sun|PREDEITY:Ra <tab> DOMAIN:Law`

At eleventh level class gets the Sun or Law domain added if their deity
is "Ra" or only Law if the deity is not "Ra".

Where it is used
----------------

Class and Class Level Line.

