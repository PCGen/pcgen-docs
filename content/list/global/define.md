+++
date = "2016-08-01"
title = "The Define Tag and Variables"
original_url = "/list/global/define.html"

[menu.main]
    identifier = "global_define"
    name = "The Define Tag and Variables"
    parent = "global"
    
+++
This page is broken into two sections. The first section will describe
the `DEFINE` tag and its uses. The second section will discuss variables
and their use in PCGen.

------------------------------------------------------------------------

<span id="define"></span> The Define Tag
----------------------------------------

The DEFINE tag is used to create new user-defined variables and set
their initial values.

**Tag Name:** DEFINE:x|y

**Variables Used (x):** Text (Name of variable)

**Variables Used (y):** Number or Formula (Can be a formula involving
system or user-defined variables or numbers.)

**What it does:**

-   Creates a variable with the name specified and sets its initial
    value to the number or formula given.
-   Many classes use `PREVARxx` tags, which are prerequisites based upon
    variable values.
-   Values are calculated by getting the value of the variable with the
    highest defined value, and then adding any bonuses which apply
    to it.
-   PCGen scans the character's race, templates, classes, feats, skills,
    deity, domains and equipped items for `DEFINE` tags that match this
    variable name.
-   If it finds more than one, it keeps the one with the higher value.
-   PCGen then scans the same list of items and looks for `BONUS:VAR`
    tags and after figuring out which ones stack, adds those to the
    highest define value.
-   The resulting value is then compared to the `PREVARxx` requirement
    and PCGen then indicates if the character meets this requirement
    or not.
-   `BONUS:VAR` tags which reference variables which have not been
    defined have no effect and the value of that variable will
    effectively remain at zero (0).
-   The standard use of `DEFINE` in PCGen release files is to use only
    one `DEFINE` per variable and to initially set the value to zero (0)
    and adjust it with `BONUS:VAR` tags as needed.

**Example:**

`DEFINE:MonkeyChop|2`

Creates a new variable named MonkeyChop and sets the initial value to 2.

`DEFINE:MonkeySwing|0 <tab> BONUS:VAR|MonkeySwing|TL/2`

Creates a new variable named **MonkeySwing** and sets the initial value
to zero, then bonuses the variable to half the character's total level.

------------------------------------------------------------------------

<span id="variables"></span> Variables
--------------------------------------

For those unfamiliar with computer programming or higher math a variable
is a symbol which represents a quantity that is not fixed. Most people's
first introduction to variables is in algebra where you might be given a
problem such as "x+y=z". In this formula, the "x", "y" and "z" are
variables. PCGen uses variables and formulas for a wide variety of
purposes throughout the program. Some variables are created in LST
files, and are henceforth called user-defined variables, while others
are system-defined, that is they are hard-coded into PCGen's code-base.
While both types of variable can be used in any formula in any LST file,
only system-defined variables can be used in any gameMode. Only
user-defined variables can be modified through the use of the
`BONUS:VAR` tag.

Here are a few notes on naming variables:

1.  You can create variable names any way you like - but we recommend
    using no spaces and a name that is both descriptive and unlikely to
    conflict with a variable name used in another source for a
    different purpose. Capitalizing the first letter of each word used
    in the variable name makes it more readable and more easily
    identified as a variable. Using all caps to name a variable should
    be reserved for pre-defined variables that are hard-coded.
2.  Sometimes the same variable name will be used in different sources
    if they work together (this happens when one class is based on a
    class from a different source).
3.  Certain variables are pre-defined, be careful not to use any of
    those names when creating your variables.

------------------------------------------------------------------------

<span id="sysdefinedvariables"></span> System-Defined Variables
---------------------------------------------------------------

All variables listed below are global in nature, unless explicitly
stated within the variable-specific documentation, and can be used in
any formula, in any file, in any gamemode.

**<span id="accheck"></span> ACCHECK**

This is the total AC Check penalty from armor and shield.

**<span id="armoraccheck"></span> ARMORACCHECK**

This is the total AC Check penalty from armor.

**<span id="bab"></span> BAB**

This is the Base Attack Bonus. The progression for the BAB is set for
each individual class in the <span class="lstfile"> class.lst </span>
file. The BAB progression is set using the global `BONUS:COMBAT|BAB`
tag, which will take a formula. As an example, `BONUS:COMBAT|BAB|CL*2`
would grant a BAB of +2 per class-level.

**<span id="basecr"></span> BASECR**

This is the unmodified Challenge Rating of the character's race.

<span id="basehd"></span> \*\*\* New 6.03.00

**BASEHD**

This is the unmodified number of hit dice of the creature in question,
as specified with the `MONSTERCLASS` race tag. If that tag is absent,
the variable will return 0.

**<span id="basespellstat"></span> BASESPELLSTAT**

