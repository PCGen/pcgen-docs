+++
date = "2016-08-01"
title = "Modern System Reference Document help file"
original_url = "/source/modern/msrd.html"

[menu.main]
    identifier = "modern"
    name = "Modern System Reference Document help file"
    parent = "source"
    
+++
**Game Mode: Modern**

MSRD &gt; COMPLETE

**MSRD Basics**

**MSRD Arcana**

**MSRD Future**

**MSRD Menaces**

MSRD &gt; PARTIAL &gt; BASICS

**Modern - Basics**

**Modern - Creatures**

**Modern - FX**

MSRD &gt; PARTIAL &gt; ARCANA

**Arcana - Basics**

**Arcana - Creatures**

**Arcana - Psionics**

MSRD &gt; PARTIAL &gt; FUTURE

**Future - Basics**

**Future - Cybernetics**

**Future - Equipment**

**Future - Mecha**

**Future - Mutations**

**Future - Robots**

The Modern System Reference Document, or MSRD, contains the core rules
for the Modern d20 role playing game published by Wizards of the Coast
under the Open Gaming License and contains much of the material found in
the core book.

Loading the MSRD
----------------

To load the MSRD set you always have to load at least the Basics. You
have two options for that: you can load the complete MSRD Basics set,
which contains all the sets from the MSRD &gt; PARTIAL &gt; BASICS
section, or you can load just the partial Modern Basics set from that
section. Other than that you can mix and match the complete section sets
with the partial sets as you like, but you should not load a Complete
section set and any of the Partial sets from that very section at the
same time because it is basically loading the same data twice.

General Issues
--------------

**Wealth**

The Wealth system in the MSRD is not fully implemented within **PCGen**
, though it is fairly easy to work around the limitations. When adding
the first level of a base class you are prompted to choose the result of
your starting wealth roll which you will need to make manually. This
roll is added to any bonuses granted from your starting occupation
and/or feats which may effect Wealth and that is your Starting Wealth
Score. The starting Wealth Score and Current Wealth Score are displayed
on the Abilities Tab in the Special Abilities window and on the Special
Abilities Block of the OS. Your Current Wealth Score is displayed in the
lower right pane of the Class Tab as well as on the first page of the
OS. Since Wealth is fluid and can change based on circumstances within
the game a Temporary Bonus exists named Wealth Adjustment which allows
you to do exactly that. You will find this in the Temporary Bonus
Sub-Tab of the Inventory Tab under Templates. You can apply a modifier
from 10 to -10, if you need more or there is more than one adjustment to
make you can apply the Wealth Adjustment as many times as is needed.
Wealth Adjustment is applied to the Current Wealth Score and leaves the
Starting Wealth Score untouched.

Buying stuff. **PCGen** does not yet support the abstract wealth system
presented in the Modern rules. As a work around we use the COST
attribute to hold the Purchase DC of the item instead of its monetary
value. You should check the box marked 'Ignore Cost', consult the
Purchase DC of the item and your Current Wealth Score and make your
rolls manually.

\*\*\* Updated 5.9.5

**Action Points**

Action Points are now granted automatically by the class that provides
them. Modification of the Action Points is still done on the *Temporary
Bonus Sub-Tab* of the *Inventory Tab* . There are now two temporary
modifiers named **Used Action Points** and **Bonus Action Points** ,
which can be used to modify a character's Action Points.

The **Used Action Points** tracker is to be applied if you spend Action
Points. It records APs as spent and thus reduces the amount of available
ones. The **Bonus Action Points** tracker can be used, if you should get
Action Points from an unexpected source, like a GM handing out Bonus APs
or some House Rule of yours. Your remaining Action Points will then be
automatically calculated from the difference of gained and spent Action
Points. Both can be applied multiple times.

\*\*\* Updated 5.13.11

**Languages**

Unlike the fantasy game, Modern does not grant bonus languages based on
the characters Intelligence Mod, however up until version 5.13.11 this
rule was erronously implemented. This has been corrected and in addition
there is no longer a pop up selector to choose the charatcers native
language. Instead all characters are granted 1 bonus language which
represents the native language and can be chosen at any time from the
Language, Weapon Prof & SA window.

Classes
-------

**Smart Hero**

Because of limitations with the **PCGen** code the Smart Hero's
**Linguist** talent will not appear as a talent choice at first level.
If you want to select it at first level anyway, instead of selecting a
talent, close the *Feat Choice* window without making a selection, add
the necessary ranks in the Read/Write Language and Speak Language skills
on the *Skills tab* , and select **Linguist** as one of the feats on the
*Feats tab* .

Equipment
---------

**Firearms and Ammunition**

Ammunition is sold in bundles, the number of which depends on the type.
In **PCGen** you will find two versions of each ammo, one is a bundle in
which it is sold and one is a single projectile. The two versions are
identical accept for the name, the Buy DC listed is always for the
bundle, you can't buy single bullets. The single projectile version
exists for the convenience of being able to add an exact amount of these
items to the character sheet, they will appear on the sheet with check
boxes handy for tracking spent ammo. You can also load bullets into
firearms in the Equipping Tab and checkboxes will appear under the
firearms listing in the main Equipment Block.

**Weapon Accessories**

Some weapon accessories only make sense when attached to a weapon. For
that matter the *Illuminator* , *Laser Sight* , *Standard Scope* ,
*Electro-optical Scope* , *Speed Loader* , and *Suppressor* were not
included as equipment in **PCGen** , but as equipment modifiers. To use
one of these items you have to select the weapon you want to apply the
item to and customize it. To do so, right-click the weapon and select "
*Create custom item* " in the menu. This will open the " *Item
Customizer* ", where you can select the modifiers you want to attach to
your weapon.



