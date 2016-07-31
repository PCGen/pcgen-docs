+++
date = "2016-08-01"
title = "VISIBLE (Data: skills.lst)"
original_url = "list/data/skills.html#visible"
categories = [ "all-tag", "skills-tag" ]
+++

## Status

None

## Syntax

`VISIBLE:x|y`

## Parameters

-   x: YES (Default)
-   x: ALWAYS
-   x: NO
-   x: DISPLAY
-   x: GUI
-   x: EXPORT
-   x: CSHEET
-   y: READONLY (Optional)



<span id="visible"></span> \*\*\* New 5.7.7

What it does
------------

-   `YES` , `ALWAYS` - Shows the skill name in PCGen and on export to a
    character sheet.
-   `NO` - Hides the skill completely.
-   `DISPLAY` , `GUI` - Displays the skill name in PCGen but not on the
    character sheet.
-   `EXPORT` , `CSHEET` - Hides the skill name from PCGen but displays
    it on the character sheet.
-   `READONLY` - This will block the user from adding Ranks to the skill
    in the Skill Tab.
-   `READONLY` is not valid when `VISIBLE` is set to `EXPORT` or
    `CSHEET` .
-   **.MOD Behavior:** When modifying a skill with the `.MOD` tag, given
    an existing `VISIBLE` tag, the data included in a new `VISIBLE` tag
    will overwrite the existing tag data.

Example
-------

`VISIBLE:YES`

Shows the skill name in PCGen and on the Output sheet.

`VISIBLE:ALWAYS`

Shows the skill name in PCGen and on the Output sheet.

`VISIBLE:DISPLAY`

Shows the skill name in PCGen but not on the Output sheet.

`VISIBLE:GUI`

Shows the skill name in PCGen but not on the Output sheet.

`VISIBLE:CSHEET`

Shows the skill name on the Output sheet but not in PCGen.

`VISIBLE:ALWAYS|READONLY`

Shows the skill name in PCGen and on the Output sheet but prohibits the
user from adding ranks to it.

**.MOD Example (Overwriting):**

Initial Skill: `Brachiation <tab> VISIBLE:EXPORT`

Modified By: `Brachiation.MOD <tab> VISIBLE:YES`

Is Equivalent To: `Brachiation <tab> VISIBLE:YES`

The modified "Brachiation" skill can be seen throughout the PCGen
experience.

