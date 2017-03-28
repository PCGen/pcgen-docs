+++
date = "2016-08-01"
title = "Abilities by Skill Ranks"
original_url = "/list/rules-guide/grig-abilities-by-skill_ranks.html"

[menu.main]
    identifier = "rules-guide_grig-abilities-by-skill_ranks"
    name = "Abilities by Skill Ranks"
    parent = "rules-guide"
    
+++
**Rule Description:** Abilities can be bought by taking ranks in the
appropriate skill.

**PCGen Version:** 5.12.1

**Gamemode/Dataset:** 35e/RSRD

**File(s) Covered:** <span class="lstfile"> statsandchecks.lst </span> ,
<span class="lstfile"> abilitycategory.lst </span> , <span
class="lstfile"> abilities.lst </span> , <span class="lstfile">
skills.lst </span>

**Tags used** (Stats and Checks File):

[DEFINE](/list/global/define.html)

**Tags used** (Ability Category File):

[ABILITYCATEGORY](/list/data/abilitycategory/abilitycategory.html) ,
[CATEGORY](/list/system/gamemode-miscinfo/category.html) ,
[PLURAL](/list/system/gamemode-miscinfo/plural.html) ,
[EDITABLE](/list/system/gamemode-miscinfo/editable.html) ,
[EDITPOOL](/list/system/gamemode-miscinfo/editpool.html) ,
[FRACTIONALPOOL](/list/system/gamemode-miscinfo/fractionalpool.html) ,
[POOL](/list/system/gamemode-miscinfo/pool.html) ,
[VISIBLE](/list/system/gamemode-miscinfo/visible.html)

**Tags used** (Skill File):

