+++
date = "2016-08-01"
title = "QUALIFIERS (Global: OTHER)"
original_url = "/list/global/other.html#qualifiers"
categories = [ "all-tag", "other-tag" ]
[menu.main]
    name = "QUALIFIERS (Global: OTHER)"
    parent = "other"
+++

## Status

None

## Syntax

`<tagname>:x
(See specific tag documentation for specific syntax.)`

## Parameters

-   x: ANY (Default)
-   x: PC
-   x: QUALIFIED



Global Sub-Tags
---------------

### <span id="qualifiers"></span> Global Qualifiers

What it does
------------

-   Global qualifiers work for any LST Object which can be qualified
    with the exception of STAT and ALIGNMENT objects. Use of the
    qualifiers has the following effect:
    -   **ANY** - Will return a list of all LST objects of the type
        requested by the `CHOOSE` tag, e.g. Template, Race, Equipment,
        Domain, etc.
    -   **PC** - Will return a list of all LST objects already taken by
        the Player Character of the type requested by the `CHOOSE`
        tag, e.g. Template, Race, Equipment, Domain, etc.
    -   **QUALIFIED** - Will return a list of all LST objects of the
        type requested by the `CHOOSE` tag, e.g. Template, Race,
        Equipment, Domain, etc., that the player character is otherwise
        qualified for.
-   Qualifiers can be logically negated by prefacing with the
    exclamation point (!), i.e. `!PC` is a valid usage.
-   Qualifiers can be logically combined by using the comma (,), logical
    **AND** , and the pipe (|), logical **OR** . Logical **AND** s are
    evaluated before logical **OR** s.

Examples
--------

See individual tag documentation for examples of use.

