+++
date = "2016-08-01"
title = "Paizo: The Pathfinder Roleplaying Game help file"
original_url = "/source/pathfinder/rpg.html"

[menu.main]
    identifier = "pathfinder_rpg"
    name = "Paizo: The Pathfinder Roleplaying Game help file"
    parent = "pathfinder"
    
+++
**Game Mode: Pathfinder\_RPG**

PAIZO PUBLISHING &gt; PATHFINDER ROLEPLAYING GAME

**Paizo - Pathfinder Roleplaying Game Core Rulebook**

### Specialized Wizard

A wizard can choose to specialize in one school of magic but must select
two other schools as his opposition schools. There are a couple of
aspects of wizard specialization that PCGen does not handle at this
time:

\
 *A wizard begins play with a spellbook containing all 0-level wizard
spells (except those from his opposition schools, if any)*

Currently PCGen will add all 0-level spells to a wizard's known spells,
you must manually remove the opposition school spells to comply with
this rule.

\
 *A wizard who prepares spells from his opposition schools must use two
spell slots of that level to prepare the spell.*

Currently PCGen cannot enforce this, you could add the spell twice to
your prepared spells list to represent the two slots.

### Ability descriptions

Paizo has allowed the use of the full text in the descriptions of
abilities. For some abilities this text can be quite long. In order to
provide an option for those who don't want to have the full text filling
up their character sheet we are utilizing a feature that has not been
use previously in the Open Source datasets. The dataset can hold two
versions of the description, a short description, which is usually the
flavor text and an optional long description or benefit text which can
contain the full text of the ability description. To set this option
choose " [Preferences](/menu/settings/preferences.html) " from the
Settings menu. Click on [Display Options in the Appearance
tree](/menu/settings/appearance/display.html) and find the " [Display
Feat Description](/menu/settings/appearance/display.html) " option. When
this is checked the short description is output, when it is unchecked
the longer benefit text is displayed if there is such text available. If
there is no benefit text the short description will be used by default.

For those who wish to have a technical explanation of how this is done
refer to the [BENEFIT](/list/data/ability/benefit.html) tag. This tag
allows the data to contain two versions of ability descriptions, the
[DESC](/list/global/other/desc.html) generally holds a short version and
[BENEFIT](/list/data/ability/benefit.html) holds the longer version.

------------------------------------------------------------------------



