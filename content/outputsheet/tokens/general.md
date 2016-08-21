+++
date = "2016-08-01"
title = "General Information Output Sheet Tokens"
original_url = "/outputsheet/tokens/general.html"

[menu.main]
    identifier = "tokens_general"
    name = "General Information Output Sheet Tokens"
    parent = "tokens"
    
+++
------------------------------------------------------------------------

**<span id="age"></span> Token Name:** AGE

**What it does:**

Displays characters age.

**Examples:**

`AGE`

Displays characters age.

------------------------------------------------------------------------

<span id="agecategory"></span> \*\*\* New 6.1.3

**<span id="agecategory"></span> Token Name:** AGE.CATEGORY

**What it does:**

Displays characters age category.

**Examples:**

`AGE.CATEGORY`

Displays characters age category.

------------------------------------------------------------------------

**<span id="alignment"></span> Token Name:** ALIGNMENT

**What it does:**

Displays characters alignment as full words, Lawful Good, Chaotic Evil,
None etc.

**Examples:**

`ALIGNMENT`

Displays characters alignment as full words.

------------------------------------------------------------------------

**<span id="alignmentshort"></span> Token Name:** ALIGNMENT.SHORT

**What it does:**

Displays characters alignment as 2 letters or 'None', LG, CE, None etc.

**Examples:**

`ALIGNMENT.SHORT`

Displays characters alignment as 2 letters or 'None'.

------------------------------------------------------------------------

**<span id="althp"></span> Token Name:** ALTHP

**What it does:**

Displays characters Alternate Hit Points as defined by the
`BONUS:HP|ALTHP|x` tag. This is used in gameModes which uses two
separate categories of hit points such as Spycraft which uses Wound
Points and Vitality Points.

**Examples:**

`ALTHP`

Displays characters Alternate Hit Points.

------------------------------------------------------------------------

**<span id="bio"></span> Token Name:** BIO

**What it does:**

Display characters biography.

If followed by a comma and text the text will be appended to the end of
each new line.

**Examples:**

`BIO`

Display characters biography. Note that for each newline in the BIO the
OS creates a gap. e.g.\
 Line 1\
 Line 2\
\
 will display as:\
 Line 1\
\
 Line 2\

`BIO,Text`

Display characters biography and appends the word 'Text' at the end of
each new line.

`BIO.beforevalue`

Display characters biography but prefixes beforevalue for each new line.

`BIO.beforevalue.aftervalue`

Display characters biography but prefixes beforevalue and appends
aftervalue for each new line.

------------------------------------------------------------------------

**<span id="birthday"></span> Token Name:** BIRTHDAY

**What it does:**

Display characters birthday.

**Examples:**

`BIRTHDAY`

Display characters birthday.

------------------------------------------------------------------------

**<span id="catchphrase"></span> Token Name:** CATCHPHRASE

**What it does:**

Display characters catch phrase.

**Examples:**

`CATCHPHRASE`

Display characters catch phrase.

------------------------------------------------------------------------

<span id="campaignhistory"></span> \*\*\* New 6.1.9

**Token Name:** CAMPAIGNHISTORY.v.x.y

**Variables Used (v):** Text (Visibility, Optional)

-   None - As per VISIBLE.
-   VISIBLE - Filter to just the entries that are marked for export.
-   HIDDEN - Filter to just the entries that are not marked for export.
-   ALL - Shows all entries.

