+++
date = "2016-08-01"
title = "Modern System Reference Document - Future section help file"
original_url = "/source/modern/msrd-future.html"

[menu.main]
    identifier = "modern_msrd-future"
    name = "Modern System Reference Document - Future section help file"
    parent = "modern"
    
+++
**Game Mode: Modern**

MSRD &gt; COMPLETE

**MSRD - Future**

MSRD &gt; PARTIAL

**Future - Basics**

**Future - Cybernetics**

**Future - Equipment**

**Future - Mecha**

**Future - Mutations**

**Future - Robots**

To run this you also need to load one of these:

**MSRD &gt; COMPLETE &gt; MSRD - Basics**

**MSRD &gt; PARTIAL &gt; BASICS &gt; Modern - Basics**

The Future section of the Modern System Reference Document, or MSRD,
contains the Future rules for the Modern d20 role playing game published
by Wizards of the Coast under the Open Gaming License and contains much
of the material found in the Future supplement.

Loading the MSRD Future parts
-----------------------------

To load the MSRD Future set you also need to load the MSRD Basics. You
have two options to accomplish this, either you can load the Complete
MSRD - Basics set (including FX and Creatures material) or you can load
the Partial Modern - Basics set and maybe add some of the other Partial
Modern sets to that. To that selection you either add the Complete MSRD
- Future set or only those parts of the MSRD Future section you desire
to use. You should not load a Complete section set and any of the
Partial sets from that very section at the same time because it is
basically loading the same data twice. The partial Future - Basics set
contains almost all classes, feats, and occupations, the partial Future
- Equipment set includes personal gear, starships, and vehicles, the
other names should be self-explanatory.

Future - Basics
===============

Classes
-------

**Astronaut Trainee, Engineer, Explorer, Space Monkey and Tracer**

All these classes offer the feat Aircraft Operation as one of their
possible Bonus Feats, but limit that feat to the selection of
*Spacecraft* if taken as a Bonus Feat. Since PCGen cannot limit this
selection at the time, you will have to make sure to take heed of this
restriction on your own.

Feats
-----

**PLUS Feats**

The feats *Charismatic Plus* , *Dedicated Plus* , *Fast Plus* , *Smart
Plus* , *Strong Plus* , and *Tough Plus* will grant you a selection of
two additional talents from the given class, but require that you cannot
select more than one talent from a single talent tree. Currently it is
not feasible within **PCGen** to limit the selection of talents granted
by these feats. It will therefore be necessary for you to make sure to
comply with these limits when making your selection.

Future - Equipment
==================

Purchase DCs
------------

For most items the *Purchase DC* will be shown in the Cost field, but we
have a problem with the *Purchase DC* s of items that get applied to a
piece of equipment (anything that only shows in the window that pops up
when you customize a piece of equipment) if it doesn't add to the base
item's *Purchase DC* but calls for an additional *Wealth check* . In
these cases the *Purchase DC* cannot be added to the base item and will
not show up at all in **PCGen** . It would have been possible to list
the additional *Purchase DCs* in the special properties of the item it
gets applied to, but many of these (especially starships) are already
quite filled with different informations, so we decided against that.
Please look up these *Purchase DC* s in the ***Future*** section of the
**MSRD** .

Gadgets
-------

**Alternate Weapon Gadget**

