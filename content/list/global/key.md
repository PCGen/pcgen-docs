+++
date = "2016-08-01"
title = "The KEY Tag"
original_url = "/list/global/key.html"

[menu.main]
    identifier = "global_key"
    name = "The KEY Tag"
    parent = "global"
    
+++
This file is broken down into three sections: the [**Tag
Description**](/list/global/key.html#key) , the [**Application
Standard**](/list/global/key.html#standard) , and the [**KEY
Glossary**](/list/global/key.html#glossary) .

**NOTE:** The KEY tag <span class="underline"> MUST </span> be unique in
the datasets and sub-datasets that it is present in.

------------------------------------------------------------------------

<span id="key"></span> Tag Description
--------------------------------------

------------------------------------------------------------------------

<span id="keytag"></span> \*\*\* Update 5.11.5

**Tag Name:** KEY:x

**Variables Used (x):** Text (Key Name)

**What it does:**

This tag creates, or references, a key by which a specific object can be
indentified within PCGen. It is a unique descriptor for the modifier. It
allows several modifiers to have the same name, which is useful if
several are needed for different equipment types. KEY's must be
universally unique. Make sure you don't use anything that's is used in
any other source you load. And don't just take out the KEY and use the
name. Potions modifier's will work without a KEY but work much better
using the KEY than the name.If a Potion includes a KEY, then the KEY
must be used for all calling purposes.

**Examples:**

`KEY:MUT_SECOND_WIND`

Creates the unique KEY for the MSRD Feat *Second Wind*

`KEY:SDA_POWER_OF_NATURE`

Creates the unique KEY for the RSRD Special Divine Abilities feat *Power
of Nature*

`KEY:SDA_UNDEAD_MASTERY`

Creates the unique KEY for the RSRD Special Divine Abilities feat
*Undead Mastery*

`KEY:FEAT_FRIGHTFUL_PRESENCE_MP`

Creates the unique KEY for - *Frightful Presence*

`KEY:SKL_DISABLE_DEVICE_MP`

Creates the unique KEY for Swords Edge Publishing's Modern Principles
*Disable Device*

------------------------------------------------------------------------

<span id="standard"></span> Application Standard
------------------------------------------------

**General Notes**

1\) The KEY is set to the item name unless you put in a KEY tag.

-   So if a KEY is used, that one will be stored in the PCG file,
    instead of the name? And if I use the previous name as the KEY, and
    change the name, will the PCG that has stored the name load the
    renamed object now based on the KEY? And is this truly global?.\
-   Works for Equipmods, Races, Feats, Domains and Classes, did not work
    for Templates, Spells.\

2\) If the name is the same but the key is different both will be
processed and displayed.

-   PCGen will determine which source is newer with a new PCC tag
    SOURCEDATE which should be set to the date of release of the source
    in the format YYYY-MM. A source without a SOURCEDATE will always be
    considered older than a source with a date.\

3\) Oh no that source name is X and they have Y in PCGen.

-   I know this would be a pain to track, but could we get those that
    are editing data files to keep track of any name changes they make?
    If we could have a file for this checked into each release and
    copied with the release when it is installed, we could have
    prettylst (or some other perl script) read the file from the
    installed release and do the work.\
-   if someone knows they'll change the names from Potion of Foo to Foo
    (Potion), they'd put: Potion of (.\*)/\$1 (Potion) into a file. We
    could use something else in place of the (.\*), slash, and \$1
    that's more human readable.\
-   If we start using Keys, even better - then, it would be possible to
    run a perl script to find all of the changes and create the above
    file, and people wouldn't have to track their changes to names
    directly.\

**General Naming Standards**

The following are the naming conventions to be used when creating a KEY.

-   Keys are to be in all capital letters and may only contain letters,
    numbers and underscores ("\_").\
-   Each word should be separated by an underscore character for ease in
    reading.\
-   The first section is the same as the SOURCESHORT: in the .pcc, on
    the second, third or more sections of the Key name is the unique ID
    of the tag.\
-   The letter limit on the second and third sections of the Key name is
    8 and 7.\
-   EQMODs for different item types (Weapon vs. Armor for example) will
    be done as separate KEYs\
-   Materials which list different pricing for different item types or
    sub-types (Light Armor vs. Medium Armor for example) will be done as
    separate KEYs for each price type.\

Standard abbreviations

-   Ammunition - AMMO\
-   Armor - ARMR\
-   Electrical - ELEC\
-   Enhancement - ENHANCE\
-   Greater - GRT\
-   Heavy - HVY\
-   Improved - IMP\
-   Instrument - INSTR\
-   Light - LT\
-   Masterwork - MWORK\
-   Medium - MED\
-   Resistance - RES\
-   Shield - SHLD\
-   Weapon - WEAP\

To see the rest of the standards, including the EQMOD KEY name list look
here: <http://pcgen.sourceforge.net/StandardsProject/>

------------------------------------------------------------------------

<span id="glossary"></span> The KEY Glossary
--------------------------------------------

### By Gamemode {#by-gamemode .indent1}

The following list of keys covers all keys used in the following
gamemodes.

