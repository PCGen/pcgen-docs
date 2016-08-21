+++
date = "2016-08-01"
title = "Lesson #2: PCC file calling"
original_url = "/list/lst-file-class/02-pcc.html"

[menu.main]
    identifier = "lst-file-class_02-pcc"
    name = "Lesson #2: PCC file calling"
    parent = "lst-file-class"
    
+++
By Professor Chris Chandler (Barak) and Professor Andrew McDougall (Tir
Gwaith).

**File(s) Covered:** \*.pcc (File calling)

**Tags used:**

`      DEITY          ,           DOMAIN          ,           SPELL          ,           RACE          ,           TEMPLATE          ,           FEAT          ,           SKILL          ,           LANGUAGE          ,           CLASS          ,           COMPANIONMOD          ,           KIT          ,           EQUIPMOD          ,           EQUIPMENT          ,           WEAPONPROF          ,           PCC          ,           INCLUDE          ,           EXCLUDE          , #`

------------------------------------------------------------------------

Basic File type calls
---------------------

Ok, this part is going to go fast. If you want to add an object (coding
term for how PCGen handles things), such as a Race, to your campaign, it
needs to be in the correct LST file type to load correctly. To do this,
you create that object in a LST file, and reference the file by one of
the tags. Valid file types are, and I'm grouping them by file types that
tend to go together (interact with others regularly in the same
grouping): DEITY, DOMAIN, SPELL, RACE, TEMPLATE, FEAT, SKILL, LANGUAGE,
CLASS, COMPANIONMOD, KIT, EQUIPMOD, EQUIPMENT, and WEAPONPROF

