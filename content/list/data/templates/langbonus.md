+++
date = "2016-08-01"
title = "LANGBONUS (Data: templates.lst)"
original_url = "list/data/templates.html#langbonus"
categories = [ "all-tag", "templates-tag" ]
+++

## Status

None

## Syntax

`LANGBONUS:x,x`

## Parameters

-   x: Text (Language Name)
-   x: TYPE=Text (Language Type)
-   x: ALL
-   x: .CLEAR



What it does
------------

-   This is a comma-delimited (,) list of the languages a character can
    choose from based upon their Intelligence Stat.
-   When using 'ALL', no other language designation is necessary.
-   **.MOD Behavior:** When modifying a template, with the `.MOD` tag,
    given an existing `LANGBONUS` tag, the data included in a new
    `LANGBONUS` tag will be appended to the existing tag data.

Example
-------

`LANGBONUS:TYPE=Spoken,Draconic`

Add all "Spoken" type languages & "Draconic" to the list of languages
that can be taken when creating a character.

**.MOD Example (Appending):**

Initial Template: `Space Monkey <tab> LANGBONUS:Simian`

Modified By: `Space Monkey.MOD <tab> LANGBONUS:Martian`

Is Equivalent To: `Space Monkey <tab> LANGBONUS:Simian,Martian` .

The character can choose between the languages "Simian" and "Martian" as
bonus languages.