This is the modifier for the class's base spell stat. This variable can
only be used in a <span class="lstfile"> class.lst </span> file.

**<span id="bl"></span> BL=name**

This will return the Bonus Spellcaster Levels to the class specified,
which usually come from Prestige classes. For example, let's say you
have 2 levels **Mystic Theurge** which add to both your **Cleric** and
**Wizard** levels, 3 levels of **Archmage** which add to your **Wizard**
level, and 1 level of **Loremaster** which adds to your **Cleric**
level. `BL=Wizard` would return 5 and `BL=Cleric` would return 3.
Replace "{" with "(" and "}" with ")", e.g. `BL=Cleric {Special}` would
return the bonus levels of "Cleric (Special)" since "(" and ")" have
other meanings in DEFINE variables. If used within a JEP formula you
will need to enclose it in a variable function e.g.
`var("BL=Cleric {Special}")` .

**<span id="casterlevel"></span> CASTERLEVEL**

This is a special variable and is valid only in Spell objects and
therefore should only be used in Spell LST Files. See the
[CASTERLEVEL](/list/data/spells/casterlevel.html) tag entry on the Spell
tag page.

**<span id="cha"></span> CHA**

This is the character's CHA modifier.

**<span id="chascore"></span> CHASCORE**

This is the character's actual Charisma score.

**<span id="cl"></span> CL**

This provides the class level for the class object in which it is being
used. This variable is valid only in the Class object and should only be
used in <span class="lstfile"> class.lst </span> files.

**<span id="clname"></span> CL=name**

Class Level of the named class. This can now be done with the
[classlevel()](/list/global/formulas.html#classlevel) JEP function.

**<span id="classname"></span> CLASS=name**

Returns a 1 if the character has the named class, otherwise 0. Replace {
with ( and } with ). e.g. CLASS=Ranger {Special} would check for Ranger
(Special) since ( and ) have other meanings in DEFINE variables. If used
within a JEP formula you will need to enclose it in a variable function
e.g. var("CLASS=Ranger {Special}")

**<span id="classlevelname"></span> CLASSLEVEL=name**

Class Level of the named class, replacing ( with { and ) with }. e.g.
CLASSLEVEL=Warrior {Ruby} would return the level of Warrior (Ruby) since
( and ) have other meanings in DEFINE variables. If used within a JEP
formula you will need to enclose it in a variable function e.g.
var("CLASSLEVEL=Warrior {Ruby}")

**<span id="con"></span> CON**

This is the character's CON modifier.

**<span id="conscore"></span> CONSCORE**

This is the character's actual Constitution score.

**<span id="countclasses"></span> COUNT\[CLASSES\]**

This is the character's number of classes.

**<span id="countdomains"></span> COUNT\[DOMAINS\]**

This is the character's number of domains.

**<span id="countfeatname"></span> COUNT\[FEATNAME=name\]**

This is the number of feats of the given name. Great for multiple feats
that grant bonuses based on the number of times taken.

**<span id="countfeats"></span> COUNT\[FEATS\]**

This is the character's number of optionally chosen feats (not automatic
or virtual).

**<span id="countfeatsall"></span> COUNT\[FEATSALL\]**

This is the character's total number of feats (includes automatic and
virtual).

**<span id="countfeattype"></span> COUNT\[FEATTYPE=type\]**

This is the character's number of feats matching specified type.

**<span id="countfollowers"></span> COUNT\[FOLLOWERS\]**

This is the character's number of Followers.

**<span id="countlanguages"></span> COUNT\[LANGUAGES\]**

This is the character's number of languages.

**<span id="countsa"></span> COUNT\[SA\]**

This is the character's number of unique special abilities.

**<span id="countskills"></span> COUNT\[SKILLS\]**

This is the character's number of skills.

**<span id="countspellclasses"></span> COUNT\[SPELLCLASSES\]**

This is the character's number of spellcasting classes.

**<span id="countstats"></span> COUNT\[STATS\]**

This is the number of defined stats.

**<span id="cr"></span> CR**

This is the character's Challenge Rating.

**<span id="dex"></span> DEX**

This is the character's DEX modifier.

**<span id="dexscore"></span> DEXSCORE**

This is the character's actual Dexterity score.

**<span id="ecl"></span> ECL**

This is the character's Effective Character Level. It is the sum of all
class levels plus any level adjustment the character might have.

**<span id="encumberance"></span> ENCUMBERANCE**

This is a value representing the character's current encumbrance level
(0=Light, 1=Medium, 2=Heavy, 3=Over-Loaded).

<span id="hands"></span> \*\*\* New 5.17.9

**HANDS**

This is the number of hands the character has.

<span id="hasdeity"></span> \*\*\* Updated 5.11.4

**HASDEITY:**