**Variables Used (x):** Number (Entry's Position)

**Variables Used (y):** Text (Entry Property, Optional)

-   None - Displays the xth entry's text.
-   CAMPAIGN - Name of the campaign
-   ADVENTURE - Name of the adventure.
-   PARTY - Name of the party.
-   DATE - Date of the event.
-   XP - Amount of XP awarded.
-   GM - Name of the game master.
-   TEXT - Text of the entry.

**What it does:**

Displays information about the xth entry in the character's campaign
history list.

Entry position (x) is a zero-based index for the entries after filtering
(see above) for visibility (v).

**Examples:**

`CAMPAIGNHISTORY.0`

Output the text of the 1st (top-most) campaign history entry that is
marked for export.

`CAMPAIGNHISTORY.ALL.0.CAMPAIGN`

Output the campaign name from the 1st (top-most) campaign history entry
regardless of if it is marked for export.

------------------------------------------------------------------------

**<span id="charactertype"></span> Token Name:** CHARACTERTYPE

**What it does:**

Display the characters type, e.g. **PC** , **NPC** , etc..

**Examples:**

`CHARACTERTYPE`

Display the character's type.

------------------------------------------------------------------------

<span id="class"></span> \*\*\* Updated 6.1.2

**Token Name:** CLASS.x.y

**Variables Used (x):** Number (The classes position in the character's
class list - 0-based index).

**Variables Used (y):** Text (Property).

-   None - Displays the xth class' name.
-   LEVEL - Displays the xth class' level.
-   TYPE - Displays the xth class' type.
-   CLASSTYPE - Displays the xth class' class type.
-   ISMONSTER - Displays the xth class' ISMONSTER flag (Y/N).

**What it does:**

Displays the xth class' name or level.

**Examples:**

`CLASS.0`

Displays the name of the 1st class.

`CLASS.0.LEVEL`

Displays the level of the 1st class.

------------------------------------------------------------------------

**<span id="classabb"></span> Token Name:** CLASSABB.x

**Variables Used (x):** Number (The classes position in the character's
class list - 0-based index).

**What it does:**

Displays the abbreviated name of the xth class.

**Examples:**

`CLASSABB.0`

Displays the abbreviated name of the 1st class.

------------------------------------------------------------------------

**<span id="classlist"></span> Token Name:** CLASSLIST

**What it does:**

Displays a comma delimited list of all your classes including their
levels.

**Examples:**

`CLASSLIST`

Displays a comma delimited list of all your classes including their
levels.

------------------------------------------------------------------------

**<span id="color"></span> Token Name:** COLOR.x

**Variables Used (x):** Text (Property).

-   EYE - Display characters eye color.
-   HAIR - Display characters hair color.
-   SKIN - Display characters skin color.

**What it does:**

Displays the color of the selected item.

**Examples:**

`COLOR.EYE`

Display characters eye color.

`COLOR.HAIR`

Display characters hair color.

`COLOR.SKIN`

Display characters skin color.

------------------------------------------------------------------------

**<span id="cr"></span> Token Name:** CR

**What it does:**

Displays characters Chalenge Rating.

**Examples:**

`CR`

Displays characters Chalenge Rating.

------------------------------------------------------------------------

<span id="deity"></span> \*\*\* Updated

**Token Name:** DEITY.x

**Variables Used (x):** Text (Property).

-   None - Displays the deity name.
-   ALIGNMENT - Displays the deity alignment.
-   APPEARANCE - Displays the deity appearance.
-   DESCRIPTION - Displays the deity description.
-   DOMAINLIST - Displays the deity domain list.
-   FAVOREDWEAPON - Displays the deity favored weapon.
-   FOLLOWERALIGNMENT - Displays the deity acceptable
    follower alignments.
-   HOLYITEM - Displays the deity holy item.
-   PANTHEONLIST - Displays the deity pantheons.
-   SA - Displays the deity granted special abilities.
-   SOURCE - Displays the deity source.
-   TITLE - Displays the deity title.
-   WORSHIPPERS - Displays the deity typical worshippers.

**What it does:**

Displays the selected property of the Deity.

**Examples:**

`DEITY.DESCRIPTION`

Prints the deity description.

------------------------------------------------------------------------

**<span id="desc"></span> Token Name:** DESC

**What it does:**

Display characters description.

If followed by a comma and text the text will be appended to the end of
each new line.

**Examples:**

`DESC`

Display characters description.

`DESC,Text`

Display characters description and appends the word 'Text' at the end of
each new line.

------------------------------------------------------------------------

**<span id="domain"></span> Token Name:** DOMAIN.x.y

**Variables Used (x):** Number (The domain's position in the character's
domain list - 0-based index).

**Variables Used (y):** Text (Property).

-   None - Displays the domain name.
-   POWER - Displays the domain powers.

**What it does:**

Displays information about the character's selected domains.

**Examples:**

`DOMAIN.1`

Displays the name of the 2 ^nd^ domain.

`DOMAIN.1.POWER`

Displays the domain powers of the 2 ^nd^ domain.

------------------------------------------------------------------------

**<span id="dr"></span> Token Name:** DR

**What it does:**

Displays characters damage reduction.

**Examples:**

`DR`

Displays characters damage reduction.

------------------------------------------------------------------------

**<span id="ecl"></span> Token Name:** ECL

**What it does:**

Displays characters Effective Character Level.

**Examples:**

`ECL`

Displays characters Effective Character Level.

------------------------------------------------------------------------

**<span id="exp"></span> Token Name:** EXP.x

**Variables Used (x):** Text (Property).

-   CURRENT - Displays current XP.
-   NEXT - Displays XP required for next level.
-   FACTOR - Displays multiplying factor for multiclassing XP.
-   PENALTY - Displays the % experience penalty for having too many
    classes with levels too far apart.

**What it does:**

Displays various information about Experience Points.

**Examples:**

`EXP.CURRENT`

Displays current Experience Points.

------------------------------------------------------------------------

**<span id="face"></span> Token Name:** FACE.x

**Variables Used (x):** Text (Property).

-   SHORT - delivers "&lt;x&gt; &lt;MOVEUNITABBREV&gt;" or "&lt;x&gt; X
    &lt;y&gt;"
-   1 - delivers "&lt;x&gt;"
-   2 - delivers "&lt;y&gt;"

**What it does:**

Displays the area you occupy.

Used for the Face statistic in 3.0 rules and the Space statistic in 3.5
rules.

The [FACE](/list/data/races/face.html) tag from which the FACE token
gets its data can be one or two integers (x,y).

**Examples:**

`FACE.SHORT`

Displays the characters Face or Space statistic.

------------------------------------------------------------------------

**<span id="favoredlist"></span> Token Name:** FAVOREDLIST

**What it does:**

Displays a comma delimited list of all your favored classes.

**Examples:**

`FAVOREDLIST`

Displays a comma delimited list of all your favored classes.

------------------------------------------------------------------------

**<span id="follower"></span> Token Name:** FOLLOWER.x.y

**Variables Used (x):** Number (The follower's position in the
character's follower list - 0-based index).

**Variables Used (y):** Text (Any valid csheet token).

**What it does:**

Prints out the result of the specified token on the specified follower.

**Examples:**

`FOLLOWER0.RACE`

Displays the 1 ^st^ followers race.

`FOLLOWER0.GENDER.LONG`

Displays the 1 ^st^ followers long version gender (e.g. Male/Female).

------------------------------------------------------------------------

**<span id="followerlist"></span> Token Name:** FOLLOWERLIST

**What it does:**

Displays a comma delimited list of follower names.

**Examples:**

`FOLLOWERLIST`

Displays a comma delimited list of follower names.

------------------------------------------------------------------------

**<span id="followerof"></span> Token Name:** FOLLOWEROF

**What it does:**

Displays the type of follower the character is and the master's name
(e.g. "Familiar of Jorge").

**Examples:**

`FOLLOWEROF`

Displays the type of follower the character is and the master's name.

------------------------------------------------------------------------

**<span id="followertype"></span> Token Name:** FOLLOWERTYPE.x.y.z

**Variables Used (x):** Text (Follower Type).

-   ANIMAL COMPANION - Followers considered to be Animal Companions.
-   FAMILIAR - Followers considered to be Familiars.
-   FOLLOWER - Followers considered to be Henchmen.
-   SPECIAL MOUNT - Followers considered to be Special Mounts.

**Variables Used (y):** Number (The follower of the type specified's
position in the character's follower list - 0-based index).

**Variables Used (z):** Text (Any valid csheet token).

**What it does:**

-   Displays the specified token for the specified follower.
-   Both the Master and the Follower must be open in PCGen for this
    token to export the proper information.

**Examples:**

`FOLLOWERTYPE.FAMILIAR.0.NAME`

The name of the 1 ^st^ familiar is displayed.

------------------------------------------------------------------------

**<span id="gamemode"></span> Token Name:** GAMEMODE

**What it does:**

Displays the current Game Mode.

**Examples:**

`GAMEMODE`

Displays the current Game Mode.

------------------------------------------------------------------------

**<span id="gender"></span> Token Name:** GENDER.x

**Variables Used (x):** Text (Gender output type).

-   blank - Displays characters gender as a single letter, M for Male, F
    for Female.
-   SHORT - Displays characters gender as a single letter, M for Male, F
    for Female.
-   LONG - Displays characters gender as the whole word, Male or Female.

**What it does:**

Displays characters gender as a single letter, M for Male, F for Female.

**Examples:**

`GENDER`

Displays characters gender as a single letter, M for Male, F for Female.

------------------------------------------------------------------------

**<span id="gold"></span> Token Name:** GOLD

**What it does:**

Displays the amount of gold displayed in the Items tab.

**Examples:**

`GOLD`

Displays the amount of gold displayed in the Items tab.

------------------------------------------------------------------------

**<span id="handed"></span> Token Name:** HANDED

**What it does:**

Displays characters handedness, Left Handed, Right Handed.

**Examples:**

`HANDED`

Displays characters handedness, Left Handed, Right Handed.

------------------------------------------------------------------------

**<span id="height"></span> Token Name:** HEIGHT.x

**Variables Used (x):** Text (Height output type).

-   blank - Displays characters complete height in the currently
    selected height unit (e.g. 6' 2").
-   FOOTPART - Displays the foot part of characters height (e.g. 6').
-   INCHPART - Displays the inch part of characters height (e.g. 2").

**What it does:**

Displays character height information.

**Examples:**

`HEIGHT`

Displays characters complete height.

------------------------------------------------------------------------

<span id="hitdice"></span> \*\*\* Updated 6.1.3

**Token Name:** HITDICE

**Variables Used (x):** Modifier

-   blank - Displays characters total hit dice in explicit format.
-   LONG - same as blank.
-   MEDIUM - Display total hit dice in Pathfinder RPG statblock
    format, e.g. "3d10+12" or "3 HD; 2d8+1d10+6".
-   SHORT - Displays characters total hit dice in short format..

**What it does:**

Displays characters total hit dice.

**Examples:**

`HITDICE`

Displays characters total hit dice.

------------------------------------------------------------------------

**<span id="hp"></span> Token Name:** HP

**What it does:**

Displays characters Hit Points.

**Examples:**

`HP`

Displays characters Hit Points.

------------------------------------------------------------------------

**<span id="interests"></span> Token Name:** INTERESTS

**What it does:**

Display characters interests.

**Examples:**

`INTERESTS`

Display characters interests.

------------------------------------------------------------------------

<span id="invalidtext"></span> \*\*\* new 6.01.04

**Token Name:** INVALIDTEXT.x

**Variables Used (x):** Text (Property).

**What it does:**

Displays the invalid text appropriate to the referenced property.

-   DAMAGE - Displays the invalid damage text as defined in the Output
    Preferences tab.
-   TOHIT - Displays the invalid to-hit text as defined in the Output
    Preferences tab.

Note: This token is used to create a new node under /character/export in
the <span class="lstfile"> base.xml </span> , similar to the `PAPERINFO`
token, which is then used in the XSLT code.

**Examples:**

Node in base.xml file:

`<invalidtext>`\

`<tohit>|INVALIDTEXT.TOHIT|</tohit>`\

`<damage>|INVALIDTEXT.DAMAGE|</damage>`\

`</invalidtext>`

Code in xslt file:

`<xsl:if test="not(w1_h1_p/to_hit = /character/export/invalidtext/tohit          and w1_h1_p/damage = /character/export/invalidtext/damage          and w2_p_oh/to_hit = /character/export/invalidtext/tohit          and w2_p_oh/damage = /character/export/invalidtext/damage)">`

Displays the invalid to-hit and damage text on the Output Sheet.

------------------------------------------------------------------------

**<span id="languages"></span> Token Name:** LANGUAGES.x

**Variables Used (x):** Text (Language output type).

-   blank - Displays a comma delimited list of known languages.
-   Number?- The languages position in the character's language list -
    0-based index.

**What it does:**

Displays character language information.

**Examples:**

`LANGUAGES`

Displays a comma delimited list of known languages.

`LANGUAGES.3`

the 3 ^rd^ language known by the character.

------------------------------------------------------------------------

**<span id="length"></span> Token Name:** LENGTH.x

**Variables Used (x):** Text (Length output type).

-   HAIR - Display characters hair length.

**What it does:**

Displays character length information.

**Examples:**

`LENGTH.HAIR`

Display characters hair length.

------------------------------------------------------------------------

**<span id="location"></span> Token Name:** LOCATION

**What it does:**

Display characters location.

**Examples:**

`LOCATION`

Display characters location.

------------------------------------------------------------------------

**<span id="misc"></span> Token Name:** MISC.x,y

**Variables Used (x):** Text (Length output type).

-   FUNDS - Displays the Funds free-form entry in the Misc tab and is
    printed exactly as it appears in that text field.
-   COMPANIONS - Displays the Companions free-form entry in the Misc tab
    and is printed exactly as it appears in that text field.
-   MAGIC - Displays the Magic free-form entry in the Misc tab and is
    printed exactly as it appears in that text field.

**Variables Used (y):** Text (HTML formating).

**What it does:**

Displays info from the Miscellaneous tab.

**Examples:**

`MISC.MAGIC,<br/>`

Displays the contents of the Magic the free-form entry in the Misc tab
and is printed exactly as it appears in that text field after outputting
a blank line.

------------------------------------------------------------------------

**<span id="move"></span> Token Name:** MOVE.x.y

**Variables Used (x):** Number?(The movement types position in the
character's movement list - 0-based index).

**Variables Used (y):** Text (Property).

-   None - Displays the name and rate in the selected unit set of the
    xth movement type.
-   NAME - Displays the name only of the xth movement type.
-   RATE - Displays the rate only in the selected unit set of the xth
    movement type.
-   SQUARES - Displays the rate in 5' squares of the xth movement type.

**What it does:**

Displays movement information.

**Examples:**

`MOVE0.NAME`

Displays the name only of the 1 ^st^ movement type.

------------------------------------------------------------------------

**<span id="movement"></span> Token Name:** MOVEMENT

**What it does:**

Displays characters movement rate.

**Examples:**

`MOVEMENT`

Displays characters movement rate.

------------------------------------------------------------------------

**<span id="name"></span> Token Name:** NAME

**What it does:**

Displays characters name.

**Examples:**

`NAME`

Displays characters name.

------------------------------------------------------------------------

**<span id="note"></span> Token Name:** NOTE.w.x.y.z

**Variables Used (w):** Number?(The note's position in the character's
note list - 0-based index).

**Variables Used (x):** Text (Property).

**Variables Used (y):** Text (lineprefix - Optional).

**Variables Used (z):** Text (linesuffix - Optional).

-   NAME - Displays the note's name.
-   VALUE - Displays the notes contents.

**What it does:**

Export the note name/header and text/value.

**Examples:**

`NOTE.0.NAME`

Displays the 1 ^st^ note name in the character's note list.

`NOTE.0.NAME.<b>.</b>`

Displays the 1 ^st^ note name in the character's note list in bold font.

**Token Name:** NOTE.v.w.x.y.z

**Variables Used (v):** Text (Label).

-   ALL - This will cycle through all the notes.
-   Number - Will report based on the xth note.
-   Text -?Will find a note by that name and report on it.

**Variables Used (w):** Text (beforeHeader).

**Variables Used (x):** Text (afterHeader).

**Variables Used (y):** Text (beforeValue).

**Variables Used (z):** Text (afterValue).

**What it does:**

-   Exports and formats notes.
-   If any of the before and after values are not included they will be
    treated as empty strings.
-   Note that the parser will treat ..? as a single .? so if you want to
    skip a field you need to put a space between them (e.g.? ".? .").

**Examples:**

`NOTE.ALL.<b>.</b>.<br>`

This would bold the header of the note (from the Notes tab) and put a
new line before the value.

------------------------------------------------------------------------

**<span id="paperinfo"></span> Token Name:** PAPERINFO.x

**Variables Used (x):** Text (Property).

-   NAME - Displays the Paper Type defined in the Output Preferences.
-   HEIGHT - Displays the height of the Paper Type defined in the Output
    Preferences in millimeters or inches based on paper type (Metric
    or US).
-   WIDTH - Displays the width of the Paper Type defined in the Output
    Preferences in millimeters or inches based on paper type (Metric
    or US).
-   MARGINTOP - Displays the top margin of the Paper Type defined in the
    Output Preferences in millimeters or inches based on paper type
    (Metric or US).
-   MARGINBOTTOM - Displays the bottom margin of the Paper Type defined
    in the Output Preferences in millimeters or inches based on paper
    type (Metric or US).
-   MARGINLEFT - Displays the left margin of the Paper Type defined in
    the Output Preferences in millimeters or inches based on paper type
    (Metric or US).
-   MARGINRIGHT - Displays the right margin of the Paper Type defined in
    the Output Preferences in millimeters or inches based on paper type
    (Metric or US).

**What it does:**

Displays information about the paper defined in preferences for the
Output Sheet.

**Examples:**

`PAPERINFO.NAME`

Displays the name of the Paper Type defined in the Output Preferences.

------------------------------------------------------------------------

**<span id="pc"></span> \*\*\* new 5.7.14**

**Token Name:** PC.x

**Variables Used (x):** Text (Property).

-   HEIGHT - Displays the height of PC in inches (or whatever the base
    unit is).
-   WEIGHT - Displays the weight of PC in pounds (or whatever base
    unit is).

**What it does:**

Display characters height or weight.

**Examples:**

`PC.HEIGHT`

Display characters height.

------------------------------------------------------------------------

**<span id="personality"></span> Token Name:** PERSONALITY.1

**What it does:**

Display characters first personality trait.

**Examples:**

`PERSONALITY.1`

Display characters first personality trait.

**Token Name:** PERSONALITY.2

**What it does:**

Display characters second personality trait.

**Examples:**

`PERSONALITY.2`

Display characters second personality trait.

------------------------------------------------------------------------

**<span id="phobias"></span> Token Name:** PHOBIAS

**What it does:**

Display characters phobias.

**Examples:**

`PHOBIAS`

Display characters phobias.

------------------------------------------------------------------------

**<span id="playername"></span> Token Name:** PLAYERNAME

**What it does:**

Displays Player's Name.

**Examples:**

`PLAYERNAME`

Displays Player's Name.

------------------------------------------------------------------------

**<span id="pool"></span> Token Name:** POOL.x

**Variables Used (x):** Text (Property).

-   COST - Displays the original cost of creating the character if it
    was done in Purchase Mode.
-   CURRENT?- Displays the remaining stat pool.

**What it does:**

Displays information about the stat pool.

**Examples:**

`POOL.CURRENT`

Displays the remaining stat pool.

------------------------------------------------------------------------

**<span id="portrait"></span> Token Name:** PORTRAIT.x

**Variables Used (x):** THUMB (Property. Optional).

**What it does:**

-   PCGen outputs the path and file name to the portrait selected on the
    DESCRIPTION tab.
-   If `THUMB` is used PCGen outputs the path and file name to the
    generated thumbnail of the portrait selected on the DESCRIPTION tab.

**Examples:**

`PORTRAIT`

Outputs the path and file name to the portrait selected on the
DESCRIPTION tab.

`PORTRAIT.THUMB`

Outputs the path and file name to the thumbnail of the portrait selected
on the DESCRIPTION tab.

------------------------------------------------------------------------

**<span id="race"></span> Token Name:** RACE

**What it does:**

Displays characters race.

**Examples:**

`RACE`

Displays characters race.

------------------------------------------------------------------------

<span id="racesubtype"></span> \*\*\* New 5.9.4

**Token Name:** RACESUBTYPE.x

**Variables Used (x):** Number (The subtypes position in the character's
subtypes list - 0-based index).

**What it does:**

Displays characters race subtype as set by the
[RACESUBTYPE](/list/data/races/racesubtype.html) race tag.

**Examples:**

`RACESUBTYPE.0`

Displays the characters first racial subtype.

------------------------------------------------------------------------

<span id="racetype"></span> \*\*\* New 5.9.4

**Token Name:** RACETYPE

**What it does:**

Displays characters race type as set by the
[RACETYPE](/list/data/races/racetype.html) race tag.

**Examples:**

`RACETYPE`

Displays characters race type.

------------------------------------------------------------------------

**<span id="reach"></span> Token Name:** REACH

**What it does:**

Displays characters reach.

**Examples:**

`REACH`

Displays characters reach.

------------------------------------------------------------------------

**<span id="region"></span> Token Name:** REGION

**What it does:**

Displays the character's region as defined by their region template.

**Examples:**

`REGION`

Displays the character's region as defined by their region template.

------------------------------------------------------------------------

**<span id="residence"></span> Token Name:** RESIDENCE

**What it does:**

Display characters residence.

**Examples:**

`RESIDENCE`

Display characters residence.

------------------------------------------------------------------------

**<span id="size"></span> Token Name:** SIZE

**What it does:**

Displays your size (based on your race) as a single letter.

**Examples:**

`SIZE`

Displays your size as a single letter.

------------------------------------------------------------------------

**<span id="sizelong"></span> Token Name:** SIZELONG

**What it does:**

Displays the full name of your size (ie.? "Medium" instead of "M").

**Examples:**

`SIZELONG`

Displays your size as a single letter.

------------------------------------------------------------------------

**<span id="speechtendency"></span> Token Name:** SPEECHTENDENCY

**What it does:**

Display characters speechtendency.

**Examples:**

`SPEECHTENDENCY`

Display characters speechtendency.

------------------------------------------------------------------------

**<span id="sr"></span> Token Name:** SR

**What it does:**

Displays characters spell resistance.

**Examples:**

`SR`

Displays characters spell resistance.

------------------------------------------------------------------------

**<span id="subregion"></span> Token Name:** SUBREGION

**What it does:**

Displays the character's subregion as defined by their region template.

**Examples:**

`SUBREGION`

Displays the character's subregion as defined by their region template.

------------------------------------------------------------------------

**<span id="total"></span> Token Name:** TOTAL.x

**Variables Used (x):** Text (Property).

-   CAPACITY?- Displays carrying capacity, in pounds, of the character.
-   LOAD?- Displays the kind of LOAD (Light, Medium, Heavy,
    or Overload).
-   VALUE?- Displays the total value of all your equipment, in
    gold pieces.
-   WEIGHT - Displays the total weight, in pounds, of equipment the
    character is carrying.

**What it does:**

Displays load information about carried equipment.

**Examples:**

`TOTAL.CAPACITY`

Displays 'total' information about carried equipment.

------------------------------------------------------------------------

**<span id="totallevels"></span> Token Name:** TOTALLEVELS

**What it does:**

Displays an integer of your total levels.

**Examples:**

`TOTALLEVELS`

Displays an integer of your total levels.

------------------------------------------------------------------------

**<span id="type"></span> Token Name:** TYPE

**What it does:**

Displays the type set by the [TYPE](/list/data/races.html#type) race
tag.

**Examples:**

`TYPE`

Displays the race type.

------------------------------------------------------------------------

<span id="unitset"></span> \*\*\* new 5.7.9

**Token Name:** UNITSET.x

**Variables Used (x):** Text (Property).

-   blank - Displays the name of the unit set.
-   HEIGHTUNIT - Displays the unit used for character height.
-   DISTANCEUNIT - Displays the unit used for distances.
-   WEIGHTUNIT - Displays the unit used for weights.

**What it does:**

Displays unit set information.

**Examples:**

`UNITSET`

Displays the name of the currently selected unit set.

`UNITSET.WEIGHTUNIT`

Displays the weight unit of the currently selected unit set.

------------------------------------------------------------------------

<span id="vision"></span> \*\*\* updated 5.9.5

**Token Name:** VISION.x

**Variables Used (x):** Text (Vision output type).

-   blank - Displays a comma delimited list of character's vision types.
-   Number?- The vision position in the character's vision list -
    0-based index.

**What it does:**

Displays character vision information.

**Examples:**

`VISION`

Displays a comma delimited list of the character's vision types.

`VISION.3`

the 3 ^rd^ vision type of the character.

------------------------------------------------------------------------

**<span id="weight"></span> Token Name:** WEIGHT.x

**Variables Used (x):** Text (Property).

-   blank - Displays characters weight in the currently selected
    weight unit.
-   NOUNIT - Displays characters weight with no units.
-   LIGHT - Displays the max weight for the Light load category.
-   MEDIUM - Displays the max weight for the Medium load category.
-   HEAVY - Displays the max weight for the Heavy load category.
-   OVERHEAD - Displays the max weight for the OverHead load category.
-   OFFGROUND - Displays the max weight for the OffGround load category.
-   PUSHDRAG - Displays the max weight for the PushDrag load category.

**What it does:**

Displays characters weight information. The last six properties are
defined in the Load.lst gameMode file with the
[ENCUMBRANCE](/list/system/gamemode-load/encumbrance.html) tag

**Examples:**

`WEIGHT`

Displays characters weight in the currently selected weight unit.

`WEIGHT.LIGHT`

Displays max weight for the light load category.

------------------------------------------------------------------------

<span id="xpaward"></span> \*\*\* New 6.1.2

**Token Name:** XPAWARD

**What it does:**

Display the experience award for this creature. This is only used for
game modes with fixed XP awards per CR, such as the Pathfinder RPG.

**Examples:**

`XPAWARD`

Display the XP award.

------------------------------------------------------------------------



