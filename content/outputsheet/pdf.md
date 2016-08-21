+++
date = "2016-08-01"
title = "Character Output Sheets: PDF Versions"
original_url = "/outputsheet/pdf.html"

[menu.main]
    identifier = "outputsheet_pdf"
    name = "Character Output Sheets: PDF Versions"
    parent = "outputsheet"
    
+++
XSLT based PDF sheets
---------------------

-   XSLT sheets are xml XSL Transformations based, more dynamic versions
    of the .fo pdf sheets and have for the most part replaced them
    by now.
-   They are dynamic in the way that if the character has a portrait it
    will be displayed. If there is no picture of the character, that
    section of the sheet is simply skipped.
-   If a character is of an spellcasting class, its spells and spellbook
    will be listed.
-   If the character is of an spellcasting class and has not yet
    received any spells, no spell progression page will be added (unlike
    the now deprecated .fo sheets).
-   The sheet will include a bio page if there is some text contained in
    the bio field. Feat descriptions are included as
    in csheet\_fantasy\_descriptions.fo.
-   The xslt intelligence is contained in the
    [base.xml](/outputsheet/base-xml.html) file in the outputsheets
    root folder.

**csheet\_fantasy\_std\_xxx.xslt**

This sheet comes in several different colors, determined by the xxx
description and produces a 3+ page sheet styled after the
csheet\_fantasy\_std.htm sheet.\
 It will display all possible variations of wielding each weapon.

-   1 - Primary hand
-   2 - Off hand
-   3 - Two handed
-   4 - Two Weapon Fighting Primary Hand (off hand weapon light)
-   5 - Two Weapon Fighting Primary Hand (off hand weapon heavy)
-   6 - Two Weapon Fighting Off hand

**csheet\_fantasy\_simple\_xxx.xslt**

This sheet also comes in several different colors, determined by the xxx
description.\
 It is the same as the std sheet apart from the fact that for melee
weapons the simple sheet only shows the primary hand attack.\
 The simple sheet is used for characters who only fight with a single
weapon in their on-hand and do not need the other 5 variations.

**csheet\_modern\_std.xslt**

Same as the fantasy sheet, only for the d20 Modern gamemode (Modern).

**csheet\_fantasy\_spellbook\_xxx.xsl**

These templates are used to export the spells the character knows or has
access to, to a nicely formatted spell list. The different templates
offer several different layouts.

.fo based PDF sheets
--------------------

**csheet\_fantasy\_Spellbook.fo**

Produces a combined spell book for the character listing all spells
(regardless of class or level) in alphabetical order with their details.

------------------------------------------------------------------------



