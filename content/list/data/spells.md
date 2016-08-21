+++
date = "2016-08-01"
title = "Spell Files"
original_url = "/list/data/spells.html"

[menu.main]
    identifier = "data_spells"
    name = "Spell Files"
    parent = "data"
    
+++
------------------------------------------------------------------------

<span id="buildingspells"></span> Building a Spell
--------------------------------------------------

The first field is the name of the spell.

`Ghost Sound`

The spell named "Ghost Sound" is to be created.

`Silent Image.MOD`

The spell named "Silent Image" is to be modified.

`Magic Aura.COPY=Nystal's Undetectable Aura`

Copy the spell "Magic Aura" and rename to "Nystal's Undetectable Aura"
in all aspects.

`Holy Smite.FORGET`

The spell "Holy Smite" is to be forgotten.

Initial Comment:\

In all four versions of KEY (Spell - Potion) or KEY (Spell - Scroll) or
KEY (Spell - Spell) or KEY (Spell - Staff, Wand & Ring) ), there is
something like:\

"Potions modifier's will work without a KEY but work much better using
the KEY than the name."\

First of all, most of these items are NOT RELEVANT to Spell LST, KEY is
a global token... I don't know if it's valuable to state it's part of
Spell (but we should be consistent with Type, which the docs also make
unique to each LST file for some reason)\

Second, it should be made clear that the KEY is an optional Token, BUT
when used, the user MUST ALWAYS use the Key to refer to the item, the
name WILL NOT WORK.\

Thus in Spell LST:\

-   ...
-   Whiz Bangy &lt;tab&gt; KEY:Foo
-   ...

In another file:

-   PRESPELL:1,Whiz Bangy
-   WILL NOT WORK
-   Requires:
-   PRESPELL:1,Foo.

------------------------------------------------------------------------

Spell File Tag Dictionary
-------------------------

------------------------------------------------------------------------

