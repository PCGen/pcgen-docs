+++
date = "2016-08-01"
title = "Starting Kit Files"
original_url = "/list/data/startingkits.html"

[menu.main]
    identifier = "data_startingkits"
    name = "Starting Kit Files"
    parent = "data"
    
+++
The "Starting Kit" file defines the "Starting Kits", or kits for short,
that are used to simplify the creation of NPCs and monsters as well as
the random generation of treasure. The page is divided into two
sections. The first section talks about [Building a Starting
Kit](/list/data/startingkits.html#howto) while the second contains the
[Starting Kit Tag Dictionary](/list/data/startingkits.html#dictionary) .
The tag dictionary is further broken down into three sub-sections, one
each for [The Region Tag](/list/data/startingkits.html#regiontags) ,
[Line Header Tags](/list/data/startingkits.html#linehdrtags) and
[Miscellaneous Tags](/list/data/startingkits.html#misctags) .

For more information about creating kits, check out the [Default Monster
Kit](/list/lst-file-class/11-kits-default-monster.html) LST File Class.

------------------------------------------------------------------------

<span id="howto"></span>Building a Starting Kit
-----------------------------------------------

Unlike most LST file objects, which are implemented on a single line for
each object, starting kits are defined as a block of lines with specific
information contained on each line. The general block structure is as
follows:

#### The Basic Starting Kit Block

Region Block (Optional)

Region line using the [`REGION`](/list/data/startingkits.html#region)
tag.

Starting Kit Block

STARTPACK line using the
[`STARTPACK`](/list/data/startingkits/startpack.html) ,
[`APPLY`](/list/data/startingkits/apply.html) ,
[`EQUIPBUY`](/list/data/startingkits/equipbuy.html) ,
[`TOTALCOST`](/list/data/startingkits/totalcost.html) and
[`VISIBLE`](/list/data/startingkits/visible.html) tags.

RACE line using the [`RACE`](/list/data/startingkits/race.html) and TBD
tags.

NAME line using the [`NAME`](/list/data/startingkits/name.html) tag.

GENDER line using the [`GENDER`](/list/data/startingkits/gender.html)
tag.

AGE line using the [`AGE`](/list/data/startingkits/age.html) tag.

ALIGN line using the [`ALIGN`](/list/data/startingkits/align.html) and
TBD tags.

STAT line using the [`STAT`](/list/data/startingkits/stat.html) and TBD
tags.

CLASS line using the [`CLASS`](/list/data/startingkits/class.html) and
[`LEVEL`](/list/data/startingkits/level.html) tags.

SKILL line for Class using the
[`SKILL`](/list/data/startingkits/skill.html) and
[`FREE`](/list/data/startingkits/free.html) ,
[`RANK`](/list/data/startingkits/rank.html) and
[`SELECTION`](/list/data/startingkits/selection.html) tags.

DEITY line using the [`DEITY`](/list/data/startingkits/deity.html) and
TBD tags.

DOMAIN line using the [`DOMAIN`](/list/data/startingkits/domain.html)
and [`COUNT`](/list/data/startingkits/count.html) tags.

PROF line using the [`PROF`](/list/data/startingkits/prof.html) ,
[`COUNT`](/list/data/startingkits/count.html) and
[`RACIAL`](/list/data/startingkits/racial.html) tags.

FEAT line using the [`FEAT`](/list/data/startingkits.html#feat) ,
[`FREE`](/list/data/startingkits/free.html) and
[`COUNT`](/list/data/startingkits/count.html) tags.

ABILITY line using the
[`ABILITY:CATEGORY`](/list/data/startingkits/category.html) and TBD
tags.

LEVELABILITY line using the
[`LEVELABILITY`](/list/data/startingkits/levelability.html) and
[`ABILITY:PROMPT`](/list/data/startingkits/ability.html) tags.

TEMPLATE line using the
[`TEMPLATE`](/list/data/startingkits/template.html) and TBD tags.

FUNDS line using the [`FUNDS`](/list/data/startingkits/funds.html) and
TBD tags.

GEAR line using the [`GEAR`](/list/data/startingkits/gear.html) ,
[`EQMOD`](/list/data/startingkits/eqmod.html) ,
[`LOCATION`](/list/data/startingkits/location.html) ,
[`LOOKUP`](/list/data/startingkits/lookup.html) ,
[`MAXCOST`](/list/data/startingkits/maxcost.html) and
[`QTY`](/list/data/startingkits/qty.html) tags.

TABLE line using the [`TABLE`](/list/data/startingkits/table.html) ,
[`LOOKUP`](/list/data/startingkits/lookup.html) and
[`VALUES`](/list/data/startingkits/values.html) tags.

SPELLS line using the [`SPELLS`](/list/data/startingkits/spells.html)
and [`COUNT`](/list/data/startingkits/count.html) tags.

Special Kit Block

SELECT line using the [`SELECT`](/list/data/startingkits/select.html)
tag in conjunction with any line listed above containing the
[`OPTION`](/list/data/startingkits/option.html) tag.

#### A Note on Prerequisites

All Starting Kit Lines are fully capable of being limited by the use of
PRExxx tags. Many of these tags grant things to the character only if
they can obtain it legally. This means that if you cannot afford all the
gear in the list, the kit will purchase as much as possible until you
run out of money. If you have previously gone to the inventory screen
and set the program to make all purchases cost zero, the kit will
purchase everything for zero. Or if the kit is set to try to give you a
feat which would normally be unavailable to you, but you have set the
program options to ignore requirements, then that is fine, the kit will
give you the feat.

#### A Note on Kit/Race Interactions

Use of a KIT tag, calling out a racial kit, in a Race object will cause
PCGen to crash if the following two conditions are met:

1.  The racial kit x contains a RACE:x tag, e.g. `RACE:Goblin`
2.  The race x object contains a KIT:x tag, e.g. `KIT:Goblin`

This combination of objects/tags will cause an infinite loop which in
turn will cause PCGen to crash. To prevent this you must use the
`!PRERACE:1,x` tag. For the example used above that would mean
`!PRERACE:1,Goblin` .

------------------------------------------------------------------------

<span id="dictionary"></span>Starting Kit Tag Dictionary
--------------------------------------------------------

Line Header Tags
----------------

Each of the tags in this section will be the first tag on their
respective line.

-   [STARTPACK](/list/data/startingkits/startpack.html)
-   [CATEGORY](/list/data/startingkits/category.html)
-   [AGE](/list/data/startingkits/age.html)
-   [ALIGN](/list/data/startingkits/align.html)
-   [CLASS](/list/data/startingkits/class.html)
-   [DEITY](/list/data/startingkits/deity.html)
-   [DOMAIN](/list/data/startingkits/domain.html)
-   [FUNDS](/list/data/startingkits/funds.html)
-   [GEAR](/list/data/startingkits/gear.html)
-   [GENDER](/list/data/startingkits/gender.html)
-   [LANGBONUS](/list/data/startingkits/langbonus.html)
-   [LEVELABILITY](/list/data/startingkits/levelability.html)
-   [NAME](/list/data/startingkits/name.html)
-   [PROF](/list/data/startingkits/prof.html)
-   [RACE](/list/data/startingkits/race.html)
-   [SELECT](/list/data/startingkits/select.html)
-   [SKILL](/list/data/startingkits/skill.html)
-   [SPELLS](/list/data/startingkits/spells.html)
-   [SPELLSSPELLBOOK](/list/data/startingkits/spellsspellbook.html)
-   [STAT](/list/data/startingkits/stat.html)
-   [SUBCLASS](/list/data/startingkits/subclass.html)
-   [TABLE](/list/data/startingkits/table.html)
-   [TEMPLATE](/list/data/startingkits/template.html)

### Misc Tags

-   [ABILITY](/list/data/startingkits/ability.html)
-   [APPLY](/list/data/startingkits/apply.html)
-   [COUNT](/list/data/startingkits/count.html)
-   [EQMOD](/list/data/startingkits/eqmod.html)
-   [EQUIPBUY](/list/data/startingkits/equipbuy.html)
-   [FREE](/list/data/startingkits/free.html)
-   [LEVEL](/list/data/startingkits/level.html)
-   [LOCATION](/list/data/startingkits/location.html)
-   [LOOKUP](/list/data/startingkits/lookup.html)
-   [MAXCOST](/list/data/startingkits/maxcost.html)
-   [OPTION](/list/data/startingkits/option.html)
-   [QTY](/list/data/startingkits/qty.html)
-   [RACIAL](/list/data/startingkits/racial.html)
-   [RANK](/list/data/startingkits/rank.html)
-   [SELECTION](/list/data/startingkits/selection.html)
-   [SIZE](/list/data/startingkits/size.html)
-   [TOTALCOST](/list/data/startingkits/totalcost.html)
-   [VALUES](/list/data/startingkits/values.html)
-   [VISIBLE](/list/data/startingkits/visible.html)

------------------------------------------------------------------------

### FEAT

-   6.05.04 (July 2015): JIRA
    [NEWTAG-477](http://jira.pcgen.org/browse/NEWTAG-477) / Github [PR
    \#380](https://github.com/PCGen/pcgen/pull/380)
-   -   The `FEAT` tag is deprecated. Use
        [`ABILITY`](/list/data/startingkits/category.html) instead.
    -   All `FEAT` tags have been **deprecated** and replaced by the
        `ABILITY` system, which is more general. The `ABILITY` system
        can model feats, racial features, class features, traits, flaws,
        temporary bonuses, and so on, all using a common format.

<div class="deprecated">

\*\* Updated 5.9.7
**Tag Name:** FEAT:x|x

**Variables Used (x):** Text (Feat name)

**Variables Used (x):** TYPE=Text (Feat TYPE)

**What it does:**

-   A pipe (|) delimited list of feats.
-   Presents the list as a choice to the user.
-   Grants the chosen feats.

**Examples:**

`FEAT:Weapon Focus (Greataxe)`

Would grant the "Greataxe Weapon Focus" feat.

`FEAT:Dodge PRESTAT:1,DEX=13`

Would grant "Dodge" if the character has a Dexterity of at least 13.

`FEAT:Dodge|Improved Initiative`

Would grant the choice of Dodge or Improved Initiative.

`FEAT:TYPE=ItemCreation`

Would grant the choice of an ItemCreation type feat.

</div>

------------------------------------------------------------------------

### <span id="regiontags"></span>The Region Tag

<span id="region"></span>\*\*\* Updated 5.9.3

**Tag Name:** REGION:x

**Variables Used (x):** Text (Region Name or None)

**What it does:**

-   This sets a prerequisite region for all kits below the tag.
-   You can use multiple REGION tags in a kit file. Each time it is used
    it will apply to the kits listed below it.
-   A character's Region may be set using the REGION global tag or with
    a REGION tag found within a template.
-   This tag is now optional in kit files.

**Example:**

`REGION:Europa`

Character must be from region Europa to apply any kits in the file.

`REGION:None`

There is no region prerequisite for these kits.

------------------------------------------------------------------------