This returns 1 if the character has the named deity, otherwise 0.

**<span id="hasfeat"></span> HASFEAT:**

This returns 1 if the character has the named feat, otherwise 0.

**<span id="hd"></span> HD**

This is the character's HD (Starting HD or Monster HD. Not HD from
classes).

**<span id="hp"></span> HP**

This is the character's maximum total hit points.

**<span id="initiativemisc"></span> INITIATIVEMISC**

This is the character's adjustment to initiative excluding any dexterity
modifier.

**<span id="initiativemod"></span> INITIATIVEMOD**

This is the character's adjustment to initiative (including dexterity
modifier and +4 if you have the Improved Initiative feat).

**<span id="int"></span> INT**

This is the character's INT modifier.

**<span id="intscore"></span> INTSCORE**

This is the character's actual Intelligence score.

<span id="legs"></span> \*\*\* New 5.17.9

**LEGS**

This is the number of legs the character has.

**<span id="movebase"></span> MOVEBASE**

This is the character's racial-based movement.

<span id="racialhdsize"></span> \*\*\* New 6.02.01

**RACIALHDSIZE**

Returns the size of the hit dice type of the creatures racial hit dice
(i.e. 6 for d6, 8 for d8, 10 for d10), if any. For creatures with no
racial hit dice, RACIALHDSIZE returns 0.

**<span id="shieldaccheck"></span> SHIELDACCHECK**

This is the total AC Check penalty from shields.

**<span id="size"></span> SIZE**

This is a value representing the character's current size. Fine=0,
Diminutive=1, Tiny=2, Small=3, Medium=4, Large=5, Huge=6, Gargantuan=7,
Colossal=8. The size designations, including abbreviations, are
dependant upon the gamemode used and may be redefined in the
sizeadjustments.lst file.

**<span id="skillrank"></span> SKILLRANK=name**

This is the character's Ranks in the named skill replacing ( with { and
) with }. e.g. SKILLRANK=Craft {Woodworking} would return the ranks of
Craft (Woodworking) since ( and ) have other meanings in DEFINE
variables. If used within a JEP formula you will need to enclose it in a
variable function e.g. var("SKILLRANK=Craft {Woodworking}")

<span class="lststatus"> **Update:** </span>

This can now be done with the
[skillinfo()](/list/global/formulas.html#skillinfo) JEP function.

**<span id="skilltotal"></span> SKILLTOTAL=name**

This is the character's total in the named skill replacing ( with { and
) with }. e.g. SKILLTOTAL=Craft {Woodworking} would return the total of
Craft (Woodworking) since ( and ) have other meanings in DEFINE
variables. If used within a JEP formula you will need to enclose it in a
variable function e.g. var("SKILLTOTAL=Craft {Woodworking}")

<span class="lststatus"> **Update:** </span>

This can now be done with the
[skillinfo()](/list/global/formulas.html#skillinfo) JEP function.

**<span id="sr"></span> SR**

This is the character's spell resistance.

**<span id="str"></span> STR**

This is the character's STR modifier.

**<span id="strscore"></span> STRSCORE**

This is the character's actual Strength score.

**<span id="tl"></span> TL**

Total Level of character, this includes all PC, NPC and Monster class
levels. It does not include any level adjustments the character may have

**<span id="vardefined"></span> VARDEFINED:**

This returns 1 if the character has the named variable, otherwise 0.

**<span id="weightcarried"></span> WEIGHT.CARRIED**

is the weight of all carried equipment.

**<span id="weightequipped"></span> WEIGHT.EQUIPPED**

is the weight of all equipped items.

**<span id="weightpc"></span> WEIGHT.PC**

is the weight of the PC.

**<span id="weighttotal"></span> WEIGHT.TOTAL**

is the weight of all carried items and PC.

**<span id="wis"></span> WIS**

This is the character's WIS modifier.

**<span id="wisscore"></span> WISSCORE**

This is the character's actual Wisdom score.

------------------------------------------------------------------------

<span id="userdefinedvariables"></span> User-defined Variables in PCGen datasets
--------------------------------------------------------------------------------

**Note:** This is not a definitive list, but a subset showing some of
the common user defined variables that PCGen uses.

**<span id="allowextraturning"></span> AllowExtraTurning**

Ability to take Extra Turning if &gt;= 1

**<span id="allowholyavenger"></span> AllowHolyAvenger**

Ability to use a Holy Avenger as a Paladin if &gt;= 1

**<span id="bardicknowledge"></span> BardicKnowledge**

Ability to use Bardic Knowledge if &gt;= 1

**<span id="bardicmusic"></span> BardicMusic**

Ability to use Bardic Music if &gt;= 1

**<span id="turnundead"></span> TurnUndead**

Ability to Turn Undead if &gt;= 1

------------------------------------------------------------------------