It is not really possible to code this gadget with the current
limitations of **PCGen** . You can apply this equipment modifier to a
weapon by creating a custom item, but all it will do is put the name of
the linked alternate weapon into the weapon's special properties. You
still have to buy the alternate weapon (you'd have to pay for it anyway)
and equip it as carried. Because there is no real link between the two
weapons, it is currently not possible to have both of them equipped to
the same hand or let them take up 1 space in a container.

**Autoloader Module Gadget**

The Autoloader Module Gadget is only allowed to be equipped to weapons
that have box magazines or power packs for ammo feed. At this time we
cannot test for the ammo feed of a weapon, you will therefore have to
pay attention to this detail on your own, when applying this gadget.

**Booby Trapped Gadget**

To be eligible to add this gadget to your weapon, you **must** apply the
*Alternate Weapon Gadget* first.

**Satellite Datalink Gadget**

This Gadget should be restricted to being applied to *gear containing
computerized communications equipment* , but it is currently set up to
allow items that have the types electronic and surveillance applied to
them. While this mostly covers the items of the wanted category, there
are a few items included that don't make much sense for this gadget, so
take heed at what item you add this gadget to.

**Storage Compartment Gadget**

All this gadget will currently do is to show up in the item name. At
this time we cannot change a piece of equipment into a container
afterwards. **You will not gain any functionality from this!**

Starships
---------

You put a starship on the vehicle slot of your character. Only when
applied there, you will see all the bonuses and effects that pertain to
your starship. At the time you equip the starship to the vehicle slot,
you may also get additional equipment granted to your character (e.g.
the starship's weapons). Every piece of starship equipment gained this
way should be equipped to *not carried* .

Starship Weapons
----------------

To add weapons to a starship you customize said starship and add those
equipment modifiers to it, which provide the wanted weapon. When you
equip your customized starship to the *Vehicle* slot of your character,
these equipment modifiers will automatically add the starship weapons to
your character (like personal weapons), but they will be unequipped and
you should equip them to *not carried* as location. This will only work
with the existing weapons that come from the sample starships in the
MSRD Future. If you want to have weapons in your starship that were
customized themselves, you can build and add these to your character,
but there is no way to have them show up as part of your starship. As a
workaround, you can hand edit the special properties of your starship
and put in a reference to the weapon there.

**Fire-linked Weapons**

At this time we are not capable of supplying you with an equipment
modifier for *fire-linked weapons* , therefore you will not be able to
simply customize a single starship weapon into groups of *fire-linked
weapons* . You will therefore be limited to those *fire-linked weapons*
that are included in the dataset.

Future - Mecha
==============

Purchase DCs
------------

The problems about *Purchase DC* described under Equipment pertain here
as well. *Purchase DC* s of items that get applied to a piece of
equipment or **Mecha** (anything that only shows in the window that pops
up when you customize a piece of equipment or **Mecha** ) if it doesn't
add to the base item's *Purchase DC* but calls for an additional *Wealth
check* cannot be added to the base item and will not show up at all in
**PCGen** . It would have been possible to list the additional *Purchase
DCs* in the special properties of the item or **Mecha** it gets applied
to, but many of these are already quite filled with different
informations, so we decided against that. Please look up these *Purchase
DC* s in the ***Future*** section of the **MSRD** .

Equipment Slots
---------------

Most equipment that gets applied to a **Mecha** needs to go to a
predetermined equipment slot. With the current **PCGen** code
limitations it is not possible to do that. You will find the information
which slot a piece of equipment may go to in the special properties, so
you can check the correctness, but there is no way to enforce this. If
you build a custom **Mecha** , you should do this outside of **PCGen**
and then customize the basic **Mecha** entries according to the built up
that you already determined. **PCGen** is not the proper tool to do that
planning, it will just allow to to record your results.

Equipping Mecha Weapons
-----------------------

There are two ways to equip a weapon to a **Mecha** : *hand held* or
*built-in* . To equip a weapon *hand held* to a **Mecha** , you just buy
the weapon and equip it to your character. To equip a *built-in* weapon
to a **Mecha** , you need to customize the **Mecha** and add the
*equipment modifier* to it, that corresponds with the chosen weapon. The
*equipment modifier* will then add the weapon itself to your character,
which you should equip as *not carried* . If you remove the **Mecha**
from your equipment later, that will not automatically remove the
**Mecha** weapons as well, so you will be required to remove those
yourself.

Piloting a Mecha
----------------

If you look at the rules for **Mecha** , you will see that these are
more of a hybrid game element, being so constituted that they include
elements from equipment as well as creature templates. To effectively
reproduce this in **PCGen** , you will have to add not only the chosen
**Mecha** from the *Equipment* tab, but also the **Mecha Pilot**
template from the *Templates* subtab on the *Race* tab. Without that
template, the **Mecha** is not going to work correctly.

The Paragon Mecha
-----------------

The *Paragon* **Mecha** should be getting the *Missile pack for M-87
Talon Missile Launcher (4)* and the *Rocket pack for M-70 EMP Rocket
Launcher (6)* twice, but the *AUTO:EQUIP* tag doesn't work well with
equipping the same item twice. You need to add the second pieces of
these equipment packs manually.

Future - Robots
===============

Building Robots
---------------

There are two sets of Robot races, one is meant for heroic characters
run by Players, the other is meant for non-heroic characters. The races
4 named **Biodroid (Medium** and **Small)** and **Bioreplica (Medium**
and **Small)** are Player races and gain feats and skills when PC
classes are gained as normal. The races whose names are formatted
**Robot(Type/Size)** are all non-heroic, they do not gain feats or skill
points as long as they are advanced in the **Robot** monster class, if
given levels of an *Ordinary* base class they will not gain feats
(unless equipped with a *Feat Web* ) but they will gain skill points,
these should be discarded unless the Robot is equipped with a *Skill
Web* .

Purchase DCs
------------

The purchase DC for a Robot is calculated and displayed in the special
ability window. The purchase DC for some robotic equipment and
accessories is not shown in the cost field but is instead displayed in
the equipment's special property display. This is because the cost of
many of these items are dependent on the cost of the Robot frame they
are installed on, thus the purchase DC can be calculated but only after
the item is equipped to the robot character. Items with straight
purchase DCs are displayed in the cost field normally.

Equipment
---------

All the Robot equipment is meant only for Robots, the bonuses they have
which provide the functionality are qualified as such and will not
benefit characters who are not Robots.

Locomotion
----------

All Robots need to have some form of locomotion equipped to them to
provide a movement speed. The speed can be increased by customizing the
locomotion equipment and adding a speed upgrade. The rules say you
cannot upgrade the speed past double its base speed but **PCGen** cannot
enforce this.

Manipulators
------------

The Manipulators are size tiny and are meant for Medium-sized Robots. To
get the proper damage for a Robot of another size you will need to
customize the Manipulators for that Robot, they should be 2 size
categories smaller than the Robot they will be installed on.

Skill Software
--------------

The Skill software equipment all needs to be customized before you can
add it to your character. This is so you can select the specific skills
the equipment emulates.

Feat Software
-------------

The Feat software could not be implemented the same way that skill
software was. Each feat has a corresponding Robot Feat Software item
which adds it as a virtual feat when the item is equipped. There are two
sets of items relating to feat software, the actual devices, feat
progit, feat net, and feat web and then there the individual feat
software which grants the virtual feat. The software has no purchase DC
but is assumed to come with the device when purchased. The Weapon
Finesse and Weapon Focus feats are missing, as they couldn't be
implemented that way.



