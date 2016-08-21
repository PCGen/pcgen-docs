+++
date = "2016-08-01"
title = "Fantasy Flight Games: Midnight - Campaign Source Book PCGen help file"
original_url = "/source/fantasy/midnight.html"

[menu.main]
    identifier = "fantasy_midnight"
    name = "Fantasy Flight Games: Midnight - Campaign Source Book PCGen help file"
    parent = "fantasy"
    
+++
**Game Mode: 3e**

ALPHA DATASETS

**FFG - Midnight - Campaign Source Book**

### The Midnight magic system

Midnight employs an unusual magic system which has been difficult to
implement in PCGen and accounts for the long time it took to appear in
the release. In Midnight any character class can learn and cast spells,
they need only have taken the proper feats. To do this some workarounds
are employed to make this work within PCGen. First all the normally
non-spellcasting classes allowed in Midnight are modified so that they
are spell casters. This is only done for the classes which exist in
Midnight, those classes which do not were left alone. Second the Spells
have been modified so that they have as a prerequisite the correct feats
necessary to learn and cast the spell.

One effect of this is that when the Midnight dataset is loaded all the
spells in the SRD have prerequisites for Midnight's requirements which
interferes with spellcasters outside of those in Midnight. If you wish
to make NPC's and monsters with spellcasting capabilities outside of the
Midnight system we have provided a template named **Unlock Midnight
Spell Prerequisites** which will bypass those prerequisites and allow
normal spellcasting.



