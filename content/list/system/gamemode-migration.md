+++
date = "2016-08-01"
title = "Game Mode: migration.lst"
original_url = "/list/system/gamemode-migration.html"

[menu.main]
    identifier = "system_gamemode-migration"
    name = "Game Mode: migration.lst"
    parent = "system"
    
+++
This file contains information on the tags used in, and how to build, a
<span class="lstfile"> migration.lst </span> file. Before we get to how
you build such a file though, let's first answer a few questions on the
migration file in general.

What the Character Migration File Does
--------------------------------------

The character migration tool works behind the scenes to smoothly load
characters from older versions of PCGen into the current version. The
file's primary purpose is to allow a character to be automatically
updated to reflect changes in the relevant data sets.

------------------------------------------------------------------------

Building a Character Migration File
-----------------------------------

The migration file consists of lines of lst code, each defining a
separate and specific migration item. Each line begines with the LST
Object tag followed by supporting tags. These tags are described below.
The LST objects currently supported include Sources, Abilities, and
Equipment. The syntax for a migration line is as follows:

Migration Line Syntax

`<Old Object Key>` &lt;tab&gt; `<New Object Key>` &lt;tab&gt;
`<Version Tags>`

------------------------------------------------------------------------

Migration File Tags
-------------------

The tags used in the <span> migration.lst </span> file consist of two
sets of tags.

Version Identification Tags

-   [MAXDEVVER](/list/system/gamemode-migration/maxdevver.html)
-   [MAXVER](/list/system/gamemode-migration/maxver.html)
-   [MINDEVVER](/list/system/gamemode-migration/mindevver.html)
-   [MINVER](/list/system/gamemode-migration/minver.html)

Source and Object Migration Line Tags

-   [ABILITY](/list/system/gamemode-migration/ability.html)
-   [EQUIPMENT](/list/system/gamemode-migration/equipment.html)
-   [NEWCATEGORY](/list/system/gamemode-migration/newcategory.html)
-   [NEWKEY](/list/system/gamemode-migration/newkey.html)
-   [RACE](/list/system/gamemode-migration/race.html)
-   [SOURCE](/list/system/gamemode-migration/source.html)

[Examples of Complete Migration
Lines.](/list/system/gamemode-migration.html#examples)

------------------------------------------------------------------------

------------------------------------------------------------------------

### <span id="examples"></span> Migration Line Examples

The examples included below are displayed in multiple lines for easy
readability. In the actual migration file all tags would be included on
the same line and separated by tabs.

**Ability Example:**

`ABILITY:Special Ability|Animal Fury`

`NEWKEY:Animal Fury ~ Rage Power`

`MAXVER:6.00.01`

`MAXDEVVER:6.01.02`

When any character last saved in v6.00.00 or earlier (or 6.01.01 in the
dev line) is loaded if it has a "Special Ability" with the key "Animal
Fury" the ability will be mapped to the new key "Animal Fury \~ Rage
Power".

**Equipment Example:**

`EQUIPMENT:Kasari Gusoku`

`NEWKEY:Kusari Gusoku`

`MAXVER:6.1.8`

If a character has the equipment "Kasari Gusoku" when last saved in
PCGen 6.1.8 or earlier, it will instead load "Kusari Gusoku" now.

**Source Example:**

`SOURCE:Paizo - Guide To Pathfinder Society Organised Play 4.0`

`NEWKEY:Guide To Pathfinder Society Organised Play`

`MAXVER:6.0.1`

`MAXDEVVER:6.1.7`

If a character used the source "Paizo - Guide To Pathfinder Society
Organised Play 4.0" when last saved in PCGen 6.0.1 or earlier (or 6.1.7
in the dev line) for it will instead load "Guide To Pathfinder Society
Organised Play" now.

------------------------------------------------------------------------



