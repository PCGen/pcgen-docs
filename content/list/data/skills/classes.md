+++
date = "2016-08-01"
title = "CLASSES (Data: skills.lst)"
original_url = "/list/data/skills.html#classes"
categories = [ "all-tag", "skills-tag" ]
[menu.main]
    name = "CLASSES"
    parent = "data_skills"
    identifier = "data_skills_CLASSES"
+++

## Status

None

## Syntax

`CLASSES:x`

## Parameters

-   x: Text (Class Name)
-   x: ALL



<span id="classes"></span> \*\*\* New 5.3.3

What it does
------------

-   Makes the given skill a class skill for the listed classes.
-   **.MOD Behavior:** When modifying a skill with the `.MOD` tag, given
    an existing `CLASSES` tag, the data included in a new `CLASSES` tag
    will be appended to the existing tag data.

Example
-------

`CLASSES:Cleric|Paladin`

The listed skill is class skill for "Cleric" or "Paladin" characters.

`CLASSES:ALL`

The listed skill is class skill for all classes.

`CLASSES:ALL|!Wizard`

The listed skill is a class skill for all classes except for "Wizard"
characters.

**.MOD Example (Appending):**

Initial Skill: `Brachiation <tab> CLASSES:Acrobat`

Modified By: `Brachiation.MOD <tab> CLASSES:Ranger`

Is Equivalent To: `Brachiation <tab> CLASSES:Acrobat|Ranger` .

The skill "Brachiation" is a class skill for both the "Acrobat" and the
"Ranger" classes.

