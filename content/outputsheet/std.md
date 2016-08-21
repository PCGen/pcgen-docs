+++
date = "2016-08-01"
title = "Character Output Sheets in PCGen"
original_url = "/outputsheet/std.html"

[menu.main]
    identifier = "outputsheet_std"
    name = "Character Output Sheets in PCGen"
    parent = "outputsheet"
    
+++
Standard Output Sheets
----------------------

### HTML Based Output Sheets

**csheet\_fantasy\_std.htm**

-   Spans 3+ pages (depending on class).
-   Includes Bio sheet full spell lists with spell details. Includes 2
    images if they exist.
-   They must have the name &lt;character\_name&gt;.jpg and
    &lt;character\_name&gt;\_Full.jpg and be in the same directory as
    the exported sheet.

**csheet\_fantasy\_compact.htm**

-   Compacted to fit on 2 pages (or one page duplexed).
-   Does not have Bio or full spell details (only spell titles).
-   Includes 2 images if they exist.
-   They must have the name &lt;character\_name&gt;.jpg and
    &lt;character\_name&gt;\_Full.jpg and be in the same directory as
    the exported sheet.

**csheet\_fantasy\_combined.htm**

-   Uses JavaScript to produce 3 different formats in the one export.
-   It has layouts similar to the previous 2 sheets and a third layout
    that is somewhere between them.
-   This sheet gives you the most flexibility but requires JavaScript
    and probably Internet Explorer to get the layout correct.
-   It also has buttons for barbarian characters to make the necessary
    changes when raging and fatigued.
-   Includes buttons to increase stats and shows the effects on AC,
    Initiative, Skills, Weapons etc.
-   Includes 2 images if they exist.
-   Only non PDF sheet that shows Skill Mastery (Rogue 10th Level
    Ability option) if picked.
-   They must have the name &lt;character\_name&gt;.jpg and
    &lt;character\_name&gt;\_Full.jpg and be in the same directory as
    the exported sheet.

**csheet\_fantasy\_statblock1.htm**

This sheet replicates the format used to present monsters in 3.0
sources.

**csheet\_fantasy\_statblock2.htm**

This sheet replicates the 3.0 statblock format.

**csheet\_fantasy\_statblock3.htm**

This sheet replicates the 3.5 statblock format.

**csheet\_fantasy\_statblock4.htm**

This sheet replicates an improved 3.5 statblock format which later
sources adopted.

**csheet\_fantasy\_statblock5.htm**

This sheet replicates the statblock format used by Paizo for the
Pathfinder Role Playing Game.

**csheet\_fantasy\_statblock\_SRD.htm**

This sheet replicates the format used to present monsters in [Andargor's
downloadable SRD](http://www.andargor.com/) .

**eqsheet\_fantasy\_consumables.htm**

Outputs all items a character has that can be considered consumables,
e.g. ammo, potions etc.\
 Includes checkboxes to keep track of what has been used and what not.

**eqsheet\_fantasy\_std.htm**

Outputs each of the equipment sets created on the Equipping Tab for the
character.

**psheet\_fantasy\_std.htm**

This sheet is primarily intended for the Game Master, it contains
condensed information on the entire party for quick reference.\
 It includes image of each character if the &lt;character\_name&gt;.jpg
file exists.\
 It lists Name, Classes, Level, HP, AC, AC Flat-footed, Initiative,
Vision, Alignment, Total Equipment Value, Fortitude, Reflex, Will,
Search, Spot, Listen and Languages.

### XML Based Output Sheets

**csheet\_fantasy\_OpenRPG.xml**

-   This sheet is aimed at the button-pushing macro-loving set of
    OpenRPG users; for those that prefer a less interactive character
    sheet, we recommend exporting to a plain text sheet that you like
    and cut/pasting your character into a text box.
-   You'll find all the dice macros on the combat tab.

**csheet\_fantasy\_rpgwebprofiler.xml and
csheet\_modern\_rpgwebprofiler.xml**

-   These sheets export to an xml format which can be imported into [RPG
    Web Profiler Online Character
    Sheets](http://www.myth-weavers.com/sheetindex.php) web based
    service (formerly [here](http://www.rpgwebprofiler.net/) )
-   Separate sheets are needed for Fantasy and Modern, the two are
    incompatible, the export sheets will set which template
    rpgwebprofiler uses.
-   PCGen cannot populate rpgwebprofilers spell list, instead the spell
    information is written to the notes section.

------------------------------------------------------------------------



