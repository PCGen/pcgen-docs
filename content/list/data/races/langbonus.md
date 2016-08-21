+++
date = "2016-08-01"
title = "LANGBONUS (Data: races.lst)"
original_url = "list/data/races.html#langbonus"
categories = [ "all-tag", "races-tag" ]
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

-   This is a comma-delimited (,) list of languages that the character
    may select from to gain as a bonus language. This does not effect
    languages granted from skills.
-   When using `ALL` , no other language designation is necessary.
-   **.MOD Behavior:** When modifying a race with the `.MOD` tag, given
    an existing `LANGBONUS` tag, the data included in a new `LANGBONUS`
    tag will be appended to the existing tag data.

Example
-------

`LANGBONUS:Dwarven,Elven,Gnome,Goblin,Orc`

Race can choose starting languages from "Dwarven", "Elven", "Gnome",
"Goblin" or "Orc".

> `Hobgoblin.MOD <tab> LANGAUTO:Gadohig <tab> LANGBONUS:.CLEAR <tab> LANGBONUS:Aeylamdyarian,Calisian,Desolati,Galkarnic,Homish,Launhymian`

Race can choose starting languages from "Aeylamdyarian", "Calisian",
"Desolati", "Galkarnic" or "Homish", or "Launhymian", in addition to the
Autoknown "Gadohig".

`LANGBONUS:Old Dwarven,Orcish,TYPE=ClanDialect,Trader's Tongue`

Race can choose starting languages from "Old Dwarven", "Orcish", any
type of "ClanDialect", or "Trader's Tongue".

**.MOD Example:**

Initial Race: `Space Monkey <tab> LANGBONUS:Simian`

Modified By: `Space Monkey.MOD <tab> LANGBONUS:Martian`

Is Equivalent To: `Space Monkey <tab> LANGBONUS:Simian,Martian` .

The character can choose between the languages "Simian" and "Martian" as
bonus languages.