> **Gamemode**
>
> > Publisher - Setting/Dataset
>
> **D&D 3.0 Edition (3e)**
>
> > [Wizards of the Coast (WotC) - Standard Reference Document
> > (3e)](/list/global/key.html#srd)\
> > [Atlas Games (AG) - Penumbra/Beyong the
> > Vail](/list/global/key.html#ag)\
> > [Bad Ass Games (BAG) - Heroes of High Favor -
> > Dwarves](/list/global/key.html#bag)\
> > [Bastion Press (BP) - Oathbound](/list/global/key.html#bp)\
> > [Battle Field Press (BFP) - Cityscape](/list/global/key.html#bfpc)\
> > [Fantasy Flight Games (FFG) - Dragonstar: Starfarers
> > Handbook](/list/global/key.html#ffgdsh)\
> > [Fantasy Flight Games (FFG) - Legends and Lairs: School of
> > Illusion](/list/global/key.html#ffgll)\
> > [Fantasy Flight Games (FFG) - Legends and Lairs: Seafarer's
> > Handbook](/list/global/key.html#ffgll)\
> > [Fantasy Flight Games (FFG) - Legends and Lairs: Sorcery and
> > Steam](/list/global/key.html#ffgll)\
> > [Fantasy Flight Games (FFG) - Midnight](/list/global/key.html#ffgm)\
> > [Fantasy Flight Games (FFG) - Midnight: Against the
> > Shadow](/list/global/key.html#ffgm)\
> > [Malhavoc Press (MP) - Book of Hallowed
> > Might](/list/global/key.html#mphm)\
> > [Mongoose Publishing (MP) - Collectors Series - Quintessential
> > Rogue](/list/global/key.html#mp)\
> > [Mongoose Publishing (MP) - Encyclopaedia Arcane - Enchantment
> > Magic](/list/global/key.html#mp)\
> > [Mongoose Publishing (MP) - Encyclopaedia Divine - Fey
> > Magic](/list/global/key.html#mp)\
> > [Mongoose Publishing (MP) - Power Classes Volume I -
> > Assassin](/list/global/key.html#mp)\
> > [Paradigm Concepts Inc (PCI) - Codex
> > Arcanis](/list/global/key.html#pcica)
>
> **D&D 3.5 Edition (35e)**
>
> > [Wizards of the Coast (WotC) - Revised Standard Reference Document
> > (35e)](/list/global/key.html#rsrd)\
> > [Alea Publishing Group (APG) - Quests](/list/global/key.html#apg)\
> > [Bards and Sages (BaS) - Neiyar Land of Heaven and the
> > Abyss](/list/global/key.html#bas)\
> > [Big Finger Games (BFG) - Masterwork
> > Qualities](/list/global/key.html#bfg)\
> > [Malhavoc Press (MP) - Complete Book of Eldritch
> > Might](/list/global/key.html#mpem)\
> > [Necromancer Games (NG) - Eldritch
> > Sorcery](/list/global/key.html#nges)\
> > [Necromancer Games (NG) - Tome of
> > Horrors](/list/global/key.html#ngtoh)\
> > [Paradigm Concepts Inc (PCI) - World of
> > Arcanis](/list/global/key.html#pciwoa)\
> > [Secular Games (SG) - Lines of Legend - Winter
> > Elves](/list/global/key.html#sg)\
> > [Swords Edge Publishing (SEP) - Modern Medieval - Modern
> > Principles](/list/global/key.html#sep)\
> > [Vigilance Press (VP) - Clash of Arms -
> > Cavalry](/list/global/key.html#vp)\
>
> **<span id="deadlands"></span> Deadlands**
>
> > [Pinnacle Entertainment (PE) - Deadlands
> > d20](/list/global/key.html#pe)
>
> **<span id="modern"></span> d20 Modern (Modern)**
>
> > [Wizards of the Coast (WotC) - Moderm Standard Reference Document
> > (MSRD)](/list/global/key.html#msrd)\
> > [Wizards of the Coast (WotC) - d20 Weapons
> > Locker](/list/global/key.html#wotc)\
> > [Battlefield Press (BFP) - Pulp Fantasy](/list/global/key.html#bfp)\
> > [Battlefield Press (BFP) - Rocket Rangers - King of the Rocket
> > Men](/list/global/key.html#bfprr)\
> > [Blue Devil Games (BDG) - Dawningstar](/list/global/key.html#bdg)\
> > [Mythic Dreams Studios (MDS) - Dark
> > Inheritance](/list/global/key.html#mds)\
> > [RPG Objects (RPGO) - Blood and Blades - The Profilers Guide to
> > Slashers](/list/global/key.html#rpgo)\
> > [RPG Objects (RPGO) - Blood and
> > Secrets](/list/global/key.html#rpgo)\
> > [RPG Objects (RPGO) - Blood and Space: Starship Construction
> > Manual](/list/global/key.html#rpgo)\
> > [RPG Objects (RPGO) - Modern Dispatch: \#1 Alternate
> > Armors](/list/global/key.html#rpgo)\
> > [RPG Objects (RPGO) - Modern Dispatch: \#10 Near Future
> > Firearms](/list/global/key.html#rpgo)\
> > [The Game Mechanics Inc (TGM) - Martial Arts
> > Mayhem](/list/global/key.html#tgm)\
> > [The Game Mechanics Inc (TGM) - Modern Player's
> > Companion](/list/global/key.html#tgm)
>
> **<span id="sidewinder"></span> Sidwinder**
>
> > [Dog House Rules (DHR) - Sidewinder
> > Recoiled](/list/global/key.html#dhr)
>
> **<span id="spycraft"></span> Spycraft**
>
> > [Crafty Games (CG) - Spycraft](/list/global/key.html#cg)\
> > [Crafty Games (CG) - Spycraft - Shadowforce
> > Archer](/list/global/key.html#cg)
>
> **<span id="xcrawl"></span> XCrawl**
>
> > [Pandahead Productions (PP) - Xcrawl](/list/global/key.html#pp)

### [The Complete Listing of Keys](/list/global/key.html#complete) {#the-complete-listing-of-keys .indent1}

**NOTE:** The information contained in the square brackets (\[ \]) is
not part of the name of the modifier. It is included in this list to
provide additional information on the intended object type of object the
modifier is intended for.

------------------------------------------------------------------------

**<span id="srd"></span> Wizards of the Coast (WotC): Standard Reference
Document** - SRD (3e)

> **SRD - Basics File.**
>
> `KEY:A_1USEMA` - Spell Effect (Single Use/Completion) \[Major\]\
> `KEY:A_1USEME` - Spell Effect (Single Use/Completion) \[Medium\]\
> `KEY:A_1USEMI` - Spell Effect (Single Use/Completion) \[Minor\]\
> `KEY:ADAM` - Adamantine <span class="new"> (deprecated) </span>\
> `KEY:ADAMANT_AMMO` - Adamantine (Ammo)\
> `KEY:ADAMANT_ARMR_HVY` - Adamantine (Armor/Heavy)\
> `KEY:ADAMANT_ARMR_LT` - Adamantine (Armor/Light)\
> `KEY:ADAMANT_ARMR_MED` - Adamantine (Armor/Medium)\
> `KEY:ADAMANT_FORT` - Adamantine (Fortification)\
> `KEY:ADAMANT_SHLD` - Adamantine (Shield)\
> `KEY:ADAMANT_WEAP` - Adamantine (Weapon)\
> `KEY:ADAMANT_WONDROUS` - Adamantine (Wondrous)\
> `KEY:ADD_TYPE` - \# Add Type\
> `KEY:ANMATD` - Animated\
> `KEY:ARCANE_ARCHER_AMMO` - Arcane Archer Enchantement\
> `KEY:ARW_DEF` - Arrow Deflection\
> `KEY:BANE_A` - Bane \[Ammunition\]\
> `KEY:BANE_M` - Bane \[Melee\]\
> `KEY:BANE_R` - Bane \[Ranged\]\
> `KEY:BASH_H` - Bashing \[Heavy\]\
> `KEY:BASH_L` - Bashing \[Light\]\
> `KEY:BIND` - Blinding\
> `KEY:BNS_AC_DEFL` - AC Bonus (Deflection)\
> `KEY:BNS_ENHC_AB` - Ability Bonus (Enhancement)\
> `KEY:BNS_ENHC_AC` - Armor Bonus (Enhancement)\
> `KEY:BNS_ENHC_NAT` - Natural Armor Bonus (Enhancement)\
> `KEY:BNS_SAV_LUC` - Save Bonus (Luck)\
> `KEY:BNS_SAV_RES` - Save Bonus (Resistance)\
> `KEY:BNS_SKL_CIR` - Skill Bonus (Circumstance)\
> `KEY:BNS_SKL_CMP` - Skill Bonus (Competence)\
> `KEY:BNS_SKL_LCK` - Skill Luck Bonus\
> `KEY:BNS_SPELL` - Bonus Spell\
> `KEY:BNS_SPL_RST` - Spell Resistance\
> `KEY:BONE` - Bone\
> `KEY:BRASS` - Brass\
> `KEY:BRI_EN_A` - Brilliant Energy \[Ammunition\]\
> `KEY:BRI_EN_M` - Brilliant Energy \[Melee\]\
> `KEY:BRI_EN_T` - Brilliant Energy \[Ranged\]\
> `KEY:BRONZE` - Bronze\
> `KEY:CHAOS_A` - Anarchic, Chaotic \[Ammunition\]\
> `KEY:CHAOS_M` - Anarchic, Chaotic \[Melee\]\
> `KEY:CHAOS_R` - Anarchic, Chaotic \[Ranged\]\
> `KEY:CHARGED_ITEM_3` - Charges (3)\
> `KEY:CHARGED_ITEM_5` - Charges (5)\
> `KEY:CHARGED_ITEM_10` - Charges (10)\
> `KEY:CHARGED_ITEM_12` - Charges (12)\
> `KEY:CHARGED_ITEM_36` - Charges (36)\
> `KEY:CHARGED_ITEM_50` - Charges (50)\
> `KEY:CHARGED_ITEM_101` - Charges (101)\
> `KEY:CLAY` - Clay\
> `KEY:CLOTH` - Cloth\
> `KEY:D_1USEMA` - Spell Effect (Single Use/Completion) \[Major\]\
> `KEY:D_1USEME` - Spell Effect (Single Use/Completion) \[Medium\]\
> `KEY:D_1USEMI` - Spell Effect (Single Use/Completion) \[Minor\]\
> `KEY:DANCE` - Dancing\
> `KEY:DARK` - Darkwood\
> `KEY:DEFEND` - Defending\
> `KEY:DISRPT` - Disruption\
> `KEY:DISTNC` - Distance\
> `KEY:ETHERE` - Etherealness\
> `KEY:FLM_A` - Flaming\
> `KEY:FLM_BR_A` - Flaming Burst \[Ammunition\]\
> `KEY:FLM_BR_M` - Flaming Burst \[Melee\]\
> `KEY:FLM_BR_R` - Flaming Burst \[Ranged\]\
> `KEY:FLM_M` - Flaming \[Melee\]\
> `KEY:FLM_R` - Flaming \[Ranged\]\
> `KEY:FROST_A` - Frost \[Ammunition\]\
> `KEY:FROST_M` - Frost \[Melee\]\
> `KEY:FROST_R` - Frost \[Ranged\]\
> `KEY:FRT_HVY` - Fortification (Heavy)\
> `KEY:FRT_LGHT` - Fortification (Light)\
> `KEY:FRT_MOD` - Fortification (Moderate)\
> `KEY:GHOST_A` - Ghost touch \[Armor and Shield\]\
> `KEY:GHOST_AM` - Ghost touch \[Ammunition\]\
> `KEY:GHOST_M` - Ghost touch \[ Melee\]\
> `KEY:GHOST_R` - Ghost touch \[Ranged\]\
> `KEY:GLAM` - Glamered\
> `KEY:GLASS` - Glass\
> `KEY:GOLD` - Gold\
> `KEY:HEMP` - Hemp\
> `KEY:HOLY_A` - Holy \[Ammunition\]\
> `KEY:HOLY_M` - Holy \[Melee\]\
> `KEY:HOLY_R` - Holy \[Ranged\]\
> `KEY:ICE` - Ice\
> `KEY:ICE_BR_A` - Icy Burst \[Ammunition\]\
> `KEY:ICE_BR_M` - Icy Burst \[Melee\]\
> `KEY:ICE_BR_R` - Icy Burst \[Ranged\]\
> `KEY:IRON` - Iron\
> `KEY:IRONWOOD` - Ironwood\
> `KEY:IRONWOOD_PLUS` - Ironwood (+1)\
> `KEY:INVULN` - Invulnerability\
> `KEY:KEEN` - Keen\
> `KEY:LAW_A` - Axiomatic, Lawful \[Ammunition\]\
> `KEY:LAW_M` - Axiomatic, Lawful \[Melee\]\
> `KEY:LAW_R` - Axiomatic, Lawful \[Ranged\]\
> `KEY:LEATHER` - Leather\
> `KEY:Lock_G` - Locked Gauntlets\
> `KEY:MI_CLE` - Mighty Cleaving\
> `KEY:MITHRAL_ARMR_HVY` - Mithral (Armor/Heavy)\
> `KEY:MITHRAL_ARMR_LT` - Mithral (Armor/Light)\
> `KEY:MITHRAL_ARMR_MED` - Mithral (Armor/Medium)\
> `KEY:MITHRAL_ITEM` - Mithral (Weapon/Ammo/Instrument)\
> `KEY:MITHRAL_SHLD` - Mithral (Shield)\
> `KEY:MTHRL` - Mithral <span class="new"> (deprecated) </span>\
> `KEY:MTHRL_MDHV` - Mithral <span class="new"> (deprecated) </span>\
> `KEY:MWORKA` - Masterwork (Armor)\
> `KEY:MWORKI` - Masterwork (Instrument)\
> `KEY:MWORKT` - Masterwork (Tool)\
> `KEY:MWORKW` - Masterwork (Weapon/Ammo)\
> `KEY:NONHUMANOID` - Nonhumanoid (Armor)\
> `KEY:PAPER` - Paper\
> `KEY:PLUS1A` - +1 (Enhancement to Armor)\
> `KEY:PLUS1S` - +1 (Enhancement to Shield)\
> `KEY:PLUS1W` - +1 (Enhancement to Weapon or Ammunition)\
> `KEY:PLUS2A` - +2 (Enhancement to Armor)\
> `KEY:PLUS2S` - +2 (Enhancement to Shield)\
> `KEY:PLUS2W` - +2 (Enhancement to Weapon or Ammunition)\
> `KEY:PLUS3A` - +3 (Enhancement to Armor)\
> `KEY:PLUS3S` - +3 (Enhancement to Shield)\
> `KEY:PLUS3W` - +3 (Enhancement to Weapon or Ammunition)\
> `KEY:PLUS4A` - +4 (Enhancement to Armor)\
> `KEY:PLUS4S` - +4 (Enhancement to Shield)\
> `KEY:PLUS4W` - +4 (Enhancement to Weapon or Ammunition)\
> `KEY:PLUS5A` - +5 (Enhancement to Armor)\
> `KEY:PLUS5S` - +5 (Enhancement to Shield)\
> `KEY:PLUS5W` - +5 (Enhancement to Weapon or Ammunition)\
> `KEY:REFLC` - Reflecting\
> `KEY:RETRN` - Returning\
> `KEY:RING` - Ring\
> `KEY:RST_ACD` - Acid Resistance\
> `KEY:RST_CLD` - Cold Resistance\
> `KEY:RST_ELE` - Electricity Resistance Lightning Resistance\
> `KEY:RST_FR` - Fire Resistance\
> `KEY:RST_SNC` - Sonic Resistance\
> `KEY:SCROLL` - SCROLL\
> `KEY:SCROLL_ARCANE` - SCROLL (Arcane)\
> `KEY:SCROLL_DIVINE` - SCROLL (Divine)\
> `KEY:SCROLL_MAJOR` - SCROLL (Major)\
> `KEY:SCROLL_MEDIUM` - SCROLL (Medium)\
> `KEY:SCROLL_MINOR` - SCROLL (Minor)\
> `KEY:SHDW` - Shadow\
> `KEY:SHK_BR_A` - Shocking Burst \[Ammunition\]\
> `KEY:SHK_BR_M` - Shocking Burst \[Melee\]\
> `KEY:SHK_BR_R` - Shocking Burst \[Ranged\]\
> `KEY:SHOCK_A` - Shock \[Ammunition\]\
> `KEY:SHOCK_M` - Shock \[Melee\]\
> `KEY:SHOCK_R` - Shock \[Ranged\]\
> `KEY:SILK` - Silk\
> `KEY:SILVER` - Silver\
> `KEY:SLK` - Slick\
> `KEY:SLNT_MV` - Silent moves\
> `KEY:SLVR` - Silvered\
> `KEY:SPEED` - Speed\
> `KEY:SPELL_RES_13` - Spell Resistance (SR 13)\
> `KEY:SPELL_RES_15` - Spell Resistance (SR 15)\
> `KEY:SPELL_RES_17` - Spell Resistance (SR 17)\
> `KEY:SPELL_RES_19` - Spell Resistance (SR 19)\
> `KEY:SPELLFOCUS` - Spell Focus Value\
> `KEY:SPELLMATERIAL` - Spell Material Component Value\
> `KEY:SPIKE_A` - Armor Spikes\
> `KEY:SPIKE_S` - Shield Spikes\
> `KEY:SPIKE_SB` - Shield Bash\
> `KEY:SPL_1USE` - Spell Effect (Single Use/Use Activated)\
> `KEY:SPL_ACT` - Spell Effect (Use Activated)\
> `KEY:SPL_CHRG` - Spell Effect (50 Charges/Spell Trigger)\
> `KEY:SPL_CMD` - Spell Effect (Command Word)\
> `KEY:SPL_RST` - Spell Resistance <span class="new"> (deprecated)
> </span>\
> `KEY:SPL_STR` - Spell Storing\
> `KEY:STEEL` - Mundane (Weapon/Ammo)\
> `KEY:STONE` - Stone\
> `KEY:THNDR_A` - Thundering \[Ammunition\]\
> `KEY:THNDR_M` - Thundering \[Melee\]\
> `KEY:THNDR_R` - Thundering \[Ranged\]\
> `KEY:THROW` - Throwing\
> `KEY:UNHLY_A` - Unholy \[Ammunition\]\
> `KEY:UNHLY_M` - Unholy \[Melee\]\
> `KEY:UNHLY_R` - Unholy \[Ranged\]\
> `KEY:VORPAL` - Vorpal\
> `KEY:WAND` - Wand\
> `KEY:WAX` - Wax\
> `KEY:WOOD` - Mundane (Weapon/Ammo)\
> `KEY:WOUND` - Wounding\
>
> **SRD - Advanced File.**
>
> `KEY:Scroll (Ice Storm)` - Scroll (Ice Storm/Arcane)\
>
> **SRD - Psionics File.**
>
> `KEY:APRTR` - Aporter\
> `KEY:ARMPR13` - \# Power Resistance (PR13) - Armor.Shield\
> `KEY:ARMPR15` - \# Power Resistance (PR15) - Armor.Shield\
> `KEY:ARMPR17` - \# Power Resistance (PR17) - Armor.Shield\
> `KEY:ARMPR19` - \# Power Resistance (PR19) - Armor.Shield\
> `KEY:AVRTR` - Averter\
> `KEY:BDY_FDR` - Body Feeder\
> `KEY:CHRGD` - Charged\
> `KEY:CRYSTAL` - Crystalline\
> `KEY:DISSIP` - Dissipater\
> `KEY:ECTO` - Ectoplasmic\
> `KEY:FERROPLASM` - Ferroplasm\
> `KEY:FLOAT` - Floating\
> `KEY:HEART` - Hearten\
> `KEY:IMPCT` - Impact\
> `KEY:LANDING` - Landing\
> `KEY:LINKED` - Linked\
> `KEY:LUCKY` - Lucky\
> `KEY:MND_ARMR` - Mindarmor\
> `KEY:MND_CRSHR` - Mindcrusher\
> `KEY:MND_FDR` - Mind Feeder\
> `KEY:MNFSTR_S` - Manifester\
> `KEY:MNFSTR_W` - Manifester\
> `KEY:MNTL_ADBL` - Mentally Audible\
> `KEY:PARRYING` - Parrying\
> `KEY:PHASING` - Phasing\
> `KEY:POWER STORING` - Power Storing\
> `KEY:PSIARMFORH` - \#Reinforcement (Heavy) - Armor.Shield\
> `KEY:PSIARMFORL` - \#Reinforcement (Light) - Armor.Shield\
> `KEY:PSIARMFORM` - \#Reinforcement (Moderate) - Armor.Shield\
> `KEY:PSIBANE` - Psibane\
> `KEY:PSYCHIC` - Psychic\
> `KEY:PWR_CRWL` - |Power Effect (Single Use/Use Activated)\
> `KEY:PWR_DRJ` - |Power Effect (50 Charges/Power Trigger)\
> `KEY:PWR_PS` - |Power Effect (Single Use/Completion)\
> `KEY:PWR_PT` - |Power Effect (Single Use/Use Activated)\
> `KEY:PWR_RST` - Power Resistance\
> `KEY:QUICKNESS` - Quickness\
> `KEY:RADIANT` - Radiant\
> `KEY:RNFRC_HVY` - Reinforcement (Heavy)\
> `KEY:RNFRC_LGHT` - Reinforcement (Light)\
> `KEY:RNFRC_MOD` - Reinforcement (Moderate)\
> `KEY:RNGED` - Ranged\
> `KEY:SIGHT` - Sight\
> `KEY:SL_FDR` - Soul Feeder\
> `KEY:SPPRSSN` - Suppression\
> `KEY:SUNDERER` - Sunderer\
> `KEY:THGHT_BSTN` - Thought Bastion\
> `KEY:TIME_BTTRS` - Time Buttress\
> `KEY:VANISHING` - Vanishing\
> `KEY:WALL` - Wall\
>
> **SRD - EQUIPMODE EXCLUDED**
>
> `KEY:EXCLUDEEQ_MAGIC` - Magic\
> `KEY:EXCLUDEEQ_MUNDANE` - Mundane\

------------------------------------------------------------------------

**<span id="rsrd"></span> Wizards of the Coast (WotC): Revised Standard
Reference Document** - RSRD (35e)

> **RSRD - Advanced File.**
>
> `KEY:ART` - Art Value\
> `KEY:GEM` - Gem Value\
> `KEY:Gloves of Swimming/Climbing` - Gloves of Swimming and Climbing\
> `KEY:Helm of Comprehending Languages and Reading Magic` - Helm of
> Comprehend Languages and Read Magic\
> `KEY:Potion(Oil of Shillelagh)` - Potion (Oil of Shillelagh)\
> `KEY:Potion(Oil of Bless Weapon)` - Potion (Oil of Bless Weapon)\
> `KEY:Potion (Darkness)` - Potion (Darkvision)\
> `KEY:Scroll (Analayze Dweomer)` - Scroll (Analyze Dweomer)\
> `KEY:Scroll (Banishement/Arcane)` - Scroll (Banishment/Arcane)\
> `KEY:Scroll (Control Water/Divine)` - Scroll (Control Water)\
> `KEY:Scroll (Control Weather/Arcane)` - Scroll (Control
> Weather/Arcane/Lvl 7)\
> `KEY:Scroll (Gate/Arcane)` - Scroll (Gate)\
> `KEY:Scroll (Protection from Energy/Arcane)` - Scroll (Protection from
> Energy)\
> `KEY:Scroll (Stone Shape/Arcane)` - Scroll (Stone Shape)\
> `KEY:Scroll (Summon Monster IX/Arcane)` - Scroll (Summon Monster IX)\
> `KEY:Scroll (Tongues/Arcane)` - Scroll (Tongues)\
> `KEY:Scroll (Wall of Stone/Arcane)` - Scroll (Wall of Stone)\
> `KEY:Sunblade (Bastard)` - Sun Blade (Bastard)\
> `KEY:Sunblade (Short)` - Sun Blade (Short)\
>
> **RSRD - Basics File.**
>
> `KEY:A_1USEMA` - Spell Effect (Single Use/Completion) \[Major
> Arcane\]\
> `KEY:A_1USEME` - Spell Effect (Single Use/Completion) \[Medium
> Arcane\]\
> `KEY:A_1USEMI` - Spell Effect (Single Use/Completion) \[Minor
> Arcane\]\
> `KEY:ADAM` - Adamantine <span class="new"> (deprecated) </span>\
> `KEY:ADAMANT_AMMO` - Adamantine (Ammo)\
> `KEY:ADAMANT_ARMR_HVY` - Adamantine (Armor/Heavy)\
> `KEY:ADAMANT_ARMR_LT` - Adamantine (Armor/Light)\
> `KEY:ADAMANT_ARMR_MED` - Adamantine (Armor/Medium)\
> `KEY:ADAMANT_SHLD` - Adamantine (Shield)\
> `KEY:ADAMANT_WEAP` - Adamantine (Weapon)\
> `KEY:ADD_TYPE` - \# Add Type\
> `KEY:ALCHM` - Alchemical Silver\
> `KEY:ALCHM/2` - 1/2 Alchemical Silver <span class="new"> (deprecated)
> </span>\
> `KEY:ANMATD` - Animated\
> `KEY:ARCANE_ARCHER_AMMO` - Arcane Archer Enchantement\
> `KEY:ARW_CAT` - Arrow Catching\
> `KEY:ARW_DEF` - Arrow Deflection\
> `KEY:BANE_A` - Bane\
> `KEY:BANE_M` - Bane\
> `KEY:BANE_R` - Bane\
> `KEY:BASH_H` - Bashing\
> `KEY:BASH_L` - Bashing\
> `KEY:BIND` - Blinding\
> `KEY:BNS_AC_DEFL` - AC Bonus (Deflection)\
> `KEY:BNS_AC_INSI` - AC Bonus (Insight)\
> `KEY:BNS_AC_LUCK` - AC Bonus (Luck)\
> `KEY:BNS_AC_OTHE` - AC Bonus (Other)\
> `KEY:BNS_AC_PROF` - AC Bonus (Profane)\
> `KEY:BNS_AC_SCRD` - AC Bonus (Sacred)\
> `KEY:BNS_ENHC_AB` - Ability Bonus (Enhancement)\
> `KEY:BNS_ENHC_AC` - Armor Bonus (Enhancement)\
> `KEY:BNS_ENHC_NAT` - Natural Armor Bonus (Enhancement)\
> `KEY:BNS_SAV_INS` - Save Bonus (Insight)\
> `KEY:BNS_SAV_LUC` - Save Bonus (Luck)\
> `KEY:BNS_SAV_OTH` - Save Bonus (Other)\
> `KEY:BNS_SAV_PRO` - Save Bonus (Profane)\
> `KEY:BNS_SAV_RES` - Save Bonus (Resistance)\
> `KEY:BNS_SAV_SAC` - Save Bonus (Sacred)\
> `KEY:BNS_SKL_CMP` - Skill Bonus (Competence)\
> `KEY:BNS_SPELL` - Bonus Spell\
> `KEY:BNS_SPL_RST` - |Spell Resistance\
> `KEY:BONE` - Bone\
> `KEY:BOWSTR` - Bow\_STR\
> `KEY:BRASS` - Brass\
> `KEY:BRI_EN_A` - Brilliant Energy\
> `KEY:BRI_EN_M` - Brilliant Energy\
> `KEY:BRI_EN_T` - Brilliant Energy\
> `KEY:BRONZE` - Bronze\
> `KEY:C_IRON` - Cold Iron\
> `KEY:C_IRON/2` - 1/2 Cold Iron <span class="new"> (deprecated)
> </span>\
> `KEY:CHAOS_A` - Anarchic, Chaotic\
> `KEY:CHAOS_M` - Anarchic, Chaotic\
> `KEY:CHAOS_R` - Anarchic, Chaotic\
> `KEY:CHARGED_ITEM_3` - Charges (3)\
> `KEY:CHARGED_ITEM_4` - Charges (4)\
> `KEY:CHARGED_ITEM_5` - Charges (5)\
> `KEY:CHARGED_ITEM_10` - Charges (10)\
> `KEY:CHARGED_ITEM_12` - Charges (12)\
> `KEY:CHARGED_ITEM_34` - Charges (34)\
> `KEY:CHARGED_ITEM_36` - Charges (36)\
> `KEY:CHARGED_ITEM_50` - Charges (50)\
> `KEY:CHARGED_ITEM_101` - Charges (101)\
> `KEY:CLAY` - Clay\
> `KEY:CLOTH` - Cloth\
> `KEY:D_1USEMA` - Spell Effect (Single Use/Completion) \[Major
> Divine\]\
> `KEY:D_1USEME` - Spell Effect (Single Use/Completion) \[Medium
> Divine\]\
> `KEY:D_1USEMI` - Spell Effect (Single Use/Completion) \[Minor
> Divine\]\
> `KEY:DANCE` - Dancing\
> `KEY:DARK` - Darkwood\
> `KEY:DEFEND` - Defending\
> `KEY:DISRPT` - Disruption\
> `KEY:DISTNC` - Distance\
> `KEY:DRACO` - Dragonhide\
> `KEY:ETHERE` - Etherealness\
> `KEY:FLM_A` - Flaming\
> `KEY:FLM_BR_A` - Flaming Burst\
> `KEY:FLM_BR_M` - Flaming Burst\
> `KEY:FLM_BR_R` - Flaming Burst\
> `KEY:FLM_M` - Flaming\
> `KEY:FLM_R` - Flaming\
> `KEY:FROST_A` - Frost\
> `KEY:FROST_M` - Frost\
> `KEY:FROST_R` - Frost\
> `KEY:FRT_HVY` - Fortification (Heavy)\
> `KEY:FRT_LGHT` - Fortification (Light)\
> `KEY:FRT_MOD` - Fortification (Moderate)\
> `KEY:GHOST_A` - Ghost touch\
> `KEY:GHOST_AM` - Ghost touch\
> `KEY:GHOST_M` - Ghost touch\
> `KEY:GHOST_R` - Ghost touch\
> `KEY:GLAM` - Glamered\
> `KEY:GLASS` - Glass\
> `KEY:GOLD` - Gold\
> `KEY:HIDE` - Hide\
> `KEY:HOLY_A` - Holy\
> `KEY:HOLY_M` - Holy\
> `KEY:HOLY_R` - Holy\
> `KEY:ICE` - Ice\
> `KEY:ICE_BR_A` - Icy Burst\
> `KEY:ICE_BR_M` - Icy Burst\
> `KEY:ICE_BR_R` - Icy Burst\
> `KEY:INVULN` - Invulnerability\
> `KEY:IRON` - Iron\
> `KEY:IRONWOOD` - Ironwood\
> `KEY:IRONWOOD_PLUS` - Ironwood (+1)\
> `KEY:KEEN` - Keen\
> `KEY:KIFOC` - Ki Focus\
> `KEY:LAW_A` - Axiomatic, Lawful\
> `KEY:LAW_M` - Axiomatic, Lawful\
> `KEY:LAW_R` - Axiomatic, Lawful\
> `KEY:LEATHER` - Leather\
> `KEY:Lock_G` - Locked Gauntlets\
> `KEY:MAGIC_COST` - Magical Enhancment Cost\
> `KEY:MAGIC_ENHANCE_1` - Magical Enhancments (+1)\
> `KEY:MAGIC_ENHANCE_2` - Magical Enhancments (+2)\
> `KEY:MAGIC_ENHANCE_3` - Magical Enhancments (+3)\
> `KEY:MAGIC_ENHANCE_4` - Magical Enhancments (+4)\
> `KEY:MAGIC_ENHANCE_5` - Magical Enhancments (+5)\
> `KEY:MAGIC_ENHANCE_6` - Magical Enhancments (+6)\
> `KEY:MAGIC_ENHANCE_7` - Magical Enhancments (+7)\
> `KEY:MAGIC_ENHANCE_8` - Magical Enhancments (+8)\
> `KEY:MAGIC_ENHANCE_9` - Magical Enhancments (+9)\
> `KEY:MAGIC_ENHANCE_10` - Magical Enhancments (+10)\
> `KEY:MERC_A` - Merciful\
> `KEY:MERC_M` - Merciful\
> `KEY:MERC_R` - Merciful\
> `KEY:MI_CLE` - Mighty Cleaving\
> `KEY:MITHRAL_ARMR_HVY` - Mithral (Armor/Heavy)\
> `KEY:MITHRAL_ARMR_LT` - Mithral (Armor/Light)\
> `KEY:MITHRAL_ARMR_MED` - Mithral (Armor/Medium)\
> `KEY:MITHRAL_ITEM` - Mithral (Weapon/Ammo/Instrument)\
> `KEY:MITHRAL_SHLD` - Mithral (Shield)\
> `KEY:MTHRL` - Mithral <span class="new"> (deprecated) </span>\
> `KEY:MTHRL_MDHV` - Mithral <span class="new"> (deprecated) </span>\
> `KEY:MWORKA` - Masterwork (Armor)\
> `KEY:MWORKI` - Masterwork (Instrument)\
> `KEY:MWORKT` - Masterwork (Tool)\
> `KEY:MWORKW` - Masterwork (Weapon/Ammo)\
> `KEY:NONHUMANOID` - Nonhumanoid (Armor)\
> `KEY:PAPER` - Paper\
> `KEY:PARCHMENT` - Parchment\
> `KEY:PLUS1A` - +1 (Enhancement to Armor)\
> `KEY:PLUS1S` - +1 (Enhancement to Shield)\
> `KEY:PLUS1W` - +1 (Enhancement to Weapon or Ammunition)\
> `KEY:PLUS2A` - +2 (Enhancement to Armor)\
> `KEY:PLUS2S` - +2 (Enhancement to Shield)\
> `KEY:PLUS2W` - +2 (Enhancement to Weapon or Ammunition)\
> `KEY:PLUS3A` - +3 (Enhancement to Armor)\
> `KEY:PLUS3S` - +3 (Enhancement to Shield)\
> `KEY:PLUS3W` - +3 (Enhancement to Weapon or Ammunition)\
> `KEY:PLUS4A` - +4 (Enhancement to Armor)\
> `KEY:PLUS4S` - +4 (Enhancement to Shield)\
> `KEY:PLUS4W` - +4 (Enhancement to Weapon or Ammunition)\
> `KEY:PLUS5A` - +5 (Enhancement to Armor)\
> `KEY:PLUS5S` - +5 (Enhancement to Shield)\
> `KEY:PLUS5W` - +5 (Enhancement to Weapon or Ammunition)\
> `KEY:REFLC` - Reflecting\
> `KEY:RES_ACD_GRT` - Acid Resistance (Greater)\
> `KEY:RES_CLD_GRT` - Cold Resistance (Greater)\
> `KEY:RES_ELE_GRT` - Electricity Resistance (Greater)\
> `KEY:RES_FR_GRT` - Fire Resistance (Greater)\
> `KEY:RES_SNC_GRT` - Sonic Resistance (Greater)\
> `KEY:RETRN` - Returning\
> `KEY:ROPE` - Rope\
> `KEY:RST_ACD` - Acid Resistance\
> `KEY:RST_ACD_IMP` - Acid Resistance (Improved)\
> `KEY:RST_CLD` - Cold Resistance\
> `KEY:RST_CLD_IMP` - Cold Resistance (Improved)\
> `KEY:RST_ELE` - Electricity Resistance Lightning Resistance\
> `KEY:RST_ELE_IMP` - Electricity Resistance (Improved)\
> `KEY:RST_FR` - Fire Resistance\
> `KEY:RST_FR_IMP` - Fire Resistance (Improved)\
> `KEY:RST_SNC` - Sonic Resistance\
> `KEY:RST_SNC_IMP` - Sonic Resistance (Improved)\
> `KEY:SCROLL_ARCANE` - SCROLL (Arcane)\
> `KEY:SCROLL_DIVINE` - SCROLL (Divine)\
> `KEY:SCROLL_MAJOR` - SCROLL(Major)\
> `KEY:SCROLL_MEDIUM` - SCROLL (Medium)\
> `KEY:SCROLL_MINOR` - SCROLL (Minor)\
> `KEY:SEEK` - Seeking\
> `KEY:SHDW` - Shadow\
> `KEY:SHDW_GRT` - Shadow (Greater)\
> `KEY:SHDW_IMP` - Shadow (Improved)\
> `KEY:SHK_BR_A` - Shocking Burst\
> `KEY:SHK_BR_M` - Shocking Burst\
> `KEY:SHK_BR_R` - Shocking Burst\
> `KEY:SHOCK_A` - Shock\
> `KEY:SHOCK_M` - Shock\
> `KEY:SHOCK_R` - Shock\
> `KEY:SILK` - Silk\
> `KEY:SILVER` - Silver\
> `KEY:SLK` - Slick\
> `KEY:SLK_GRT` - Slick (Greater)\
> `KEY:SLK_IMP` - Slick (Improved)\
> `KEY:SLNT_MV` - Silent moves\
> `KEY:SLNT_MV_GRT` - Silent moves (Greater)\
> `KEY:SLNT_MV_IM` - Silent moves (Improved)\
> `KEY:SPEED` - Speed\
> `KEY:SPELL_RES_13` - Spell Resistance (SR 13)\
> `KEY:SPELL_RES_15` - Spell Resistance (SR 15)\
> `KEY:SPELL_RES_17` - Spell Resistance (SR 17)\
> `KEY:SPELL_RES_19` - Spell Resistance (SR 19)\
> `KEY:SPELLFOCUS` - Spell Focus Value\
> `KEY:SPELLMATERIAL` - Spell Material Component Value\
> `KEY:SPIKE_A` - Armor Spikes\
> `KEY:SPIKE_S` - Shield Spikes\
> `KEY:SPIKE_SB` - Shield Bash\
> `KEY:SPL_1USE` - Spell Effect (Single Use/Use Activated)\
> `KEY:SPL_ACT` - Spell Effect (Use Activated)\
> `KEY:SPL_CHRG` - Spell Effect (50 Charges/Spell Trigger)\
> `KEY:SPL_CMD` - Spell Effect (Command Word)\
> `KEY:SPL_CON_ROUND` - |Spell Effect (Continuous/Spell duration
> measured in rounds)\
> `KEY:SPL_CON_MINUTES` - |Spell Effect (Continuous/Spell duration 1
> minute/level)\
> `KEY:SPL_CON_HOURS` - |Spell Effect (Continuous/Spell duration 10
> minutes/level)\
> `KEY:SPL_CON_DAYS` - |Spell Effect (Continuous/Spell duration 24-hours
> or more)\
> `KEY:SPL_STR` - Spell Storing\
> `KEY:SPL_RST` - Spell Resistance <span class="new"> (deprecated)
> </span>\
> `KEY:STEEL` - Mundane (Weapon/Ammo)\
> `KEY:STONE` - Stone\
> `KEY:THNDR_A` - Thundering\
> `KEY:THNDR_M` - Thundering\
> `KEY:THNDR_R` - Thundering\
> `KEY:THROW` - Throwing\
> `KEY:THROWN_AMMO` - Thrown Ammunition\
> `KEY:UNDEAD` - Undead controlling\
> `KEY:UNHLY_A` - Unholy\
> `KEY:UNHLY_M` - Unholy\
> `KEY:UNHLY_R` - Unholy\
> `KEY:VICIOU` - Vicious\
> `KEY:VORPAL` - Vorpal\
> `KEY:WAX` - Wax\
> `KEY:WILD_A` - Wild\
> `KEY:WILD_S` - Wild\
> `KEY:WOOD` - Mundane (Weapon/Ammo)\
> `KEY:WOUND` - Wounding\
>
> **RSRD - Divine File.**
>
> `KEY:SDA_POWER_OF_NATURE` - Power of Nature\
> `KEY:SDA_UNDEAD_MASTERY` - Undead Mastery\
>
> **RSRD - Epic File.**
>
> `KEY:ACID_BLAST_AMMO` - Acidic Blast\
> `KEY:ACID_BLAST_MELEE` - Acidic Blast\
> `KEY:ACID_BLAST_RANGED` - Acidic Blast\
> `KEY:ACID_WARD` - Acid Warding\
> `KEY:ARROW_DEFLECT_EXC` - Exceptional Arrow Deflection\
> `KEY:ARROW_DEFLECT_INF` - Infinite Arrow Deflection\
> `KEY:CHAOS_POWER_AMMO` - Anarchic Energy\
> `KEY:CHAOS_POWER_MELEE` - Anarchic Energy\
> `KEY:CHAOS_POWER_RANGED` - Anarchic Energy\
> `KEY:COLD_WARD` - Cold Warding\
> `KEY:DISRUPTION_MIGHTY` - Mighty Disruption\
> `KEY:DISTANT_SHOT` - Distant Shot\
> `KEY:DREAD_AMMO` - Dread\
> `KEY:DREAD_MELEE` - Dread\
> `KEY:DREAD_RANGED` - Dread\
> `KEY:ELECTRIC_WARD` - Lightning Warding\
> `KEY:EPIC_ABILITY_BONUS_ENHANCE` - |Epic Ability Bonus (Enhancement)\
> `KEY:EPIC_AC_BONUS_DEFLECT` - |Epic AC Bonus (Deflection)\
> `KEY:EPIC_AC_BONUS_LUCK` - |Epic AC Bonus (Luck)\
> `KEY:EPIC_AC_BONUS_INSIGHT` - |Epic AC Bonus (Insight)\
> `KEY:EPIC_AC_BONUS_SACRED` - |Epic AC Bonus (Sacred)\
> `KEY:EPIC_AC_BONUS_PROFANE` - |Epic AC Bonus (Profane)\
> `KEY:EPIC_AC_BONUS_OTHER` - |Epic AC Bonus (Other)\
> `KEY:EPIC_BONUS_ARMR_ENHANCE` - |Epic Armor Bonus (Enhancement)\
> `KEY:EPIC_BONUS_SPELL` - |Epic Bonus Spell\
> `KEY:EPIC_NATURAL_ARMR_ENHANCE` - |Epic Natural Armor Bonus
> (Enhancement)\
> `KEY:EPIC_SAVE_BONUS_INSIGHT` - |Epic Save Bonus (Insight)\
> `KEY:EPIC_SAVE_BONUS_LUCK` - |Epic Save Bonus (Luck)\
> `KEY:EPIC_SAVE_BONUS_OTHER` - |Epic Save Bonus (Other)\
> `KEY:EPIC_SAVE_BONUS_PROFANE` - |Epic Save Bonus (Profane)\
> `KEY:EPIC_SAVE_BONUS_SACRED` - |Epic Save Bonus (Sacred)\
> `KEY:EPIC_SAVE_BONUS_RES` - |Epic Save Bonus (Resistance)\
> `KEY:EPIC_SKILL_BONUS_COMPETANCE` - |Epic Skill Bonus (Competance)\
> `KEY:EPIC_SPELL_RES` - |Epic Spell Resistance\
> `KEY:EVERDANCING` - Everdancing\
> `KEY:FIRE_BLAST_AMMO` - Fiery Blast\
> `KEY:FIRE_BLAST_MELEE` - Fiery Blast\
> `KEY:FIRE_BLAST_RANGED` - Fiery Blast\
> `KEY:FIRE_WARD` - Fire Warding\
> `KEY:HOLY_POWER_AMMO` - Holy Power\
> `KEY:HOLY_POWER_MELEE` - Holy Power\
> `KEY:HOLY_POWER_RANGED` - Holy Power\
> `KEY:ICE_BLAST_AMMO` - Icy Blast\
> `KEY:ICE_BLAST_MELEE` - Icy Blast\
> `KEY:ICE_BLAST_RANGED` - Icy Blast\
> `KEY:INVULN_GRT_5E` - Greater Invulnerability (+6)\
> `KEY:INVULN_GRT_10E` - Greater Invulnerability (+7)\
> `KEY:INVULN_GRT_10M` - Greater Invulnerability (+4)\
> `KEY:INVULN_GRT_15M` - Greater Invulnerability (+5)\
> `KEY:LAW_POWER_AMMO` - Axiomatic Power\
> `KEY:LAW_POWER_MELEE` - Axiomatic Power\
> `KEY:LAW_POWER_RANGED` - Axiomatic Power\
> `KEY:NEGATING` - Negating\
> `KEY:PLUS_6_ARMR` - +6 (Enhancement to Armor)\
> `KEY:PLUS_6_SHLD` - +6 (Enhancement to Shield)\
> `KEY:PLUS_6_WEAP` - +6 (Enhancement to Weapon or Ammunition)\
> `KEY:PLUS_7_ARMR` - +7 (Enhancement to Armor)\
> `KEY:PLUS_7_SHLD` - +7 (Enhancement to Shield)\
> `KEY:PLUS_7_WEAP` - +7 (Enhancement to Weapon or Ammunition)\
> `KEY:PLUS_8_ARMR` - +8 (Enhancement to Armor)\
> `KEY:PLUS_8_SHLD` - +8 (Enhancement to Shield)\
> `KEY:PLUS_8_WEAP` - +8 (Enhancement to Weapon or Ammunition)\
> `KEY:PLUS_9_ARMR` - +9 (Enhancement to Armor)\
> `KEY:PLUS_9_SHLD` - +9 (Enhancement to Shield)\
> `KEY:PLUS_9_WEAP` - +9 (Enhancement to Weapon or Ammunition)\
> `KEY:PLUS_10_ARMR` - +10 (Enhancement to Armor)\
> `KEY:PLUS_10_SHLD` - +10 (Enhancement to Shield)\
> `KEY:PLUS_10_WEAP` - +10 (Enhancement to Weapon or Ammunition)\
> `KEY:REFLECT_GRT` - Greater Reflection\
> `KEY:SCROLL_ARCANE_EPIC` - |Spell Effect (Single Use/Completion)\
> `KEY:SCROLL_DIVINE_EPIC` - |Spell Effect (Single Use/Completion)\
> `KEY:SHOCK_BLAST_AMMO` - Lightning Blast\
> `KEY:SHOCK_BLAST_MELEE` - Lightning Blast\
> `KEY:SHOCK_BLAST_RANGED` - Lightning Blast\
> `KEY:SONIC_BLAST_AMMO` - Sonic Blast\
> `KEY:SONIC_BLAST_MELEE` - Sonic Blast\
> `KEY:SONIC_BLAST_RANGED` - Sonic Blast\
> `KEY:SONIC_WARD` - Sonic Warding\
> `KEY:SPELL_RES_21` - Greater Spell Resistance (SR 21)\
> `KEY:SPELL_RES_23` - Greater Spell Resistance (SR 23)\
> `KEY:SPELL_RES_25` - Greater Spell Resistance (SR 25)\
> `KEY:SPELL_RES_27` - Greater Spell Resistance (SR 27)\
> `KEY:TRIPLE_THROW` - Triple Throw\
> `KEY:UNERRING_ACCURACY` - Unerring Accuracy\
> `KEY:UNHOLY_POWER_AMMO` - Unholy Power\
> `KEY:UNHOLY_POWER_MELEE` - Unholy Power\
> `KEY:UNHOLY_POWER_RANGED` - Unholy Power\
>
> **RSRD - Psionics File.**
>
> `KEY:APORT` - Aporter\
> `KEY:AVRTR` - Averter\
> `KEY:BODYFEED` - Bodyfeeder\
> `KEY:COLLI_A` - Collision (+2)\
> `KEY:COLLI_M` - Collision (+2)\
> `KEY:COLLI_R` - Collision (+2)\
> `KEY:COUPGR_A` - Coup de Grace (+5)\
> `KEY:COUPGR_M` - Coup de Grace (+5)\
> `KEY:COUPGR_R` - Coup de Grace (+5)\
> `KEY:CRYS_DEEP` - Crystal (Deep)\
> `KEY:CRYS_DEEP_ITEM` - Crystal (Deep)\
> `KEY:CRYS_MUN` - Crystal (Mundane)\
> `KEY:CRYS_MUN_ITEM` - Crystal (Mundane)\
> `KEY:DISLOC_A` - Dislocator (+3)\
> `KEY:DISLOC_GRT_A` - Dislocator (Greater) (+4)\
> `KEY:DISLOC_GRT_M` - Dislocator (Greater) (+4)\
> `KEY:DISLOC_GRT_R` - Dislocator (Greater) (+4)\
> `KEY:DISLOC_M` - Dislocator (+3)\
> `KEY:DISLOC_R` - Dislocator (+3)\
> `KEY:DISSIP` - Dissipater\
> `KEY:ECTOPLAS` - Ectoplasmic\
> `KEY:FLOAT` - Floating\
> `KEY:GLEAM` - Gleaming\
> `KEY:HEART` - Heartening\
> `KEY:LANDI` - Landing\
> `KEY:LNKED` - Linked\
> `KEY:LUCKY` - Lucky\
> `KEY:MANIF_SHLD` - Manifester\
> `KEY:MANIF_WPN_M` - Manifester\
> `KEY:MANIF_WPN_R` - Manifester\
> `KEY:MNDARMR` - Mindarmor\
> `KEY:MINDCRU` - Mindcrusher\
> `KEY:MINDFEED` - Mind Feeder\
> `KEY:PARRYING` - Parrying\
> `KEY:PHASING` - Phasing\
> `KEY:PKIN_A` - Psychokinetic\
> `KEY:PKIN_BR_A` - Psychokinetic Burst\
> `KEY:PKIN_BR_M` - Psychokinetic Burst\
> `KEY:PKIN_BR_R` - Psychokinetic Burst\
> `KEY:PKIN_M` - Psychokinetic\
> `KEY:PKIN_R` - Psychokinetic\
> `KEY:PSIBANE_A` - Psibane\
> `KEY:PSIBANE_M` - Psibane\
> `KEY:PSIBANE_R` - Psibane\
> `KEY:PSIBLADE` - Psionic Blade\
> `KEY:PSYCHIC` - Psychic\
> `KEY:PWR_CRWL` - |Power Effect (Single Use/Use Activated)\
> `KEY:PWR_DRJ` - |Power Effect (50 Charges/Power Trigger)\
> `KEY:PWR_PCWN_1` - |Power Effect (Power Trigger/1st Power)\
> `KEY:PWR_PCWN_2` - |Power Effect (Power Trigger/2nd Power)\
> `KEY:PWR_PCWN_3` - |Power Effect (Power Trigger/3+ Power)\
> `KEY:PWR_PS` - |Power Effect (Single Use/Completion)\
> `KEY:PWR_PT` - |Power Effect (Single Use/Use Activated)\
> `KEY:PWR_PT_P` - |Power Effect (Single Use/Use Activated/Personal)\
> `KEY:PWRRST_13` - Power Resistance (13)\
> `KEY:PWRRST_15` - Power Resistance (15)\
> `KEY:PWRRST_17` - Power Resistance (17)\
> `KEY:PWRRST_19` - Power Resistance (19)\
> `KEY:PWRSTOR` - Power Storing\
> `KEY:QUICKN` - Quickness\
> `KEY:RADIANT` - Radiant\
> `KEY:RNGD` - Ranged\
> `KEY:SEEING` - Seeing\
> `KEY:SOULBREAK` - Soulbreaker\
> `KEY:SUNDERER` - Sunderer\
> `KEY:SUPPRESS_A` - Suppression\
> `KEY:SUPPRESS_M` - Suppression\
> `KEY:SUPPRESS_R` - Suppression\
> `KEY:T_PSIBLADE` - Thrown Psiblade\
> `KEY:TIMEBUT` - Time Buttress\
> `KEY:TPORTING` - Teleporting\
> `KEY:VANISH` - Vanishing\
> `KEY:WALL` - Wall\
>
> **RSRD - EQUIPMODE EXCLUDED**

------------------------------------------------------------------------

<span id="msrd"></span> **Wizards of the Coast(WotC): Modern Standard
Reference Documen (MSRD)** - d20 Modern (Modern)

> **MSRD - Arcana Basics File.**
>
> `KEY:ACID_RES` - Acid Resistance\
> `KEY:ACIDIC` - Acidic\
> `KEY:ANIMATED` - Animated\
> `KEY:ARMR_PIERCING` - Armor Piercing\
> `KEY:BANE_AMMO` - Bane\
> `KEY:BANE_MELEE` - Bane\
> `KEY:BANE_RANGED` - Bane\
> `KEY:BASH_HVY` - Bashing\
> `KEY:BASH_LT` - Bashing\
> `KEY:BLADEGUN1` - Bladegun\
> `KEY:BLADEGUN2` - Bladegun\
> `KEY:BLADEGUN3` - Bladegun\
> `KEY:BLINDING` - Blinding\
> `KEY:BRILNT_MELEE` - Brilliant\
> `KEY:BUMP_BLAST` - Bumpers of Blasting\
> `KEY:BUMP_RAM` - Bumper of the Ram\
> `KEY:CATCHING` - Catching\
> `KEY:CHAOTIC_MELEE` - Chaotic\
> `KEY:CHAOTIC_RANGED` - Chaotic\
> `KEY:CHARGED_ITEM_7` - Charges (7)\
> `KEY:COLD_RES` - Cold Resistance\
> `KEY:CPNT_ABLATV` - Ablative Paint Job\
> `KEY:CPNT_BLUR` - Paint Job of Blurring\
> `KEY:CPNT_FLAME` - Flame Job\
> `KEY:CPNT_NDSCRPT` - Nondescript Paint Job\
> `KEY:CPNT_SHRNK` - Shrinking Paint Job\
> `KEY:CTAR_TRNKMSK` - Trunk of Masking\
> `KEY:DAMAGE_REDUCT_5` - Damage Reduction (5/+1)\
> `KEY:DAMAGE_REDUCT_10` - Damage Reduction (10/+1)\
> `KEY:DANCING` - Dancing\
> `KEY:DBL_SIDED` - Double-sided\
> `KEY:DEFENDING` - Defending\
> `KEY:DISRUPTING` - Disruption\
> `KEY:DISTANCE` - Distance\
> `KEY:ELAC_PRLTCAL` - Paralytic Alarm\
> `KEY:ELEC_RES` - Electricity Resistance\
> `KEY:ELAC_SLNTWRN` - Silent Warning Alarm\
> `KEY:ENERGY_BLAST_ACID` - Acid Blast\
> `KEY:ENERGY_BLAST_COLD` - Icy Blast\
> `KEY:ENERGY_BLAST_ELEC` - Electrical Blast\
> `KEY:ENERGY_BLAST_FIRE` - Fiery Blast\
> `KEY:ENERGY_BLAST_SONIC` - Concussive Blast\
> `KEY:ENGN_INFSPD` - Engine of Infernal Speed\
> `KEY:EVIL_MELEE` - Unholy\
> `KEY:EVIL_RANGED` - Unholy\
> `KEY:FIRE_RES` - Fire Resistance\
> `KEY:FLAMING_MELEE` - Flaming\
> `KEY:FLAMING_RANGED` - Flaming\
> `KEY:FLECHETTE_AMMO` - Flechette\
> `KEY:FORT_HVY` - Fortification (Heavy)\
> `KEY:FORT_LT` - Fortification (Light)\
> `KEY:FORT_MODERATE` - Fortification (Moderate)\
> `KEY:FRANGIBLE_AMMO` - Frangible\
> `KEY:FROST_MELEE` - Frost\
> `KEY:FROST_RANGED` - Frost\
> `KEY:GHOST_ARMR` - Ghost Touch\
> `KEY:GHOST_MELEE` - Ghost touch\
> `KEY:GLAMER` - Glamered\
> `KEY:GOOD_MELEE` - Holy\
> `KEY:GOOD_RANGED` - Holy\
> `KEY:HDLT_BLND` - Headlights of Blinding\
> `KEY:HI_EXPLOSIVE` - High Explosive\
> `KEY:HOSI_BLST` - Horn of Blasting\
> `KEY:HOSI_DRED` - Horn of Dread\
> `KEY:KEEN` - Keen\
> `KEY:LAWFUL_MELEE` - Lawful\
> `KEY:LAWFUL_RANGED` - Lawful\
> `KEY:MERCIFUL_MELEE` - Merciful\
> `KEY:MERCIFUL_RANGED` - Merciful\
> `KEY:MIGHTY_CLEAVE` - Mighty Cleaving\
> `KEY:NAKAMURA_ANGR` - Nakamura Blade / Personality (Angry) /\
> `KEY:NAKAMURA_BLDT` - Nakamura Blade / Personality (Bloodthirsty) /\
> `KEY:NAKAMURA_IMPT` - Nakamura Blade / Personality (Impatient) /\
> `KEY:NAKAMURA_INST` - Nakamura Blade / Personality (Insightful) /\
> `KEY:NAKAMURA_PCLV` - Nakamura Blade / Personality (Peace Loving) /\
> `KEY:NAKAMURA_PTNT` - Nakamura Blade / Personality (Patient) /\
> `KEY:NAKAMURA_STHG` - Nakamura Blade / Personality (Soothing) /\
> `KEY:NAKAMURA_VLNT` - Nakamura Blade / Personality (Violent) /\
> `KEY:NEAC_FDOL` - Fuzzy Dice of Luck\
> `KEY:NEAC_FIG_HUM` - Dashboard Figurine \[humorous\]\
> `KEY:NEAC_FIG_MON` - Dashboard Figurine \[monstrous\]\
> `KEY:NEAC_FIG_REL` - Dashboard Figurine \[religious\]\
> `KEY:RETURNING` - Returning\
> `KEY:RUBBER_ROUND` - Rubber Round\
> `KEY:SEAT_HLDMNSTR` - Seat of Hold Monster\
> `KEY:SEAT_SAFETY` - Seats of Safety\
> `KEY:SHADOW` - Shadow\
> `KEY:SHOCK_MELEE` - Shock\
> `KEY:SHOCK_RANGED` - Shock\
> `KEY:SILENT_MOVES` - Silent Moves\
> `KEY:SILVER_AMMO` - Silver\
> `KEY:SLICK` - Slick\
> `KEY:SONIC_RES` - Sonic Resistance\
> `KEY:SPEED` - Speed\
> `KEY:SPELL_RES_15` - Spell Resistance 15\
> `KEY:SPELL_RES_19` - Spell Resistance 19\
> `KEY:SPELL_RES_23` - Spell Resistance 23\
> `KEY:SPONSOR` - Sponsorship\
> `KEY:SUBSONIC_AMMO` - Subsonic\
> `KEY:THUNDER_MELEE` - Thundering\
> `KEY:THUNDER_RANGED` - Thundering\
> `KEY:TIRE_IMPVS` - Impervious Tires\
> `KEY:TIRE_REINFLT` - Reinflating Tires\
> `KEY:TIRE_ZEPHYR` - Zephyr Tires\
> `KEY:TRACER_AMMO` - Tracer\
> `KEY:WHITE_PHOSPHOR` - White Phosphorous\
> `KEY:WNDW_DCPTN` - Windows of Deception\
> `KEY:WOUNDING` - Wounding\
>
> **MSRD - Modern Basics File.**
>
> `KEY:AAVEHICLE` - Vehicle\
> `KEY:ADD_TYPE` - \#Add Type\
> `KEY:ALUMINIUM` - Aluminium\
> `KEY:AUTOFIRE` - Autofire\
> `KEY:BURSTFIRE` - Burst fire\
> `KEY:CERAMIC` - Ceramic\
> `KEY:CLOTH` - Cloth\
> `KEY:CONCRETE` - Concrete\
> `KEY:DBLTAP` - Double Tap fire\
> `KEY:GLASS` - Glass\
> `KEY:ICE` - Ice\
> `KEY:ILLUMINATOR` - Illuminator\
> `KEY:ILLUMINATOR` - \#Illuminator\
> `KEY:LSR_SIGHT` - Laser Sight\
> `KEY:LSR_SIGHT` - \#Laser Sight\
> `KEY:MASTERCRAFT_ARMR_1` - Mastercraft +1\
> `KEY:MASTERCRAFT_ARMR_2` - Mastercraft +2\
> `KEY:MASTERCRAFT_ARMR_3` - Mastercraft +3\
> `KEY:MASTERCRAFT_SHLD_1` - Mastercraft +1\
> `KEY:MASTERCRAFT_SHLD_2` - Mastercraft +2\
> `KEY:MASTERCRAFT_SHLD_3` - Mastercraft +3\
> `KEY:MASTERCRAFT_TOOL_1` - Mastercraft +1\
> `KEY:MASTERCRAFT_TOOL_2` - Mastercraft +2\
> `KEY:MASTERCRAFT_TOOL_3` - Mastercraft +3\
> `KEY:MASTERCRAFT_WEAP_DAM_1` - Mastercraft +1 Damage\
> `KEY:MASTERCRAFT_WEAP_DAM_2` - Mastercraft +2 Damage\
> `KEY:MASTERCRAFT_WEAP_DAM_3` - Mastercraft +3 Damage\
> `KEY:MASTERCRAFT_WEAP_HIT_1` - Mastercraft +1 To Hit\
> `KEY:MASTERCRAFT_WEAP_HIT_2` - Mastercraft +2 To Hit\
> `KEY:MASTERCRAFT_WEAP_HIT_3` - Mastercraft +3 To Hit\
> `KEY:MWORKA` - Masterwork\
> `KEY:MWORKT` - Masterwork\
> `KEY:MWORKW` - Masterwork\
> `KEY:PLASTIC_HARD` - Hard Plastic\
> `KEY:PLASTIC_SOFT` - Soft Plastic\
> `KEY:PAPER` - Paper\
> `KEY:ROPE` - Rope\
> `KEY:SCP_ELE_OP` - Scope (Electro-optical)\
> `KEY:SCP_STD` - Scope (Standard)\
> `KEY:SCP_STD` - \#Scope (Standard)\
> `KEY:SPEED_LD` - Speed Loader\
> `KEY:SPPRSS_PIS` - Suppressor (Pistol)\
> `KEY:SPPRSS_RFL` - Suppressor (Rifle)\
> `KEY:SPPRSS_RFL` - \#Suppressor (Rifle)\
> `KEY:STEEL` - Steel\
> `KEY:UPGRADE` - Upgrade\
> `KEY:WOOD` - Wood\
>
> **MSRD - Modern FX File.**
>
> `KEY:CHARGED_ITEM_3` - Charges (3)\
> `KEY:CHARGED_ITEM_5` - Charges (5)\
> `KEY:CHARGED_ITEM_10` - Charges (10)\
> `KEY:CHARGED_ITEM_12` - Charges (12)\
> `KEY:CHARGED_ITEM_14` - Charges (14)\
> `KEY:CHARGED_ITEM_36` - Charges (36)\
> `KEY:CHARGED_ITEM_50` - Charges (50)\
> `KEY:CHARGED_ITEM_101` - Charges (101)\
> `KEY:PLUS1A` - +1 (Enhancement to Armor)\
> `KEY:PLUS1S` - +1 (Enhancement to Shield)\
> `KEY:PLUS1W` - +1 (Enhancement to Weapon\
> `KEY:PLUS2A` - +2 (Enhancement to Armor)\
> `KEY:PLUS2S` - +2 (Enhancement to Shield)\
> `KEY:PLUS2W` - +2 (Enhancement to Weapon)\
> `KEY:PLUS3A` - +3 (Enhancement to Armor)\
> `KEY:PLUS3S` - +3 (Enhancement to Shield)\
> `KEY:PLUS3W` - +3 (Enhancement to Weapon)\
> `KEY:PLUS4A` - +4 (Enhancement to Armor)\
> `KEY:PLUS4S` - +4 (Enhancement to Shield)\
> `KEY:PLUS4W` - +4 (Enhancement to Weapon)\
> `KEY:PLUS5A` - +5 (Enhancement to Armor)\
> `KEY:PLUS5S` - +5 (Enhancement to Shield)\
> `KEY:PLUS5W` - +5 (Enhancement to Weapon)\
> `KEY:SCROLL_ARCANE` - |Spell Effect (Arcane Scroll)\
> `KEY:SCROLL_DIVINE` - |Spell Effect (Divine Scroll)\
> `KEY:SPL_1USE` - |Spell Effect (Single Use/Use Activated)\
> `KEY:SPL_ACT_RING` - |Spell Effect (Use Activated Ring)\
> `KEY:SPL_CHRG` - |Spell Effect (50 Charges/Spell Trigger)\
> `KEY:TATTOO_ARCANE` - |Spell Effect (Arcane Tattoo)\
> `KEY:TATTOO_DIVINE` - |Spell Effect (Divine Tattoo)\
> `KEY:TATTOO_PSIONIC` - |Power Effect (Psionic Tattoo)\
>
> **MSRD - Future Cybernetics File.**
>
> `KEY:ARTIFICIALORGAN` - Artificial Organ\
> `KEY:EDUCATEDFEATIMPLANT` - Educated Feat Implant\
> `KEY:SKILLIMPLANT` - Skill Implant\
>
> **MSRD - Future Equipment File.**
>
> `KEY:AASTARSHIP_LB` - Starship\
> `KEY:AASTARSHIP_TON` - Starship\
> `KEY:AAVEHICLE_FUTURE` - Vehicle\
> `KEY:ALT_WPN_GDGT` - Alternate Weapon Gadget\
> `KEY:ANTI_ACCDNT_SYS` - Anti-Accident System\
> `KEY:AOO_PNT_DEF_SYS` - Point-defense system\
> `KEY:ARMR_ABLATIVE` - Ablative Armor\
> `KEY:ARMR_ALLOY_PLATING` - Alloy Plating Armor\
> `KEY:ARMR_CERAMETAL` - Cerametal Armor\
> `KEY:ARMR_DEFLECTIVE` - Deflective Armor\
> `KEY:ARMR_NANOFLUIDIC` - Nanofluidic Armor\
> `KEY:ARMR_NEUTRONITE` - Neutronite Armor\
> `KEY:ARMR_POLYMERIC` - Polymeric Armor\
> `KEY:ARMR_VANADIUM` - Vanadium Armor\
> `KEY:ATFR_MDL_GDGT` - Autofire Module Gadget\
> `KEY:ATLDR_MDL_GDGT` - Autoloader Module Gadget\
> `KEY:ATTK_ANTIMATTER` - Antimatter Gun\
> `KEY:ATTK_ANTIMATTER_4B` - Battery of 4 Antimatter Guns\
> `KEY:ATTK_AUTOMASER` - Blacklaser\
> `KEY:ATTK_BLACKLASER` - Blacklaser\
> `KEY:ATTK_CHE_MISSL` - CHE Missile Launcher\
> `KEY:ATTK_CHE_MISSL_2` - 2 CHE Missile Launcher\
> `KEY:ATTK_CHE_MISSL_2B_2` - 2 Batteries of 2 CHE Missile Launcher\
> `KEY:ATTK_CHE_MISSL_3B` - Battery of 3 CHE Missile Launcher\
> `KEY:ATTK_EMP_CANN` - EMP Cannon\
> `KEY:ATTK_FUSN_BEAM` - Fusion Beam\
> `KEY:ATTK_FUSN_BEAM_2L` - 2 fire-linked Fusion Beams\
> `KEY:ATTK_FUSN_BEAM_4B` - Battery of 4 Fusion Beams\
> `KEY:ATTK_GAUSS_GUN` - Gauss Gun\
> `KEY:ATTK_GAUSS_GUN_3B` - Battery of 3 Gauss Guns\
> `KEY:ATTK_HLASER` - Heavy Laser\
> `KEY:ATTK_HLASER_2L` - 2 fire-linked Heavy Laser\
> `KEY:ATTK_HLASER_3B` - Battery of 3 Heavy Laser\
> `KEY:ATTK_HLASER_4B` - Battery of 4 Heavy Laser\
> `KEY:ATTK_HLASER_4L` - 4 fire-linked Heavy Laser\
> `KEY:ATTK_HMASER_CANN` - Heavy Maser Cannon\
> `KEY:ATTK_HMASS_CANN` - Heavy Mass Cannon\
> `KEY:ATTK_HMASS_CANN_4B` - Battery of 4 heavy Mass Cannons\
> `KEY:ATTK_HNTRN_GUN` - Heavy Neutron Gun\
> `KEY:ATTK_HNTRN_GUN_2F` - 2 fire-linked Heavy Neutron Guns\
> `KEY:ATTK_HNTRN_GUN_3B` - Battery of 3 Heavy Neutron Guns\
> `KEY:ATTK_HNTRN_GUN_4F` - 4 fire-linked Heavy Neutron Guns\
> `KEY:ATTK_HPRTCL_BEAM` - Heavy Particle Beam\
> `KEY:ATTK_HPTCL_BEAM_3B_2` - 2 Batteries of 3 Heavy Particle Beams\
> `KEY:ATTK_HPTCL_BEAM_4L` - 4 fire-linked Heavy Particle Beams\
> `KEY:ATTK_HPLASM_CANN` - Heavy Plasma Cannon\
> `KEY:ATTK_HPLASM_CANN_2L` - 2 fire-linked Heavy Plasma Cannons\
> `KEY:ATTK_HPLASM_CANN_3L` - 3 fire-linked Heavy Plasma Cannons\
> `KEY:ATTK_KES_MISSL` - KE Submunition Missile Launcher\
> `KEY:ATTK_KNTC_LANCE` - Kinetic Lance\
> `KEY:ATTK_LASER` - Laser\
> `KEY:ATTK_LASER_5B` - Battery of 5 Laser\
> `KEY:ATTK_MASER_CANN` - Maser Cannon\
> `KEY:ATTK_MASER_CANN_2L` - 2 fire-linked Maser Cannons\
> `KEY:ATTK_MASS_CANN` - Mass Cannon\
> `KEY:ATTK_MASS_CANN_5B` - Battery of 5 Mass Cannons\
> `KEY:ATTK_MASS_MISSL` - Mass Reaction Missile Launcher\
> `KEY:ATTK_MASS_MISSL_2L` - 2 fire-linked Mass Reaction Missile
> Launcher\
> `KEY:ATTK_MINELAYER` - Minelayer\
> `KEY:ATTK_NDL_DRVR` - Needle Driver\
> `KEY:ATTK_NTRN_GUN` - Neutron Gun\
> `KEY:ATTK_NTRN_GUN_5B` - Battery of 5 Neutron Guns\
> `KEY:ATTK_NTRNM_DRVR` - Neutronium Driver\
> `KEY:ATTK_NOVA_MISSL` - Nova Burst Missile Launcher\
> `KEY:ATTK_NUKE_MISSL` - Nuclear Missile Launcher\
> `KEY:ATTK_NUKE_MISSL_2` - 2 Nuclear Missile Launcher\
> `KEY:ATTK_NUKE_MISSL_2L` - 2 fire-linked Nuclear Missiles Launcher\
> `KEY:ATTK_PRTCL_BEAM` - Particle Beam\
> `KEY:ATTK_PRTCL_BEAM_2L` - 2 fire-linked Particle Beams\
> `KEY:ATTK_PRTCL_BEAM_4B` - Battery of 4 Particle Beams\
> `KEY:ATTK_PLASMA_CANN` - Plasma Cannon\
> `KEY:ATTK_PLASMA_CANN_4B` - Battery of 4 Plasma Cannons\
> `KEY:ATTK_PLSM_MISSL` - Plasma Missile Launcher\
> `KEY:ATTK_PLSM_MISSL_2B` - Battery of 2 Plasma Missile Launcher\
> `KEY:ATTK_PLSM_MISSL_3B` - Battery of 3 Plasma Missile Launcher\
> `KEY:ATTK_QUNTM_CANN` - Quantum Cannon\
> `KEY:ATTK_QUNTM_CANN_2L` - 2 fire-linked Quantum Cannons\
> `KEY:ATTK_QUNTM_CANN_4L` - 4 fire-linked Quantum Cannons\
> `KEY:ATTK_RAIL_CANNON` - Rail Cannon\
> `KEY:ATTK_RAIL_CANNON_2L` - 2 fire-linked rail Cannons\
> `KEY:ATTK_RAIL_CANNON_4L` - 4 fire-linked rail Cannons\
> `KEY:ATTK_SNGLRT_CANN` - Singularity Cannon\
> `KEY:ATTK_SLIVER_GUN` - Sliver Gun\
> `KEY:ATTK_STRLD_MISSL` - Starload Missile Launcher\
> `KEY:ATTK_STRNG_PRJCTR` - String Projector\
> `KEY:ATTK_ZERO_BORE` - Zero Bore\
> `KEY:AUTOCMP_DRVR_DERVISH` - Dervish AI-400 (Driver Autocomp)\
> `KEY:AUTOCMP_DRVR_PEGASUS` - Pegasus AI-200 (Driver Autocomp\
> `KEY:AUTOCMP_DRVR_ROADLRD` - Roadlord AI-GA (Driver Autocomp\
> `KEY:AUTOCMP_DRVR_TWISTER` - Twister AI-800 (Driver Autocomp\
> `KEY:AUTOCMP_DRVR_ZEPHYR` - Zephyr AI-1200 (Driver Autocomp\
> `KEY:AUTOCMP_GUNR_ADDER` - Adder AI-G2 (Gunner Autocomp)\
> `KEY:AUTOCMP_GUNR_DEADEYE` - Deadeye AI-G4 (Gunner Autocomp\
> `KEY:AUTOCMP_GUNR_HOTSHOT` - Hotshot AI-G8 (Gunner Autocomp)\
> `KEY:AUTOCMP_GUNR_MARKSMN` - Marksman AI-GA (Gunner Autocomp)\
> `KEY:AUTOCMP_GUNR_RTTLSNK` - Rattlesnake AI-GX (Gunner Autocomp)\
> `KEY:BATTERY_OF_2` - Battery of 2\
> `KEY:BATTERY_OF_3` - Battery of 3\
> `KEY:BATTERY_OF_4` - Battery of 4\
> `KEY:BATTERY_OF_5` - Battery of 5\
> `KEY:BB_TRP_GDGT_BRB` - Booby Trapped Gadget (Barbs)\
> `KEY:BB_TRP_GDGT_ELS` - Booby Trapped Gadget (Electric Shock)\
> `KEY:BB_TRP_GDGT_STB` - Booby Trapped Gadget (Stun Bolt)\
> `KEY:BB_TRP_GDGT_TIW` - Booby Trapped Gadget (Trigger Integrated
> Weapon)\
> `KEY:CHMLNC_SRFC_GDGT` - Chameleonic Surface Gadget\
> `KEY:CLLPSBL_GDGT` - Collapsible Gadget\
> `KEY:CMPCT_GDGT_EQP` - Compact Gadget\
> `KEY:CMPCT_GDGT_WPN` - Compact Gadget\
> `KEY:COL_JUMP_DRIVE` - Jump Drive (Colossal)\
> `KEY:COMM_ANSIBLE` - Ansible\
> `KEY:COMM_DRIVE_TRNSCVR` - Drive Transceiver\
> `KEY:COMM_DRIVESAT` - Drivesat Comm Array\
> `KEY:COMM_INTERNAL_AUDIO` - Internal Audio Comm System\
> `KEY:COMM_INTERNAL_VIDEO` - Internal Video Comm System\
> `KEY:COMM_LASER_TRNSCVR` - Laser Transceiver\
> `KEY:COMM_MASS_TRNSCVR` - Mass Transceiver\
> `KEY:COMM_RADIO_TRNSCVR` - Radio Transceiver\
> `KEY:D_DRV_GNRTR8` - D-Drive Generator (PL8)\
> `KEY:D_DRV_GNRTR9` - D-Drive Generator (PL9)\
> `KEY:DFNS_ADV_DMG_CTRL` - Advanced Damage Control\
> `KEY:DFNS_AUTOPILOT` - Autopilot System\
> `KEY:DFNS_CHAFF_LNCH` - Chaff launcher\
> `KEY:DFNS_CHAFF_LNCH_8` - Chaff launcher\
> `KEY:DFNS_CHAFF_LNCH_8_2` - 2 Chaff launchers\
> `KEY:DFNS_CLOAK_SCRN` - Cloaking Screen\
> `KEY:DFNS_DMG_CTRL_SYS` - Damage Control System\
> `KEY:DFNS_DECOY_LNCH` - Decoy drone launcher\
> `KEY:DFNS_DECOY_LNCH_2` - Decoy drone launcher\
> `KEY:DFNS_DECOY_LNCH_4_2` - 2 Decoy drone launchers\
> `KEY:DFNS_DECOY_LNCH_8` - Decoy drone launcher\
> `KEY:DFNS_DISPLACER` - Displacer\
> `KEY:DFNS_HEAVY_FRTFCTN` - Heavy Fortification\
> `KEY:DFNS_IMP_AUTOPILOT` - Improved Autopilot System\
> `KEY:DFNS_IMP_DMG_CTRL` - Improved Damage Control\
> `KEY:DFNS_LGHT_FRTFCTN` - Light Fortification\
> `KEY:DFNS_MGNT_FLD` - Magnetic Field\
> `KEY:DFNS_MEDM_FRTFCTN` - Medium Fortification\
> `KEY:DFNS_NANITE_REPAIR` - Nanite Repair Array\
> `KEY:DFNS_PRTCL_FLD` - Particle Field\
> `KEY:DFNS_RAD_SHLD` - Radiation Shielding\
> `KEY:DFNS_REPAIR_DRONE` - Repair drones\
> `KEY:DFNS_SLF_DSTR_SYS` - Self-destruct System\
> `KEY:DFNS_SNSR_JAM` - Sensor Jammer\
> `KEY:DFNS_STLTH_SCRN` - Stealth Screen\
> `KEY:ENGN_FUSION` - Fusion Torch\
> `KEY:ENGN_GRAVITIC` - Gravitic Redirector\
> `KEY:ENGN_INDCTN` - Induction Engine\
> `KEY:ENGN_INRT_FLUX` - Inertial Flux Engine\
> `KEY:ENGN_ION` - Ion Engine\
> `KEY:ENGN_PARTCL` - Particle Impulse\
> `KEY:ENGN_PHOTON` - Photon Sails\
> `KEY:ENGN_SPATIAL` - Spatial Compressor\
> `KEY:ENGN_THRUST` - Thrusters\
> `KEY:ENVRNMNT_SL_GDGT` - Environment Seal Gadget\
> `KEY:GNTC_TGS_GDGT` - Genetic Tags Gadget\
> `KEY:GRAP_GRAPPLER` - Grappler\
> `KEY:GRAP_TRACTOR_BEAM` - Tractor Beam Emitter\
> `KEY:GRG_JUMP_DRIVE` - Jump Drive (Gargantuan)\
> `KEY:GRVT_ANCHR_GDGT` - Gravity Anchor Gadget\
> `KEY:HGE_JUMP_DRIVE` - Jump Drive (Huge)\
> `KEY:HUD_SFTWR_AMMO_TRK` - HUD Software (Ammunition Tracker)\
> `KEY:HUD_SFTWR_AMMO_TRK_AMR` - HUD Software (Ammunition Tracker)\
> `KEY:HUD_SFTWR_BIOSNSR` - HUD Software (Biosensor)\
> `KEY:HUD_SFTWR_BIOSNSR_AMR` - HUD Software (Biosensor)\
> `KEY:HUD_SFTWR_SNSR_LNK` - HUD Software (Sensor Link)\
> `KEY:HUD_SFTWR_SNSR_LNK_AMR` - HUD Software (Sensor Link)\
> `KEY:HUD_SFTWR_TRGT` - HUD Software (Targetting)\
> `KEY:HUD_SFTWR_TRGT_AMR` - HUD Software (Targetting)\
> `KEY:HUD_SFTWR_VHCL_LNK` - HUD Software (Vehicle Link)\
> `KEY:HUD_SFTWR_VHCL_LNK_AMR` - HUD Software (Vehicle Link)\
> `KEY:INT_EQ_GDGT_AMR` - Integrated Equipment Gadget\
> `KEY:INT_EQ_GDGT_WPN` - Integrated Equipment Gadget\
> `KEY:INT_WPN_GDGT` - Integrated Weapon Gadget\
> `KEY:MDFNS_CLOAK_SCRN` - Cloaking Screen\
> `KEY:MDFNS_DISPLACER` - Displacer\
> `KEY:MDFNS_MGNT_FLD` - Magnetic Field\
> `KEY:MDFNS_PRTCL_FLD` - Particle Field\
> `KEY:MDFNS_STLTH_SCRN` - Stealth Screen\
> `KEY:MLTPL_US_ITM_GDGT` - Multiple Use Item Gadget\
> `KEY:MNTRZD_GDGT_EQP` - Miniaturized Gadget\
> `KEY:MNTRZD_GDGT_WPN` - Miniaturized Gadget\
> `KEY:MRPH_MTL_ALL_GDGT` - Morphic Metal Alloy Gadget\
> `KEY:NEG_GRV_BOOST_GDGT` - Neg-grav Boosters Gadget\
> `KEY:PNT_ON_LCD_GDGT_AMR` - Paint-On LCD Gadget\
> `KEY:PNT_ON_LCD_GDGT_EQP` - Paint-On LCD Gadget\
> `KEY:PNT_ON_LCD_GDGT_WPN` - Paint-On LCD Gadget\
> `KEY:PRHNSL_APPNDG_GDGT` - Prehensile Appendage Gadget\
> `KEY:REMOTE_SHUTDOWN_SYS` - Remote Shutdown System\
> `KEY:RGFD_LSR_SCP_GDGT` - Rangefinding Laser Scope Gadget\
> `KEY:SAT_DTALNK_GDGT` - Satellite Datalink Gadget\
> `KEY:SLF_RPRNG_GDGT` - Self-Repairing Gadget - Armor\
> `KEY:SLF_RPRNG_GDGT_EQM` - Self-Repairing Gadget - Goods\
> `KEY:SND_SPPRSSR_GDGT_EQP` - Sound Suppressor Gadget\
> `KEY:SND_SPPRSSR_GDGT_WPN` - Sound Suppressor Gadget\
> `KEY:SNSR_ACHILLES` - Achilles Targeting Software\
> `KEY:SNSR_BFFLNG_GDGT` - Sensor Baffling Gadget\
> `KEY:SNSR_CLASS_1` - Class I Sensor Array\
> `KEY:SNSR_CLASS_2` - Class II Sensor Array\
> `KEY:SNSR_CLASS_3` - Class III Sensor Array\
> `KEY:SNSR_CLASS_4` - Class IV Sensor Array\
> `KEY:SNSR_CLASS_5` - Class V Sensor Array\
> `KEY:SNSR_CLASS_6` - Class VI Sensor Array\
> `KEY:SNSR_CLASS_7` - Class VII Sensor Array\
> `KEY:SNSR_CLASS_8` - Class VIII Sensor Array\
> `KEY:SNSR_CLASS_9` - Class IX Sensor Array\
> `KEY:SNSR_IMP_TRGT_SYS` - Improved Targeting System\
> `KEY:SNSR_TRGT_SYS` - Targeting System\
> `KEY:SPRNG_LDD_GDGT` - Spring Loaded Gadget\
> `KEY:STN_MDL_GDGT_12` - Stun Module Gadget (Fort DC 12)\
> `KEY:STN_MDL_GDGT_15` - Stun Module Gadget (Fort DC 15)\
> `KEY:STN_MDL_GDGT_18` - Stun Module Gadget (Fort DC 18)\
> `KEY:STOR_CMPRT_GDGT_AMR` - Storage Compartment Gadget\
> `KEY:STOR_CMPRT_GDGT_EQP` - Storage Compartment Gadget\
> `KEY:T_DRV_GNRTR` - Temporal Drive Generator (PL9)\
> `KEY:T_ORG_MUP_GDGT_AMR` - Techno-Organic Makeup Gadget\
> `KEY:T_ORG_MUP_GDGT_WPN` - Techno-Organic Makeup Gadget\
> `KEY:TLPRT_MAG_GDGT` - Teleporting Magazine Gadget\
> `KEY:ULTRLT_CMPSTN_GDGT` - Ultralight Composition Gadget\
> `KEY:VAR_AMMNTN_GDGT` - Variable Ammunition Gadget\
> `KEY:VAR_CHRG_GDGT` - Variable Charge Gadget\
> `KEY:VC_RCGNTN_SYS_GDGT` - Voice Recognition System Gadget\
> `KEY:VHCL_ALUMISTEEL_ARMR` - Alumisteel Armor (PL5)\
> `KEY:VHCL_DURAPLASTC_ARMR` - Duraplastic Armor (PL5)\
> `KEY:VHCL_DURALLOY_ARMR` - Duralloy Armor (PL6)\
> `KEY:VHCL_RESILIUM_ARMR` - Resilium Armor (PL6)\
> `KEY:VHCL_CRSTL_CRBN_ARMR` - Crystal Carbon Armor (PL7)\
> `KEY:VHCL_MEGATANIUM_ARMR` - Megatanium Armor (PL8)\
> `KEY:VHCL_NEOVULCANM_ARMR` - Neovulcanium Armor (PL7)\
> `KEY:VHCL_REACTIVE_ARMR` - Reactive Armor (PL8)\
> `KEY:VID_SCP_GDGT` - Video Scope Gadget\
> `KEY:XP_MGZN_GDGT` - Expanded Magazine Gadget\
>
> **MSRD - Future Mecha File.**
>
> `KEY:A3X_DRGN_FLMTHRWR` - A3X Dragon Flame-Thrower (PL 5)\
> `KEY:ADVANCD_DGNSTCS` - Advanced Diagnostics (PL 7)\
> `KEY:AFTRBRNR_SYS` - Afterburner System (PL6)\
> `KEY:ALUMISTL` - Alumisteel (PL5)\
> `KEY:ALUMISTL_ARMR` - Alumisteel Armor (PL5)\
> `KEY:AMMO_LT5_LNGSHT_MSSDRV` - Ammo bay for LT-5 Longshot Mass Driver\
> `KEY:AMMO_M9_BRRGE_CHAINGUN` - 6 50-round ammo belts for M-9 Barrage
> chaingun\
> `KEY:AMMO_M53_FRST_RCKTLNCH` - 6-rocket pack for M-53 Firestar Rocket
> Launcher\
> `KEY:AMMO_M55_CRUD_RCKTLNCH` - 6-rocket pack for M-55 Crud Rocket
> Launcher\
> `KEY:AMMO_M70_EMP_RCKTLNCHR` - 6-rocket pack for M-70 EMP Rocket
> Launcher\
> `KEY:AMMO_M75_CRKT_RCKTLNCH` - 6-rocket pack for M-75 Cricket Rocket
> Launcher\
> `KEY:AMMO_M87_TALN_MSSLLNCH` - 4-missile pack for M-87 Talon Missile
> Launcher\
> `KEY:AMMO_T95_CVLCD_CHAINGN` - 6 50-round ammo belts for T-95
> Cavalcade Chaingun\
> `KEY:AMMO_WARPTH_RCLLSS_RFL` - 20-round magazine for Warpath
> Recoilless Rifle\
> `KEY:AMMO2_M70_EMP_RCKTLNCHR` - 6-rocket pack for M-70 EMP Rocket
> Launcher\
> `KEY:AMMO2_M87_TALN_MSSLLNCH` - 4-missile pack for M-87 Talon Missile
> Launcher\
> `KEY:BLWK_TAC_SHLD` - Bulwark Tactical Shield (PL5)\
> `KEY:BRCD_TAC_SHLD` - Barricade Tactical Shield (PL7)\
> `KEY:BSTN_TAC_SHLD` - Bastion Tactical Shield (PL6)\
> `KEY:CHRSNTHMM_LSR_ARR` - Chrysanthemum Laser Array (PL 6)\
> `KEY:CL1_SNSR_SYS` - Class I Sensor System (PL6)\
> `KEY:CL2_SNSR_SYS` - Class II Sensor System (PL6)\
> `KEY:CL3_SNSR_SYS` - Class III Sensor System (PL6)\
> `KEY:CL4_SNSR_SYS` - Class IV Sensor System (PL7)\
> `KEY:CL5_SNSR_SYS` - Class V Sensor System (PL7)\
> `KEY:CL6_SNSR_SYS` - Class VI Sensor System (PL8)\
> `KEY:CLOAKING_SCRN` - Cloaking Screen (PL8)\
> `KEY:COCKPIT_COPILOT` - Cockpit (Copilot)\
> `KEY:COCKPIT_PASSNGR` - Cockpit (Passenger)\
> `KEY:COCKPIT_PILOT` - Cockpit (Pilot)\
> `KEY:COL_AVNG_ELCT_SCM` - Avenger Electro-Scimitar (PL 8)\
> `KEY:COL_LK8_AMRPCG_PK` - LK8 Armor-Piercing Pike (PL 6)\
> `KEY:COL_MCH` - Colossal Mecha\
> `KEY:COL_PS15_PNTR_CLW` - PS-15 Panther Claws (PL 5)\
> `KEY:COL_PS25_TIGR_CLW` - PS-25 Tiger Claws (PL 7)\
> `KEY:COL_PTHN_ELCT_WHP` - XJ-A Python Electro-Whip (PL 7)\
> `KEY:COL_QUAD_MCH` - Quadrupedal\
> `KEY:COL_RP91_RPR_LSCT` - RP-91 Reaper Laser Scythe (PL 8)\
> `KEY:COL_THNDRB_SHK_RD` - Thunderbolt Shock Rod (PL 5)\
> `KEY:COMM_SYSTEM` - Comm System\
> `KEY:CORONA_MICROWV_BM` - Corona Microwave Beam (PL 6)\
> `KEY:CRKRJCK_NRL_LNK` - Crackerjack Neural Link (PL 8)\
> `KEY:CRSTLCBN_ARMR` - Crystal Carbon Armor (PL7)\
> `KEY:DEFLECTN_FLD1` - Deflection Field Mk 1(PL8)\
> `KEY:DEFLECTN_FLD2` - Deflection Field Mk 2(PL8)\
> `KEY:DEFLECTN_FLD3` - Deflection Field Mk 3(PL8)\
> `KEY:DEFLECTN_FLD4` - Deflection Field Mk 4(PL8)\
> `KEY:DEFLECTN_FLD5` - Deflection Field Mk 5(PL8)\
> `KEY:DLPHI_DEF_ST1` - Delphi Defense Suite Mk 1 (PL7)\
> `KEY:DLPHI_DEF_ST2` - Delphi Defense Suite Mk 2 (PL7)\
> `KEY:DLPHI_DEF_ST3` - Delphi Defense Suite Mk 3 (PL7)\
> `KEY:DLPHI_DEF_ST4` - Delphi Defense Suite Mk 4 (PL7)\
> `KEY:DLPHI_DEF_ST5` - Delphi Defense Suite Mk 5 (PL7)\
> `KEY:DURALLOY` - Duralloy (PL6)\
> `KEY:DURALLOY_ARMR` - Duralloy Armor (PL6)\
> `KEY:DURPLSTC_ARMR` - Duraplastic Armor (PL5)\
> `KEY:ENGM_SNSR_ST` - Enigma Sensor Suite (PL6)\
> `KEY:GRG_AVNG_ELCT_SCM` - Avenger Electro-Scimitar (PL 8)\
> `KEY:GRG_LK8_AMRPCG_PK` - LK8 Armor-Piercing Pike (PL 6)\
> `KEY:GRG_MCH` - Gargantuan Mecha\
> `KEY:GRG_PS15_PNTR_CLW` - PS-15 Panther Claws (PL 5)\
> `KEY:GRG_PS25_TIGR_CLW` - PS-25 Tiger Claws (PL 7)\
> `KEY:GRG_PTHN_ELCT_WHP` - XJ-A Python Electro-Whip (PL 7)\
> `KEY:GRG_QUAD_MCH` - Quadrupedal\
> `KEY:GRG_RP91_RPR_LSCT` - RP-91 Reaper Laser Scythe (PL 8)\
> `KEY:GRG_THNDRB_SHK_RD` - Thunderbolt Shock Rod (PL 5)\
> `KEY:HEVY_FORTFCTN` - Heavy Fortification (PL9)\
> `KEY:HGE_AVNG_ELCT_SCM` - Avenger Electro-Scimitar (PL 8)\
> `KEY:HGE_LK8_AMRPCG_PK` - LK8 Armor-Piercing Pike (PL 6)\
> `KEY:HGE_MCH` - Huge Mecha\
> `KEY:HGE_PS15_PNTR_CLW` - PS-15 Panther Claws (PL 5)\
> `KEY:HGE_PS25_TIGR_CLW` - PS-25 Tiger Claws (PL 7)\
> `KEY:HGE_PTHN_ELCT_WHP` - XJ-A Python Electro-Whip (PL 7)\
> `KEY:HGE_QUAD_MCH` - Quadrupedal\
> `KEY:HGE_RP91_RPR_LSCT` - RP-91 Reaper Laser Scythe (PL 8)\
> `KEY:HGE_THNDRB_SHK_RD` - Thunderbolt Shock Rod (PL 5)\
> `KEY:HV5_HVN_ESCP_PD` - HV-5 Haven Escape Pod (PL 6)\
> `KEY:JETPACK` - Jetpack (PL6)\
> `KEY:JETASSSTWNGS` - Jet-Assist Wings (PL7)\
> `KEY:LF_SPPRT_SYSTEM` - Life Support System\
> `KEY:LGHT_FORTFCTN` - Light Fortification (PL7)\
> `KEY:LRG_AVNG_ELCT_SCM` - Avenger Electro-Scimitar (PL 8)\
> `KEY:LRG_LK8_AMRPCG_PK` - LK8 Armor-Piercing Pike (PL 6)\
> `KEY:LRG_MCH` - Large Mecha\
> `KEY:LRG_PS15_PNTR_CLW` - PS-15 Panther Claws (PL 5)\
> `KEY:LRG_PS25_TIGR_CLW` - PS-25 Tiger Claws (PL 7)\
> `KEY:LRG_PTHN_ELCT_WHP` - XJ-A Python Electro-Whip (PL 7)\
> `KEY:LRG_QUAD_MCH` - Quadrupedal\
> `KEY:LRG_RP91_RPR_LSCT` - RP-91 Reaper Laser Scythe (PL 8)\
> `KEY:LRG_THNDRB_SHK_RD` - Thunderbolt Shock Rod (PL 5)\
> `KEY:LT5_LNGSHT_MSSDRV` - LT-5 Longshot Mass Driver (PL 8)\
> `KEY:LX10_ANTISHCK` - LX-10 Antishock Array (PL6)\
> `KEY:LX20_ANTISHCK` - LX-20 Antishock Array (PL7)\
> `KEY:M9_BRRGE_CHAINGUN` - M-9 Barrage Chaingun (PL 5)\
> `KEY:M21_COMET_AUTOLSR` - M-21 Comet Autolaser (PL 6)\
> `KEY:M53_FRST_RCKTLNCH` - M-53 Firestar Rocket Launcher (PL 5)\
> `KEY:M55_CRUD_RCKTLNCH` - M-55 Crud Rocket Launcher (PL 5)\
> `KEY:M70_EMP_RCKTLNCHR` - M-70 EMP Rocket Launcher (PL 6)\
> `KEY:M75_CRKT_RCKTLNCH` - M-75 Cricket Rocket Launcher (PL 6)\
> `KEY:M87_TALN_MSSLLNCH` - M-87 Talon Missile Launcher (PL 5)\
> `KEY:MECHA_M300_RHINO_MSSCNN` - M-300 Rhino Mass Cannon (PL 7)\
> `KEY:MEDM_FORTFCTN` - Medium Fortification (PL8)\
> `KEY:MEGATANM` - Megatanium (PL 8)\
> `KEY:MEGATANM_ARMR` - Megatanium Armor (PL8)\
> `KEY:NANOREPAIR_UNIT` - Nanorepair Unit (PL 8)\
> `KEY:NEOVLCNM` - Neovulcanium (PL 7)\
> `KEY:NEOVLCNM_ARMR` - Neovulcanium Armor (PL7)\
> `KEY:NEUTRONT` - Neutronite (PL7)\
> `KEY:NKP_PUMA_PPUP_TRT` - NKP Puma Pop-Up Turret (PL 6)\
> `KEY:ORCL_TG_SYS1` - Oracle Targeting System Mk 1 (PL6)\
> `KEY:ORCL_TG_SYS2` - Oracle Targeting System Mk 2 (PL6)\
> `KEY:ORCL_TG_SYS3` - Oracle Targeting System Mk 3 (PL6)\
> `KEY:ORCL_TG_SYS4` - Oracle Targeting System Mk 4 (PL6)\
> `KEY:ORCL_TG_SYS5` - Oracle Targeting System Mk 5 (PL6)\
> `KEY:REACTIVE_ARMR` - Reactive Armor (PL8)\
> `KEY:RESILIUM_ARMR` - Resilium Armor (PL6)\
> `KEY:RJTTHRST_BTS` - Ramjet Thruster Boots (PL8)\
> `KEY:SPACE_SKIN` - Space Skin (PL 6)\
> `KEY:STEALTH_SUITE` - Stealth Suite (PL 6)\
> `KEY:STRCTRL_ENHNCMT` - Structural Enhancement (PL 7)\
> `KEY:STRCTRL_ENHNCMT2` - Structural Enhancement (PL 7)\
> `KEY:T95_CVLCD_CHAINGN` - T-95 Cavalcade Chaingun (PL 6)\
> `KEY:THRUSTER_BTS` - Thruster Boots (PL7)\
> `KEY:TSNM_480_PLSM_CNN` - Tsunami 480 Plasma Cannon (PL 7)\
> `KEY:TYPHN_240_LSR_CNN` - Typhoon 240 Laser Cannon (PL 6)\
> `KEY:VANADIUM` - Vanadium (PL6)\
> `KEY:WARPTH_RCLLSS_RFL` - Warpath Recoilless Rifle (PL 5)\
> `KEY:ZERO_G_STABILZR` - Zero-G Stabilizer (PL 7)\
>
> **MSRD - Future Mutations File.**
>
> `KEY:MUT_SECOND_WIND` - Second Wind\
>
> **MSRD - Future Robots File.**
>
> `KEY:ROBOT_FLY_05` - +5 Speed\
> `KEY:ROBOT_FLY_10` - +10 Speed\
> `KEY:ROBOT_FLY_15` - +15 Speed\
> `KEY:ROBOT_FLY_20` - +20 Speed\
> `KEY:ROBOT_FLY_25` - +25 Speed\
> `KEY:ROBOT_FLY_30` - +30 Speed\
> `KEY:ROBOT_FLY_35` - +35 Speed\
> `KEY:ROBOT_FLY_40` - +40 Speed\
> `KEY:ROBOT_SPEED_05` - +5 Speed\
> `KEY:ROBOT_SPEED_10` - +10 Speed\
> `KEY:ROBOT_SPEED_15` - +15 Speed\
> `KEY:ROBOT_SPEED_20` - +20 Speed\
> `KEY:ROBOT_SPEED_25` - +25 Speed\
> `KEY:ROBOT_SPEED_30` - +30 Speed\
> `KEY:ROBOT_SWIM_05` - +5 Speed\
> `KEY:ROBOT_SWIM_10` - +10 Speed\
> `KEY:ROBOT_SWIM_15` - +15 Speed\
> `KEY:ROBOT_SWIM_20` - +20 Speed\
> `KEY:SKILLCHIP1` - Skill Software\
> `KEY:SKILLCHIP2` - Skill Software\
> `KEY:SKILLCHIP3` - Skill Software\
> `KEY:SKILLCHIP4` - Skill Software\
> `KEY:SKILLCHIP5` - Skill Software\
> `KEY:SKILLCHIP6` - Skill Software\
> `KEY:SKILLCHIP7` - Skill Software\
> `KEY:SKILLCHIP8` - Skill Software\
> `KEY:SKILLNET4A` - Skill Software 1\
> `KEY:SKILLNET4B` - Skill Software 2\
> `KEY:SKILLNET4C` - Skill Software 3\
> `KEY:SKILLNET4D` - Skill Software 4\
> `KEY:SKILLNET8A` - Skill Software 1\
> `KEY:SKILLNET8B` - Skill Software 2\
> `KEY:SKILLNET8C` - Skill Software 3\
> `KEY:SKILLNET8D` - Skill Software 4\
> `KEY:SKILLNET12A` - Skill Software 1\
> `KEY:SKILLNET12B` - Skill Software 2\
> `KEY:SKILLNET12C` - Skill Software 3\
> `KEY:SKILLNET12D` - Skill Software 4\
> `KEY:SKILLPROGIT4` - Skill Software 1\
> `KEY:SKILLPROGIT8` - Skill Software 1\
> `KEY:SKILLPROGIT12` - Skill Software 1\
>
> **MSRD - EQUIPMODE EXCLUDED**

------------------------------------------------------------------------

<span id="apg"></span> **Alea Publishing Group (APG) - Quests (35e)**

> **APG Game Enhancement - Quests File.**
>
> `KEY:CORRUPTED` - Corrupted\
> `KEY:CORRUPTING` - Corrupting\
> `KEY:HONORABLE` - Honorable\
> `KEY:REDEEMING` - Redeeming\
> `KEY:SUPPRESSION` - Suppression\
>
> **APG - EQUIPMODE EXCLUDED**

------------------------------------------------------------------------

<span id="ag"></span> **Atlas Games (AG) - Penumbra (3e)**

> **AG - Penumbra: Beyond the Veil File.**
>
> `KEY:BTVSUNDER` - Sundering\
>
> **AG - EQUIPMODE EXCLUDED**

[Bad Ass Games (BAG) - Heroes of High Favor -
Dwarves](/list/global/key.html#bag)\

------------------------------------------------------------------------

<span id="bag"></span> **Bad Ass Games (BAG) - Heroes of High Favor -
Dwarves (3e)**

> **BAG Heroes of High Favor - Dwarves File.**
>
> `KEY:CUSTL1` - Custom Fitx1 \[Light Armor\]\
> `KEY:CUSTL2` - Custom Fitx2 \[Light Armor\]\
> `KEY:CUSTL3` - Custom Fitx3 \[Light Armor\]\
> `KEY:CUSTM1` - Custom Fitx1 \[Medium Armor\]\
> `KEY:CUSTM2` - Custom Fitx2 \[Medium Armor\]\
> `KEY:CUSTM3` - Custom Fitx3 \[Medium Armor\]\
> `KEY:CUSTH1` - Custom Fitx1 \[Heavy Armor\]\
> `KEY:CUSTH2` - Custom Fitx2 \[Heavy Armor\]\
> `KEY:CUSTH3` - Custom Fitx3 \[Heavy Armor\]\
> `KEY:DURAL1` - Durabilityx1 \[Light Armor\]\
> `KEY:DURAL2` - Durabilityx2 \[Light Armor\]\
> `KEY:DURAL3` - Durabilityx3 \[Light Armor\]\
> `KEY:DURAL4` - Durabilityx4 \[Light Armor\]\
> `KEY:DURAL5` - Durabilityx5 \[Light Armor\]\
> `KEY:DURAM1` - Durabilityx1 \[Medium Armor\]\
> `KEY:DURAM2` - Durabilityx2 \[Medium Armor\]\
> `KEY:DURAM3` - Durabilityx3 \[Medium Armor\]\
> `KEY:DURAM4` - Durabilityx4 \[Medium Armor\]\
> `KEY:DURAM5` - Durabilityx5 \[Medium Armor\]\
> `KEY:DURAH1` - Durabilityx1 \[Heavy Armor\]\
> `KEY:DURAH2` - Durabilityx2 \[Heavy Armor\]\
> `KEY:DURAH3` - Durabilityx3 \[Heavy Armor\]\
> `KEY:DURAH4` - Durabilityx4 \[Heavy Armor\]\
> `KEY:DURAH5` - Durabilityx5 \[Heavy Armor\]\
> `KEY:ENH_ALL1` - Enhanced Alloyx1\
> `KEY:ENH_ALL2` - Enhanced Alloyx2\
> `KEY:ENH_ALL3` - Enhanced Alloyx3\
> `KEY:HARDL1` - Hardenedx1 \[Light Armor\]\
> `KEY:HARDL2` - Hardenedx2 \[Light Armor\]\
> `KEY:HARDS1` - Hardenedx1 \[Shield\]\
> `KEY:HARDS2` - Hardenedx2 \[Shield\]\
> `KEY:HARDM1` - Hardenedx1 \[Medium Armor\]\
> `KEY:HARDM2` - Hardenedx2 \[Medium Armor\]\
> `KEY:HARDH1` - Hardenedx1 \[Heavy Armor\]\
> `KEY:HARDH2` - Hardenedx2 \[Heavy Armor\]\
> `KEY:MMARK` - Maker's Mark\
> `KEY:MOBILITY_ARMR_LT` - Mobility \[Light Armor\]\
> `KEY:MOBILITY_ARMR_MED` - Mobility \[Medium Armor\]\
> `KEY:MOBILITY_ARMR_HVY` - Mobility \[Heavy Armor\]\
> `KEY:RWT` - Reduced Weight\
> `KEY:SBALL1` - Superb Balancex1 \[Light Armor\]\
> `KEY:SBALL2` - Superb Balancex2 \[Light Armor\]\
> `KEY:SBALM1` - Superb Balancex1 \[Medium Armor\]\
> `KEY:SBALM2` - Superb Balancex2 \[Medium Armor\]\
> `KEY:SBALH1` - Superb Balancex1 \[Heavy Armor\]\
> `KEY:SBALH2` - Superb Balancex2 \[Heavy Armor\]\
>
> **BAG - EQUIPMODE EXCLUDED**

------------------------------------------------------------------------

<span id="bp"></span> **Bastion Press (BP) - Oathbound (3e)**

> **BP Oathbound File.**
>
> `KEY:ARMRDBCL` - Celestial Bone\
> `KEY:ARMRDFL1` - Deflecting +1\
> `KEY:ARMRDFL2` - Deflecting +2\
> `KEY:ARMRDFL3` - Deflecting +3\
> `KEY:ARMRDFL4` - Deflecting +4\
> `KEY:ARMRRSHP` - Reshaping\
> `KEY:WPNDBLD` - Blinding\
> `KEY:WPNDBLK` - Blinking\
> `KEY:WPNDBCL` - Celestial Bone\
> `KEY:WPNDFL1` - Deflecting +1\
> `KEY:WPNDFL2` - Deflecting +2\
> `KEY:WPNDFL3` - Deflecting +3\
> `KEY:WPNDFL4` - Deflecting +4\
> `KEY:WPNDPRS` - Persuading\
>
> **BP - EQUIPMODE EXCLUDED**

------------------------------------------------------------------------

<span id="bas"></span> **Bards and Sages (BaS) - Neiyar Land of Heaven
and the Abyss (35e)**

> **BaS - Neiyar Land of Heaven and the Abyss File.**
>
> `KEY:RAGE_FLAW` - Rage\
>
> **BaS - EQUIPMODE EXCLUDED**

------------------------------------------------------------------------

<span id="bfpc"></span> **Battle Field Press (BFP) - Cityscape (3e)**

> **BFP - Cityscape File.**
>
> `KEY:ARMCAM` - Camouflage\
> `KEY:ARMREF` - Reflective\
>
> **BFP - EQUIPMODE EXCLUDED**

------------------------------------------------------------------------

<span id="bfp"></span> **Battle Field Press (BFP) - Pulp Fantasy
(Modern)**

> **BFP - Pulp Fantasy File.**
>
> `KEY:AAVEHICLE` - Vehicle\
> `KEY:CHARGED_ITEM_12` - Charges (12)\
> `KEY:GDGT_EXTND` - Extend Invention Feat\
> `KEY:GDGT_FDBCK` - Feedback Flaw\
> `KEY:GDGT_IMPRO` - Improvised Invention Feat\
> `KEY:GDGT_INV_LVL` - Base Invention Level\
> `KEY:GDGT_LOSS_AB` - Ability Loss Flaw\
> `KEY:GDGT_MINI` - Miniaturize Invention Feat\
> `KEY:GDGT_PWR_DRN` - Power Drain Flaw\
> `KEY:GDGT_SMPL` - Simplified Invention Feat\
> `KEY:GDGT_SPL_CMD1` - |1st level Spell Effect (50 Uses/Gadget)\
> `KEY:GDGT_SPL_CMD2` - |2nd level Spell Effect (50 Uses/Gadget)\
> `KEY:GDGT_SPL_CMD3` - |3rd level Spell Effect (50 Uses/Gadget)\
> `KEY:GDGT_SPL_CMD4` - |4th level Spell Effect (50 Uses/Gadget)\
> `KEY:GDGT_SPL_CMD5` - |5th level Spell Effect (50 Uses/Gadget)\
> `KEY:GDGT_SPL_CMD6` - |6th level Spell Effect (50 Uses/Gadget)\
> `KEY:GDGT_SPL_CMD7` - |7th level Spell Effect (50 Uses/Gadget)\
> `KEY:GDGT_SPL_CMD8` - |8th level Spell Effect (50 Uses/Gadget)\
> `KEY:GDGT_SPL_CMD9` - |9th level Spell Effect (50 Uses/Gadget)\
> `KEY:GDGT_SPR_SHDN` - Sporadic Shut Down Flaw\
> `KEY:Linguist_BP_PFF` - Linguist\
>
> **BFP - EQUIPMODE EXCLUDED**

------------------------------------------------------------------------

<span id="bfprr"></span> **Battle Field Press (BFP) - Rocket Rangers -
King of the Rocket Men (Modern)**

> **BFP - Pulp Fantasy - Rocket Rangers File.**
>
> `KEY:AAVEHICLE` - Vehicle\
> `KEY:GDGT_EXTND` - Extend Invention Feat\
> `KEY:GDGT_FDBCK` - Feedback Flaw\
> `KEY:GDGT_IMPRO` - Improvised Invention Feat\
> `KEY:GDGT_INV_LVL` - Base Invention Level\
> `KEY:GDGT_LOSS_AB` - Ability Loss Flaw\
> `KEY:GDGT_MINI` - Miniaturize Invention Feat\
> `KEY:GDGT_PWR_DRN` - Power Drain Flaw\
> `KEY:GDGT_SMPL` - Simplified Invention Feat\
> `KEY:GDGT_SPL_CMD1` - |1st level Spell Effect (50 Uses/Gadget)\
> `KEY:GDGT_SPL_CMD2` - |2nd level Spell Effect (50 Uses/Gadget)\
> `KEY:GDGT_SPL_CMD3` - |3rd level Spell Effect (50 Uses/Gadget)\
> `KEY:GDGT_SPL_CMD4` - |4th level Spell Effect (50 Uses/Gadget)\
> `KEY:GDGT_SPL_CMD5` - |5th level Spell Effect (50 Uses/Gadget)\
> `KEY:GDGT_SPL_CMD6` - |6th level Spell Effect (50 Uses/Gadget)\
> `KEY:GDGT_SPL_CMD7` - |7th level Spell Effect (50 Uses/Gadget)\
> `KEY:GDGT_SPL_CMD8` - |8th level Spell Effect (50 Uses/Gadget)\
> `KEY:GDGT_SPL_CMD9` - |9th level Spell Effect (50 Uses/Gadget)\
> `KEY:GDGT_SPR_SHDN` - Sporadic Shut Down Flaw\
>
> **BFP - EQUIPMODE EXCLUDED**

------------------------------------------------------------------------

<span id="bfg"></span> **Big Finger Games (BFG) - Masterwork Qualities
(35e)**

> **BFG - Masterwork Qualities File.**
>
> `KEY:ARTICULATED` - Articulated\
> `KEY:BAL_THROWN` - Balanced\
> `KEY:BAL_RANGE` - Balanced\
> `KEY:BARBED` - Barbed\
> `KEY:CUST_HILT` - Custom Hilt\
> `KEY:DIRE` - Dire\
> `KEY:FLEXIBLE` - Flexible\
> `KEY:FORTIFIED` - Fortified\
> `KEY:GUARD` - Guard\
> `KEY:HOOK` - Hook\
> `KEY:INSULATED` - Insulated\
> `KEY:MULTIPART` - Multipart\
> `KEY:PERF_BAL` - Perfect Balance - Weapon\
> `KEY:PERF_EDGE` - Perfect Edge - Weapon\
> `KEY:REINFRCD_ARMR` - Reinforced - Armor\
> `KEY:REINFRCD_WEAP` - Reinforced - Weapon\
> `KEY:SERRATED` - Serrated\
> `KEY:TASSLE` - Tassel\
> `KEY:TRAP` - Trap\
>
> **BFG - EQUIPMODE EXCLUDED**

------------------------------------------------------------------------

<span id="bdg"></span> **Blue Devil Games (BDG) - Dawningstar (Modern)**

> **BDG - Dawningstar: Operation Quick Launch File.**
>
> `KEY:CERAMIC_ARM` - Ceramics\
> `KEY:CERAMIC_WEAP` - Ceramics\
> `KEY:DURASTEEL_ARM` - Durasteel\
> `KEY:DURASTEEL_SHIELD` - Durasteel\
> `KEY:DURASTEEL_WEAP` - Durasteel\
> `KEY:HONED_DURA_WEAP` - Honed Durasteel\
> `KEY:LUMINSTONE` - Luminstone\
> `KEY:PLAS_EFF_MAT` - Plasma Efficiency Matrix\
> `KEY:REF_SPR_MOD` - Reflecting Spread Module\
> `KEY:SMART_LINK` - Smart Link\
>
> **BDG - EQUIPMODE EXCLUDED**

------------------------------------------------------------------------

<span id="cg"></span> **Crafty Games (CG) - Spycraft (Spycraft)**

> **CG - Spycraft: Shadow Force Archer File.**
>
> `KEY:BACKFIRE_PALMPRINT_ID` - Backfire Palmprint ID\
> `KEY:BACKUP_IDCARD` - Backup ID\
> `KEY:BLINDMAN_EARIMPLANT` - Blindman Unit\
> `KEY:BLOWBACK_PALMPRINT_ID` - Blowback Palmprint ID\
> `KEY:DANGER_EARIMPLANT` - Danger Unit\
> `KEY:DIVINGSUIT_PROPELLERS` - Propellers\
> `KEY:DUPLICATION_IDCARD` - Duplication\
> `KEY:ELECTRONIC_LOCKPICK_IDCARD` - Electronic Lockpick\
> `KEY:FLUID_BREATH_TANKS` - Fluid Breath Tanks\
> `KEY:GARAGE_SUITE` - Garage Suite\
> `KEY:MARK_I_STANDARD_PALMPRINT_ID` - Mark I Standard Palmprint ID\
> `KEY:MEDICAL_SUITE` - Medical Suite\
> `KEY:PHONE_REMOTE_CONTROL` - Remote Control\
> `KEY:PHONE_SLIP_AWAY_UNIT` - Slip-Away Unit\
> `KEY:POLYGRAPH_EARIMPLANT` - Polygraph/Voice Stress Analyzer\
> `KEY:PROPS_SUITE` - Props Suite\
> `KEY:SURVEILLANCE_SUITE` - Surveillance Suite\
> `KEY:TRACKING_MODIFICATION_PALMPRINT_ID` - Tracking Modification
> Palmprint ID\
> `KEY:WARNING_SIGNAL_IDCARD` - Warning Signal\
>
> **CG - Spycraft File.**
>
> `KEY:ALL_IN_ONE` - All-in-one\
> `KEY:AUTO_TINT` - Auto-tint\
> `KEY:AUTOPILOT` - Autopilot\
> `KEY:BLACK_HEADLIGHTS` - Black headlights\
> `KEY:BLADE_SHOE` - Blade\
> `KEY:BOOBY_TRAPPED` - Booby trapped\
> `KEY:BREAKDOWN_GUN` - Electronic Scope\
> `KEY:CBQ_WEAPON` - CBQ\
> `KEY:CLOAKING_DEVICE` - Cloaking device\
> `KEY:COMPUTER_PLUS_1` - +1\
> `KEY:COMPUTER_PLUS_2` - +2\
> `KEY:COMPUTER_PLUS_3` - +3\
> `KEY:CONCEALED_MACHINE_GUN` - Concealed machine gun\
> `KEY:COPYCAT` - Copycat\
> `KEY:COUNTER_SURVEILLANCE` - Counter surveillance\
> `KEY:DUMMY_LINE` - Dummy line\
> `KEY:EJECTION_SEATS` - Ejection seats\
> `KEY:ELECTRIFIED_FRAME` - Electrified frame\
> `KEY:EXPLOSIVE_WATCH` - Explosive\
> `KEY:EXTRA_ARMOR` - Extra armor\
> `KEY:FACEPRINT_LENSES` - Faceprint\
> `KEY:FLASH_SUPPRESSOR` - Flash Suppressor\
> `KEY:GARROTE_WATCH` - Garrote\
> `KEY:GPS_WATCH` - GPS\
> `KEY:GUN_SHOE` - Gun\
> `KEY:HEADS_UP_DISPLAY` - Heads Up Display\
> `KEY:HIDDEN_COMPARTMENT` - Hidden compartment\
> `KEY:HOMING_BEACON_SHOE` - Homing beacon\
> `KEY:HUSH_PUPPY` - Hush Puppy\
> `KEY:HYPNOSIS_LENSES` - Hypnosis\
> `KEY:IMPROVED_HANDLING` - Improved handling\
> `KEY:IRIS_LENSES` - Iris\
> `KEY:LASER_MOUNT` - Laser mount\
> `KEY:LASER_SIGHT` - Laser Sight\
> `KEY:LCD_LENSES` - LCD\
> `KEY:LOCKPICK_SET` - Lockpick set\
> `KEY:MACHINE_PISTOL` - Machine pistol\
> `KEY:MAGIC_BOX` - Magic box\
> `KEY:MAGNET_EYES_LENSES` - Magnet eyes\
> `KEY:MATCH_GRADE_WEAPON` - Match grade weapon\
> `KEY:MEMORY_CACHE_WATCH` - Memory cache\
> `KEY:NITROUS_OXIDE_SYSTEM` - Nitrous oxide system\
> `KEY:NON_SINUSOIDAL` - Non-sinusoidal transmission\
> `KEY:OIL_SLICK` - Oil slick\
> `KEY:OTHER_DIRECTIONAL_GLASSES` - Other directional glasses\
> `KEY:PHONE_SHOE` - Phone\
> `KEY:PIEZO_BUG` - Piezo-bug\
> `KEY:POISON_SPIKE_WATCH` - Poison spike\
> `KEY:POP_UP_SHIELD` - Pop-up shield\
> `KEY:PORTABLE_PC` - Portable PC\
> `KEY:PROTEUS_PACKAGE` - Proteus package\
> `KEY:RAZORS_EDGE` - Razor's edge\
> `KEY:REINFORCED_TIRES` - Reinforced tires\
> `KEY:REMOTE_CONTROL` - Remote control\
> `KEY:REVOLVING_LICENSE_PLATE` - Revolving license plate\
> `KEY:ROCKET_LAUNCHER` - Rocket launcher\
> `KEY:ROLLER_ICE_BLADES_SHOE` - Roller/ice blades\
> `KEY:ROTARY_SAW_WATCH` - Rotary saw\
> `KEY:SAFE_PASSAGE` - Safe passage\
> `KEY:SEALED_LENSES` - Sealed lenses\
> `KEY:SHOCK_TIP_SHOE` - Shock tip\
> `KEY:SILENCED_REVOLVER` - Silenced revolver\
> `KEY:SILENCER` - Silencer\
> `KEY:SMOKE_SCREEN` - Smoke screen\
> `KEY:SPIKE_DROPPER` - Spike dropper\
> `KEY:STARLIGHT_LENSES` - Starlight lenses\
> `KEY:SUBMACHINE_GUN` - Submachine gun\
> `KEY:SUCTION_SHOE` - Suction\
> `KEY:SURVEILLANCE` - Surveillance\
> `KEY:TELESCOPIC_LENSES` - Telescopic lenses\
> `KEY:TELESCOPIC_SIGHT` - Telescopic Sight\
> `KEY:THERMPGRAPHIC_LENSES` - Thermpgraphic lenses\
> `KEY:TIRE_SLASHER` - Tire slasher\
> `KEY:TRANSLATOR_LENSES` - Translator lenses\
> `KEY:TRANSMITTER_LENSES` - Transmitter lenses\
> `KEY:TREADS_SHOE` - Treads\
> `KEY:TRI_FERENCE_PHOTOGRAPHY` - Tri-ference photography\
> `KEY:TUBULAR_SPACE_FRAME` - Tubular space frame\
> `KEY:VOICE_ACTIVATED_COMMAND` - Voice Activated Command System\
> `KEY:WEAPON_ACCURIZING` - Weapon accurizing\
> `KEY:WIND_RESISTANCE_REDUCTION_1` - Wind resistance reduction (+1)\
> `KEY:WIND_RESISTANCE_REDUCTION_2` - Wind resistance reduction (+2)\
> `KEY:X_RAY_LENSES` - X ray lenses\
>
> **AEG - EQUIPMODE EXCLUDED**

------------------------------------------------------------------------

<span id="dhr"></span> **Dog House Rules (DHR) - Sidewinder
(Sidewinder)**

> **DHR - Sidewinder Recoiled File.**
>
> `KEY:CUSGRIP` - Custom Grip\
> `KEY:CUSSIT` - Custom Sights\
> `KEY:DETSTK` - Detachable Stock\
> `KEY:HRTRGR` - Hair Trigger\
> `KEY:LNGBRL_L` - Lengthened Barrel\
> `KEY:LNGBRL_P` - Lengthened Barrel\
> `KEY:SAWBRL` - Sawed-Off Barrel\
> `KEY:SHTBRL_L` - Shortened Barrel\
> `KEY:SHTBRL_P` - Shortened Barrel\
>
> **DHR - EQUIPMODE EXCLUDED**

------------------------------------------------------------------------

<span id="ffgm"></span> **Fantasy Flight Games (FFG) - Midnight (3e)**

> **FFG - Midnight File.**
>
> `KEY:ICEWD` - Icewood\
>
> **FFG - Midnight: Against the Shadow File.**
>
> `KEY:BONE` - Bone\
> `KEY:FOLD` - Foldable\
> `KEY:HORN` - Horn\
> `KEY:ROPE` - Rope\
> `KEY:STONE` - Stone\

<span id="ffgdsh"></span> **Fantasy Flight Games (FFG) - Dragonstar
(3e)**

> **FFG - Dragonster: Starfarers Handbook File.**
>
> `KEY:SF_CAMO` - Camouflage\
> `KEY:SF_DATA` - Program\
> `KEY:SF_ELECSCOPE` - Electronic Scope\
> `KEY:SF_KNBLD_WEAP` - Keenblade\
> `KEY:SF_LASERSIGHT` - Laser Sight\
> `KEY:SF_SECURITY` - Security Upgrade\
> `KEY:SF_SILENCER` - Silencer\
> `KEY:SF_SPELLWARE_1` - Spellware\_1st\_lev\
> `KEY:SF_SPELLWARE_2` - Spellware\_2nd\_lev\
> `KEY:SF_SPELLWARE_3` - Spellware\_3rd\_lev\
> `KEY:SF_SPELLWARE_4` - Spellware\_4th\_lev\
> `KEY:SF_SPELLWARE_5` - Spellware\_5th\_lev\
> `KEY:SF_SPELLWARE_6` - Spellware\_6th\_lev\
> `KEY:SF_SPELLWARE_7` - Spellware\_7th\_lev\
> `KEY:SF_SPELLWARE_8` - Spellware\_8th\_lev\
> `KEY:SF_SPELLWARE_9` - Spellware\_9th\_lev\
> `KEY:SF_TOOLSMW` - Masterwork\
> `KEY:SF_TOOLSNM` - Normal\
> `KEY:SF_TOOLSSP` - Specialized\
> `KEY:SF_TOOLSSPM` - Specialized Masterwork\
>
> **FFG - EQUIPMODE EXCLUDED**

<span id="ffgll"></span> **Fantasy Flight Games (FFG) - Legends and
Lairs (3e)**

> **FFG - Legends and Lairs: School of Illusion File.**
>
> `KEY:FIREWRK` - Masterwork - Firework\
>
> **FFG - Legends and Lairs: Seafarers Handbook File.**
>
> `KEY:ADAMANTITE` - Adamantite Plated\
> `KEY:HULL_BUILT` - Built to Last\
> `KEY:HULL_BULL` - Bull of the Sea\
> `KEY:HULL_BUOYANCY` - Improved Buoyancy\
> `KEY:HULL_CLEAVER` - Clever Construction\
> `KEY:HULL_FIRE_TESTED` - Fire Tested\
> `KEY:HULL_GRACE` - Grace Under Pressure\
> `KEY:HULL_ICE_QUEEN` - Ice Queen\
> `KEY:HULL_MIGHTY-OARS` - Mighty Oars\
> `KEY:HULL_OCEABWORTHY` - Oceanworthy\
> `KEY:HULL_SEA_SCRAPPER` - Sea Scrapper\
> `KEY:HULL_SEA_SKIMMER` - Sea Skimmer\
> `KEY:HULL_STORM_RIDER` - Storm Rider\
> `KEY:HULL_TOUGH` - Tough Old Girl\
> `KEY:HULL_TOUGH_SAILS` - Reinforced Sails\
> `KEY:HULL_TRANSPORT` - Transport\
> `KEY:HULL_WAR_DOG` - War Dog\
> `KEY:HULL_WAVE_RIDER` - Wave Rider\
> `KEY:IRON_PLATED` - Iron Plated\
> `KEY:MITHRAL_PLATED` - Mithral Plated\
> `KEY:SE_1COMPLET_WP` - |Spell Effect (Single/Completion)\
> `KEY:WaterbaneArm` - Waterbane - Armor\
> `KEY:WaterbaneWeap` - Waterbane - Weapon\
> `KEY:WOOD_PLATED` - Wood Plated\
>
> **FFG - Legends and Lairs: Sorcery and Steam File.**
>
> `KEY:BAYONET` - Bayonet\
> `KEY:GUN_GLYPH_WEAPON` - Gun Glyph Weapon\
> `KEY:OPTICAL_SCOPE` - Optical Scope\
> `KEY:SAS_AIR_FINLTERS` - Air Filters\
> `KEY:SAS_AQUATIC_GEAR` - Aquatic Gear\
> `KEY:SAS_CLIMBING_CLAWS` - Climbing Claws\
> `KEY:SAS_ELEM_FIELD` - Electrical Field\
> `KEY:SAS_ELEM_RES_ACID_5` - Elemental Resistance (Acid 5)\
> `KEY:SAS_ELEM_RES_ACID_10` - Elemental Resistance (Acid 10)\
> `KEY:SAS_ELEM_RES_FIRE_5` - Elemental Resistance (Fire 5)\
> `KEY:SAS_ELEM_RES_FIRE_10` - Elemental Resistance (Fire 10)\
> `KEY:SAS_ELEM_RES_COLD_5` - Elemental Resistance (Cold 5)\
> `KEY:SAS_ELEM_RES_COLD_10` - Elemental Resistance (Cold 10)\
> `KEY:SAS_ELEM_RES_ELEC_5` - Elemental Resistance (Electricity 5)\
> `KEY:SAS_ELEM_RES_ELEC_10` - Elemental Resistance (Electricity 10)\
> `KEY:SAS_ELEM_RES_SONIC_5` - Elemental Resistance (Sonic 5)\
> `KEY:SAS_ELEM_RES_SONIC_10` - Elemental Resistance (Sonic 10)\
> `KEY:SAS_HEAVY_SHIELDING` - Heavy Shielding\
> `KEY:SAS_INTERNAL_CHRONOMETER` - Internal Chronometer\
> `KEY:SAS_NIGHT_OWL_LENSES` - Lenses of the Night Owl\
> `KEY:SAS_NOISE_BAFFLERS` - Noise Bafflers\
> `KEY:SAS_ORNAMENTATION` - Ornamentation\
> `KEY:SAS_PARTING_GAUNTLETS` - Parting Gauntlets\
> `KEY:SAS_REINFORCED_STRUCTURE` - Reinforced Structure\
> `KEY:SAS_SERVO_ARTICULATION_2` - Servomotor Articulation (2)\
> `KEY:SAS_SERVO_ARTICULATION_4` - Servomotor Articulation (4)\
> `KEY:SAS_SERVO_ARTICULATION_6` - Servomotor Articulation (6)\
> `KEY:SAS_SERVO_ARTICULATION_8` - Servomotor Articulation (8)\
> `KEY:SAS_SERVO_ARTICULATION_10` - Servomotor Articulation (10)\
> `KEY:SAS_SNAP_SHIELD` - Snap Shield\
> `KEY:SAS_SOUND_GATHERERS` - Sound Gatherers\
> `KEY:SAS_SPEED_ENHANCERS_5` - Speed Enhancers (+5 ft.)\
> `KEY:SAS_SPEED_ENHANCERS_10` - Speed Enhancers (+10 ft.)\
> `KEY:SAS_STRENGTH_BOOSTING_2` - Strength Boosting (+2)\
> `KEY:SAS_STRENGTH_BOOSTING_4` - Strength Boosting (+4)\
> `KEY:SAS_STRENGTH_BOOSTING_6` - Strength Boosting (+6)\
>
> **FFG - EQUIPMODE EXCLUDED**

------------------------------------------------------------------------

<span id="mpem"></span> **Malhavoc Press (MP) - Book of Eldritch Might
(35e)**

> **MP - Complete Book of Eldritch Might File.**
>
> `KEY:ARCBLAST_M` - Arcane Blasting - Weapon.Melee\
> `KEY:ARCBLAST_R` - Arcane Blasting - Weapon.Ranged\
> `KEY:ARMPIERC_A` - Armor Piercing - Ammunition\
> `KEY:ARMPIERC_R` - Armor Piercing - Weapon.Ranged\
> `KEY:ARMSHATTER` - Armor Shattering - Weapon.Melee\
> `KEY:BANE_AR` - Bane\
> `KEY:CAST` - Spellcasting\
> `KEY:CASTSUP` - Spellcasting (Superior)\
> `KEY:CHAMPDET` - Champion Detecting\
> `KEY:CLIMB` - Climbing\
> `KEY:COMFORT` - Comfort\
> `KEY:CREATDET` - Creature Detecting\
> `KEY:DEMONREP` - Demon Repelling\
> `KEY:DISPEL` - Dispelling\
> `KEY:ELDBLAST_M` - Eldritch Blasting - Weapon.Melee\
> `KEY:ELDBLAST_R` - Eldritch Blasting - Weapon.Ranged\
> `KEY:GRACE` - Grace\
> `KEY:GRIP2` - Gripping (+2)\
> `KEY:GRIP4` - Gripping (+4)\
> `KEY:GRIP6` - Gripping (+6)\
> `KEY:GRIP8` - Gripping (+8)\
> `KEY:GRIP10` - Gripping (+10)\
> `KEY:HARDENED1` - Hardened (+1)\
> `KEY:HARDENED2` - Hardened (+2)\
> `KEY:HARDENED3` - Hardened (+3)\
> `KEY:HARDENED4` - Hardened (+4)\
> `KEY:HARDENED5` - Hardened (+5)\
> `KEY:HIDE` - Hiding\
> `KEY:KARMIC` - Karmic\
> `KEY:KICHAN` - Ki Channel\
> `KEY:KNOCKBACK` - Knockback\
> `KEY:MAGETUNE` - Mage Tuned\
> `KEY:MANAWALL` - Manawall Crushing\
> `KEY:MANAWALLELD` - Manawall Crushing (Eldritch)\
> `KEY:MANEU` - Maneuvering\
> `KEY:MANEUGR` - Maneuvering (Greater)\
> `KEY:MOVESIL` - Moving Silently\
> `KEY:NONLETHAL` - Nonlethal\
> `KEY:POISON1` - Poisonwarding (+1)\
> `KEY:POISON2` - Poisonwarding (+2)\
> `KEY:POISON3` - Poisonwarding (+3)\
> `KEY:POISON4` - Poisonwarding (+4)\
> `KEY:POISON5` - Poisonwarding (+5)\
> `KEY:POISONST` - Potion Storing\
> `KEY:ROGUEFR` - Roguefriend\
> `KEY:SHLDPIERC_A` - Shield Piercing - Ammunition\
> `KEY:SHLDPIERC_R` - Shield Piercing - Weapon.Ranged\
> `KEY:SPELLW1` - Spellwarding (+1)\
> `KEY:SPELLW2` - Spellwarding (+2)\
> `KEY:SPELLW3` - Spellwarding (+3)\
> `KEY:SPELLW4` - Spellwarding (+4)\
> `KEY:SPELLW5` - Spellwarding (+5)\
> `KEY:TRAPW1` - Trapwarding (+1)\
> `KEY:TRAPW2` - Trapwarding (+2)\
> `KEY:TRAPW3` - Trapwarding (+3)\
> `KEY:TRAPW4` - Trapwarding (+4)\
> `KEY:TRAPW5` - Trapwarding (+5)\
> `KEY:TUMBLE` - Tumbling\
> `KEY:UNCANNY` - Uncanny Protection\
> `KEY:UNRULY` - Unruly\

<span id="mphm"></span> **Malhavoc Press (MP) - Book of Hallowed Might
(3e)**

> **MP - Book of Hallowed Might File.**
>
> `KEY:BOHMASABCOUR` - Absolute Courage\
> `KEY:BOHMASABPUR` - Absolute Purity\
> `KEY:BOHMASCHAR` - Charity\
> `KEY:BOHMASCOUR` - Courage\
> `KEY:BOHMASCRYS` - Crystal\
> `KEY:BOHMASDWARD` - Deathward\
> `KEY:BOHMASFAITH` - Faith\
> `KEY:BOHMASGOLD` - Gold\
> `KEY:BOHMASPLAT` - Platinum\
> `KEY:BOHMASPUR` - Purity\
> `KEY:BOHMASSILV` - Silver\
> `KEY:BOHMWEAPCRYS` - Crystal\
> `KEY:BOHMWEAPGLD` - Gold\
> `KEY:BOHMWEAPPLAT` - Platinum\
> `KEY:BOHMWEAPSILV` - Silver\
>
> **MP - EQUIPMODE EXCLUDED**

------------------------------------------------------------------------

<span id="mp"></span> **Mongoose Publishing (MP) - SRD (3e)**

> **MP - Collectors Series: Quintessential Rogue File.**
>
> `KEY:ARMRPAD` - Padding\
>
> **MP - Encyclopedia Arcane: Enchantment File.**
>
> `KEY:ASSUMPTION` - Assumption\
>
> **MP - Encyclopedia Divine: Fey Magic File.**
>
> `KEY:FEY_EARTHEN_GRASP` - Earthen Grasp\
> `KEY:FEY_SLUMBER` - Slumber\
> `KEY:FEY_TRACKLESS` - Trackless\
> `KEY:FEY_TREE` - Tree\
> `KEY:FEY_UNSEEN` - Unseen\
>
> **MP - Power Classes Volume I: Assassin File**
>
> `KEY:RINGFinerQuality` - Finer Quality\
> `KEY:RINGHighQuality` - High Quality\
> `KEY:RINGPoisonDrip` - Poison Dripper\
> `KEY:RINGPoisonNeedle` - Poison Needle\
> `KEY:RINGPoisonSquirt` - Poison Squirter\
>
> **MP - EQUIPMODE EXCLUDED**\

------------------------------------------------------------------------

<span id="mds"></span> **Mythic Dreams Studios (MDS) - Dark Inheritance
(Modern)**

> **MDS - Dark Inheritance: Modern File.**
>
> `KEY:ARNOLDSCLIP` - Arnold's Clip\
> `KEY:STWL_STUNTMN` - Stuntman's Steering Wheel\
> `KEY:UNRELIABLE` - Unreliable\
>
> **MDS - EQUIPMODE EXCLUDED**

------------------------------------------------------------------------

<span id="nges"></span> **Necromancer Games (NG) - Eldritch Sorcery
(35e)**

> **NG - Eldritch Sorcery File.**
>
> `KEY:TRANSSTEEL` - Transparent Steel\
>
> **NG - EQUIPMODE EXCLUDED**

<span id="ngtoh"></span> **Necromancer Games (NG) - Tome of Horrors
(35e)**

> **NG - Tome of Horrors File.**
>
> `KEY:CRUSH` - Crushing\
> `KEY:SMITE` - Smiting\
> `KEY:TELE` - Telescoping\
>
> **NG - EQUIPMODE EXCLUDED**

------------------------------------------------------------------------

**Pandahead Productions (PP) - Xcrawl (Xcrawl)**

> **PP - Sellout File.**
>
> `KEY:BLBD` - Billboard\
> `KEY:CHTR` - Chemical Treating\
> `KEY:DWMW` - Dwarven Masterwork\
> `KEY:ELMW` - Elvish Masterwork\
> `KEY:EOLA` - Easy-Off (Light Armor)\
> `KEY:EOLM` - Easy-Off (Medium Armor)\
> `KEY:EOLH` - Easy-Off (Heavy Armor)\
> `KEY:EXTR` - Exterior Tread\
> `KEY:GNMW` - Gnomish Masterwork\
> `KEY:HFMW` - Halfling Mastework\
> `KEY:HTRES` - Heat Resistant\
> `KEY:PKNIFE` - Popknife\
> `KEY:SECCOMP` - Secret Compartment\
> `KEY:SHCOR` - Shock Core\
> `KEY:WPNBAL` - Weapon Balancing\
>
> **PP - EQUIPMODE EXCLUDED**

------------------------------------------------------------------------

<span id="pcica"></span> **Paradigm Concepts Inc (PCI) - Codex Arcanis
(3e)**

> **PCI - Codex Arcanis File.**
>
> `KEY:FLINTGRMW` - Greater Mastercraft\
> `KEY:HVYARMALTHST` - Altherian Steel\
> `KEY:LTMEDARMALTHST` - Altherian Steel\
> `KEY:SHIELDALTHST` - Altherian Steel\
> `KEY:TOOLSGRMW` - Greater Mastercraft\
> `KEY:WEAPALTHST` - Altherian Steel\
> `KEY:WEAPGRMW` - Greater Mastercraft\

------------------------------------------------------------------------

<span id="pciwoa"></span> **Paradigm Concepts Inc (PCI) - World of
Arcanis (35e)**

> **PCI - Players Guide to Arcanis File.**
>
> `KEY:CUSTOMA` - Custom - Armor.Shield\
> `KEY:CUSTOMW` - Custom - Weapon\
> `KEY:GMWORKA` - Greater Masterwork - Armor.Shield\
> `KEY:GMWORKR` - Greater Masterwork - Ranged\
> `KEY:GMWORKW` - Greater Masterwork - Melee.Ammunition\
> `KEY:LEGENDWA` - Legendary 2 - Weapon\
> `KEY:LEGENDWB` - Legendary 3 - Weapon\
> `KEY:LEGENDWC` - Legendary 4 - Weapon\
> `KEY:LEGENDWD` - Legendary 5 - Weapon\
> `KEY:LEGENDAFA` - Fitted Legendary 2 - Armor.Shield\
> `KEY:LEGENDAFB` - Fitted Legendary 3 - Armor.Shield\
> `KEY:LEGENDAFC` - Fitted Legendary 4 - Armor.Shield\
> `KEY:LEGENDAFD` - Fitted Legendary 5 - Armor.Shield\
> `KEY:LEGENDANA` - Nimble Legendary 2 - Armor.Shield\
> `KEY:LEGENDANB` - Nimble Legendary 3 - Armor.Shield\
> `KEY:LEGENDANC` - Nimble Legendary 4 - Armor.Shield\
> `KEY:LEGENDAND` - Nimble Legendary 5 - Armor.Shield\
> `KEY:LEGENDAPA` - Proof Legendary 2 - Armor.Shield\
> `KEY:LEGENDAPB` - Proof Legendary 3 - Armor.Shield\
> `KEY:LEGENDAPC` - Proof Legendary 4 - Armor.Shield\
> `KEY:LEGENDAPD` - Proof Legendary 5 - Armor.Shield\
> `KEY:PLUS1A` - +1 (Enhancement to Armor)\
> `KEY:PLUS1S` - +1 (Enhancement to Shield)\
> `KEY:PLUS1W` - +1 (Enhancement to Weapon or Ammunition)\
> `KEY:PLUS2A` - +2 (Enhancement to Armor)\
> `KEY:PLUS2S` - +2 (Enhancement to Shield)\
> `KEY:PLUS2W` - +2 (Enhancement to Weapon or Ammunition)\
> `KEY:PLUS3A` - +3 (Enhancement to Armor)\
> `KEY:PLUS3S` - +3 (Enhancement to Shield)\
> `KEY:PLUS3W` - +3 (Enhancement to Weapon or Ammunition)\
> `KEY:PLUS4A` - +4 (Enhancement to Armor)\
> `KEY:PLUS4S` - +4 (Enhancement to Shield)\
> `KEY:PLUS4W` - +4 (Enhancement to Weapon or Ammunition)\
> `KEY:PLUS5A` - +5 (Enhancement to Armor)\
> `KEY:PLUS5S` - +5 (Enhancement to Shield)\
> `KEY:PLUS5W` - +5 (Enhancement to Weapon or Ammunition)\
> `KEY:SAR_GMWLARM` - GMW Sarishan Steel (Lg)\
> `KEY:SAR_GMWLSHD` - GMW Sarishan Steel (Lg)\
> `KEY:SAR_GMWLWEAP` - GMW Sarishan Steel (Lg)\
> `KEY:SAR_GMWSARM` - GMW Sarishan Steel (Sm)\
> `KEY:SAR_GMWSSHD` - GMW Sarishan Steel (Sm)\
> `KEY:SAR_GMWSWEAP` - GMW Sarishan Steel (Sm)\
> `KEY:SAR_GMWMARM` - GMW Sarishan Steel (Med)\
> `KEY:SAR_GMWMSHD` - GMW Sarishan Steel (Med)\
> `KEY:SAR_GMWMWEAP` - GMW Sarishan Steel (Med)\
> `KEY:SARISH_GMWLBRD` - GMW Sarishan Steel (Lg)\
> `KEY:SARISH_GMWMBRD` - GMW Sarishan Steel (Med)\
> `KEY:SARISH_LARM` - Sarishan Steel (Lg)\
> `KEY:SARISH_LBRD` - Sarishan Steel (Lg)\
> `KEY:SARISH_LSHD` - Sarishan Steel (Lg)\
> `KEY:SARISH_LWEAP` - Sarishan Steel (Lg)\
> `KEY:SARISH_MARM` - Sarishan Steel (Med)\
> `KEY:SARISH_MBRD` - Sarishan Steel (Med)\
> `KEY:SARISH_MSHD` - Sarishan Steel (Med)\
> `KEY:SARISH_MWEAP` - Sarishan Steel (Med)\
> `KEY:SARISH_SARM` - Sarishan Steel (Sm)\
> `KEY:SARISH_SSHD` - Sarishan Steel (Sm)\
> `KEY:SARISH_SWEAP` - Sarishan Steel (Sm)\
>
> **PCI - EQUIPMODE EXCLUDED**

------------------------------------------------------------------------

<span id="pe"></span> **Pinnacle Entertainment (PE) - Deadlands d20
(Deadlands)**

> **PE - Deadlands d20 File.**
>
> `KEY:AMMOMW` - Masterwork - Ammunition\
> `KEY:AMMOSLVR` - Silvered - Ammunition\
> `KEY:ARMRMW` - Masterwork - Armor.Shield\
> `KEY:DAGSLVR` - Silvered - Dagger\
> `KEY:INSTMW` - Masterwork - Instruments\
> `KEY:TOOLSMW` - Masterwork - Tools\
> `KEY:WEAPMW` - Masterwork - Weapon\
>
> **PE - EQUIPMODE EXCLUDED**

------------------------------------------------------------------------

<span id="rpgo"></span> **RPG Objects (RPGO) - Blood and Blades - The
Profilers Guide to Slashers (Modern)**

> **RPGO - Blood and Blades: The Profilers Guide to Slashers File.**
>
> `KEY:BNB_IMPROVED_CRITICAL` - Improved Critical\
> `KEY:BNB_IMPROVED_GRAPPLE` - Improved Grapple\
> `KEY:BNB_IMPROVED_OVERRUN` - Improved Overrun\
> `KEY:BNB_MASTER_OF_DISGUISE` - Master of Disguise\
> `KEY:BNB_SCENT` - Scent\
>
> **RPGO - Blood and Space: Starship Construction Manual File.**
>
> `KEY:ATTK_SLNG_MSSDRVR` - Slingshot Massdriver\
>
> **RPGO - Blood and Secrets File.**
>
> `KEY:BNS_EVASIVE_MANEUVERS` - Evasive Maneuvers\
> `KEY:BNS_FIGHTER_ESCORT` - Fighter Escort\
> `KEY:BNS_FORMATION_FLYING` - Formation Flying\
> `KEY:BNS_SEMPER_FI` - Semper Fi\
> `KEY:BNS_WINGMAN` - Wingman\
>
> **RPGO - Modern Dispatch: \#1 Alternate Armors File.**
>
> `KEY:ARMR_PENETRATION_AMMO_1` - Armor Penetration (+1)\
> `KEY:ARMR_PENETRATION_AMMO_2` - Armor Penetration (+2)\
> `KEY:ARMR_PENETRATION_BLUDGEONING` - Armor Penetration\
> `KEY:ARMR_PENETRATION_EXPL0SIVE` - Armor Penetration\
> `KEY:ARMR_PENETRATION_EXPL0SIVE_ENH` - Armor Penetration (Enhanced)\
> `KEY:ARMR_PENETRATION_FIREARM` - EArmor Penetration\
> `KEY:ARMR_PENETRATION_PIERCING` - Armor Penetration\
> `KEY:ARMR_PENETRATION_SLASHING` - Armor Penetration\
> `KEY:DR_CONVERSION_ARCHAIC` - Damage Reduction Conversion\
> `KEY:DR_CONVERSION_MODERN` - Damage Reduction Conversion\
> `KEY:DR_CONVERSION_POWERED` - Damage Reduction Conversion\
> `KEY:INSERT_ANTI_STAB` - Anti Stab Insert\
> `KEY:INSERT_BUOYANCY` - Buoyancy Insert\
> `KEY:INSERT_FLEX_TRAUMA` - Flexible Trauma Insert\
> `KEY:INSERT_HVY_CERAMIC` - Heavy Ceramic Insert\
> `KEY:INSERT_LT_CERAMIC` - Light Ceramic Insert\
> `KEY:INSERT_MED_CERAMIC` - Medium Ceramic Insert\
> `KEY:INSERT_STEEL_TRAUMA` - Steel Trauma Insert\
> `KEY:INSERT_TITAN_TRAUMA` - Titanium Trauma Insert\
> `KEY:OUTERSHELL` - Outershell\
> `KEY:TACTICAL_OUTERSHELL` - Tactical Outershell\
>
> **RPGO - Modern Dispatch: \#10 Near Future Firearms.**
>
> `KEY:AIR_TAZER_CT_SOCOM` - Air Tazer CT SOCOM\
>
> **RPGO - EQUIPMODE EXCLUDED**

------------------------------------------------------------------------

<span id="sg"></span> **Secular Games (SG) - Lines of Legend - Winter
Elves (35e)**

> **SG - Lines of Legend - Winter Elves File.**
>
> `KEY:MAG_ENH_FUR_ARMOR` - Magic Enhanced Fur\
> `KEY:MAG_ENH_FUR_CLOTHING` - Magic Enhanced Fur\
>
> **SG - EQUIPMODE EXCLUDED**

------------------------------------------------------------------------

<span id="sep"></span> **Swords Edge Publishing (SEP) - Modern Medieval
- Modern Principles (35e)**

> **SEP - Modern Medieval - Modern Principles File.**
>
> `KEY:FEAT_FRIGHTFUL_PRESENCE_MP` - Frightful Presence\
> `KEY:SKL_DISABLE_DEVICE_MP` - Disable Device\
>
> **SG - EQUIPMODE EXCLUDED**

------------------------------------------------------------------------

<span id="tgm"></span> **The Game Mechanics (TGM) - d20 Modern
(Modern)**

> **TGM - Martial Arts Mayhem File.**
>
> `KEY:ARW_DRGN_TNG_A` - Dragon's Tongue\
> `KEY:ARW_EXPLSV_A` - Explosive\
> `KEY:ARW_HIKIME_A` - Hikime\
> `KEY:ARW_SLVR_A` - Silver\
> `KEY:ARW_WT_PHSPHR_A` - White Phosphorous\
> `KEY:ARW_WLLW_LF_A` - Willow Leaf\
> `KEY:CLOTHYRD_SHAFT` - Clothyard Shaft\
> `KEY:SPIKE_S` - Shield Spikes\
>
> **TGM - Modern Players Companion File.**
>
> `KEY:AMMO_AET` - \#Accelerated Energy Transfer\
> `KEY:AMMO_AP` - \#Armor Piercing\
> `KEY:AMMO_HOT_LOAD` - Hot Loads\
> `KEY:AMMO_COLD_LOAD` - Cold Loads\
> `KEY:AMMO_EXPLOSIVE` - \#Explosive\
> `KEY:AMMO_FLECHETTE` - \#Flechette\
> `KEY:AMMO_GLASER` - \#Glaser\
> `KEY:AMMO_HOLLOW_POINT` - \#Hollow-point\
> `KEY:AMMO_INCENDIARY` - \#Incendiary\
>
> **TGM - EQUIPMODE EXCLUDED**

------------------------------------------------------------------------

<span id="wotc"></span> **Wizards of the Coast (WotC) - d20 Modern
(Modern)**

> **WotC - d20 Modern Weapons Locker File.**
>
> `KEY:KAHLES_SIGHT` - Kahles ZF69\
> `KEY:MOUNT_SCP_RFL` - Rifle Scope Mount\
> `KEY:SPPRSS_FN57` - FN Five-seveN Suppressor\
> `KEY:SPPRSS_MAC10` - Ingram MAC-10 Suppressor\
> `KEY:SPPRSS_MAC11` - Ingram MAC-11 Suppressor\
> `KEY:SPPRSS_OTS02` - OTs-02 Kiparis Suppressor\
> `KEY:SPPRSS_SCH21` - SCH-21 Gorda Suppressor Barrel\
> `KEY:SPPRSS_MPI69` - Steyr MPi69 Suppressor\
> `KEY:SPPRSS_MPI81` - Steyr MPi81 Suppressor\
> `KEY:SPPRSS_PGM_UR` - Silenced Barrel\
> `KEY:SUSAT_SIGHT` - SUSAT\
>
> **WotC - EQUIPMODE EXCLUDED**

[Vigilance Press (VP) - Clash of Arms -
Cavalry](/list/global/key.html#vp)\

------------------------------------------------------------------------

<span id="vp"></span> **Vigilance Press (VP) - Clash of Arms - Cavalry
(35e)**

> **VP - Clash of Arms - Cavalry File.**
>
> `KEY:MOUNT_BAG_OF_BONES` - Mount Quality (Bag of Bones)\
> `KEY:MOUNT_CHARGER` - Mount Quality (Charger)\
> `KEY:MOUNT_COURSER` - Mount Quality (Courser)\
> `KEY:MOUNT_FLIGHTY` - Mount Quality (Flighty)\
> `KEY:MOUNT_NAG` - Mount Quality (Nag)\
> `KEY:MOUNT_NOBLE_STEED` - Mount Quality (Noble Steed)\
> `KEY:MOUNT_OLD_NAG` - Mount Quality (Old Nag)\
> `KEY:MOUNT_RACER` - Mount Quality (Racer)\
> `KEY:MOUNT_STEED` - Mount Quality (Steed)\
>
> **WotC - EQUIPMODE EXCLUDED**

------------------------------------------------------------------------

<span id="complete"></span> **Complete Listing of Keys**

------------------------------------------------------------------------

> `KEY:A_1USEMA` - Spell Effect (Single Use/Completion)\
> `KEY:A_1USEME` - Spell Effect (Single Use/Completion)\
> `KEY:A_1USEMI` - Spell Effect (Single Use/Completion)\
> `KEY:AOO_PNT_DEF_SYS` - Point-defense system\
> `KEY:A3X_DRGN_FLMTHRWR` - A3X Dragon Flame - Thrower (PL 5)\
> `KEY:AASTARSHIP_LB` - Starship\
> `KEY:AASTARSHIP_TON` - Starship\
> `KEY:AAVEHICLE` - Vehicle\
> `KEY:AAVEHICLE_FUTURE` - Vehicle\
> `KEY:ACID_BLAST_AMMO` - Acidic Blast\
> `KEY:ACID_BLAST_MELEE` - Acidic Blast\
> `KEY:ACID_BLAST_RANGED` - Acidic Blast\
> `KEY:ACID_RES` - Acid Resistance\
> `KEY:ACID_WARD` - Acid Warding\
> `KEY:ACIDIC` - Acidic\
> `KEY:ADAM` - Adamantine <span class="new"> (deprecated) </span>\
> `KEY:ADAMANT_AMMO` - Adamantine (Ammo)\
> `KEY:ADAMANT_ARMR_HVY` - Adamantine (Armor/Heavy)\
> `KEY:ADAMANT_ARMR_LT` - Adamantine (Armor/Light)\
> `KEY:ADAMANT_ARMR_MED` - Adamantine (Armor/Medium)\
> `KEY:ADAMANT_FORT` - Adamantine (Fortification)\
> `KEY:ADAMANT_SHLD` - Adamantine (Shield)\
> `KEY:ADAMANT_WEAP` - Adamantine (Weapon)\
> `KEY:ADAMANT_WONDROUS` - Adamantine (Wondrous)\
> `KEY:ADAMANTITE` - Adamantite Plated\
> `KEY:ADD_TYPE` - \#Add Type\
> `KEY:ADDTYPE` - Add Type\
> `KEY:ADVANCD_DGNSTCS` - Advanced Diagnostics (PL 7)\
> `KEY:AFTRBRNR_SYS` - Afterburner System (PL6)\
> `KEY:AIR_TAZER_CT_SOCOM` - Air Tazer CT SOCOM\
> `KEY:ALCHM` - Alchemical Silver\
> `KEY:ALCHM/2` - 1/2 Alchemical Silver <span class="new"> (deprecated)
> </span>\
> `KEY:ALL_IN_ONE` - All-in-one\
> `KEY:ALT_WPN_GDGT` - Alternate Weapon Gadget\
> `KEY:ALUMINIUM` - Aluminium\
> `KEY:ALUMISTL` - Alumisteel (PL5)\
> `KEY:ALUMISTL_ARMR` - Alumisteel Armor (PL5)\
> `KEY:AMMO_AET` - \#Accelerated Energy Transfer\
> `KEY:AMMO_AP` - \#Armor Piercing\
> `KEY:AMMO_HOT_LOAD` - Hot Loads\
> `KEY:AMMO_COLD_LOAD` - Cold Loads\
> `KEY:AMMO_EXPLOSIVE` - \#Explosive\
> `KEY:AMMO_FLECHETTE` - \#Flechette\
> `KEY:AMMO_GLASER` - \#Glaser\
> `KEY:AMMO_HOLLOW_POINT` - \#Hollow-point\
> `KEY:AMMO_INCENDIARY` - \#Incendiary\
> `KEY:AMMO_LT5_LNGSHT_MSSDRV` - Ammo bay for LT-5 Longshot Mass Driver\
> `KEY:AMMO_M9_BRRGE_CHAINGUN` - 6 50-round ammo belts for M-9 Barrage
> chaingun\
> `KEY:AMMO_M53_FRST_RCKTLNCH` - 6-rocket pack for M-53 Firestar Rocket
> Launcher\
> `KEY:AMMO_M55_CRUD_RCKTLNCH` - 6-rocket pack for M-55 Crud Rocket
> Launcher\
> `KEY:AMMO_M70_EMP_RCKTLNCHR` - 6-rocket pack for M-70 EMP Rocket
> Launcher\
> `KEY:AMMO_M75_CRKT_RCKTLNCH` - 6-rocket pack for M-75 Cricket Rocket
> Launcher\
> `KEY:AMMO_M87_TALN_MSSLLNCH` - 4-missile pack for M-87 Talon Missile
> Launcher\
> `KEY:AMMO_T95_CVLCD_CHAINGN` - 6 50-round ammo belts for T-95
> Cavalcade Chaingun\
> `KEY:AMMO_WARPTH_RCLLSS_RFL` - 20-round magazine for Warpath
> Recoilless Rifle\
> `KEY:AMMOMW` - Masterwork - Ammunition\
> `KEY:AMMOSLVR` - Silvered - Ammunition\
> `KEY:AMMO2_M70_EMP_RCKTLNCHR` - 6-rocket pack for M-70 EMP Rocket
> Launcher\
> `KEY:AMMO2_M87_TALN_MSSLLNCH` - 4-missile pack for M-87 Talon Missile
> Launcher\
> `KEY:ANIMATED` - Animated\
> `KEY:ANMATD` - Animated\
> `KEY:ANTI_ACCDNT_SYS` - Anti-Accident System\
> `KEY:APORT` - Aporter\
> `KEY:APRTR` - Aporter\
> `KEY:ARCBLAST_M` - Arcane Blasting - Weapon.Melee\
> `KEY:ARCBLAST_R` - Arcane Blasting - Weapon.Ranged\
> `KEY:ARCANE_ARCHER_AMMO` - Arcane Archer Enchantement\
> `KEY:ARMCAM` - Camouflage\
> `KEY:ARMR_PIERCING` - Armor Piercing\
> `KEY:ARMRDBCL` - Celestial Bone\
> `KEY:ARMRDFL1` - Deflecting +1\
> `KEY:ARMRDFL2` - Deflecting +2\
> `KEY:ARMRDFL3` - Deflecting +3\
> `KEY:ARMRDFL4` - Deflecting +4\
> `KEY:ARMREF` - Reflective\
> `KEY:ARMRMW` - Masterwork - Armor.Shield\
> `KEY:ARMRPAD` - Padding\
> `KEY:ARMRRSHP` - Reshaping\
> `KEY:ARMPIERC_A` - Armor Piercing - Ammunition\
> `KEY:ARMPIERC_R` - Armor Piercing - Weapon.Ranged\
> `KEY:ARMPR13` - \# Power Resistance (PR13) - Armor.Shield\
> `KEY:ARMPR15` - \# Power Resistance (PR15) - Armor.Shield\
> `KEY:ARMPR17` - \# Power Resistance (PR17) - Armor.Shield\
> `KEY:ARMPR19` - \# Power Resistance (PR19) - Armor.Shield\
> `KEY:ARMR_ABLATIVE` - Ablative Armor\
> `KEY:ARMR_ALLOY_PLATING` - Alloy Plating Armor\
> `KEY:ARMR_CERAMETAL` - Cerametal Armor\
> `KEY:ARMR_DEFLECTIVE` - Deflective Armor\
> `KEY:ARMR_NANOFLUIDIC` - Nanofluidic Armor\
> `KEY:ARMR_NEUTRONITE` - Neutronite Armor\
> `KEY:ARMR_PENETRATION_AMMO_1` - Armor Penetration (+1)\
> `KEY:ARMR_PENETRATION_AMMO_2` - Armor Penetration (+2)\
> `KEY:ARMR_PENETRATION_BLUDGEONING` - Armor Penetration\
> `KEY:ARMR_PENETRATION_EXPL0SIVE` - Armor Penetration\
> `KEY:ARMR_PENETRATION_EXPL0SIVE_ENH` - Armor Penetration (Enhanced)\
> `KEY:ARMR_PENETRATION_FIREARM` - EArmor Penetration\
> `KEY:ARMR_PENETRATION_PIERCING` - Armor Penetration\
> `KEY:ARMR_PENETRATION_SLASHING` - Armor Penetration\
> `KEY:ARMR_PIERCING` - Armor Piercing\
> `KEY:ARMR_POLYMERIC` - Polymeric Armor\
> `KEY:ARMR_VANADIUM` - Vanadium Armor\
> `KEY:ARMRDBCL` - Celestial Bone\
> `KEY:ARMRDFL1` - Deflecting +1\
> `KEY:ARMRDFL2` - Deflecting +2\
> `KEY:ARMRDFL3` - Deflecting +3\
> `KEY:ARMRDFL4` - Deflecting +4\
> `KEY:ARMRRSHP` - Reshaping\
> `KEY:ARMSHATTER` - Armor Shattering - Weapon.Melee\
> `KEY:ARMRMW` - Masterwork - Armor.Shield\
> `KEY:ARNOLDSCLIP` - Arnold's Clip\
> `KEY:ARROW_DEFLECT_EXC` - Exceptional Arrow Deflection\
> `KEY:ARROW_DEFLECT_INF` - Infinite Arrow Deflection\
> `KEY:ART` - Art Value\
> `KEY:ARTICULATED` - Articulated\
> `KEY:ARTIFICIALORGAN` - Artificial Organ\
> `KEY:ARW_CAT` - Arrow Catching\
> `KEY:ARW_DEF` - Arrow Deflection\
> `KEY:ARW_DRGN_TNG_A` - Dragon's Tongue\
> `KEY:ARW_EXPLSV_A` - Explosive\
> `KEY:ARW_HIKIME_A` - Hikime\
> `KEY:ARW_SLVR_A` - Silver\
> `KEY:ARW_WT_PHSPHR_A` - White Phosphorous\
> `KEY:ARW_WLLW_LF_A` - Willow Leaf\
> `KEY:ASSUMPTION` - Assumption\
> `KEY:ATFR_MDL_GDGT` - Autofire Module Gadget\
> `KEY:ATLDR_MDL_GDGT` - Autoloader Module Gadget\
> `KEY:ATTK_ANTIMATTER` - Antimatter Gun\
> `KEY:ATTK_ANTIMATTER_4B` - Battery of 4 Antimatter Guns\
> `KEY:ATTK_AUTOMASER` - Automaser\
> `KEY:ATTK_BLACKLASER` - Blacklaser\
> `KEY:ATTK_CHE_MISSL` - CHE Missile Launcher\
> `KEY:ATTK_CHE_MISSL_2` - 2 CHE Missile Launcher\
> `KEY:ATTK_CHE_MISSL_2B_2` - 2 Batteries of 2 CHE Missile Launcher\
> `KEY:ATTK_CHE_MISSL_3B` - Battery of 3 CHE Missile Launcher\
> `KEY:ATTK_EMP_CANN` - EMP Cannon\
> `KEY:ATTK_FUSN_BEAM` - Fusion Beam\
> `KEY:ATTK_FUSN_BEAM_2L` - 2 fire-linked Fusion Beams\
> `KEY:ATTK_FUSN_BEAM_4B` - Battery of 4 Fusion Beams\
> `KEY:ATTK_GAUSS_GUN` - Gauss Gun\
> `KEY:ATTK_GAUSS_GUN_3B` - Battery of 3 Gauss Guns\
> `KEY:ATTK_HLASER` - Heavy Laser\
> `KEY:ATTK_HLASER_2L` - 2 fire-linked Heavy Laser\
> `KEY:ATTK_HLASER_3B` - Battery of 3 Heavy Laser\
> `KEY:ATTK_HLASER_4B` - Battery of 4 Heavy Laser\
> `KEY:ATTK_HLASER_4L` - 4 fire-linked Heavy Laser\
> `KEY:ATTK_HMASER_CANN` - Heavy Maser Cannon\
> `KEY:ATTK_HMASS_CANN` - Heavy Mass Cannon\
> `KEY:ATTK_HMASS_CANN_4B` - Battery of 4 heavy Mass Cannons\
> `KEY:ATTK_HNTRN_GUN` - Heavy Neutron Gun\
> `KEY:ATTK_HNTRN_GUN_2F` - 2 fire-linked Heavy Neutron Guns\
> `KEY:ATTK_HNTRN_GUN_3B` - Battery of 3 Heavy Neutron Guns\
> `KEY:ATTK_HNTRN_GUN_4F` - 4 fire-linked Heavy Neutron Guns\
> `KEY:ATTK_HPRTCL_BEAM` - Heavy Particle Beam\
> `KEY:ATTK_HPTCL_BEAM_3B_2` - 2 Batteries of 3 Heavy Particle Beams\
> `KEY:ATTK_HPTCL_BEAM_4L` - 4 fire-linked Heavy Particle Beams\
> `KEY:ATTK_HPLASM_CANN` - Heavy Plasma Cannon\
> `KEY:ATTK_HPLASM_CANN_2L` - 2 fire-linked Heavy Plasma Cannons\
> `KEY:ATTK_HPLASM_CANN_3L` - 3 fire-linked Heavy Plasma Cannons\
> `KEY:ATTK_KES_MISSL` - KE Submunition Missile Launcher\
> `KEY:ATTK_KNTC_LANCE` - Kinetic Lance\
> `KEY:ATTK_LASER` - Laser\
> `KEY:ATTK_LASER_5B` - Battery of 5 Laser\
> `KEY:ATTK_MASER_CANN` - Maser Cannon\
> `KEY:ATTK_MASER_CANN_2L` - 2 fire-linked Maser Cannons\
> `KEY:ATTK_MASS_CANN` - Mass Cannon\
> `KEY:ATTK_MASS_CANN_5B` - Battery of 5 Mass Cannons\
> `KEY:ATTK_MASS_MISSL` - Mass Reaction Missile Launcher\
> `KEY:ATTK_MASS_MISSL_2L` - 2 fire-linked Mass Reaction Missile
> Launcher\
> `KEY:ATTK_MINELAYER` - Minelayer\
> `KEY:ATTK_NDL_DRVR` - Needle Driver\
> `KEY:ATTK_NTRN_GUN` - Neutron Gun\
> `KEY:ATTK_NTRN_GUN_5B` - Battery of 5 Neutron Guns\
> `KEY:ATTK_NTRNM_DRVR` - Neutronium Driver\
> `KEY:ATTK_NOVA_MISSL` - Nova Burst Missile Launcher\
> `KEY:ATTK_NUKE_MISSL` - Nuclear Missile Launcher\
> `KEY:ATTK_NUKE_MISSL_2` - 2 Nuclear Missile Launcher\
> `KEY:ATTK_NUKE_MISSL_2L` - 2 fire-linked Nuclear Missiles Launcher\
> `KEY:ATTK_PRTCL_BEAM` - Particle Beam\
> `KEY:ATTK_PRTCL_BEAM_2L` - 2 fire-linked Particle Beams\
> `KEY:ATTK_PRTCL_BEAM_4B` - Battery of 4 Particle Beams\
> `KEY:ATTK_PLASMA_CANN` - Plasma Cannon\
> `KEY:ATTK_PLASMA_CANN_4B` - Battery of 4 Plasma Cannons\
> `KEY:ATTK_PLSM_MISSL` - Plasma Missile Launcher\
> `KEY:ATTK_PLSM_MISSL_2B` - Battery of 2 Plasma Missile Launcher\
> `KEY:ATTK_PLSM_MISSL_3B` - Battery of 3 Plasma Missile Launcher\
> `KEY:ATTK_QUNTM_CANN` - Quantum Cannon\
> `KEY:ATTK_QUNTM_CANN_2L` - 2 fire-linked Quantum Cannons\
> `KEY:ATTK_QUNTM_CANN_4L` - 4 fire-linked Quantum Cannons\
> `KEY:ATTK_RAIL_CANNON` - Rail Cannon\
> `KEY:ATTK_RAIL_CANNON_2L` - 2 fire-linked rail cannons\
> `KEY:ATTK_RAIL_CANNON_4L` - 4 fire-linked rail cannons\
> `KEY:ATTK_SNGLRT_CANN` - Singularity Cannon\
> `KEY:ATTK_SLNG_MSSDRVR` - Slingshot Massdriver\
> `KEY:ATTK_SLIVER_GUN` - Sliver Gun\
> `KEY:ATTK_STRLD_MISSL` - Starload Missile Launcher\
> `KEY:ATTK_STRNG_PRJCTR` - String Projector\
> `KEY:ATTK_ZERO_BORE` - Zero Bore\
> `KEY:AUTO_TINT` - Auto-tint\
> `KEY:AUTOFIRE` - Autofire\
> `KEY:AUTOCMP_DRVR_DERVISH` - Dervish AI-400 (Driver Autocomp)\
> `KEY:AUTOCMP_DRVR_PEGASUS` - Pegasus AI-200 (Driver Autocomp)\
> `KEY:AUTOCMP_DRVR_ROADLRD` - Roadlord AI-GA (Driver Autocomp)\
> `KEY:AUTOCMP_DRVR_TWISTER` - Twister AI-800 (Driver Autocomp)\
> `KEY:AUTOCMP_DRVR_ZEPHYR` - Zephyr AI-1200 (Driver Autocomp)\
> `KEY:AUTOCMP_GUNR_ADDER` - Adder AI-G2 (Gunner Autocomp)\
> `KEY:AUTOCMP_GUNR_DEADEYE` - Deadeye AI-G4 (Gunner Autocomp)\
> `KEY:AUTOCMP_GUNR_HOTSHOT` - Hotshot AI-G8 (Gunner Autocomp)\
> `KEY:AUTOCMP_GUNR_MARKSMN` - Marksman AI-GA (Gunner Autocomp)\
> `KEY:AUTOCMP_GUNR_RTTLSNK` - Rattlesnake AI-GX (Gunner Autocomp)\
> `KEY:AUTOFIRE` - Autofire\
> `KEY:AUTOPILOT` - Autopilot\
> `KEY:APRTR` - Aporter\
> `KEY:BACKFIRE_PALMPRINT_ID` - Backfire Palmprint ID\
> `KEY:BACKUP_IDCARD` - Backup ID\
> `KEY:BAL_THROWN` - Balanced\
> `KEY:BAL_RANGE` - Balanced\
> `KEY:BANE_A` - Bane\
> `KEY:BANE_AMMO` - Bane\
> `KEY:BANE_AR` - Bane\
> `KEY:BANE_M` - Bane\
> `KEY:BANE_MELEE` - Bane\
> `KEY:BANE_R` - Bane\
> `KEY:BANE_RANGED` - Bane\
> `KEY:BARBED` - Barbed\
> `KEY:BASH_H` - Bashing\
> `KEY:BASH_HVY` - Bashing\
> `KEY:BASH_L` - Bashing\
> `KEY:BASH_LT` - Bashing\
> `KEY:BATTERY_OF_2` - Battery of 2\
> `KEY:BATTERY_OF_3` - Battery of 3\
> `KEY:BATTERY_OF_4` - Battery of 4\
> `KEY:BATTERY_OF_5` - Battery of 5\
> `KEY:BAYONET` - Bayonet\
> `KEY:BB_TRP_GDGT_BRB` - Booby Trapped Gadget (Barbs)\
> `KEY:BB_TRP_GDGT_ELS` - Booby Trapped Gadget (Electric Shock)\
> `KEY:BB_TRP_GDGT_STB` - Booby Trapped Gadget (Stun Bolt)\
> `KEY:BB_TRP_GDGT_TIW` - Booby Trapped Gadget (Trigger Integrated
> Weapon)\
> `KEY:BDY_FDR` - Body Feeder\
> `KEY:BIND` - Blinding\
> `KEY:BLACK_HEADLIGHTS` - Black headlights\
> `KEY:BLADE_SHOE` - Blade\
> `KEY:BLADEGUN1` - Bladegun\
> `KEY:BLADEGUN2` - Bladegun\
> `KEY:BLADEGUN3` - Bladegun\
> `KEY:BLBD` - Billboard\
> `KEY:BLINDING` - Blinding\
> `KEY:BLINDMAN_EARIMPLANT` - Blindman Unit\
> `KEY:BLOWBACK_PALMPRINT_ID` - Blowback Palmprint ID\
> `KEY:BLWK_TAC_SHLD` - Bulwark Tactical Shield (PL5)\
> `KEY:BNB_IMPROVED_CRITICAL` - Improved Critical\
> `KEY:BNB_IMPROVED_GRAPPLE` - Improved Grapple\
> `KEY:BNB_IMPROVED_OVERRUN` - Improved Overrun\
> `KEY:BNB_MASTER_OF_DISGUISE` - Master of Disguise\
> `KEY:BNB_SCENT` - Scent\
> `KEY:BNS_AC_DEFL` - AC Bonus (Deflection)\
> `KEY:BNS_AC_INSI` - AC Bonus (Insight)\
> `KEY:BNS_AC_LUCK` - AC Bonus (Luck)\
> `KEY:BNS_AC_OTHE` - AC Bonus (Other)\
> `KEY:BNS_AC_PROF` - AC Bonus (Profane)\
> `KEY:BNS_AC_SCRD` - AC Bonus (Sacred)\
> `KEY:BNS_ENHC_AB` - Ability Bonus (Enhancement)\
> `KEY:BNS_ENHC_AC` - Armor Bonus (Enhancement)\
> `KEY:BNS_ENHC_NAT` - Natural Armor Bonus (Enhancement)\
> `KEY:BNS_EVASIVE_MANEUVERS` - Evasive Maneuvers\
> `KEY:BNS_FIGHTER_ESCORT` - Fighter Escort\
> `KEY:BNS_FORMATION_FLYING` - Formation Flying\
> `KEY:BNS_SAV_INS` - Save Bonus (Insight)\
> `KEY:BNS_SAV_LUC` - Save Bonus (Luck)\
> `KEY:BNS_SAV_OTH` - Save Bonus (Other)\
> `KEY:BNS_SAV_PRO` - Save Bonus (Profane)\
> `KEY:BNS_SAV_RES` - Save Bonus (Resistance)\
> `KEY:BNS_SAV_SAC` - Save Bonus (Sacred)\
> `KEY:BNS_SEMPER_FI` - Semper Fi\
> `KEY:BNS_SKL_CIR` - Skill Bonus (Circumstance)\
> `KEY:BNS_SKL_CMP` - Skill Bonus (Competence)\
> `KEY:BNS_SKL_LCK` - Skill Luck Bonus\
> `KEY:BNS_SPELL` - Bonus Spell\
> `KEY:BNS_SPL_RST` - Spell Resistance\
> `KEY:BNS_WINGMAN` - Wingman\
> `KEY:BODYFEED` - Bodyfeeder\
> `KEY:BOHMASABCOUR` - Absolute Courage\
> `KEY:BOHMASABPUR` - Absolute Purity\
> `KEY:BOHMASCHAR` - Charity\
> `KEY:BOHMASCOUR` - Courage\
> `KEY:BOHMASCRYS` - Crystal\
> `KEY:BOHMASDWARD` - Deathward\
> `KEY:BOHMASFAITH` - Faith\
> `KEY:BOHMASGOLD` - Gold\
> `KEY:BOHMASPLAT` - Platinum\
> `KEY:BOHMASPUR` - Purity\
> `KEY:BOHMASSILV` - Silver\
> `KEY:BOHMWEAPCRYS` - Crystal\
> `KEY:BOHMWEAPGLD` - Gold\
> `KEY:BOHMWEAPPLAT` - Platinum\
> `KEY:BOHMWEAPSILV` - Silver\
> `KEY:BONE` - Bone\
> `KEY:BOOBY_TRAPPED` - Booby trapped\
> `KEY:BOWSTR` - Bow\_STR\
> `KEY:BOWSTR` - \#Bow\_STR\
> `KEY:BRASS` - Brass\
> `KEY:BREAKDOWN_GUN` - Electronic Scope\
> `KEY:BRCD_TAC_SHLD` - Barricade Tactical Shield (PL7)\
> `KEY:BRI_EN_A` - Brilliant Energy\
> `KEY:BRI_EN_M` - Brilliant Energy\
> `KEY:BRI_EN_T` - Brilliant Energy\
> `KEY:BRILNT_MELEE` - Brilliant\
> `KEY:BRONZE` - Bronze\
> `KEY:BSTN_TAC_SHLD` - Bastion Tactical Shield (PL6)\
> `KEY:BTVSUNDER` - Sundering\
> `KEY:BUMP_BLAST` - Bumpers of Blasting\
> `KEY:BUMP_RAM` - Bumper of the Ram\
> `KEY:BURSTFIRE` - Burst fire\
> `KEY:C_IRON` - Cold Iron\
> `KEY:C_IRON/2` - 1/2 Cold Iron <span class="new"> (deprecated)
> </span>\
> `KEY:CAST` - Spellcasting\
> `KEY:CASTSUP` - Spellcasting (Superior)\
> `KEY:CATCHING` - Catching\
> `KEY:CBQ_WEAPON` - CBQ\
> `KEY:CERAMIC` - Ceramic\
> `KEY:CERAMIC_ARM` - Ceramics\
> `KEY:CERAMIC_WEAP` - Ceramics\
> `KEY:CHAMPDET` - Champion Detecting\
> `KEY:CHARGED_ITEM_12` - Charges (12)\
> `KEY:CHAOS_A` - Anarchic, Chaotic\
> `KEY:CHAOS_M` - Anarchic, Chaotic\
> `KEY:CHAOS_POWER_AMMO` - Anarchic Energy\
> `KEY:CHAOS_POWER_MELEE` - Anarchic Energy\
> `KEY:CHAOS_POWER_RANGED` - Anarchic Energy\
> `KEY:CHAOS_R` - Anarchic, Chaotic\
> `KEY:CHAOTIC_MELEE` - Chaotic\
> `KEY:CHAOTIC_RANGED` - Chaotic\
> `KEY:CHARGED_ITEM_3` - Charges (3)\
> `KEY:CHARGED_ITEM_4` - Charges (4)\
> `KEY:CHARGED_ITEM_5` - Charges (5)\
> `KEY:CHARGED_ITEM_7` - Charges (7)\
> `KEY:CHARGED_ITEM_10` - Charges (10)\
> `KEY:CHARGED_ITEM_12` - Charges (12)\
> `KEY:CHARGED_ITEM_14` - Charges (14)\
> `KEY:CHARGED_ITEM_34` - Charges (34)\
> `KEY:CHARGED_ITEM_36` - Charges (36)\
> `KEY:CHARGED_ITEM_50` - Charges (50)\
> `KEY:CHARGED_ITEM_101` - Charges (101)\
> `KEY:CHMLNC_SRFC_GDGT` - Chameleonic Surface Gadget\
> `KEY:CHRGD` - Charged\
> `KEY:CHRSNTHMM_LSR_ARR` - Chrysanthemum Laser Array (PL 6)\
> `KEY:CHTR` - Chemical Treating\
> `KEY:CLAY` - Clay\
> `KEY:CLIMB` - Climbing\
> `KEY:CLOTH` - Cloth\
> `KEY:CL1_SNSR_SYS` - Class I Sensor System (PL6)\
> `KEY:CL2_SNSR_SYS` - Class II Sensor System (PL6)\
> `KEY:CL3_SNSR_SYS` - Class III Sensor System (PL6)\
> `KEY:CL4_SNSR_SYS` - Class IV Sensor System (PL7)\
> `KEY:CL5_SNSR_SYS` - Class V Sensor System (PL7)\
> `KEY:CL6_SNSR_SYS` - Class VI Sensor System (PL8)\
> `KEY:CLLPSBL_GDGT` - Collapsible Gadget\
> `KEY:CLOAKING_DEVICE` - Cloaking device\
> `KEY:CLOAKING_SCRN` - Cloaking Screen (PL8)\
> `KEY:CLOTHYRD_SHAFT` - Clothyard Shaft\
> `KEY:CLLPSBL_GDGT` - Collapsible Gadget\
> `KEY:CMPCT_GDGT_EQP` - Compact Gadget\
> `KEY:CMPCT_GDGT_WPN` - Compact Gadget\
> `KEY:COCKPIT_COPILOT` - Cockpit (Copilot)\
> `KEY:COCKPIT_PASSNGR` - Cockpit (Passenger)\
> `KEY:COCKPIT_PILOT` - Cockpit (Pilot)\
> `KEY:COL_AVNG_ELCT_SCM` - Avenger Electro-Scimitar (PL 8)\
> `KEY:COL_JUMP_DRIVE` - Jump Drive (Colossal)\
> `KEY:COL_LK8_AMRPCG_PK` - LK8 Armor-Piercing Pike (PL 6)\
> `KEY:COL_MCH` - Colossal Mecha\
> `KEY:COL_PS15_PNTR_CLW` - PS-15 Panther Claws (PL 5)\
> `KEY:COL_PS25_TIGR_CLW` - PS-25 Tiger Claws (PL 7)\
> `KEY:COL_PTHN_ELCT_WHP` - XJ-A Python Electro-Whip (PL 7)\
> `KEY:COL_QUAD_MCH` - Quadrupedal\
> `KEY:COL_RP91_RPR_LSCT` - RP-91 Reaper Laser Scythe (PL 8)\
> `KEY:COL_THNDRB_SHK_RD` - Thunderbolt Shock Rod (PL 5)\
> `KEY:COLD_RES` - Cold Resistance\
> `KEY:COLD_WARD` - Cold Warding\
> `KEY:COLLI_A` - Collision (+2)\
> `KEY:COLLI_M` - Collision (+2)\
> `KEY:COLLI_R` - Collision (+2)\
> `KEY:COMFORT` - Comfort\
> `KEY:COMM_ANSIBLE` - Ansible\
> `KEY:COMM_DRIVE_TRNSCVR` - Drive Transceiver\
> `KEY:COMM_DRIVESAT` - Drivesat Comm Array\
> `KEY:COMM_INTERNAL_AUDIO` - Internal Audio Comm System\
> `KEY:COMM_INTERNAL_VIDEO` - Internal Video Comm System\
> `KEY:COMM_LASER_TRNSCVR` - Laser Transceiver\
> `KEY:COMM_MASS_TRNSCVR` - Mass Transceiver\
> `KEY:COMM_RADIO_TRNSCVR` - Radio Transceiver\
> `KEY:COMM_SYSTEM` - Comm System\
> `KEY:COMPUTER_PLUS_1` - +1\
> `KEY:COMPUTER_PLUS_2` - +2\
> `KEY:COMPUTER_PLUS_3` - +3\
> `KEY:CONCEALED_MACHINE_GUN` - Concealed machine gun\
> `KEY:CONCRETE` - Concrete\
> `KEY:COPYCAT` - Copycat\
> `KEY:CORONA_MICROWV_BM` - Corona Microwave Beam (PL 6)\
> `KEY:CORRUPTED` - Corrupted\
> `KEY:CORRUPTING` - Corrupting\
> `KEY:COUNTER_SURVEILLANCE` - Counter surveillance\
> `KEY:COUPGR_A` - Coup de Grace (+5)\
> `KEY:COUPGR_M` - Coup de Grace (+5)\
> `KEY:COUPGR_R` - Coup de Grace (+5)\
> `KEY:CPNT_ABLATV` - Ablative Paint Job\
> `KEY:CPNT_BLUR` - Paint Job of Blurring\
> `KEY:CPNT_FLAME` - Flame Job\
> `KEY:CPNT_NDSCRPT` - Nondescript Paint Job\
> `KEY:CPNT_SHRNK` - Shrinking Paint Job\
> `KEY:CREATDET` - Creature Detecting\
> `KEY:CRKRJCK_NRL_LNK` - Crackerjack Neural Link (PL 8)\
> `KEY:CRSTLCBN_ARMR` - Crystal Carbon Armor (PL7)\
> `KEY:CRUSH` - Crushing\
> `KEY:CRYS_DEEP` - Crystal (Deep)\
> `KEY:CRYS_DEEP_ITEM` - Crystal (Deep)\
> `KEY:CRYS_MUN` - Crystal (Mundane)\
> `KEY:CRYS_MUN_ITEM` - Crystal (Mundane)\
> `KEY:CRYSTAL` - Crystalline\
> `KEY:CTAR_TRNKMSK` - Trunk of Masking\
> `KEY:CUSGRIP` - Custom Grip\
> `KEY:CUSSIT` - Custom Sights\
> `KEY:CUST_HILT` - Custom Hilt\
> `KEY:CUSTH1` - Custom Fitx1 \[Heavy Armor\]\
> `KEY:CUSTH2` - Custom Fitx2 \[Heavy Armor\]\
> `KEY:CUSTH3` - Custom Fitx3 \[Heavy Armor\]\
> `KEY:CUSTL1` - Custom Fitx1 \[Light Armor\]\
> `KEY:CUSTL2` - Custom Fitx2 \[Light Armor\]\
> `KEY:CUSTL3` - Custom Fitx3 \[Light Armor\]\
> `KEY:CUSTM1` - Custom Fitx1 \[Medium Armor\]\
> `KEY:CUSTM2` - Custom Fitx2 \[Medium Armor\]\
> `KEY:CUSTM3` - Custom Fitx3 \[Medium Armor\]\
> `KEY:CUSTOMA` - Custom - Armor.Shield\
> `KEY:CUSTOMW` - Custom - Weapon\
> `KEY:D_DRV_GNRTR8` - D-Drive Generator (PL8)\
> `KEY:D_DRV_GNRTR9` - D-Drive Generator (PL9)\
> `KEY:D_1USEMA` - Spell Effect (Single Use/Completion)\
> `KEY:D_1USEME` - Spell Effect (Single Use/Completion)\
> `KEY:D_1USEMI` - Spell Effect (Single Use/Completion)\
> `KEY:DAGSLVR` - Silvered - Dagger\
> `KEY:DAMAGE_REDUCT_5` - Damage Reduction (5/+1)\
> `KEY:DAMAGE_REDUCT_10` - Damage Reduction (10/+1)\
> `KEY:DANCE` - Dancing\
> `KEY:DANCING` - Dancing\
> `KEY:DANGER_EARIMPLANT` - Danger Unit\
> `KEY:DARK` - Darkwood\
> `KEY:DBL_SIDED` - Double-sided\
> `KEY:DBLTAP` - Double Tap fire\
> `KEY:DEFEND` - Defending\
> `KEY:DEFENDING` - Defending\
> `KEY:DEFLECTN_FLD1` - Deflection Field Mk 1(PL8)\
> `KEY:DEFLECTN_FLD2` - Deflection Field Mk 2(PL8)\
> `KEY:DEFLECTN_FLD3` - Deflection Field Mk 3(PL8)\
> `KEY:DEFLECTN_FLD4` - Deflection Field Mk 4(PL8)\
> `KEY:DEFLECTN_FLD5` - Deflection Field Mk 5(PL8)\
> `KEY:DEMONREP` - Demon Repelling\
> `KEY:DETSTK` - Detachable Stock\
> `KEY:DFNS_ADV_DMG_CTRL` - Advanced Damage Control\
> `KEY:DFNS_AUTOPILOT` - Autopilot System\
> `KEY:DFNS_CHAFF_LNCH` - Chaff launcher\
> `KEY:DFNS_CHAFF_LNCH_8` - Chaff launcher\
> `KEY:DFNS_CHAFF_LNCH_8_2` - 2 Chaff launchers\
> `KEY:DFNS_CLOAK_SCRN` - Cloaking Screen\
> `KEY:DFNS_DMG_CTRL_SYS` - Damage Control System\
> `KEY:DFNS_DECOY_LNCH` - Decoy drone launcher\
> `KEY:DFNS_DECOY_LNCH_2` - Decoy drone launcher\
> `KEY:DFNS_DECOY_LNCH_4_2` - 2 Decoy drone launchers\
> `KEY:DFNS_DECOY_LNCH_8` - Decoy drone launcher\
> `KEY:DFNS_DISPLACER` - Displacer\
> `KEY:DFNS_HEAVY_FRTFCTN` - Heavy Fortification\
> `KEY:DFNS_IMP_AUTOPILOT` - Improved Autopilot System\
> `KEY:DFNS_IMP_DMG_CTRL` - Improved Damage Control\
> `KEY:DFNS_LGHT_FRTFCTN` - Light Fortification\
> `KEY:DFNS_MGNT_FLD` - Magnetic Field\
> `KEY:DFNS_MEDM_FRTFCTN` - Medium Fortification\
> `KEY:DFNS_NANITE_REPAIR` - Nanite Repair Array\
> `KEY:DFNS_PRTCL_FLD` - Particle Field\
> `KEY:DFNS_RAD_SHLD` - Radiation Shielding\
> `KEY:DFNS_REPAIR_DRONE` - Repair drones\
> `KEY:DFNS_SLF_DSTR_SYS` - Self-destruct System\
> `KEY:DFNS_SNSR_JAM` - Sensor Jammer\
> `KEY:DFNS_STLTH_SCRN` - Stealth Screen\
> `KEY:DIRE` - Dire\
> `KEY:DISLOC_A` - Dislocator (+3)\
> `KEY:DISLOC_GRT_A` - Dislocator (Greater) (+4)\
> `KEY:DISLOC_GRT_M` - Dislocator (Greater) (+4)\
> `KEY:DISLOC_GRT_R` - Dislocator (Greater) (+4)\
> `KEY:DISLOC_M` - Dislocator (+3)\
> `KEY:DISLOC_R` - Dislocator (+3)\
> `KEY:DISPEL` - Dispelling\
> `KEY:DISRPT` - Disruption\
> `KEY:DISRUPTING` - Disruption\
> `KEY:DISRUPTION_MIGHTY` - Mighty Disruption\
> `KEY:DISSIP` - Dissipater\
> `KEY:DISTANT_SHOT` - Distant Shot\
> `KEY:DISTANCE` - Distance\
> `KEY:DISTNC` - Distance\
> `KEY:DIVINGSUIT_PROPELLERS` - Propellers\
> `KEY:DLPHI_DEF_ST1` - Delphi Defense Suite Mk 1 (PL7)\
> `KEY:DLPHI_DEF_ST2` - Delphi Defense Suite Mk 2 (PL7)\
> `KEY:DLPHI_DEF_ST3` - Delphi Defense Suite Mk 3 (PL7)\
> `KEY:DLPHI_DEF_ST4` - Delphi Defense Suite Mk 4 (PL7)\
> `KEY:DLPHI_DEF_ST5` - Delphi Defense Suite Mk 5 (PL7)\
> `KEY:DR_CONVERSION_ARCHAIC` - Damage Reduction Conversion\
> `KEY:DR_CONVERSION_MODERN` - Damage Reduction Conversion\
> `KEY:DR_CONVERSION_POWERED` - Damage Reduction Conversion\
> `KEY:DRACO` - Dragonhide\
> `KEY:DREAD_AMMO` - Dread\
> `KEY:DREAD_MELEE` - Dread\
> `KEY:DREAD_RANGED` - Dread\
> `KEY:DUMMY_LINE` - Dummy line\
> `KEY:DUPLICATION_IDCARD` - Duplication\
> `KEY:DURAH1` - Durabilityx1 \[Heavy Armor\]\
> `KEY:DURAH2` - Durabilityx2 \[Heavy Armor\]\
> `KEY:DURAH3` - Durabilityx3 \[Heavy Armor\]\
> `KEY:DURAH4` - Durabilityx4 \[Heavy Armor\]\
> `KEY:DURAH5` - Durabilityx5 \[Heavy Armor\]\
> `KEY:DURAL1` - Durabilityx1 \[Light Armor\]\
> `KEY:DURAL2` - Durabilityx2 \[Light Armor\]\
> `KEY:DURAL3` - Durabilityx3 \[Light Armor\]\
> `KEY:DURAL4` - Durabilityx4 \[Light Armor\]\
> `KEY:DURAL5` - Durabilityx5 \[Light Armor\]\
> `KEY:DURAM1` - Durabilityx1 \[Medium Armor\]\
> `KEY:DURAM2` - Durabilityx2 \[Medium Armor\]\
> `KEY:DURAM3` - Durabilityx3 \[Medium Armor\]\
> `KEY:DURAM4` - Durabilityx4 \[Medium Armor\]\
> `KEY:DURAM5` - Durabilityx5 \[Medium Armor\]\
> `KEY:DURALLOY` - Duralloy (PL6)\
> `KEY:DURALLOY_ARMR` - Duralloy Armor (PL6)\
> `KEY:DURASTEEL_ARM` - Durasteel\
> `KEY:DURASTEEL_SHIELD` - Durasteel\
> `KEY:DURASTEEL_WEAP` - Durasteel\
> `KEY:DURPLSTC_ARMR` - Duraplastic Armor (PL5)\
> `KEY:DWMW` - Dwarven Masterwork\
> `KEY:ECTO` - Ectoplasmic\
> `KEY:ECTOPLAS` - Ectoplasmic\
> `KEY:EDUCATEDFEATIMPLANT` - Educated Feat Implant\
> `KEY:EJECTION_SEATS` - Ejection seats\
> `KEY:ELAC_PRLTCAL` - Paralytic Alarm\
> `KEY:ELEC_RES` - Electricity Resistance\
> `KEY:ELAC_SLNTWRN` - Silent Warning Alarm\
> `KEY:ELDBLAST_M` - Eldritch Blasting - Weapon.Melee\
> `KEY:ELDBLAST_R` - Eldritch Blasting - Weapon.Ranged\
> `KEY:ELECTRIC_WARD` - Lightning Warding\
> `KEY:ELECTRIFIED_FRAME` - Electrified frame\
> `KEY:ELECTRONIC_LOCKPICK_IDCARD` - Electronic Lockpick\
> `KEY:ELMW` - Elvish Masterwork\
> `KEY:ENERGY_BLAST_ACID` - Acid Blast\
> `KEY:ENERGY_BLAST_COLD` - Icy Blast\
> `KEY:ENERGY_BLAST_ELEC` - Electrical Blast\
> `KEY:ENERGY_BLAST_FIRE` - Fiery Blast\
> `KEY:ENERGY_BLAST_SONIC` - Concussive Blast\
> `KEY:ENGM_SNSR_ST` - Enigma Sensor Suite (PL6)\
> `KEY:ENGN_FUSION` - Fusion Torch\
> `KEY:ENGN_GRAVITIC` - Gravitic Redirector\
> `KEY:ENGN_INDCTN` - Induction Engine\
> `KEY:ENGN_INFSPD` - Engine of Infernal Speed\
> `KEY:ENGN_INRT_FLUX` - Inertial Flux Engine\
> `KEY:ENGN_ION` - Ion Engine\
> `KEY:ENGN_PARTCL` - Particle Impulse\
> `KEY:ENGN_PHOTON` - Photon Sails\
> `KEY:ENGN_SPATIAL` - Spatial Compressor\
> `KEY:ENGN_THRUST` - Thrusters\
> `KEY:ENH_ALL1` - Enhanced Alloyx1\
> `KEY:ENH_ALL2` - Enhanced Alloyx2\
> `KEY:ENH_ALL3` - Enhanced Alloyx3\
> `KEY:ENVRNMNT_SL_GDGT` - Environment Seal Gadget\
> `KEY:EOLA` - Easy-Off (Light Armor)\
> `KEY:EOLM` - Easy-Off (Medium Armor)\
> `KEY:EOLH` - Easy-Off (Heavy Armor)\
> `KEY:EPIC_ABILITY_BONUS_ENHANCE` - |Epic Ability Bonus (Enhancement)\
> `KEY:EPIC_AC_BONUS_DEFLECT` - |Epic AC Bonus (Deflection)\
> `KEY:EPIC_AC_BONUS_LUCK` - |Epic AC Bonus (Luck)\
> `KEY:EPIC_AC_BONUS_INSIGHT` - |Epic AC Bonus (Insight)\
> `KEY:EPIC_AC_BONUS_SACRED` - |Epic AC Bonus (Sacred)\
> `KEY:EPIC_AC_BONUS_PROFANE` - |Epic AC Bonus (Profane)\
> `KEY:EPIC_AC_BONUS_OTHER` - |Epic AC Bonus (Other)\
> `KEY:EPIC_BONUS_ARMR_ENHANCE` - |Epic Armor Bonus (Enhancement)\
> `KEY:EPIC_BONUS_SPELL`

