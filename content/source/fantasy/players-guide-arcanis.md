+++
date = "2016-08-01"
title = "Paradigm Concepts: Player's Guide to Arcanis for PCGen help file"
original_url = "/source/fantasy/players-guide-arcanis.html"

[menu.main]
    identifier = "fantasy_players-guide-arcanis"
    name = "Paradigm Concepts: Player's Guide to Arcanis for PCGen help file"
    parent = "fantasy"
    
+++
**Game Mode: 35e**

ALPHA DATASETS

**PCI - Player's Guide to Arcanis**

**<span class="alpha"> Warning </span>** : This is a campaign dataset,
in addition to loading data specific to Arcanis this set loads the parts
of the RSRD set used in an Arcanis campaign. You should not load the
RSRD complete set nor should you load the Basics, Advanced or Psionics
Partial sets with the Player's Guide to Arcanis set or you will likely
encounter problems. The Monster, Epic and Divine Partial sets are not
loaded by this set and are probably safe to load in conjunction with the
Player's Guide to Arcanis.

**Character Creation** {#character-creation .indent1}
----------------------

**Making A Point Buy System in PCGen for playing Living Arcanis.**

If you don't have a point buy method set up yet, do the following:

1.Go to Settings --&gt; Preferences on the PCGen menu bar\
 2.On the screen that comes up (Character Stats), make the radio button
for purchase mode is selected.\
 3.Click the "Purchase Mode Configuration..." button\
 4.Adjust the "Purchase Score Min" and "Purchase Score Max" values using
the + and - buttons to be 8 and 18 respectively.\
 5.Click in each box under the "Cost" column and adjust each ability
score accordingly (8 should be 0, 9 should be 1, 10 should be 2, etc.
just remember that the cost in each box is cumulative.\
 6.Click the "New" button.\
 7.Type a name you will remember (I used Living Arcanis) then put 32 in
the "points" box.\
 8.Click okay.\
 9.Click Okay again\
 10.Close out of the setup dialog box.

### **Race** {#race .indent1}

When you select your race, when you go to do another function, it will
prompt you for several items. If you selected a race with a sub-race
(Dwarf, Elorii, Val) it will prompt you to select your sub-race first,
then your region and sub-region. If you selected a race without
sub-races, you will be prompted for your region and sub-region only.

**A Special Note on Vals**

Your Bloodranks are done through templates. To select your first
bloodrank, go to the Race tab. In the templates sub-tab, select "First
Bloodrank". After selecting it, you will be prompted for your bloodline
power selection. If you want to have more bloodranks at the beginning,
select Second Bloodrank, and Third Bloodrank (if you are going that
high). If you are using point buy, just make sure that when you are
buying your attributes, you only spend the appropriate number of points.
(only spend 24 if you are buying a second bloodrank, 20 if you are
buying 3 bloodranks). The program will prompt you to say that you
haven't spent all your points. It will allow you to continue even if you
didn't spend all your attribute points. Be careful, the program will let
you spend more points than you are allowed.

### **Deity** {#deity .indent1}

Make sure you select a Deity before adding any class levels, feats,
skills, etc., whether your class depends on worshipping a specific deity
or not. You never know when a class feature might rely on what deity you
are worshipping or when a class won’t allow you to select it if you do
not worship a specific deity.

### Regions and Sub-regions {#regions-and-sub-regions .indent1}

Currently the only regions listed are those from the Player’s Guide.

Known Issues {#known-issues .indent1}
------------

### Classes {#classes .indent1}

**Clerics**\
 The Clerics of various deities are handled by subclasses. However,
despite attempts to make it so, the program does not limit you to
choosing a particular deity. So be good and choose the correct deity for
the cleric you create.

**Cleric of Larissa**\
 The program will not force you to choose either the Pleasure or
Divination domains. You will have to do that yourself. Making the
program assign one actually assigns them both which causes other issues.
This is something that will hopefully be fixed in future versions of
PCGen.

**Holy Judge of Nier**\
 When you reach 20th level, you will have to adjust the HP manually to
their max level.\
 On the Summary tab, click the HP button and adjust the HP to equal 200
+ (20 x your CON bonus)

**Paladin of Sarish**\
 Sarishan Steel Weapon: You will have to custom make and add the weapon
to your equipment ignoring cost on your own. Be advised, this is only
possible if you have the LARC loaded. Sarishan Steel is not in the
PgtA.\
 To create the custom item, go to the Inventory tab, and the Gear sub
tab. Find the weapon you want. Right click it and choose "Create
Custom". Select Sarishan Steel from the options that show up and click
the "ADD" button. Click okay. Put a check mark in the box in the lower
right corner that says "Ignore Cost". Highlight the custom item and
click the "&gt;" button at the top to move it over to the right hand
panel. Congratulations! You are the proud owner of a Sarishan Steel
weapon.

### Prestige Classes {#prestige-classes .indent1}

**Gladiator**\
 Andabatae Style: Due to limitations in the program, the Andabatae has
to be it's own class. The rest are subclasses of the Gladiator subclass.
So just make sure you know which one you are going for ahead of time.

Samnite style: The two Weapon Focus and Specialization feats you gain
from this style are coded in, however, due to a bug in the program, only
the Short Sword Focus and Specialization feat will show up in the
display. But if you print a character sheet, both feats will show on
there and it will be factored into both weapons properly. If you are
using 5.8 or later, this may already be fixed.

**Obsidian Sniper**\
 At 9th level, the program gives you Improved Critical (Shortbow) and
Superior Critical (Shortbow). Enhanced Critical is not an actual feat
and was printed in the PGtA erroneously.

**Onaran Templar**\
 As of right now, the domain spells are not being added to the PCs known
spells automatically. Once you have attained fourth level you will have
to double click on the domain spells to add them to your known spell
list.\
 The War domain is automatically added at 4th level, however, due to a
bug in the PCGen code, the feats from it are not added automatically.
You have to go to the Domains tab and deselect the domain by
highlighting it and pressing the Select button, then reselecting it by
highlighting it and pressing select. This is slated to be fixed for
PCGen 5.8.

**Weapon Savant**\
 When you achieve the second level of the class, you get to finesse all
your weapons. However, if you were to take Weapon Finesse afterwards (or
before) you would get double your Dex bonus. Be good and don’t do this.

### Feats {#feats .indent1}

**Sabbatical**\
 Due to program limitations, you will have to manually add the Skill
points to use from this feat. Under the Skills tab, type the new
appropriate skill total in the TOTAL SKILL POINTS LEFT box.

### Equipment {#equipment .indent1}

**Lorica, Andrean Plate and Milandisian Cuirass**

Due to inherent limitations in the PCGen code, each of these is two
separate armors. If you are not proficient with the armor, use the
regular version. If you are proficient with it, use the (Proficient)
version. If necessary, change the SELL PERCENTAGE drop down box under
the gear tab to sell back at 100 percent, sell it, then "repurchase" the
proficient armor. Make sure to remember to set the SELL PERCENTAGE drop
down back to 50 when you are done.



