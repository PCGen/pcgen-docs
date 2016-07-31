+++
date = "2016-08-01"
title = "Official Release LST standards"
original_url = "/list/lst-standards.html"

[menu.main]
    identifier = "list_lst-standards"
    name = "Official Release LST standards"
    parent = "list"
    
+++
Guidelines for Official Release source submissions.

Please put \[SUBMIT\] in the subject line when emailing the team with
submissions issues.

**RULE 1**: Be true to the Source Product (i.e. do not make any judgment
calls). If the source doesn't say it, it doesn't go in. It is better to
leave incorrect or unclear information out.

**RULE 2**: Leave any calls about gray areas to the PCGen Submission
Team member.

**RULE 3**: Mechanics are NOT to be described. If the final result can
be displayed, that is good, but no describing the mechanics behind it on
the character sheet.

**RULE 4:** Capitalization:

-   HARDCODE = ALLCAPS.
-   Defined in List files (GameMode or otherwise) = ProperCase.

**Example:**\
`BONUS:COMBAT|AC|5|TYPE=MyType`

BONUS, COMBAT, AC, and TYPE= are all hardcoded. MyType is defined in the
List file (because it just got added!)

**Example:**\
`VISIBLE:YES, VISIBLE:NO, VISIBLE:DISPLAY, VISIBLE:EXPORT`

YES, NO, DISPLAY, and EXPORT are the only valid values of the VISIBLE
tag.  Since those values and what they do are hardcoded into PCGen, they
are done in ALLCAPS in the data files.

Basics:
-------

1.  Plain TEXT file, with a .LST ending for data files, or .PCC for
    campaign files, instead of .txt\
     Use Text editors, such as Wordpad (notepad sometimes has problems
    with the length of the lines), UltraEdit, Textpad, vi, or ee.\
     Microsoft Word has problems with formatting and layout of text, it
    is not recommended to be used to create files.\
     Some LST Monkeys use Excel, and export to a tab delimitated file,
    which works.

2.  Tabs between objects. No spaces before or after those tabs. Tab
    should NEVER be the first character on a line.

3.  Make sure the first character is either a \# (for comment) or a name
    of the object being defined such as a TAG.\
     Tabs and spaces are hard to see, and cause loading issues.

4.  Set your text editor to 6 spaces per tab, as that is the standard
    for columnizing the files.

5.  Comments on ANYTHING you are unsure about, or haven't been able to
    implement correctly.\
     Comments are always done on their own line, and start with \#.\
    -   If you have a suggestion on how to do something, but not totally
        sure, include that.
    -   If you have a suggestion on how to do something that would
        require some code changes, comment on that.\

6.  Comment line at top of LST files: \# Original Entry by: &lt;your
    name&gt;.\
     You want credit for the hard work you've done, right?