[TYPE](/list/global/type.html#skill) ,
[VISIBILE](/listfilepages/datafilestagpages/datafilesskill.html#visibile)
, [BONUS:ABILITYPOOL](/list/global/bonus/abilitypool.html)

**Tags used** (Ability File):

[CATEGORY](/list/data/ability/category2.html) ,
[TYPE](/list/global/type.html#feat) ,
[VISIBLE](/list/data/ability/visible.html) ,
[PREABILITY](/list/global/pre/preability.html) ,
[PRESKILL](/list/global/pre/preskill.html) ,
[PREVARLT](/list/global/pre/prevar.html) ,
[DESC](/list/global/other/desc.html) ,
[BONUS:VAR](/list/global/bonus/var.html)

**Tags used** (Class File):

[BONUS:ADD](/list/data/classes.html) (Note 2016-07-16: Class file "ADD"
tag no longer exists)

In this section we will discuss only those LST tags specific to this
implementation, and how they are used to implement the subject rule. For
more general information on the associated tags, please visit the [LST
File Tag Index](/navlistindex.html) section of the PCGen Documentation.

------------------------------------------------------------------------

Implementation Discussion
-------------------------

Implementing "Abilities by Skill Ranks" requires modifications to one
Gamemode file and four Data files. The gamemode file we need to modify
is the <span class="lstfile"> statsandchecks.lst </span> file where we
will be modifying the **Intelligence** stat. The data files include the
<span class="lstfile"> abilitycategory.lst </span> file where we will be
adding a new category of abilities called the "AbilitybySkills", the
<span class="lstfile"> skill.lst </span> file where we will be creating
a new skill called the "Skills to Abilities", the <span class="lstfile">
ability.lst </span> file where we will be creating three new abilities,
one to initialize the "Abilities by Skill Rank" mechanism for the
character, one to be purchased by skill ranks and one to increase the
maximum number of abilities that can be bought, and the <span
class="lstfile"> class.lst </span> file where we will demonstrate how
abilities are granted through the "Abilities by Skill Ranks" mechanism
at level-up. For the purposes of this implementation, we will call these
abilities <span class="lstobj"> Initialize Abilities by Skill </span> ,
<span class="lstobj"> Generic Skill Bought Ability </span> , and <span
class="lstobj"> Increasing Skill Bought Ability Max </span> .

The mechanics of this rule, as implemented on this page, work this way:

-   When the character is loaded, the <span class="lstvar">
    AbilitybySkillMax </span> variable is initialized and set to half of
    the characters total level.
-   Each rank taken in the skill named "Skills to Abilities" adds one
    point to the ability pool for the "AbilitybySkill" category
    of abilities.
-   "AbilitybySkill" abilities become available under the
    "AbilitybySkill" sub-tab on the feats tab.
-   The first such ability the character takes defines and initializes
    the <span class="lstvar"> AbilitybySkillCount </span> variable.
-   Subsequent AbilitybySkill abilities taken by the character increases
    the value of the variable, <span class="lstvar"> AbilitybySkillCount
    </span> , by one.
-   Once <span class="lstvar"> AbilitybySkillCount </span> equals or
    exceeds <span class="lstvar"> AbilitybySkillMax </span> ,
    AbilitybySkill abilities become unavailable until the character goes
    up a level, thereby increasing the <span class="lstvar">
    AbilitybySkillMax </span> variable.

We will discuss, below, each of the LST entries required, and the tags
that make them work, to implement "Abilities by Skill Rank". For
assistance in understanding how to read this page you may review the
[Rules Style Guide](/list/rules-guide/reading-instructions.html) .

------------------------------------------------------------------------

### Statsandchecks.lst File

Note: The <span class="lstfile"> statsandchecks.lst </span> file is a
gamemode file and as such is not referenced in the <span
class="lstfile"> \*.pcc </span> file. It can be found in the <span
class="lstfile"> pcgen/system/gamemodes/35e </span> directory.

The <span class="lstfile"> statsandchecks.lst </span> file entry
required in this implementation consists of the modification of an
existing entry. The following tag is added to the line defining the
intelligence stat:

> **Tag Used:** `DEFINE:AbilitybySkillMax|TL/2`
>
> **What it Does:** This tag is used to define the variable <span
> class="lstvar"> AbilitybySkillMax </span> to have a value of half the
> character's total level.

You will find the modified [Intellegence
Stat](/list/rules-guide/grig-abilities-by-skill_ranks.html#statsandschecks)
below.

------------------------------------------------------------------------

### AbilityCategory.lst File

The specific <span class="lstfile"> abilitycategory.lst </span> file
entry required to implement "Abilities by Skill Ranks" consists of the
definition of a single ability category called "AbilitybySkill". The
tags used to do this are explained below:

> **Tag Used:** `ABILITYCATEGORY:AbilitybySkill`
>
> **What it Does:** This creates a new ability category called
> "AbilitybySkill". This is what will show in the PCGen user interface,
> under the FEATs tab.

> **Tag Used:** `CATEGORY:AbilitybySkill`
>
> **What it Does:** This sets the new category's parent category as the
> same as the new category.

> **Tag Used:** `PLURAL:AbilitybySkills`
>
> **What it Does:** This establishes the pluralform of the ability
> category name. (Used primarily for Internatinalization.)

> **Tag Used:** `EDITABLE:YES`
>
> **What it Does:** This establishes that a user can select
> abilities in this category.

> **Tag Used:** `EDITPOOL:NO`
>
> **What it Does:** The pool for this category of ability cannot be
> modified by the user.

> **Tag Used:** `FRACTIONALPOOL:NO`
>
> **What it Does:** Restricts the ability pool for this category of
> ability to whole numbers only.

> **Tag Used:** `POOL:AbilitybySkillPool`
>
> **What it Does:** This establishes the base ability pool for
> AbilitybySkill equal to the value of the variable <span
> class="lstvar"> AbilitybySkillPool </span> . (See DEFINE tag below.)

> **Tag Used:** `DEFINE:AbilitybySkillPool|0`
>
> **What it Does:** This tag is used to define the variable <span
> class="lstvar"> AbilitybySkillPool </span> and initialize its value to
> zero.

> **Tag Used:** `VISIBLE:QUALIFY`
>
> **What it Does:** Makes this category of ability visible in the PCGen
> GUI only when the character puts points into the skill, thereby adding
> points to the ability pool.

You will find the completed
[AbilitybySkill](/list/rules-guide/grig-abilities-by-skill_ranks.html#miscinfo)
Ability Category Definition below.

------------------------------------------------------------------------

### Skills.lst File

Only one new entry is required in the <span class="lstfile"> skill.lst
</span> file. This is the new skill "Skills to Abilities". The purpose
of this skill is to add bonus points to the pool of available points for
the AbilitybySkill category of abilities, one for each skill rank taken.
The tags used to do this are explained below:

> **Tag Used:** `TYPE:NoStat`
>
> **What it Does:** This skill is assigned a type of "NoStat".

> **Tag Used:** `VISIBLE:DISPLAY`
>
> **What it Does:** This skill will only be visible in PCGen's graphical
> user interface (GUI). It will not appear on the Character sheet.

> **Tag Used:**
> `BONUS:ABILITYPOOL|AbilitybySkillPool|SKILL.Skills to Abilities.RANK`
>
> **What it Does:** Breaking down the tag we are saying to give a bonus
> to the ABILITYPOOL of the AbilitybySkill category for each skill rank
> placed in the skill.

You will find the completed [Skills to
Abilities](/list/rules-guide/grig-abilities-by-skill_ranks.html#skills)
below.

------------------------------------------------------------------------

### Ability.lst File

The specific entries in the <span class="lstfile"> ability.lst </span>
file will consist of one entry per line for each of the AbilitybySkill
abilities you wish. The first item on each line will be the name of the
particular ability being defined. We include below notes on the creation
of three abilities called "Generic Skill Bought Ability", "Increasing
Skill Bought Ability Max", and "Level Granted Skill Bought Ability".

#### Generic Skill Bought Ability {#generic-skill-bought-ability .indent0}

\[Explanation of this ability.\] The tags used to do this are explained
below:

> **Tag Used:** `CATEGORY:AbilitybySkill`
>
> **What it Does:** This places the "Generic Skill Bought Ability"
> ability into the AbilitybySkill category. (See <span class="lstfile">
> abilitycategory.lst </span> above.)

> **Tag Used:** `TYPE:AbilitybySkill.Movement`
>
> **What it Does:** Sets the TYPE for this ability to "AbilitybySkill"
> and "Movement".

> **Tag Used:** `VISIBLE:QUALIFY`
>
> **What it Does:** Allows the user to see this ability within the PCGen
> GUI when all prerequisites have been met.

> **Tag Used:**
> `!PREABILITY:1,CATEGORY=AbilitybySkill,Generic Skill Bought Ability`
>
> **What it Does:** Sets a prerequisite for the "Generic Skill Bought
> Ability" ability. Specifically, the character must not currently have
> the "Generic Skill Bought Ability" ability that has been defined as
> belonging to the AbilitybySkill category. An ability called "Ac Ba" of
> any other category will not disqualify the character from selecting
> this ability. (The inclusion of this tag is a temporary workaround as
> there is currently a bug with the ability object not respecting the
> default of MULT:NO.)

> **Tag Used:** `PRESKILL:1,Tumble=12`
>
> **What it Does:** Sets a prerequisite for the "Generic Skill Bought
> Ability" ability. Specifically, the character must have at least 12
> ranks in the **Tumble** skill in order to select this ability.

> **Tag Used:** `PREVARLT:AbilitybySkillCount,AbilitybySkillMax`
>
> **What it Does:** Sets a prerequisite for the "Generic Skill Bought
> Ability" ability. Specifically, the variable <span class="lstvar">
> AbilitybySkillCount </span> must be less than the variable <span
> class="lstvar"> AbilitybySkillMax </span> in order for the ability to
> be selected.

> **Tag Used:** `DEFINE:AbilitybySkillCount|0`
>
> **What it Does:** This tag is used to define the variable <span
> class="lstvar"> AbilitybySkillCount </span> and to initialize it to
> the value zero.

> **Tag Used:** `DESC:<appropriate description>`
>
> **What it Does:** This is where you type the text you want to appear
> with your chosen ability. This will be displayed on the character
> sheet UNLESS the ability is set to NO or DISPLAY. In that case you
> would skip this tag and may instead use SA: in it's place. That tag is
> discussed in another lesson.

> **Tag Used:** `BONUS:VAR|AbilitybySkillCount|1`
>
> **What it Does:** This bonus tag increases the value of the variable
> <span class="lstvar"> AbilitybySkillCount </span> by 1.

#### Increasing Skill Bought Ability Max {#increasing-skill-bought-ability-max .indent0}

\[Explanation of this ability.\] The tags used to do this are explained
below:

> **Tag Used:**
>
> **What it Does:**

You will find the completed [skill purchased
abilities](/list/rules-guide/grig-abilities-by-skill_ranks.html#ability)
below.

------------------------------------------------------------------------

### Class.lst File

\[Explanation of how this class grants an ability upon level-up. The
tags used to do this are explained below:

> **Tag Used:**
> `ADD:ABILITY|FEAT|AUTOMATIC|Initialize Abilities by Skill`
>
> **What it Does:**

> **Tag Used:**
> `ADD:ABILITY|AbilitybySkill|AUTOMATIC|TYPE=AbilitybySkill`
>
> **What it Does:**

You will find the modified
[""](/list/rules-guide/grig-abilities-by-skill_ranks.html#class) class
below.

------------------------------------------------------------------------

### Known Issues

None?

------------------------------------------------------------------------

### LST File Entry Examples

These LST objects are being presented as examples only and are not part
of any official PCGen dataset.

#### <span id="statsandschecks"></span> Stats and Checks Gamemode File Entry: {#stats-and-checks-gamemode-file-entry .indent1}

> `STATNAME:Intelligence`
>
> `ABB:INT`
>
> `STATMOD:floor(SCORE/2)-5`
>
> `DEFINE:MAXLEVELSTAT=INT|INTSCORE-10`
>
> `DEFINE:AbilitybySkillMax|0` (This tag is added to the existing
> entry.)
>
> `DEFINE:AbilitybySkillCount|0` (This tag is added to the existing
> entry.)
>
> `BONUS:VAR|AbilitybySkillMax|TL` (This tag is added to the existing
> entry.)
>
> `BONUS:LANG|BONUS|INT`
>
> `BONUS:MODSKILLPOINTS|NUMBER|INT`

#### <span id="abilitycategory"></span> AbilityCategory File Entry: {#abilitycategory-file-entry .indent1}

> `ABILITYCATEGORY:AbilitybySkill`
>
> `CATEGORY:AbilitybySkill`
>
> `PLURAL:AbilitybySkills`
>
> `EDITABLE:YES`
>
> `EDITPOOL:NO`
>
> `FRACTIONALPOOL:NO`
>
> `VISIBLE:QUALIFY`

#### <span id="skills"></span> Skills File Entry: {#skills-file-entry .indent1}

> `Skills to Abilities`
>
> `TYPE:None`
>
> `VISIBLE:DISPLAY`
>
> `BONUS:ABILITYPOOL|AbilitybySkill|SKILL.Skills to Abilities.RANK`

#### <span id="ability"></span> Ability File Entry: {#ability-file-entry .indent1}

> `Generic Skill Bought Ability`
>
> `CATEGORY:AbilitybySkill`
>
> `TYPE:AbilitybySkill.Movement`
>
> `VISIBLE:QUALIFY`
>
> `!PREABILITY:1,CATEGORY=AbilitybySkill,Generic Skill Bought Ability`
>
> `PRESKILL:1,Tumble=12`
>
> `PREVARLT:AbilitybySkillCount,AbilitybySkillMax`
>
> `DEFINE:AbilitybySkillCount|0`
>
> `DESC:<appropriate description>`
>
> `BONUS:VAR|AbilitybySkillCount|1`

#### <span id="class"></span> Class File Entry: {#class-file-entry .indent1}

> `CLASS:Generic Class`
>
> `CLASS:Generic Class`
>
> `CLASS:Generic Class`
>
> `1` \[ `ADD:ABILITY|FEAT|AUTOMATIC|Initialize Abilities by Skill` \]
> (Add this tag to an existing class)
>
> `2`
>
> `3`
>
> `4``ADD:ABILITY|AbilitybySkill|AUTOMATIC|TYPE=AbilitybySkill <tab> BONUS:VAR|AbilitybySkillMax|1`
> (Add these two tags to an existing class level lines)
>
> `5`
>
> `6`

------------------------------------------------------------------------



