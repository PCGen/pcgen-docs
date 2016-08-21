+++
date = "2016-08-01"
title = "CHOICE (Data: classes.lst)"
original_url = "list/data/classes.html#choice"
categories = [ "all-tag", "classes-tag" ]
+++

## Status

None

## Syntax

`CHOICE:x|y`

## Parameters

-   x: DESCRIPTOR
-   x: SCHOOL
-   x: SUBSCHOOL
-   y: Text (Descriptor, school, or subschool name)



<span id="choice"></span> \*\*\* Updated 5.13.x

What it does
------------

-   Indicates the specialty, by descriptor, school, or subschool,
    applicable to the subclass/specialty selected.
-   All descriptors, schools, and subschools used within the loaded lst
    files are valid choices.
-   **Note:** Due to the diversity of publishers and material we
    support, we cannot list all descriptors, schools, or
    subschools available.

Examples
--------

`SUBCLASS:Illusionist <tab> CHOICE:SCHOOL|Illusion`

For an Illusionist.

`SUBCLASS:Abjure <tab> CHOICE:SCHOOL|Abjuration`

For an Abjurer.

`SUBCLASS:Diviner <tab> CHOICE:SCHOOL|Divination`

For a Diviner.

`SUBCLASS:Savant <tab> CHOICE:SCHOOL|Psychokinesis`

For a Psychokinesis.

`SUBCLASS:Shaper <tab> CHOICE:SCHOOL|Illusion.CLEAR`

Removes the choice for an Illusionist.

`SUBCLASS:Nomad <tab> CHOICE:SCHOOL|Abjuration.MOD <tab> CHOICE:SCHOOL|Divination`

Replaces the choice for an Abjurer with Diviner.

Where it is used
----------------

Subclass Line.