There can only be one of these tags per line, but one can have more than
one line with the same reference (we tend to break monsters and
equipment down into more than one file for official releases, so we
often will have more than one EQUIPMENT or RACE line in the same
campaign. All of these tags call LST files, each of which follow their
own format and tags that can be used in them. We will get to that later.

For example, one of the lines for my classes is
"CLASS:mystuffclassesbase.lst". Another one (entered on a new line) is
"CLASS:mystuffclassesprestige.lst". My feat file is
"FEAT:mystufffeats.lst".

Notice something about all the filenames I've chosen for the different
types of data? They all start with "mystuff". This is the common naming
convention and just makes it easy to determine at a glance what files
belong together with what PCC.

So now the PCC file looks like this (and is complete; we are building on
lesson \#1 here.):

> `-------------------------------            CAMPAIGN:My Stuff            GAMEMODE:3e            RANK:1            TYPE:PCGenLstMonkey.Campaign Setting.My World            SOURCELONG:PCGenLstMonkey SOURCESHORT:PCGLM            SOURCEWEB:http://www.mystuffcampaign.com            ISOGL:YES            COPYRIGHT:PCGenLstMonkey Copyright 2003            INFOTEXT:This data set contains all the information necessary to            create a character for the mystuff campaign world.            DEITY:mystuffdeities.lst            FEAT:mystufffeats.lst            TEMPLATE:mystufftemplates.lst            CLASS:mystuffclassesbase.lst            CLASS:mystuffclassesprestige.lst            DOMAIN:mystuffdomains.lst            LANGUAGE:mystufflanguages.lst            RACE:mystuffraces.lst            SKILL:mystuffskills.lst            SPELL:mystuffspells.lst            KIT:mystuffkits.lst            COMPANIONMOD:mystuffkits.lst            EQUIPMOD:mystuffequipmodsmundane.lst            EQUIPMOD:mystuffequipmodsmagical.lst            EQUIPMENT:mystuffequip.lst            WEAPONPROF:mystuffweaponprofs.lst            -------------------------------`

That is ALL you need to include in a Campaign file to have objects load,
so long as the files themselves exist and there isn't anything wrong
with the files themselves (bad LST format, weird character, etc.). Note
that you do not need all of those type. Several sources may only have
two or three of them.

What we are going to go into now is some slightly more advanced items
that will help with your custom datasets...

------------------------------------------------------------------------

PCC: calling other PCGen Campaign Configuration files.
------------------------------------------------------

Let's say I want to have everything in the SRD, but I don't want to
select the SRD every time on the sources screen. I and my players want
to just load MyCampaign. To do this I can use a PCC tag in the
mystuff.pcc. This works just like any of the other File Type loading
tags, but it will load EVERYTHING from a given PCC file.

So I can load the complete SRD and my own stuff and I could do it just
by clicking on MyCampaign and loading that. All the info in the SRD
would be included! More specifically, what is mentioned in the PCC I
call is loaded as if it were listed in the mystuff.pcc...

Since PCC's tend to be in the same folder as their files, and each
campaign in its own folder, I've held this one off till after the
calling from other directories, since you need that first. So, I need to
know where the PCC in question is. In this case, it is
(PCgenHome}/data/d20ogl/srd/srd.pcc. So I'm going to add
PCC:@/data/d20ogl/srd/srd.pcc

The "@" character when used in a PCC file will be replaced when the
program goes looking for the file by the path you have set in the
preferences as the PCGen home directory.

You may also load a PCC using the full path/filename (useful if you keep
your sources in places other than the normal PCGen path) such as
PCC:C:/pcgen/data/d20ogl/srd/srd.pcc.

------------------------------------------------------------------------

LSTEXCLUDE: removing a file completely.
---------------------------------------

I want to use the SRD materials but I have invented my own feats and
wish to use them and \*not\* have the ones from the SRD available. I can
use the LSTEXCLUDE tag to prevent them from being loaded. This tag will
prevent the named files from being loaded even if they are referenced in
another PCC that you have chosen to include. For this to work properly,
it must come before any PCC listings to take effect in them.

So, for mystuff.pcc I will insert "LSTEXCLUDE:srdfeats.lst" on a line
prior to my PCC call from the last section.

------------------------------------------------------------------------

INCLUDE/EXCLUDE: loading only parts of files
--------------------------------------------

Thinking about it some more I realize that I want to include a couple of
bits from some other data sets. While I could re-enter them, why go to
all that trouble. Looking through my stuff, I want to include the races
from FFG's Mythic Races... but looking at them, I don't particularly
like the Fairy race, nor the Anaema (that just sounds too close to
something else :P) and would like to leave them out.

This is what we use the EXCLUDE tag for.  So I enter another race tag
for that file, but on the end I put "|(EXCLUDE:Fairy|Anaema)". The
complete entry reads:

> `RACE:@/data/d20ogl/fantasyflightgames/legendsandlairs/mythicraces/mythicracesraces.lst| (EXCLUDE:Fairy|Anaema)`

On that same note, I really like the Hide Spell metamagic feat from
Sword and Sorcery Studios book Relics and Rituals, but I don't want to
include any of the other feats. To do this I'll use the INCLUDE tag. I
enter another feat tag, and at the end I put "|(INCLUDE:Hide Spell)".
The complete line would read:

> `FEAT:@/data/d20ogl/swordandsorcerystudios/scarredlands/relicsrituals/relicsritualsfeats.lst| (INCLUDE:Hide Spell)`

------------------------------------------------------------------------

\#: Comments
------------

Some PCC files can be complicated and might need some explanation for
how things are being done or you may just wish to use have some
reminders of how you've organized the file.  For that you enter a
comment. A comment is indicated by using the "\#" character as the first
character on the line, followed by any text you wish to enter for the
comment.

I think I'll just pop a note into the PCC indicating source material
that is not from my setting. "\# Non My Campaign setting files".

Our PCC file now looks like this:

> `-------------------------------            CAMPAIGN:My Stuff            GAMEMODE:3e            RANK:1            TYPE:PCGenLstMonkey.Campaign Setting.My World            SOURCELONG:PCGenLstMonkey SOURCESHORT:PCGLM            SOURCEWEB:http://www.mystuffcampaign.com            ISOGL:YES            COPYRIGHT:PCGenLstMonkey Copyright 2003            INFOTEXT:This data set contains all the information necessary to            create a character for the mystuff campaign world.            DEITY:mystuffdeities.lst            FEAT:mystufffeats.lst            TEMPLATE:mystufftemplates.lst            CLASS:mystuffclassesbase.lst            CLASS:mystuffclassesprestige.lst            DOMAIN:mystuffdomains.lst            LANGUAGE:mystufflanguages.lst            RACE:mystuffraces.lst            SKILL:mystuffskills.lst            SPELL:mystuffspells.lst            KIT:mystuffkits.lst            COMPANIONMOD:mystuffkits.lst            EQUIPMOD:mystuffequipmodsmundane.lst            EQUIPMOD:mystuffequipmodsmagical.lst            EQUIPMENT:mystuffequip.lst            WEAPONPROF:mystuffweaponprofs.lst            # Non My Campaign setting files            LSTEXCLUDE:srdfeats.lst            PCC:@/data/d20ogl/srd/srd.pcc            RACE:@/data/d20ogl/fantasyflightgames/legendsandlairs/mythicraces/myth            icracesraces.lst|(EXCLUDE:Fairy|Anaema)            FEAT:@/data/d20ogl/swordandsorcerystudios/scarredlands/relicsrituals/r            elicsritualsfeats.lst|(INCLUDE:Hide Spell)            -------------------------------`

Barak, Tir Gwaith\
 LST Chimps



