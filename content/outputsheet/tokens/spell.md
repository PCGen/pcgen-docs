+++
date = "2016-08-01"
title = "Spell Related Output Sheet Tokens"
original_url = "/outputsheet/tokens/spell.html"

[menu.main]
    identifier = "tokens_spell"
    name = "Spell Related Output Sheet Tokens"
    parent = "tokens"
    
+++
------------------------------------------------------------------------

\*\*\* new 5.7.12

**<span id="maxspelllevel"></span> Token Name:** MAXSPELLLEVEL.x

**Variables Used (x):** Number (The class number).

**What it does:**

The value returned is an integer containing the highest spell level that
the class can cast (for most RSRD classes this will either be 9 (for
Wizards) or 4 (for Rangers etc)).

------------------------------------------------------------------------

\*\*\* new 5.10.1

**<span id="spellbook"></span> Token Name:** SPELLBOOK.x.y

**Variables Used (x):** Number (The Spell book Number of the spell book
you wish to display).

\* The known spell book is spell book number 0.

\* The racial innate spell book is spell book number 1.

\* Other innate spell books are spell book number 2 or up.

\* The innate spell books will not exist if the character does not have
innate spells.

**Variables Used (y):** Text (The property of the spell book you wish to
display).

\* NAME - Display the name of the indicated spell book or list.

\* NUMPAGES - Display the total number of pages in the spell book (or 0
if there are no pages, such as in a prepared spell list).

\* NUMPAGESUSED - Display the number of pages currently in use for the
spell book (or 0 if there are no pages, such as in a prepared spell
list).

\* NUMSPELLS - Display the number of spells in the spell book or list.

\* PAGEFORMULA - Display the page formula for the spell book (or an
empty string if there are no pages, such as in a prepared spell list).

\* TYPE - Display the type (e.g. Known Spells, Prepared List) of the
spell book or list.

**What it does:**

Displays information about the character's spell book or spell list.

**Example:**

`SPELLBOOK.0.NAME`

Displays the name of the 1st spell book for the character.

------------------------------------------------------------------------

**<span id="spellbookname"></span> Token Name:** SPELLBOOKNAME.x

**Variables Used (x):** Number (The book number of the spellbook title
you wish to display).

**What it does:**

-   Displays the title of spellbook x in the character spellbook list.
-   The Known Spellbook is any class but 0, spellbook number 0.
-   The Racial Innate Spellbook is class 0, spellbook number 1.
-   Other Innate Spellbooks are class 0, spellbook number 2 or up.
-   The Innate spellbooks will not exist if the character does not have
    innate spells.
-   The -1 Spellbook should not be used any more.

**Example:**

`SPELLBOOKNAME.0`

Display Spell Book 0 (the default spellbook).

------------------------------------------------------------------------

\*\*\* updated 5.17.7

**<span id="spelllist"></span> Token Name:** SPELLLISTx.y.z

**Variables Used (x):** Text (Spellbook Option. See below)

**Variables Used (y):** Number (Class Number - 0 index array).

**Variables Used (z):** Number (Spellcasting Level - 0-9).

**Variables Used (w):** Number (Book Number. Optional).

**What it does:**

-   Displays information about spellcasting ability, and
    spells themselves.
-   Spellbook options include the following sub-tokens:
    -   `BOOK` - Displays a comma delimited list of spells known to
        spellcaster class number y for level z of book w.
    -   `CAST` - Displays the number of spells you can cast for
        spellcaster class number y for level z.
    -   `CLASS` - Displays the spellcaster class information.
        -   `CLASS.y` - Displays the spellcaster classname for class
            number y.
        -   `CLASS.y.CASTERLEVEL` - Displays the effective casting level
            for spells cast by spellcaster class y, including bonus
            levels from other classes.
        -   `CLASS.y.CONCENTRATION` - Displays the concentration check
            bonus for spells cast by spellcaster class y (empty if no
            formula is defined in the game mode).
        -   `CLASS.y.LEVEL` - Displays the spellcaster's class level for
            spellcasting class y.
    -   `DC` - Displays the casting DC for a z level spell for
        spellcaster class y.
    -   `DCSTAT` - Displays the STAT used to figure out the DC of a z
        level spell cast by spallcaster class y.
    -   `MEMORIZE` - Returns a boolean "true" if the spellcaster class y
        needs to memorize spells, "false" if otherwise.
    -   `TYPE` - Displays the spell type (e.g. Arcane or Divine) of
        spellcaster class y.
    -   `KNOWN` - Displays how many spells spellcaster class y can know
        for level z. For Clerics with domains, this does not include
        domain spells.

**Example:**

`SPELLLISTCAST.0.1`