OGL Compliance {#ogl-compliance name="ogl"}
--------------

The Open Game License (OGL) is a royalty free copyright license
developed by Wizards of the Coast. The OGL has revitalized the RPG
industry by creating a way for third party publishers to easily create
and publish material they might not otherwise be free to. Publishers use
the OGL to release Open Game Content (OGC) which can be used by other
publishers seeking publish content based on the original publishers
work. Open Game Content is any material that is distributed using the
Open Game License clearly identified by the publisher as Open Game
Content.

You can read the OGL [here in our
documentation](/credits/ogl-license.html) or here at [Wizards of the
Coast's web site](http://www.wizards.com/default.asp?x=d20/welcome)
which contains additional information about the OGL.

PCGen publishes its data via the OGL. As an OGL publisher we have to
insure that the data we publish complies in all respects with the Open
Game License. All data is reviewed for OGL Compliance before being
entered into the project data files.

At this time we only publish Open Game Content. Though not required by
the OGL, PCGen also seeks permission from publishers before including
their data in our releases.

OGC vs. Product Identity:
-------------------------

**OGC**: For OGL sources, OGC is declared somewhere in the book. It is
usually on the title/copyright page (front of book) or the OGL page
(usually in the very back). Including that declaration in a separate
file with your submission will greatly speed its inclusion into PCGen,
since it will give us a quick way of verifying Product Identity to
ensure compliance with the OGL on our part.

**Product Identity**: For names of objects, use the NAMEISPI:YES tag in
your submission. For a first submission, please do not include any other
Product Identity unless you have discussed it with a PCGen Submission
Team member. If you receive a go ahead, follow the restrictions set by
it down to the letter.

Other Topics:
-------------

### Copyright (in PCC)

1.  ONLY and EXACTLY what is in the Sec. 15 of the OGL. **VERBATIM**.\
     If there are Typos, leave them in.  Weird characters, leave them
    in.  Stupid comments, leave them in.\
     Including a scanned page from the book with your submission would
    be nice but not completely necessary.

2.  List each source mentioned in the Section 15 in its own COPYRIGHT
    tag line - see Cityscape files (by Battlefield Press) for a
    superb example.

### General Object Naming Standards

These are general rules for the naming of classes, feats, races and
other objects.

Characters approved for use in object names are: upper and lower case
letters, numbers, single spaces in between multiple words (never before
or after) and the following glyphs: underscore (\_), dash (-),
apostrophe ('), parentheses (), slash (/), and a tilde (\~).

Characters which should never be used in object names are Commas (,),
Pipes (|), Backslashes (\\), Colons (:), Semicolons (;), Periods (.),
Brackets (\[\]), Percent (%), Asterisk (\*) and Equals (=).

Two words separated by a dash should both be capitalized.

If the name of the object must be different from the source (due to
commas or math symbols in the name or other reasons), an OUTPUTNAME: tag
with the EXACT name must be included.

Potions should be listed as Potion (&lt;name&gt;) with OUTPUTNAME:Potion
of \[NAME\] unless the source lists it as otherwise (see part 1 for
rules to follow in that case). Poisons, Rods, Staffs, Wands and same way
as Potions.

Within these limits the name should be as close as possible to the
published source.

### Additional Restrictions

No object may be named a valid number (even 0x45 or 1e20 could be a
problem) as items with optional count can fail.

No object may be called "ANY" or "ALL" or "LIST".

No Class may be called "HIGHESTLEVELCLASS".

No Equipment may be called "Total".

No Weaponprof may be called "DEITYWEAPON".

No equipment (or eqmod ITYPE) may use the types "ADD" or "REMOVE".

### General EQMOD Naming Standards

EQMOD keys are to be in all capital letters and may only contain
letters, numbers and underscores ("\_").

Each word should be separated by an underscore character for ease in
reading.

For purposes of abbreviation the letter limit on the first and second
sections of the Key name is 8 and 7.

EQMODs for different item types (Weapon vs. Armor for example) will be
done as separate EQMODs.

Materials which list different pricing for different item types or sub
types (Light Armor vs. Medium Armor for example) will be done as
separate EQMODs for each price type.

### File names

LST file names for PCGen follow a certain naming conventions. You should
use all lowercase letters in the file name. The first part of any file
will be a short version of the source name, for example if the source is
named 'The Foo Handbook' we can shorten it to foohandbook or even fhb.
The source name will be followed by words indicating what type of
objects the file contains. These words are separated an underscore (\_)
symbol. Using our example here are some names for a typical source.
These are not required but it does help to quickly identify the contents
of the file. This list is incomplete but should give you a good idea of
how you should name your files as well as how you should divide up the
contents of your dataset. Take a look at other sources that come with
PCGen for more examples.

`fhb.pcc` - loads all the LST files

`fhb_classes_base.lst` - Contains base classes

`fhb_classes_prestige.lst` - Contains prestige classes

`fhb_companionmods.lst` - Contains companion mods

`fhb_deities.lst` - Contains deities

`fhb_domains.lst` - Contains domains

`fhb_equip.lst` - Contains general equipment

`fhb_equipmods.lst` - Contains equipment mods

`fhb_feats.lst` - Contains feats

`fhb_feats_hidden.lst` - Contains hidden feats

`fhb_equip_armorshields.lst` - Contains armor and shields

`fhb_equip_armorshields_specific.lst` - Contains specific kinds of armor
and shields, magical, extraordinary, etc..

`fhb_equip_equip_weap_melee.lst` - Contains melee weapons

`fhb_equip_equip_weap_ranged.lst` - Contains ranged weapons

`fhb_equip_wondrousitems.lst` - Contains wondrous items

### SOURCELONG, SOURCESHORT, SOURCEWEB, SOURCEPAGE

SOURCELONG, SOURCESHORT, and SOURCEWEB are defined in both the PCC and
the top of the LST files. These can be easily be changed by the
submission team, so do not feel bad if they are. **Note:** Prior to
version 5.10 SOURCE header tags were grouped in a single block separated
with pipe (|) symbols. This has been changed to allow for easier
parsing, SOURCE header tags should still be put on one line at the top
of the file but should be separated by tabs instead of pipes.

Formats should be as follows:

-   **SOURCELONG**:&lt;name of publisher&gt; - \[&lt;name of product
    group, if any&gt; - \] &lt;name of product

-   **SOURCESHORT**:&lt;10 letter or less abbreviation of the name of
    the product&gt;\
     Leave the first name of the product whole, if possible.

-   **SOURCEWEB**:http://&lt;web address of publisher, or product group
    if the publisher has a page for that&gt;

-   **SOURCEPAGE** is done on object lines.\
     Use the first page the object is described (so if a class is
    defined on pages 51-54, the tag would read SOURCEPAGE:p.51)\
     Format should be SOURCEPAGE:p.\#

### <span id="STDSPELLNAME"></span>Standard Spellbook Names

Spellbook names for the `SPELLS` tags are used to identify the source of
a Spell Like Ability (SLA). The Spellbook is the first variable in the
SPELLS tag, in the following example "innate" is the name of the
spellbook.

`SPELLS:Innate|TIMES=5|TIMEUNIT=Week|Wall of Stone`

Using the word "Class" or "Race" alone as a spellbook name creates a
problem within PCGen. The standard convention is to use one of three
spellbook names to indicate the origin of the spell-like ability.

1.  **Innate** - For racial and template acquired SLA's\
     If it comes from a race, the race name (Gnome, etc)\
    \
2.  **Class Ability** - For SLA's derived from classes.\
     If it comes from a class, the class name (Sentinel, Paladin, etc)\
    \
3.  **Magic Item** - For SLA's provided by equipment.\
     If it comes from an magic item, the item name (Belt of Magic
    Spells, etc)\
    \

### SAB (formerly SA)

1.  Name ONLY

2.  Type of Special ability in Parentheses only if mentioned in
    Source: (Ex) (Su) (Sp) etc. If not mentioned, don't put one.

3.  If there is a Dynamic formula, and the formula can be calculated, it
    can be included, but no Formulas described.\
     See Monk Stun, and Dragon SA's. If it has a static range (like 10'
    no matter what) then that should not be listed.\
     The user will need to own the source in that case. The dynamic
    formulas should be done via DEFINE/BONUS:VAR tags.

### DESC (Feats, Spells, Deities, Domains)

1.  Check for Open Game Content.  If the DESC (see below for what to
    look for) is not OGC, leave as DESC:See text.

2.  If OGC, for Feats: Use only a 1 line description w/o mechanics. This
    is best by grabbing the "flavor" line after the feat name but before
    the "Benefits" or mechanics portion of the feat. This is usually
    before any prerequisites are listed.

3.  If OGC, for Spells: Use only a 1 line description that comes with
    the class spell lists. Some sources have a purely descriptive
    element for the Spells that are NOT OGC. Consulting with the
    publisher (and getting permission for the IP/PI) is for the PCGen
    Submissions Team. Please leave those with See Text, and when
    submitting the files, include a file with comments such as this, so
    we know where we stand, and can progress with acquiring permission
    for the PI or leaving it.

4.  If permission is granted for closed content PI by the publisher
    (submission team will inform you if so), then the DESC can be filled
    in with the same rules as above, but a DESCISPI:YES tag must also
    be added.

### DEFINE/BONUS:VAR and Variable Naming Standards

These two tags are used to track variables across different objects.

1.  Variables syntax should start with a letter and should be composed
    of only letters, \_ and numbers (no spaces). The standard Convention
    is to use only letters, capitalizing individual words
    for readability.

2.  Full words where possible (no over compressing to the point where it
    isn't readily understandable to what you are referring to).

3.  Please use formulas where possible. Such as CL=Name in for
    class abilities. 1 Bonus statement with a formula is processed
    faster than a BONUS statement on ever class line.

4.  Where it is possible to do so there should be only one DEFINE
    statement per variable and the DEFINE should be set at 0 with a
    BONUS:VAR used to adjust the value.

5.  Variable names in all capitals are reserved for hard coded variables
    or variables defined within the system files.

6.  Where it is possible to do so variables should be DEFINEd within the
    parent object where it is first used or encountered.

It is good practice to leave comments within the data sets LST code
explaining what variables have been used in the set, what their purpose
is and how they are to be used.

### DR / Damage Reduction

This tag is used to track Damage Reduction. Recent Code enchantments
compare different DRs, and list only the highest per type. This requires
some standardization in how DR is coded up, to ensure items are being
compared properly.

1.  Types of DR (after the /) are in Proper Case.

2.  Numerical DR, as used in 3.0 format is +\#

3.  DR that has no bypass is listed as -

4.  Several Key names are used across the datasets.
    -   +1, +2, +3, +4, +5
    -   Silver, Adamantine, Cold Iron
    -   Magic, Epic
    -   Lawful, Chaotic, Good, Evil
    -   Bludgeoning, Piercing, Slashing, Ballistic

5.  Use ' and ' and ' or ' between types in the same DR tag.
    -   Bludgeoning or Piercing
    -   Magic and Silver
    -   Epic and Evil
    -   Good or Silver
    -   Cold Iron or Good
    -   Lawful or Good
    -   Bludgeoning and Magic

[![Valid HTML 4.01
Strict](../images/system/valid-html401.png)](http://validator.w3.org/check?uri=referer)

