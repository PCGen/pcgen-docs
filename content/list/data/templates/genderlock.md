+++
date = "2016-08-01"
title = "GENDERLOCK (Data: templates.lst)"
original_url = "/list/data/templates.html#genderlock"
categories = [ "all-tag", "templates-tag" ]
[menu.main]
    name = "GENDERLOCK (Data: templates.lst)"
    parent = "templates"
+++

## Status

Updated 5.11.13

## Syntax

`GENDERLOCK:x`

## Parameters

-   x: Text (Gender)



What it does
------------

-   Sets the character's gender and disables the ability to change it.
-   Gender values are defined in Game Mode File &gt; Bio Settings &gt;
    [SEX](/list/system/biosettings/sex.html) tag.
-   **.MOD Behavior:** When modifying a template, with the `.MOD` tag,
    given an existing `GENDERLOCK` tag, the data included in a new
    `GENDERLOCK` tag will overwrite the existing tag data.

Example
-------

`GENDERLOCK:Female`

The character's gender is set to and locked as "Female".

**.MOD Example:**

Initial Template: `Darkling Sorcerer <tab> GENDERLOCK:Female`

Modified By: `Darkling Sorcerer.MOD <tab> GENDERLOCK:Male`

Is Equivalent To: `Darkling Sorcerer <tab> GENDERLOCK:Male`

The Darkling Sorcerer's gender is set to "Male" and the ability to
change it is disabled.