Displays how many spells the character can cast for the 1 ^st^ level of
the 1 ^st^ spellcaster class the character has.

`SPELLLISTTYPE.0.1`

Displays the spell list type of the 1 ^st^ spellcaster class the
character has.

------------------------------------------------------------------------

\*\*\* updated 6.1.9

**<span id="spellmem"></span> Token Name:** SPELLMEM.v.w.x.y.z

**Variables Used (v):** Number (Spell class).

**Variables Used (w):** Number (Spellbook).

**Variables Used (x):** Number (Spell level).

**Variables Used (y):** Number (Number of the spell in known spells
list).

**Variables Used (z):** Text (Spell property).

**What it does:**

-   Displays information about the spells in the character spellbooks.
-   Standard Class/Spellbook combinations are as follows:
    -   The Known Spellbook is any class but 0, spellbook number 0.
    -   The Racial Innate Spellbook is class 0, spellbook number 1.
    -   Other Innate Spellbooks are class 0, spellbook number 2 or up.
    -   The Innate spellbooks will not exist if the character does not
        have innate spells.
    -   A spellbook number of "-1" should no longer be used.
-   Spell properties are identified as follows:
    -   `APPLIEDNAME` - Display a list of adjectives for metamagic feats
        or abilities modifying this spell.
    -   `BASENAME` - Display the name of the spell, unmodified by
        abilities such as metamagic feats or abilities.
    -   `BASEPPCOST` - Display the PPCOST for the a spell.
    -   `BONUSSPELL` - Display an \* is the spell is a domain/specialty
        spell, display \*\* if it is ONLY a domain/specialty spell.
    -   `COMPONENTS` - Display the necessary components of the
        indicated spell.
    -   `CASTERLEVEL` - Display the caster level (including bonuses) of
        the indicated spell.
    -   `CASTINGTIME` - Display the casting time of the indicated spell.
    -   `CLASS` - Indicates spellcaster classname.
    -   `CONCENTRATION` - Displays the concentration check bonus for the
        indicated spell (empty if no formula is defined in the
        game mode).
    -   `CT` - Display the Casting Threshold of the indicated spell.
    -   `DC` - Display the DC of the indicated spell.
    -   `DCSTAT` - Display the STAT used to figure out DC of spell
    -   `DESC` - Display the description of the indicated spell.
    -   `DESCRIPTION` - Display the description of the indicated spell.
    -   `DESCRIPTOR` - Display the discriptor of the indicated spell.
    -   `DURATION` - Display the duration of the indicated spell.
    -   `EFFECT` - Display the effect of the indicated spell.
    -   `EFFECTTYPE` - Display the type of effect of the
        indicated spell.
    -   `FULLSCHOOL` - Display the school, if any, of the indicated
        spell in long form.
    -   `NAME` - Display the name of the indicated spell.
    -   `RANGE` - Display the range of the indicated spell.
    -   `SAVEINFO` - Display the save info of the indicated spell.
    -   `SCHOOL` - Display the school, if any, of the indicated spell in
        short form.
    -   `SOURCE` - Display the source of the indicated spell in
        long form.
    -   `SOURCELEVEL` - Display all the sources and levels of the
        indicated spell (Wiz3,Sor3).
    -   `SOURCELINK` - Display the URL of the online system reference
        document for the indicated spell.
    -   `SOURCEPAGE` - Display the source page of the indicated spell.
    -   `SOURCESHORT` - Display the source of the indicated spell in
        short form.
    -   `SOURCEWEB` - Display the URL of the source of the
        indicated spell.
    -   `SUBSCHOOL` - Display the subschool, if any, of the
        indicated spell.
    -   `SR` - Display the spell resistance properties of the
        indicated spell.
    -   `SRSHORT` - Returns an "N" if spell the spell ignores
        resistance, "Y" if it does not.
    -   `TARGET` - Display the target of the indicated spell (contents
        of the TARGETAREA lst tag).
    -   `TIMES` - Display the number of times the indicated spell is in
        the spellbook.
    -   `TIMEUNIT` - Display the unit of time (i.e. Encounter, Week,
        Month, etc.).
    -   `TYPE` - Display the type (i.e. Arcane or Divine) of
        spell class.

**Example:**

`SPELLMEM.0.1.2.3.NAME`

Displays the Name of the fourth 2 ^nd^ level spell in the second
spellbook for the first character class.

------------------------------------------------------------------------

**<span id="spellpoints"></span> Token Name:** SPELLPOINTS

**What it does:**

Use only for Deadlands. Gives the number of Spellpoints the character
has.

**Example:**

`SPELLPOINTS`

Gives the number of Spellpoints the character has.

------------------------------------------------------------------------



