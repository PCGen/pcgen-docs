+++
date = "2016-08-01"
title = "NAMEOPT (Data: equipment_modifiers.lst)"
original_url = "/list/data/equipmentmodifiers.html#nameopt"
categories = [ "all-tag", "equipmentmodifiers-tag" ]
[menu.main]
    name = "NAMEOPT"
    parent = "data_equipmentmodifiers"
+++

## Status

None

## Syntax

`NAMEOPT:x`

## Parameters

-   x: NOLIST
-   x: NONAME
-   x: NORMAL
-   x: NOTHING
-   x: SPELL
-   x: TEXT=&lt;text&gt;



<span id="nameopt"></span> \*\*\* Updated 5.9.8

What it does
------------

This is used to set the naming convention used when an EQMOD is added to
an equipment item. Without this tag the EQMOD name is added as is to the
equipment name in parentheses after the original equipment name and
separated from other EQMOD names by slashes. If an EQMOD has a CHOOSE in
it normally the choice made will follow the name of the EQMOD in
parentheses. Available options work as follows:

-   NAMEOPT:NORMAL - Passes the name and choice to the equipment, same
    effect if the NAMEOPT tag is not present.
-   NAMEOPT:NOLIST - Passes the name of the EQMOD but not the choice
    (if any) to the equipment.
-   NAMEOPT:NONAME - Passes the choice made to the equipment but not the
    name of the EQMOD.
-   NAMEOPT:NOTHING - No text is added to the equipment name.
-   NAMEOPT:SPELL - If the EQMOD has a spell chooser this option passes
    the spell details to the equipment. The details displayed are:
    SpellName/Metamagic feat applied/Class/Level.
-   NAMEOPT:TEXT=&lt;Text&gt; - Specified text is passed to
    the equipment.

Example
-------

`Craft[tab]CHOOSE:SKILL|TYPE=CRAFT[tab]BONUS:SKILL|%CHOICE|2[tab]`

selecting "Craft (Armorsmithing)" in the chooser with:

-   NAMEOPT:NOLIST - generate "Craft" as the name.
-   NAMEOPT:NONAME - generate "Craft (Armorsmithing)" as the name.
-   NAMEOPT:NORMAL - generate "Craft (Craft (Armorsmithing))" as
    the name.

Example
-------

`NAMEOPT:SPELL`

Customizing boots with an invisibility spell might generate: Boots
(Invisibility/Extend Spell/Wizard/5th).

