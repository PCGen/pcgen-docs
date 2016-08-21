+++
date = "2016-08-01"
title = "SCHOOLS (Global: CHOOSE)"
original_url = "list/global/choose.html#schools"
categories = [ "all-tag", "choose-tag" ]
+++

## Status

Updated 5.17.4

## Syntax

`CHOOSE:SCHOOLS|x|x`

## Parameters

-   x: Text (School name)
-   x: FEAT=Text (Feat, by name or key)
-   x: ALL



What it does
------------

-   This will produce a list of "Schools" of magic (e.g. Abjuration,
    Evocation, etc.).
-   Use of the `FEAT` subtag will provide the **SCHOOL** selection made
    in the referenced feat. The feat referenced must contain a
    `CHOOSE:SCHOOLS` tag.
-   The [SELECT](/list/global/other/select.html) tag is used in
    conjunction with this `CHOOSE` tag to define the number of
    "selections" that can be made.

Example
-------

`CHOOSE:SCHOOLS|ALL`

This will produce a list of all schools of magic (abjuration, evocation,
etc.).

`CHOOSE:SCHOOLS|FEAT=Spell Focus`

This will produce a list of all schools for which the character has the
"Spell Focus" feat.

**Deprecated Syntax:**

`CHOOSE:SCHOOLS` becomes `CHOOSE:SCHOOLS|ALL`

Where it is Used
----------------

Ability, Domain, Feat, Race, and Template files.

