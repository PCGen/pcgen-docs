+++
date = "2016-08-01"
title = "CHOOSELANGAUTO (Data: templates.lst)"
original_url = "/list/data/templates.html#chooselangauto"
categories = [ "all-tag", "templates-tag" ]
[menu.main]
    name = "CHOOSELANGAUTO (Data: templates.lst)"
    parent = "templates"
+++

## Status

None

## Syntax

`CHOOSE:LANGAUTO:x|x`

## Parameters

-   x: Text (Language Name)



What it does
------------

-   This is a pipe-delimited (|) list of languages for the character to
    choose from that are automatically granted and do not count against
    the language limit determined by an ability score/stat.
-   **.MOD Behavior:** When modifying a template with the `.MOD` tag,
    the data included in this tag will be overwritten by the new
    `CHOOSE:LANGAUTO` tag if one is included in the modification.

Example
-------

`CHOOSE:LANGAUTO:Abyssal|Infernal`

"Abyssal" & "Infernal" are granted as bonus languages.

**.MOD Example:**

Initial Template: `Darkling <tab> CHOOSE:LANGAUTO:Abyssal|Infernal`

Modified By: `Darkling.MOD <tab> CHOOSE:LANGAUTO:Ignan|Undercommon`

Is Equivalent To: `Darkling <tab> CHOOSE:LANGAUTO:Undercommon`

Darklings are allowed to choose either "Ignan" or "Undercommon" as an
automatic language.

