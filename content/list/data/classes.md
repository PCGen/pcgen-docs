+++
date = "2016-08-01"
title = "Class Files"
original_url = "/list/data/classes.html"

[menu.main]
    identifier = "data_classes"
    name = "Class Files"
    parent = "data"
    
+++
Class files are where each class is listed, given it's important
information for the correct output and functioning of the class.

This section consists of two major sections: [Class Building
101](/list/data/classes.html#classbuilding) and the [Tag
List](/list/data/classes.html#taglist) .

------------------------------------------------------------------------

<span id="classbuilding"></span> Class Building 101
---------------------------------------------------

Classes have three types of elements. These consist of the Class and
Class Level Lines, the Sub-Class and Sub-Class Level Lines, and the
Subsitution Class and Substitution Level Lines.

### Class and Class Level Lines

The Class and Class Level Lines are mandatory for all classes.

**The Main Class Line**

-   Begins with the `CLASS:<class name>` tag.
-   Multiple Class Lines may exist for each class being created.
-   Only tags identified as Class Line tags should be used on this line.

**The Class Level Line**

-   Begins with a numeric (i.e. 1, 2, 3, etc.) identifying the level
    that the line represents.
-   Only tags identified as Class Level Line tags may be used on
    ths line.

**A Basic Class Example**

> `CLASS:Rogue . . .`\
> `CLASS:Rogue . . .`\
> `1 . . .`\
> `2 . . .`\
> `.`\
> `.`\
> `.`\
> `19 . . .`\
> `20 . . .`

### Sub-Class and Sub-Class Level Lines

The Subclass tags were designed to implement the wizard subclasses and
has primary application in such rules mechanisms, i.e. take the subclass
and gain 'spell' related advantages and disadvantages in comparison to
the base class. You pick a subclass and your characters abilities are
changed throughout as defined by the subclass tags;
`      SUBCLASS     ` and `      SUBCLASSLEVEL     ` tags.

**The Sub-Class Line**

-   **NOTE:** `HASSUBCLASS` is no longer required to create sub-classes.
-   Begins with the `SUBCLASS:<sub-class name>` tag.
-   Placed between the Class Lines and the Sub-Class Level Lines that
    define the levels for the sub- class.
-   Only tags identified as Sub-Class Line or Class Line tags should be
    used on this line.

**The Sub-Class Level Line**

-   Begins with the `SUBCLASSLEVEL:<level number>` tag.
-   Placed after the Sub-Class Level Lines that define the
    associated sub-class.
-   Only the Sub-Class Level Lines that contain tags need to
    be included.
-   Only tags identified as Sub-Class Line or Class Line tags should be
    used on this line.
    -   `SPELLLIST` does not work on Class Line if a subclass or
        substitution class is present. In these cases, the `SPELLLIST`
        tag must be placed on each SubClass or Substitution Class Line
        (Not the SubClass/Substitution Level Line).

**A Sub-Class Example**

> `CLASS:Wizard . . .`\
> `CLASS:Wizard . . . ALLOWBASECLASS:NO`\
> `CLASS:Wizard . . .`\
> `SUBCLASS:Abjurer <tab> COST:2 <tab> CHOICE:SCHOOL|Abjuration <tab> KNOWNSPELLSFROMSPECIALTY:1`\
> `SUBCLASSLEVEL:1 <tab> FEATAUTO:Abjurer Learning Bonus`\
> `SUBCLASSLEVEL:10 <tab> SA:Immune to Acid`\
> `1 . . .`\
> `2 . . .`\
> `.`\
> `.`\
> `.`\
> `19 . . .`\
> `20 . . .`

### Substitution Class and Substitution Level Lines

The Substitution Level tags were added to PCGen to support the
substitution level mechanism used by WotC in their race books.
Substitution levels are used to replace a standard levels, removing and
replacing abilities with a different set without effecting any previous
or subsequent levels. You can have as many substitution levels as you
desire in your set and when your character reaches a level with a
substitution level he/she will be able to select the substitution level
or the standard level as he/she desires. Substitution levels can be
implemented with the inclusion of the `      SUBSTITUTIONCLASS     ` and
`      SUBSTITUTIONLEVEL     ` tags.

**The Substitution Class Line**

-   **NOTE:** `HASSUBSTITUTIONLEVEL` is no longer required to create a
    substitution level.
-   Begins with the `SUBSTITUTIONCLASS:<substitution class name>` tag.
-   Placed between the Class Lines and the Substitution Level Lines that
    define the levels for the substitution class.
-   Only tags identified as Substitution Class Line or Class Line tags
    should be used on this line.

**The Substitution Level Line**

-   Begins with the `SUBSTITUTIONLEVEL:<level number>` tag.
-   Placed after the Substitution Class Lines that define the associated
    substitution class.
-   Only the Substitution Level Lines that contain tags need to
    be included.
-   Only tags identified as Substitution Level Line or Class Level Line
    tags should be used on this line.
    -   SPELLLIST does not work on CLASS Line IF SUBCLASS or
        SUBSTITUTIONCLASS is present. In those cases, the SPELLLIST tag
        must be placed ON EACH SUBCLASS or SUBSTITUTION class line (Not
        Level Line).
    -   Another noted behavior - mainly code bug: Such classes will NOT
        display their Known Spells OR cast information on the
        spells tab.
    -   This behavior is expected to be fixed once CDOM is operational.

**A Substitution Level Example: Part of a Base Class Entry**

> `CLASS:Ranger . . .`\
> `CLASS:Ranger . . .`\
> `SUBSTITUTIONCLASS:Orc Ranger`\
> `SUBSTITUTIONLEVEL:4 <tab> HITDIE:12 <tab> SA:Goblin Slave (Ex)`\
> `SUBSTITUTIONLEVEL:10 <tab> HITDIE:12`\
> `1 . . .`\
> `2 . . .`\
> `.`\
> `.`\
> `.`\
> `19 . . .`\
> `20 . . .`

**A Substitution Level Example: A .MODed Class Entry**

> `CLASS:Ranger.MOD`\
> `SUBSTITUTIONCLASS:Orc Ranger`\
> `SUBSTITUTIONLEVEL:4 <tab> HITDIE:12 <tab> SA:Goblin Slave (Ex)`\
> `SUBSTITUTIONLEVEL:10 <tab> HITDIE:12`\

------------------------------------------------------------------------

<span id="taglist"></span> Tag List
-----------------------------------

The tag list is broken down into six parts:

### Tags Required for all Classes

-   [ABB](/list/data/classes/abb.html) (Obsolete - use FACT)
-   [ATTACKCYCLE](/list/data/classes/attackcycle.html)
-   [CLASS](/list/data/classes/class.html)
-   [CLASSTYPE](/list/data/classes/classtype.html) (Deprecated)
-   [HD](/list/data/classes/hd.html)
-   [MAXLEVEL](/list/data/classes/maxlevel.html)
-   [STARTSKILLPTS](/list/data/classes/startskillpts.html)
-   [XTRAFEATS](/list/data/classes/xtrafeats.html)

### Tags for spell-casting classes

-   [ADDDOMAINS](/list/data/classes/adddomains.html)
-   [CASTERLEVEL](/list/data/classes/casterlevel.html)
-   [BONUSSPELLSTAT](/list/data/classes/bonusspellstat.html)
-   [CAST](/list/data/classes/cast.html)
-   [DEITY](/list/data/classes/deity.html)
-   [DOMAIN](/list/data/classes/domain.html)
-   [ITEMCREATE](/list/data/classes/itemcreate.html)
-   [KNOWN](/list/data/classes/known.html)
-   [KNOWNSPELLS](/list/data/classes/knownspells.html)
-   [MEMORIZE](/list/data/classes/memorize.html)
-   [PROHIBITED](/list/data/classes/prohibited.html)
-   [PROHIBITSPELL](/list/data/classes/prohibitspell.html)
-   [ROLE](/list/data/classes/role.html)
-   [ROLE](/list/data/classes/role.html)
-   [SPELLBOOK](/list/data/classes/spellbook.html)
-   [SPELLLIST](/list/data/classes/spelllist.html)
-   [SPELLSTAT](/list/data/classes/spellstat.html)
-   [SPELLTYPE](/list/data/classes/spelltype.html) (Deprecated -
    use FACT)
-   [SPECIALTYKNOWN](/list/data/classes/specialtyknown.html)

### Tags for sub-classes

-   [ALLOWBASECLASS](/list/data/classes/allowbaseclass.html)
-   [CHOICE](/list/data/classes/choice.html)
-   [COST](/list/data/classes/cost.html)
-   [KNOWNSPELLSFROMSPECIALTY](/list/data/classes/knownspellsfromspecialty.html)
-   [PROHIBITCOST](/list/data/classes/prohibitcost.html)
-   [SUBCLASS](/list/data/classes/subclass.html)
-   [SUBCLASSLEVEL](/list/data/classes/subclasslevel.html)

### Tags for substitution classes

-   [SUBSTITUTIONCLASS](/list/data/classes/substitutionclass.html)
-   [SUBSTITUTIONLEVEL](/list/data/classes/substitutionlevel.html)

### Other optional tags for classes

-   [CLASSSKILLS](/list/data/classes/classskills.html)
-   [BONUSSKILLPOOL](/list/data/classes/bonusskillpool.html)
-   [DONOTADD](/list/data/classes/donotadd.html)
-   [EXCLASS](/list/data/classes/exclass.html)
-   [EXCHANGELEVEL](/list/data/classes/exchangelevel.html)
-   [HITDIE](/list/data/classes/hitdie.html)
-   [LANGBONUS](/list/data/classes/langbonus.html)
-   [REPEATLEVEL](/list/data/classes/repeatlevel.html)
-   [SKILLLIST](/list/data/classes/skilllist.html)
-   [TEMPLATE](/list/data/classes/template.html)
-   [TEMPLATEADDCHOICE](/list/data/classes/templateaddchoice.html)
-   [TEMPLATECHOOSE](/list/data/classes/templatechoose.html)
-   [VISIBLE](/list/data/classes/visible.html)
-   [WEAPONBONUS](/list/data/classes/weaponbonus.html)

### Monster-specific tags

-   [LEVELSPERFEAT](/list/data/classes/levelsperfeat.html)
-   [MODTOSKILLS](/list/data/classes/modtoskills.html)
-   [MONNONSKILLHD](/list/data/classes/monnonskillhd.html)
-   [MONSKILL](/list/data/classes/monskill.html)
-   [PRERACETYPE](/list/data/classes/preracetype.html)

------------------------------------------------------------------------

