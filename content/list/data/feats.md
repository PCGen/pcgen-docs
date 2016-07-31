+++
date = "2016-08-01"
title = "Feat Files"
original_url = "/list/data/feats.html"

[menu.main]
    identifier = "data_feats"
    name = "Feat Files"
    parent = "data"
    
+++
-   6.05.04 (July 2015): JIRA
    [NEWTAG-477](http://jira.pcgen.org/browse/NEWTAG-477) / Github [PR
    \#380](https://github.com/PCGen/pcgen/pull/380)
-   -   The feat files described below is deprecated. [Use the Ability
        system
        instead](/list/data/ability.html) .
    -   To implement a feat, write an
        [ability](/list/data/ability.html)
        belonging to the `FEAT`[ability
        category](/list/data/abilitycategory.html)
        , i.e. `CATEGORY:FEAT` .
    -   The feats may still be contained in a file called `feats.lst`
        (see `/data/35e/wizards_of_the_coast/rsrd/basics/feats.lst` for
        an example.) However this file must use the [`ability.lst`
        format](/list/data/ability.html)
        , not the obsolete format described below.
    -   All `FEAT` tags have been **deprecated** and replaced by the
        `ABILITY` system, which is more general. The `ABILITY` system
        can model feats, racial features, class features, traits, flaws,
        temporary bonuses, and so on, all using a common format

------------------------------------------------------------------------

Each feat takes one line and the first field must be the feat's name.

------------------------------------------------------------------------

<span id="featbuilding"></span> Building Feats
----------------------------------------------

**Naming Feats**

When naming feats you should only use parentheses at the end of the name
if the name is not duplicated elsewhere. This is because of how PCGen
names feats which can be taken multiple times. For example, the Feat
Weapon Focus when taken will display as Weapon Focus(Dagger). Another
example is Armor Proficiency (Light), there is no feat named Armor
Proficiency so this name is fine. What is happening is when PCGen finds
a feat with parentheses that duplicates the name of another feat it
assumes that feat is an instance of the one without parentheses and does
not display the one with parentheses.

`Improved Critical`

The feat named "Improved Critical" is to be created.

`Acrobatic.MOD`

The feat named "Acrobatic" is to be modified.

`Occupation (Emergency Services).FORGET`

The feat named "Occupation (Emergency Services)" is to be forgotten.

When the `POINTPOOLNAME` trigger tag is present in the <span
class="lstfile"> miscinfo.lst </span> file, the **Summary Tab** Will
display total points/points remaining (i.e. Development Points 160/135)
on the same line as the stat total and stat mod total

Skills Tab - Instead of skill points by class/level requirement to spend
skill points, it's just a pool this is also populated by the classes
STARTSKILLPTS and miscinfo SKILLMULTIPLIER

Feats Tab - Will show total point pool as reported on the skills tab

------------------------------------------------------------------------

<span id="taglist"></span> Feat Tag List
----------------------------------------

