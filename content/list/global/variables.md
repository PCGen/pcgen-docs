+++
date = "2016-08-01"
title = "The TYPE: Variables"
original_url = "/list/global/variables.html"

[menu.main]
    identifier = "global_variables"
    name = "The TYPE: Variables"
    parent = "global"
    
+++
This is a list in progress. Just because the TYPE: variable that you
want to use is not listed does not mean that you cannot use it, just
that it has not been listed yet

------------------------------------------------------------------------

<span id="standard"></span> Application Standard
------------------------------------------------

**General Notes**

-   The preferred version of multiple word TYPE: variables is
    OneTwoThree, AKA HeavyGyroJetLauncher.
-   The use of Heavy\_GyroJet\_Launcher is also permitted.
-   The use of Heavy GyroJet Launcher will cause indexing problems and
    is not permitted.

<!-- -->

-   For searching purposes, put all like items in the same TYPE:
    statement, separated by periods (.). The exact sequence of variables
    listed does not matter, can be alphabetical, numbertical, or mixed.
-   TYPE:Class.Hidden.RadiantEnlightenment
-   This will cause this item to show up in searches of Class, Hidden,
    and RadiantEnlightenment in hidden\_feats groups.
-   TYPE:NPC.Base
-   This will cause this item to show up in searches of NPC and Base in
    Classes groups.

------------------------------------------------------------------------

-   A problem with one of the parser. When it looks at some of the
    variables it parses them strangely. It is best to avoid the use of
    MIN and MAX in your variables till the parser is replaced in the
    area of 6.0+
-   For some idea of other things to avoid try [Math Operators and
    Formulas](/globalfilesformulas.html) .
-   The variable CHAMIN3 is coming out as min(CHA,3).
-   The variable MindBladeECL is coming out as ()MIN(dBladeECL).
-   The TYPE Illumination is apparently coming out as (Illu)MIN(ation).

<span id="glossary"></span> The Variable Glossary
-------------------------------------------------

### By Gamemode {#by-gamemode .indent1}

The following list of keys covers all keys used in the following
gamemodes.

> **Gamemode**
>
> > Publisher - Setting/Dataset
>
> **D&D 3.0 Edition (3e)**
>
> > [Bastion Press (BP) - Faeries](/list/global/variables.html#bp)
>
> **D&D 3.5 Edition (35e)**
>
> > [Alea Publishing Group (APG) - A Question of
> > Loyalty](/list/global/variables.html#apg1)\
> > [Alea Publishing Group (APG) - Honor and
> > Corruption](/list/global/variables.html#apg2)\
> > [Bards and Sages (BaS) - Neiyar](/list/global/variables.html#bas)\
> > [Behemoth3 (B3) - Masters and
> > Minions](/list/global/variables.html#b3)\
> > [Big Finger Games (BFG) - Fantasy Folio - Masterwork
> > Qualities](/list/global/variables.html#bfg)\
> > [Bloodstone Press (BSP) - God
> > Spells](/list/global/variables.html#bsp)\
> > [Bloodstone Press (BSP) - Spellbinder's
> > Sourcebook](/list/global/variables.html#bsp1)\
> > [Bloodstone Press (BSP) - Spellbinder's Sourcebook
> > II](/list/global/variables.html#bsp2)\
>
> **<span id="deadlands"></span> Deadlands**
>
> **<span id="modern"></span> d20 Modern (Modern)**
>
> > [Battlefield Press (BP) - Pulp
> > Fantasy](/list/global/variables.html#bfp)\
> > [Bloodstone Press (BSP) - 22 Talent
> > Trees](/list/global/variables.html#bsp3)\
> > [Blue Devil Games (BDG) -
> > Dawningstar](/list/global/variables.html##bdg)\
>
> **<span id="sidewinder"></span> Sidwinder**
>
> **<span id="spycraft"></span> Spycraft**
>
> **<span id="xcrawl"></span> XCrawl**
>
> ------------------------------------------------------------------------
>
> <span id="apg1"></span> **Alea Publishing Group (APG) - A Question of
> Loyalty (35e)**
>
> > **APG questionloyalty\_class\_prestige.lst File.**
> >
> > `TYPE:PC.Prestige`
> >
> > **APG questionloyalty\_feats.lst File.**
> >
> > `TYPE:General`\
> > `TYPE:General.Fighter`\
> > `TYPE:Order`
> >
> > **APG questionloyalty\_feats\_hidden.lst File.**
> >
> > `TYPE:Class.Hidden`\
> > `TYPE:Class.Hidden.AncientHealing`\
> > `TYPE:Class.Hidden.RadiantEnlightenment`\
> > `TYPE:Class.Hidden.SecretEnlightenment`\
> > `TYPE:Class.Hidden.TeutonicKnightCombat`\
> > `TYPE:Internal`
> >
> > **APG questionloyalty\_races\_monsters.lst File.**
> >
> > `TYPE:Animal`\
> > `TYPE:Undead`\
> > `TYPE:Vermin`\
> >
> > **APG questionloyalty\_skills.lst File.**
> >
> > `TYPE:None`
> >
> > **APG questionloyalty\_spells.lst File.**
> >
> > `TYPE:Divine`
> >
> > **APG questionloyalty\_templates.lst File.**
> >
> > `TYPE:KnighthoodAPG`
>
> <span id="apg2"></span> **Alea Publishing Group (APG) - Honor and
> Corruption (35e)**
>
> > **APG honorcorruption\_feats.lst File.**
> >
> > `TYPE:General`\
> > `TYPE:Metamagic`\
> > `TYPE:Rogue`
> >
> > **APG honorcorruption\_feats\_hidden.lst File.**
> >
> > `TYPE:Subclass.Hidden.KnightHP`\
> > `TYPE:Subclass.Hidden.ScoundrelHP`
> >
> > **APG honorcorruption\_races.lst File.**
> >
> > `TYPE:Humanoid`\
>
> ------------------------------------------------------------------------
>
> <span id="ap"></span> **Avalanche Press (AP) - Vlad the Impaler (3e)**
>
> > **AP vlad\_classes.lst File.**
> >
> > `TYPE:PC.Prestige`\
> > `TYPE:NPC.Base`
> >
> > **AP vlad\_feats.lst File.**
> >
> > `TYPE:General`
> >
> > **AP vlad\_skills.lst File.**
> >
> > `TYPE:Intelligence.Knowledge`
> >
> > **AP vlad\_templates.lst File.**
> >
> > `TYPE:Undead`
> >
> > **AP vlad\_weaponprofs.lst File.**
> >
> > `TYPE:Arquebus`\
> > `TYPE:Cannon`
> >
> > **AP vlad\_weapons.lst File.**
> >
> > `TYPE:Weapon.Arquebus.Ranged.Projectile`\
> > `TYPE:Weapon.Cannon.Ranged.Projectile`
>
> ------------------------------------------------------------------------
>
> <span id="bas"></span> **Bards and Sages (BaS) - Neiyar (35e)**
>
> > **BaS neiyar\_classes.lst File.**
> >
> > `TYPE:Base.PC`\
> > `TYPE:PC.Prestige`
> >
> > **BaS neiyar\_eqmods.lst File.**
> >
> > `TYPE:Weapon.Slashing.Melee`
> >
> > **BaS neiyar\_equip\_magic\_items.lst File.**
> >
> > `TYPE:Armor.Light.Suit.Specific.Nonmetal`\
> > `TYPE:Enhancement.Ammunition.SpecificArrow.Individual`\
> > `TYPE:Enhancement.Shield.Heavy.Specific`\
> > `TYPE:Enhancement.Weapon.Melee.Martial.Specific.Bashing.Mace`\
> > `TYPE:Enhancement.Weapon.Melee.Martial.Specific.Slashing.Sword`\
> > `TYPE:Goods`\
> > `TYPE:Goods.Alchemical.Consumable`\
> > `TYPE:Goods.Book`\
> > `TYPE:Goods.Boot`\
> > `TYPE:Goods.Container`\
> > `TYPE:Goods.Food`\
> > `TYPE:Goods.Glove`\
> > `TYPE:Goods.Poison`\
> > `TYPE:Goods.Tools.Instrument.Percussion.Resizable.Weapon.Melee.Exotic.Slashing`\
> > `TYPE:Goods.Tools.Instrument.Wind.Resizable.Weapon.Melee.Simple.Bashing`\
> > `TYPE:Goods.Tools.SurgeryTools`\
> > `TYPE:Goods.Weapon.Melee`\
> > `TYPE:Magic.Artifact`\
> > `TYPE:Magic.Artifact.Armor.Light.Suit.Specific.Nonmetal`\
> > `TYPE:Magic.Artifact.Armor.Medium.Suit.Specific`\
> > `TYPE:Magic.Artifact.Enhancement.Shield.Heavy.Specific`\
> > `TYPE:Magic.Artifact.Enhancement.Weapon.Melee.Martial.Specific.Slashing.Sword`\
> > `TYPE:Magic.Artifact.Enhancement.Weapon.Melee.Simple.Specific.Bludgeoning.Mace`\
> > `TYPE:Magic.Potion.Consumable`\
> > `TYPE:Magic.Ring`\
> > `TYPE:Magic.Staff`\
> > `TYPE:Magic.Wand`\
> > `TYPE:Magic.Wondrous`\
> > `TYPE:Magic.Wondrous.Amulet`\
> > `TYPE:Magic.Wondrous.Boot`\
> > `TYPE:Magic.Wondrous.Bracelet`\
> > `TYPE:Magic.Wondrous.Headgear`\
> > `TYPE:Shield.Buckler.Standard`\
> > `TYPE:Shield.Heavy.Standard`\
> > `TYPE:Weapon.Exotic.Melee.Standard.Slashing.Sword`\
> > `TYPE:Weapon.Exotic.Ranged.Standard.Thrown`\
> > `TYPE:Weapon.Melee.Exotic.Reach.Finesseable.Subdual.Slashing`\
> > `TYPE:Weapon.Melee.Finesseable.Martial.Standard.Piercing.Sword`\
> > `TYPE:Weapon.Melee.Finesseable.Ranged.Thrown.Simple.Standard.Piercing.Slashing.Dagger`
> >
> > **BaS neiyar\_feats.lst File.**
> >
> > `TYPE:Clerical`\
> > `TYPE:Fighter`\
> > `TYPE:General`
> >
> > **BaS neiyar\_feats\_flaws.lst File.**
> >
> > `TYPE:Flaw`
> >
> > **BaS neiyar\_feats\_hidden.lst File.**
> >
> > `TYPE:BenevolentSpirit`\
> > `TYPE:Class.Hidden`\
> > `TYPE:HearthMagic`\
> > `TYPE:ShalraekuZarakku`
> >
> > **BaS neiyar\_languages.lst File.**
> >
> > `TYPE:Read.Written.Spoken`\
> > `TYPE:Spoken`
> >
> > **BaS neiyar\_races\_base.lst File.**
> >
> > `TYPE:Humanoid`
> >
> > **BaS neiyar\_races\_monster.lst File.**
> >
> > `TYPE:Animal`\
> > `TYPE:Humanoid`\
> > `TYPE:Plant`\
> > `TYPE:Undead`\
> > `TYPE:Vermin`
> >
> > **BaS neiyar\_skills.lst File.**
> >
> > `TYPE:HearthMagic`\
> > `TYPE:Intelligence.Craft`\
> > `TYPE:Intelligence.Knowledge`\
> > `TYPE:Wisdom.Profession`
> >
> > **BaS neiyar\_spells.lst File.**
> >
> > `TYPE:Arcane`\
> > `TYPE:Arcane.Divine`\
> > `TYPE:Divine`
> >
> > **BaS neiyar\_weaponprof.lst File.**
> >
> > `TYPE:Exotic`\
> > `TYPE:Simple`
>
> ------------------------------------------------------------------------
>
> <span id="bp"></span> Bastion Press (BP) - Faeries (3e)
>
> > **BP faeries\_classes.lst File.**
> >
> > `TYPE:PC.Prestige`
> >
> > **BP faeries\_feats.lst File.**
> >
> > `TYPE:Fey`\
> > `TYPE:General`\
> > `TYPE:ItemCreation`\
> > `TYPE:Metamagic`\
> > `TYPE:Special`
> >
> > **BP faeries\_feats\_aspects.lst File.**
> >
> > `TYPE:AspectOfNature`
> >
> > **BP faeries\_feats\_hidden.lst File.**
> >
> > `TYPE:FaerieRacialTrait`\
> >
> > `TYPE:FeyArts`\
> >
> > `TYPE:Special.RacialTraitCost`\
> >
> > `TYPE:Special.UncannyDodge`
> >
> > **BP faeries\_languages.lst File.**
> >
> > `TYPE:Spoken`
> >
> > **BP faeries\_skills.lst File.**
> >
> > `TYPE:Intelligence.Knowledge`
> >
> > **BP faeries\_spells.lst File.**
> >
> > `TYPE:Arcane`\
> > `TYPE:Divine`
> >
> > **BP faeries\_templates\_focus.lst File.**
> >
> > `TYPE:Fey`\
> > `TYPE:Humanoid`\
> > `TYPE:Giant`
>
> ------------------------------------------------------------------------
>
> <span id="bfp"></span> Battlefield Press (BP) - Pulp Fantasy (Modern)
>
> > **BP pulpfantasy\_abilities.lst File.**
> >
> > `TYPE:`\
> > `TYPE:AddTalent.FastTalent.ToughTalent.SmartTalent.DedicatedTalent.CharismaticTalent`\
> > `TYPE:AddTalent.StrongTalent.FastTalent.SmartTalent.DedicatedTalent.CharismaticTalent`\
> > `TYPE:AddTalent.StrongTalent.FastTalent.ToughTalent.SmartTalent.CharismaticTalent`\
> > `TYPE:AddTalent.StrongTalent.FastTalent.ToughTalent.SmartTalent.DedicatedTalent`\
> > `TYPE:AddTalent.StrongTalent.ToughTalent.SmartTalent.DedicatedTalent.CharismaticTalent`\
> > `TYPE:CharismaticPlus`\
> > `TYPE:DedicatedPlus`\
> > `TYPE:Talent.CharismaticTalent.Authority`\
> > `TYPE:Talent.CharismaticTalent.ByGraceOfFortune`\
> > `TYPE:Talent.DedicatedTalent.Attentive`\
> > `TYPE:Talent.FastTalent.Elusive`\
> > `TYPE:Talent.FastTalent.InstinctiveResponse`\
> > `TYPE:Talent.FastTalent.NeedForSpeed`\
> > `TYPE:Talent.FastTalent.Precision`\
> > `TYPE:Talent.SmartTalent.BrainsOverBrawn`\
> > `TYPE:Talent.SmartTalent.Deduction`\
> > `TYPE:Talent.SmartTalent.FastLearner`\
> > `TYPE:Talent.SmartTalent.MechanicalAptitude`\
> > `TYPE:Talent.SmartTalent.Prodigy`\
> > `TYPE:Talent.SmartTalent.Research`\
> > `TYPE:Talent.StrongTalent.Brawler`\
> > `TYPE:Talent.StrongTalent.Soldiery`\
> > `TYPE:Talent.ToughTalent.Rage`\
> > `TYPE:Talent.ToughTalent.Survivalist`
> >
> > **BP pulpfantasy\_classes\_advanced.lst File.**
> >
> > `TYPE:Advanced.PC`
> >
> > **BP pulpfantasy\_classes\_monster.lst File.**
> >
> > `TYPE:Monster`
> >
> > **BP pulpfantasy\_equip.lst File.**
> >
> > `TYPE:Gadget`\
> > `TYPE:Goods.Boot`\
> > `TYPE:Goods.General`\
> > `TYPE:Goods.Clothing`\
> > `TYPE:Goods.Clothing.Belt`\
> > `TYPE:Goods.Container.General`\
> > `TYPE:Goods.General`\
> > `TYPE:Goods.Headgear`\
> > `TYPE:Goods.Tools`\
> > `TYPE:Goods.Tools.Consumer`\
> > `TYPE:Goods.Tools.Consumer.Photo`\
> > `TYPE:Goods.Tools.Medical`\
> > `TYPE:Goods.Tools.Medical.Consumable`\
> > `TYPE:Goods.WeaponAccessory.Consumable`
> >
> > **BP pulpfantasy\_equip\_armor.lst File.**
> >
> > `TYPE:Armor.Light.Suit.Tactical`\
> > `TYPE:Armor.Medium.Suit.Tactical`\
> > `TYPE:Armor.Heavy.Suit.Tactical`
> >
> > **BP pulpfantasy\_equip\_poisons.lst File.**
> >
> > `TYPE:Goods.Poison.Consumable`
> >
> > **BP pulpfantasy\_equip\_vehicles.lst File.**
> >
> > `TYPE:Goods.Transportation.Civilian.Aircraft`\
> > `TYPE:Goods.Transportation.Civilian.Car`\
> > `TYPE:Goods.Transportation.Civilian.Motorcycle`\
> > `TYPE:Goods.Transportation.Military.Aircraft`\
> > `TYPE:Goods.Transportation.Military.Armored`\
> > `TYPE:Goods.Transportation.Military.Motorcycle.Tracked`\
> > `TYPE:Goods.Transportation.Military.U-boat`
> >
> > **BP pulp\_fantasy\\pulpfantasy\_equip\_weap.lst File.**
> >
> > `TYPE:Explosive.Slashing`
> >
> > **BP pulpfantasy\_equip\_weap\_ammo.lst File.**
> >
> > `TYPE:Ammunition.Standard.Metal.Bullet`\
> > `TYPE:Ammunition.Standard.Metal.Bullet.Individual`
> >
> > **BP pulpfantasy\_equip\_weap\_melee.lst File.**
> >
> > `TYPE:Weapon.Natural.Melee.Simple.Unarmed.Mystic.Bludgeoning.Finesseable`
> >
> > **BP pulpfantasy\_equip\_weap\_ranged.lst File.**
> >
> > `TYPE:Weapon.Ranged.Standard.Firearm.Pistol.Ballistic.Personal.Semiauto.Container.Projectile`\
> > `TYPE:Weapon.Ranged.Standard.Firearm.Longarm.Ballistic.Personal.Semiauto.Container.Projectile`\
> > `TYPE:Weapon.Ranged.Standard.Firearm.Longarm.Ballistic.Personal.Semiauto.Automatic.Container.Projectile`\
> > `TYPE:Weapon.Ranged.Standard.Firearm.Heavy.Ballistic.Exotic.Automatic.Container.Projectile`\
> > `TYPE:Weapon.Ranged.Standard.Firearm.Heavy.Ballistic.Exotic`\
> > `TYPE:Weapon.Ranged.Standard.Cannon.Vehicle.Ballistic.Exotic.Automatic`\
> > `TYPE:Weapon.Ranged.Standard.Cannon.Vehicle.Ballistic.Exotic.Semiauto`\
> > `TYPE:Weapon.Ranged.Standard.Cannon.Vehicle.Concussion.Exotic.Semiauto`\
> > `TYPE:Weapons.Ranged.Standard.Archaic.Piercing.Wooden.Container`
> >
> > **BP pulpfantasy\_equipmods.lst File.**
> >
> > `TYPE:Gadget`
> >
> > **BP pulpfantasy\_feats.lst File.**
> >
> > `TYPE:General.Ambassador`\
> > `TYPE:General.Driver`\
> > `TYPE:General.Explorer`\
> > `TYPE:General.Mystery_Man.Operator`\
> > `TYPE:General.Operator`\
> > `TYPE:General.Smart.Explorer`
> >
> > **BP pulpfantasy\_feats\_hidden.lst File.**
> >
> > `TYPE:AddWealth`\
> > `TYPE:AmbassadorAbility`\
> > `TYPE:BrawlerAbility`\
> > `TYPE:CombatAceAbility`\
> > `TYPE:CrossTraining`\
> > `TYPE:DetectiveAbility`\
> > `TYPE:DriverAbility`\
> > `TYPE:EclecticSelections`\
> > `TYPE:ExplorerAbility`\
> > `TYPE:FastLearnerLevel`\
> > `TYPE:GManAbility`\
> > `TYPE:HeirWorkaround`\
> > `TYPE:MoveReputationOne`\
> > `TYPE:MoveReputationTwo`\
> > `TYPE:MoveReputationThree`\
> > `TYPE:MysteryManAbility`\
> > `TYPE:MysticAbility`\
> > `TYPE:NewsHoundAbility`\
> > `TYPE:OperatorAbility`\
> > `TYPE:RelicHunterAbility`\
> > `TYPE:ScientistAbility`\
> > `TYPE:ShadowyAvengerAbility`\
> > `TYPE:SidekickBonus`\
> > `TYPE:SignatureKitChoice`\
> > `TYPE:Special.Hunter.Operator`\
> > `TYPE:SpyAbility`\
> > `TYPE:WeirdInventorAbility`\
> > `TYPE:X-Training`
> >
> > **BP pulpfantasy\_feats\_mod.lst File.**
> >
> > `TYPE:Adventurer.Athlete.Circus_Performer.Explorer.Mystic_PF.Scientist.Soldier`\
> > `TYPE:Adventurer.Athlete.Criminal.Investigative.Military.Rural.CombatAce.Daredevil.Detective.Driver.Explorer.G_Man.Gangster.Mystery_Man.Soldier`\
> > `TYPE:Adventurer.Criminal.Investigative.Law_Enforcement.Military.Rural.Brawler.Detective.Mystery_Man.Scientist`\
> > `TYPE:Ambassador.Bureaucrat.Detective.Explorer.Mystery_Man.Relic_Hunter.Scientist.World_Traveller`\
> > `TYPE:Ambassador.Daredevil.Detective.Driver.Explorer.Mystery_Man.Relic_Hunter.Shadowy_Avenger.Operator`\
> > `TYPE:Ambassador.Gangster`\
> > `TYPE:Ambassador.Operator`\
> > `TYPE:Ambassador.Operator.Politician.World_Traveller`\
> > `TYPE:Antiques_Dealer.Explorer.Scientist`\
> > `TYPE:Antiques_Dealer.Fortuneteller.World_Traveller.Ambassador.Explorer.Scientist`\
> > `TYPE:Brawler.CombatAce.Daredevil.Driver.G_Man.Gangster.Law_Enforcement.Military.Shadowy_Avenger.Soldier`\
> > `TYPE:Brawler.CombatAce.Explorer.Gangster`\
> > `TYPE:Brawler.Daredevil.Detective.Explorer.Gangster.Mystery_Man.Soldier`\
> > `TYPE:Brawler.Daredevil.Detective.Mystery_Man.Soldier`\
> > `TYPE:Brawler.Daredevil.Explorer.Gangster.Mystery_Man.Soldier`\
> > `TYPE:Brawler.Detective.Mystery_Man.Soldier`\
> > `TYPE:Brawler.G_Man.Operator`\
> > `TYPE:Brawler.Mystic_PF`\
> > `TYPE:Bureaucrat.Fortuneteller.Politician.World_Traveller.Ambassador.Driver.Explorer.Gangster.Relic_Hunter.Scientist`\
> > `TYPE:Circus_Performer.Daredevil.Mystic_PF.Relic_Hunter.Shadowy_Avenger`\
> > `TYPE:CombatAce.Daredevil`\
> > `TYPE:CombatAce.Explorer.G_Man`\
> > `TYPE:CombatAce.Mystery_Man.Shadowy_Avenger.Operator`\
> > `TYPE:Craftsperson.CombatAce.Driver.Scientist`\
> > `TYPE:Craftsperson.Driver`\
> > `TYPE:Daredevil.Detective.Mystery_Man.Soldier`\
> > `TYPE:Daredevil.Driver.Explorer.Gangster`\
> > `TYPE:Daredevil.Driver.G_Man`\
> > `TYPE:Daredevil.Explorer.Relic_Hunter.Shadowy_Avenger.Operator`\
> > `TYPE:Daredevil.G_Man`\
> > `TYPE:Daredevil.Scientist`\
> > `TYPE:Daredevil.Shadowy_Avenger.Operator`\
> > `TYPE:Detective.Mystery_Man`\
> > `TYPE:Driver.G_Man.Gangster`\
> > `TYPE:Escape_Artist.Fortuneteller.Stage_Magician.Gangster.Shadowy_Avenger`\
> > `TYPE:Escape_Artist.Stage_Magician.Daredevil.Explorer`\
> > `TYPE:Explorer.G_Man.Mystic_PF.Soldier.Operator`\
> > `TYPE:Explorer.G_Man.Soldier.Operator`\
> > `TYPE:Explorer.Mystery_Man`\
> > `TYPE:Explorer.Operator`\
> > `TYPE:Gangster.Operator`\
> > `TYPE:Gangster.Politician.Relic_Hunter`\
> > `TYPE:Gangster.Relic_Hunter.Shadowy_Avenger`\
> > `TYPE:General`\
> > `TYPE:Hunter.Detective.Mystery_Man.Scientist.Operator`\
> > `TYPE:Hunter.Gangster.Relic_Hunter`\
> > `TYPE:Hunter.Relic_Hunter.World_Traveller`\
> > `TYPE:Hunter.Soldier.Operator`\
> > `TYPE:Mystery_Man`\
> > `TYPE:Mystic_PF.Shadowy_Avenger.Soldier.Operator`\
> > `TYPE:Operator`\
> > `TYPE:Relic_Hunter.Scientist.Shadowy_Avenger.Operator`\
> > `TYPE:Soldier`\
> > `TYPE:World_Traveller.Gangster`
> >
> > **BP pulpfantasy\_feats\_occupations.lst File.**
> >
> > `TYPE:Antiques_Dealer_Skills.Bureaucrat_Skills.Craftsperson_Skills.Engineer_Skills.Fortuneteller_Skills.Politician_Skills`\
> > `TYPE:Antiques_Dealer_Skills.Bureaucrat_Skills.Domestic_Skills.Fortuneteller_Skills.Politician_Skills.World_Traveller_Skills`\
> > `TYPE:Antiques_Dealer_Skills.Circus_Performer_Skills.Fortuneteller_Skills.Outcast_Skills`\
> > `TYPE:Antiques_Dealer_Skills.Craftsperson_Skills.Domestic_Skills.Engineer_Skills.Laborer_Skills`\
> > `TYPE:Artist_Skills.Bureaucrat_Skills.Domestic_Skills.Escape_Artist_Skills.Fortuneteller_Skills.Politician_Skills.Stage_Magician_Skills.World_Traveller_Skills`\
> > `TYPE:Artist_Skills.Bureaucrat_Skills.Domestic_Skills.Politician_Skills`\
> > `TYPE:Artist_Skills.Bureaucrat_Skills.Heir_Skills`\
> > `TYPE:Artist_Skills.Bureaucrat_Skills.Politician_Skills`\
> > `TYPE:Artist_Skills.Circus_Performer_Skills.Heir_Skills`\
> > `TYPE:Artist_Skills.Craftsperson_Skills.Heir_Skills`\
> > `TYPE:Artist_Skills.Domestic_Skills`\
> > `TYPE:Artist_Skills.Heir_Skills`\
> > `TYPE:Artist_Skills.Outcast_Skills`\
> > `TYPE:Artist_Skills.Stage_Magician_Skills`\
> > `TYPE:Bureaucrat_Skills.Circus_Performer_Skills.Domestic_Skills.Escape_Artist_Skills.Heir_Skills.Politician_Skills.World_Traveller_Skills`\
> > `TYPE:Bureaucrat_Skills.Circus_Performer_Skills.Escape_Artist_Skills.Heir_Skills.Politician_Skills.World_Traveller_Skills`\
> > `TYPE:Bureaucrat_Skills.Domestic_Skills.Fortuneteller_Skills.Politician_Skills`\
> > `TYPE:Bureaucrat_Skills.Domestic_Skills.Heir_Skills.Politician_Skills`\
> > `TYPE:Bureaucrat_Skills.Heir_Skills.Politician_Skills.World_Traveller_Skills`\
> > `TYPE:Bureaucrat_Skills.Politician_Skills`\
> > `TYPE:Circus_Performer_Skills.Domestic_Skills.Laborer_Skills`\
> > `TYPE:Circus_Performer_Skills.Escape_Artist_Skills.Laborer_Skills`\
> > `TYPE:Craftsperson_Skills.Engineer_Skills.Escape_Artist_Skills.Laborer_Skills.Stage_Magician_Skills`\
> > `TYPE:Craftsperson_Skills.Engineer_Skills.Laborer_Skills`\
> > `TYPE:Craftsperson_Skills.Escape_Artist_Skills.Stage_Magician_Skills`\
> > `TYPE:Craftsperson_Skills.Outcast_Skills`\
> > `TYPE:Craftsperson_Skills.Stage_Magician_Skills`\
> > `TYPE:Domestic_Skills.Engineer_Skills.Laborer_Skills.World_Traveller_Skills`\
> > `TYPE:Domestic_Skills.Laborer_Skills.Politician_Skills`\
> > `TYPE:Domestic_Skills.Outcast_Skills.Stage_Magician_Skills`\
> > `TYPE:Domestic_Skills.Stage_Magician_Skills`\
> > `TYPE:Escape_Artist_Skills.Fortuneteller_Skills.Stage_Magician_Skills`\
> > `TYPE:Fortuneteller_Skills.Politician_Skills`\
> > `TYPE:Heir_Skills.Laborer_Skills`\
> > `TYPE:Hunter_Skills.Outcast_Skills.World_Traveller_Skills`\
> > `TYPE:Occupation_Skill.Engineer_Skills`\
> > `TYPE:Occupation_Skill.Academic_Skills.Adventurer_Skills.Antiques_Dealer_Skills.Artist_Skills.Circus_Performer_Skills.Escape_Artist_Skills.Fortuneteller_Skills`\
> > `TYPE:Politician_Skills`\
> > `TYPE:Stage_Magician_Skills`\
> > `TYPE:World_Traveller_Skills`
> >
> > **BP pulpfantasy\_languages.lst File.**
> >
> > `TYPE:Spoken.Caddoan`\
> > `TYPE:Spoken.Iroquoian`\
> > `TYPE:Spoken.Muskogean`\
> > `TYPE:Spoken.Sahaptian`\
> > `TYPE:Spoken.Signaling`\
> > `TYPE:Spoken.Siouian`\
> > `TYPE:Spoken.Uto-Aztecan`\
> > `TYPE:Written.Braille`\
> > `TYPE:Written.Caddoan`
> >
> > `TYPE:Written.Iroquoian`\
> > `TYPE:Written.Muskogean`\
> > `TYPE:Written.Sahaptian`\
> > `TYPE:Written.Signaling`\
> > `TYPE:Written.Siouian`\
> > `TYPE:Written.Uto-Aztecan`\
> >
> > **BP pulpfantasy\_races.lst File.**
> >
> > `TYPE:Animal`
> >
> > **BP pulpfantasy\_skills.lst File.**
> >
> > `TYPE:Intelligence`\
> > `TYPE:Intelligence.Knowledge`\
> > `TYPE:Intelligence.Knowledge.Science`
> >
> > **BP pulpfantasy\_weaponprofs.lst File.**
> >
> > `TYPE:Archaic`\
> > `TYPE:ExoticFirearms`\
> > `TYPE:PersonalFirearm`
>
> ------------------------------------------------------------------------
>
> <span id="b3"></span> Behemoth3 (B3) - Masters and Minions (35e)
>
> > **B3 mazeminotaur\_classes.lst File.**
> >
> > `TYPE:Monster`\
> > `TYPE:PC.Prestige`
> >
> > **B3 mazeminotaur\_equip.lst File.**
> >
> > `TYPE:Goods.Alchemical.Consumable.Flask`\
> > `TYPE:Goods.General`\
> > `TYPE:Goods.Trade`
> >
> > **B3 mazeminotaur\_feats\_hidden.lst File.**
> >
> > `TYPE:SpecialQuality.Extraordinary`\
> > `TYPE:SpecialQuality.Supernatural`\
> >
> > `TYPE:SpecialAttack.Extraordinary`\
> >
> > `TYPE:SpecialQuality.Extraordinary`\
> >
> > **BP faeries\_languages.lst File.**
> >
> > `TYPE:Spoken`
> >
> > **B3 mazeminotaur\_races.lst File.**
> >
> > `TYPE:Monstrous Humanoid`\
> >
> > `TYPE:Magical Beast`
> >
> > **BP faeries\_skills.lst File.**
> >
> > `TYPE:Intelligence.Knowledge`
> >
> > **BP faeries\_spells.lst File.**
> >
> > `TYPE:Arcane`\
> > `TYPE:Divine`
> >
> > **BP faeries\_templates\_focus.lst File.**
> >
> > `TYPE:Fey`\
> > `TYPE:Humanoid`\
> > `TYPE:Giant`
>
> ------------------------------------------------------------------------
>
> <span id="bfg"></span> Big Finger Games (BFG) - Fantasy Folio -
> Masterwork Qualities (35e)
>
> > **BFG masterworkqualities\_equip\_weap\_melee.lst File.**
> >
> > `TYPE:Weapon.Melee.Martial.Specific.Slashing.Sword`\
> > `TYPE:Weapon.Melee.Ranged.Simple.Thrown.Specific.Piercing.Slashing.Dagger`
> >
> > **BFG masterworkqualities\_equipmods.lst File.**
> >
> > `TYPE:Weapon`\
> > `TYPE:Ammunition`\
> > `TYPE:Armor`
>
> ------------------------------------------------------------------------
>
> Bloodstone Press (BSP) - God Spells (35e)
>
> > **BSP godspells\_spells.lst File.**
> >
> > `TYPE:Arcane.Divine`
>
> Bloodstone Press (BSP) - Spellbinder's Sourcebook (35e)
>
> > **BSP spellbinder\_spells.lst File.**
> >
> > `TYPE:Arcane.Divine`
> >
> > **BSP spellbinder\_templates.lst File.**
> >
> > `TYPE:Magical Beast`
>
> Bloodstone Press (BSP) - Spellbinder's Sourcebook II (35e)
>
> > **BSP spellbinder2\_spells.lst File.**
> >
> > `TYPE:Arcane.Divine`
>
> Bloodstone Press (BSP) - 22 Talent Trees (Modern)
>
> > **BSP 22talenttrees\_abilities\_talents.lst File.**
> >
> > `TYPE:Talent.StrongTalent.Brute.HeavyLoad.Hurling.LikeRock.Might`\
> > `TYPE:Talent.FastTalent.Elusive.Finesse.NeedSpeed.QuickerThanEye`\
> > `TYPE:Talent.ToughTalent.FXResistance.ToxinResistance`\
> > `TYPE:Talent.SmartTalent.FastLearner.QuickThinking.Tactician`\
> > `TYPE:Talent.DedicatedTalent.AnimalAffinity.AnimalFriendship.Oracle.Selfless.Virtue`\
> > `TYPE:Efficacious`\
> > `TYPE:Talent.CharismaticTalent.Efficacious.Facetious.Intimidating.Pulchritudinous`
>
> ------------------------------------------------------------------------
>
> Blue Devil Games (BDG) - Dawningstar (35e)
>
> > **BDG ds\_oql\_abilities\_talents.lst File.**
> >
> > `TYPE:Talent.StrongTalent.HeavyGravityResistance.StrongRage.ThrowingArm.StrongPlus`\
> > `TYPE:Talent.FastTalent.Footwork.Sharpshooter.FastPlus`\
> > `TYPE:Talent.ToughTalent.ToughRage.RadiationResistnace.StunResistance.ToughPlus`\
> > `TYPE:Talent.SmartTalent.Investigation.Navigation.Scholar.Xenotech.SmartPlus`\
> > `TYPE:Talent.DedicatedTalent.Survival.SwornEnemy.RebuilderSwornEnemy.Treatment.DedicatedPlus`\
> > `TYPE:Talent.CharismaticTalent.AnimalHusbandry.Command.Diplomatic.Mercantile.CharismaticPlus`
> >
> > **BDG ds\_oql\_class\_advanced.lst File.**
> >
> > `TYPE:PC.Advanced`
> >
> > **BDG ds\_oql\_class\_prestige.lst File.**
> >
> > `TYPE:PC.Prestige.Advanced`
> >
> > **BDG ds\_oql\_class\_race.lst File.**
> >
> > `TYPE:PC.Race`
> >
> > **BDG ds\_oql\_companionmod.lst File.**
> >
> > `TYPE:SpecialMount`
> >
> > **BDG ds\_oql\_equip.lst File.**
> >
> > `TYPE:Goods.Tools.Masterwork.Resizable`\
> > `TYPE:Goods.General.PL2.PL5.PL6`\
> > `TYPE:Cybernetics.PL6`\
> > `TYPE:Cybernetics.Weapon.Ranged.Laser.Fire.Piercing`\
> > `TYPE:Goods.Tools.Electronic`\
> > `TYPE:Goods.Transportation.Civilian.Motorcycles.Truck.Wheel.Aircraft`\
> > `TYPE:Goods.Transportation.Military.Wheel.Track.Aircraft`\
> > `TYPE:Ammunition.Standard.Bullet.Energy.Gyrojet.Missile`\
> > `TYPE:Goods.Transportaiton.Mecha.Superstructure.PL6.PL7`\
> > `TYPE:Goods.Transportation.Starship.Mediumweight.HeavyDestroyer`\
> > `TYPE:Goods.Transportation.Starship.Ultralight.AtmosphericShuttle`\
> > `TYPE:Goods.Transportation.Starship.Superheavy.EvacuationShip.Spacestation`\
> > `TYPE:Goods.Transportation.Starship.Light.Frigate.Scout`
> >
> > **BDG masterworkqualities\_equipmods.lst File.**
> >
> > `TYPE:Weapon`\
> > `TYPE:Ammunition`\
> > `TYPE:Armor`

### [The Complete Listing of Variables](/list/global/variables.html#complete) {#the-complete-listing-of-variables .indent1}

**<span id="abilities"></span> Group Name:** -- abilities.lst

-   AddTalent
-   Attentive
-   Authority
-   BrainsOverBrawn
-   Brawler
-   ByGraceOfFortune
-   CharismaticPlus
-   CharismaticTalent
-   DedicatedPlus
-   DedicatedTalent
-   Deduction
-   Elusive
-   FastLearner
-   FastTalent
-   InstinctiveResponse
-   MechanicalAptitude
-   NeedForSpeed
-   Precision
-   Prodigy
-   Rage
-   Research
-   SmartTalent
-   Soldiery
-   StrongTalent
-   Survivalist
-   Talent
-   ToughTalent

**<span id="classes"></span> Group Name:** -- classes.lst

-   Base
-   Monster
-   NPC
-   PC
-   Prestige

**<span id="classes_advanced"></span> Group Name:** --
classes\_advanced.lst

-   Advanced
-   Monster
-   PC

**<span id="class_core"></span> Group Name:** -- class\_core.lst

-   Base
-   PC

**<span id="classes_legendary"></span> Group Name:** --
classes\_legendary.lst

-   PC
-   Prestige

**<span id="classes_monster"></span> Group Name:** --
classes\_monster.lst

-   Monster

**<span id="class_prestige"></span> Group Name:** -- class\_prestige.lst

-   Advanced
-   PC
-   Prestige

**<span id="class_race"></span> Group Name:** -- class\_race.lst

-   PC
-   Race

**<span id="classes_variant"></span> Group Name:** --
classes\_variant.lst

-   Base
-   PC

**<span id="companionmod"></span> Group Name:** -- companionmod.lst

-   SpecialMount

**<span id="eqmods"></span> Group Name:** -- eqmods.lst

-   Ammunition
-   Armor
-   Gadget
-   Melee
-   Shield
-   Slashing
-   Weapon

**<span id="equip_ammunition"></span> Group Name:** -- equip.lst
TYPE:Ammunition

-   Bullet
-   Energy
-   Gyrojet
-   Missile
-   Standard

**<span id="equip_goods"></span> Group Name:** -- equip.lst TYPE:Goods

-   Alchemical
-   Belt.Boot
-   Clothing.Consumable.Container.Cybernetics
-   Fire.Flask
-   Gadget.General
-   Headgear
-   Laser
-   Masterwork
-   Piercing
-   PL2.PL5.PL6
-   Ranged.Resizable
-   Weapon

**<span id="equip_goods_tools"></span> Group Name:** -- equip.lst
TYPE:Goods.Tools

-   Consumable.Consumer
-   Electronic
-   Gadget.General
-   Masterwork.Medical
-   Photo.PL2.PL5.PL6
-   Resizable
-   Trade
-   WeaponAccessory

**<span id="equip_goods_transportaiton"></span> Group Name:** --
equip.lst TYPE:Goods.Transportaiton

-   Aircraft
-   Civilian
-   Military
-   Motorcycles
-   Track
-   Truck
-   Wheel

**<span id="equip_goods_transportaiton_mecha"></span> Group Name:** --
equip.lst TYPE:Goods.Transportaiton.Mecha

-   Superstructure
-   PL6.PL7

**<span id="equip_goods_transportation_starship"></span> Group Name:**
-- equip.lst TYPE:Goods.Transportation.Starship

-   AtmosphericShuttle
-   EvacuationShip
-   Frigate
-   HeavyDestroyer
-   Light
-   Mediumweight
-   Scout.Spacestation.Superheavy
-   Ultralight

**<span id="equip_weap"></span> Group Name:** -- equip\_weap.lst
TYPE:Weapon.Exotic

-   Piercing
-   Projectile
-   (Race Type)
-   Ranged
-   Slashing
-   Standard
-   Thrown

**<span id="equip_armor"></span> Group Name:** -- equip\_armor.lst
TYPE:Armor

-   Heavy
-   Light
-   Medium
-   Nonmetal
-   Specific
-   Suit
-   Tactical

**<span id="equip_armorshield"></span> Group Name:** --
equip\_armorshield.lst TYPE:Armor

-   Archaic
-   Heavy
-   Light
-   Medium
-   PL3
-   PL4
-   PL5
-   PL6
-   Powered
-   Shield
-   Suit
-   Tactical

**<span id="equip_magic_items_armor"></span> Group Name:** --
equip\_magic\_items.lst TYPE:Armor

-   Light
-   Nonmetal
-   Specific
-   Suit

**<span id="equip_magic_items_goods"></span> Group Name:** --
equip\_magic\_items.lst TYPE:Goods

-   Alchemical
-   Consumable

**<span id="equip_magic_items_enhancement_ammunition"></span> Group
Name:** -- equip\_magic\_items.lst TYPE:Enhancement.Ammunition

-   Individual
-   SpecificArrow

**<span id="equip_magic_items_enhancement_shield"></span> Group Name:**
-- equip\_magic\_items.lst TYPE:Enhancement.Shield

-   Heavy
-   Specific

**<span id="equip_magic_items_enhancement.weapon"></span> Group Name:**
-- equip\_magic\_items.lst TYPE:Enhancement.Weapon

-   Bashing
-   Mace
-   Martial
-   Melee
-   Slashing
-   Specific
-   Sword

**<span id="equip_magic_items_goods"></span> Group Name:** --
equip\_magic\_items.lst TYPE:Goods

-   Alchemical
-   Book
-   Boot
-   Consumable
-   Container
-   Food
-   Glove
-   Melee
-   Poison
-   Weapon

**<span id="equip_magic_items_goods_tools"></span> Group Name:** --
equip\_magic\_items.lst TYPE:Goods.Tools

-   Bashing
-   Exotic
-   Instrument
-   Melee
-   Percussion
-   Resizable
-   Simple
-   Slashing
-   SurgeryTools
-   Weapon
-   Wind

**<span id="equip_magic_items_magic_artifact"></span> Group Name:** --
equip\_magic\_items.lst TYPE:Magic.Artifact

-   Armor
-   Bludgeoning
-   Consumable
-   Container
-   Enhancement
-   Heavy
-   Light
-   Mace
-   Martial
-   Medium
-   Melee
-   Nonmetal
-   Potion
-   Ring
-   Shield
-   Simple
-   Slashing
-   Specific
-   Staff
-   Suit
-   Sword
-   Wand
-   Weapon

**<span id="equip_magic_items_magic_wondrous"></span> Group Name:** --
equip\_magic\_items.lst TYPE:Magic.Wondrous

-   Amulet
-   Boot
-   Bracelet
-   Headgear

**<span id="equip_magic_items_shield"></span> Group Name:** --
equip\_magic\_items.lst TYPE:Shield

-   Buckler
-   Heavy
-   Standard

**<span id="equip_magic_items_weapon_exotic"></span> Group Name:** --
equip\_magic\_items.lst TYPE:Weapon.Exotic

-   Melee
-   Ranged
-   Standard
-   Slashing
-   Sword
-   Thrown

**<span id="equip_magic_items_weapon_melee"></span> Group Name:** --
equip\_magic\_items.lst TYPE:Weapon.Melee

-   Dagger
-   Exotic
-   Finesseable
-   Martial
-   Piercing
-   Ranged
-   Reach
-   Simple
-   Slashing
-   Standard
-   Subdual
-   Sword
-   Thrown

**<span id="equip_poisons_goods"></span> Group Name:** --
equip\_poisons.lst TYPE:Goods

-   Consumable
-   Poison

**<span id="equip_shields_shield"></span> Group Name:** -- --
equip\_shields.lst TYPE:Shield

-   Heavy
-   Exotic
-   Standard

**<span id="equipment_staves"></span> Group Name:** --
equipment\_staves.lst

-   Bludgeoning
-   Double
-   Magic
-   Melee
-   Quarterstaff
-   Simple
-   Staff
-   Standard
-   TwoHanded
-   Weapon

**<span id="equip_vehicles_goods_transportation_civilian"></span> Group
Name:** -- equip\_vehicles.lst TYPE:Goods.Transportation.Civilian

-   Aircraft
-   Car
-   Hovervehicle
-   Truck
-   Wheel

**<span id="equip_vehicles_goods_transportation_military"></span> Group
Name:** -- equip\_vehicles.lst TYPE:Goods.Transportation.Military

-   Aircraft
-   Armored
-   Motorcycle
-   Track
-   Tracked
-   U-boat
-   Wheel

**<span id="equip_weap_explosive"></span> Group Name:** --
equip\_weap.lst TYPE:Explosive

-   Slashing

**<span id="equip_weap_ammo_ammunition"></span> Group Name:** --
equip\_weap\_ammo.lst TYPE:Ammunition

-   Bullet
-   Individual
-   Metal
-   Standard

**<span id="equip_weap_melee_weapon_melee"></span> Group Name:** --
equip\_weap\_melee.lst TYPE:Weapon.Melee

-   Bladestaff
-   Bludgeoning
-   Chainball
-   Club
-   Dagger
-   Double
-   Electricity
-   Exotic
-   Finesseable
-   Fire
-   Gore
-   Hookchain
-   Martial
-   Melee
-   Metal
-   Piercing
-   PL2
-   PL5
-   PL6
-   PL7
-   (Race Type)
-   Ranged
-   Reach
-   Simple
-   Slashing
-   Specific
-   Standard
-   Sword
-   Thrown
-   Weapon
-   Wristblade
-   Wooden

**<span id="equip_weap_melee_weapon_natural"></span> Group Name:** --
equip\_weap\_melee.lst TYPE:Weapon.Natural

-   Bludgeoning
-   Finesseable
-   Melee
-   Mystic
-   Simple
-   Unarmed

**<span id="equip_weap_ranged_weapon_ranged_standard"></span> Group
Name:** -- equip\_weap\_ranged.lst TYPE:Weapon.Ranged.Standard

-   Archaic
-   Automatic
-   Ballistic
-   Cannon
-   Concussion
-   Container
-   Disintegration
-   Exotic
-   Fire
-   Firearm
-   GrenadeLauncher
-   Heavy
-   HeavyGyroJetLauncher
-   HMG
-   Laser
-   LMG
-   Longarm
-   Plasma
-   Personal
-   Pistol
-   PlasmaCannon
-   PL2
-   PL4
-   PL5
-   PL6
-   PL7
-   PL8
-   PL9
-   Piercing
-   Precision
-   Projectile
-   Pistol
-   Radiation
-   RocketLauncher
-   Semiauto
-   Standard
-   Vehicle
-   WarBow
-   Wooden

**<span id="equipmods"></span> Group Name:** -- equipmods.lst

-   Ammunition
-   Armor
-   Gadget
-   Weapon

**<span id="feats"></span> Group Name:** -- feats.lst

-   Ambassador
-   Charismatic
-   CharismaticPreferred
-   Clerical
-   Cultural
-   Dedicated
-   DedicatedFavored
-   Driver
-   Explorer
-   Fast
-   FastPreferred
-   Fey
-   Fighter
-   General
-   ItemCreation
-   Metamagic
-   Mystery\_Man
-   Operator
-   Order
-   Rogue
-   Smart
-   SmartPreferred
-   Special
-   Spellcaster
-   Theurgic

**<span id="feats_aspects"></span> Group Name:** -- feats\_aspects.lst

-   AspectOfNature

**<span id="feats_flaws"></span> Group Name:** -- feats\_flaws.lst

-   Flaw

**<span id="feats_hidden"></span> Group Name:** -- feats\_hidden.lst

-   AddTalent
-   AddWealth
-   AmbassadorAbility
-   AncientHealing
-   Attentive
-   Authority
-   BenevolentSpirit
-   BrainsOverBrawn
-   Brawler
-   BrawlerAbility
-   ByGraceOfFortune
-   CharismaticPlus
-   CharismaticTalent
-   CircleWalkerChoice
-   Class
-   ClassAbility
-   CombatAceAbility
-   CrossTraining
-   DawnArcherLPL1
-   DawnArcherLPL2
-   DawnArcherLPL3
-   DawnArcherLPL4
-   DawnArcherLPL5
-   DedicatedPlus
-   DetectiveAbility
-   DedicatedTalent
-   Deduction
-   DiscipleMysteryDiscipline
-   DoppelAltForm
-   DriverAbility
-   EclecticSelections
-   Elusive
-   EnergyResistances
-   EpicGeneralLPL1
-   EpicGeneralLPL2
-   EpicGeneralLPL3
-   EpicGeneralLPL4
-   EpicGeneralLPL5
-   ExplorerAbility
-   Extraordinary
-   FaerieRacialTrait
-   FastLearner
-   FastLearnerLevel
-   FastTalent
-   FeyArts
-   FeyTravelerChoice
-   FleetwindLPL1
-   FleetwindLPL2
-   FleetwindLPL3
-   FleetwindLPL4
-   FleetwindLPL5
-   ForceLaw
-   GangsterAbility
-   GManAbility
-   HearthMagic
-   HeirWorkaround
-   Hidden
-   HTA1
-   HAT2
-   HTA3
-   HTrueStaunchBonus
-   Hunter
-   IconLPL1
-   IconLPL2
-   IconLPL3
-   IconLPL4
-   IconLPL5
-   InstinctiveResponse
-   Internal
-   KnightHP
-   LegendaryArcaneResistance
-   LegendaryCaptivatingSpeach
-   LegendaryCheatDeath
-   LegendaryCombatSense
-   LegendaryCripplingAccuracy
-   LegendaryDeadeye
-   LegendaryDrainResistance
-   LegendaryEnchantedBow
-   LegendaryEnhancedSTR
-   LegendaryEnhancedDEX
-   LegendaryEnhancedCON
-   LegendaryEnhancedINT
-   LegendaryEnhancedWIS
-   LegendaryEnhancedCHA
-   LegendaryFearfulPresence
-   LegendaryHeroicInspiration
-   LegendaryMasterMundaneArts
-   LegendaryNaturalLeader
-   LegendaryPath
-   LegendaryRageAgainstDeath
-   LegendarySecondNatureSenses
-   LegendaryShieldedMind
-   LegendarySkillMastery
-   LegendarySorceryOverpower
-   LegendaryStunningSpeed
-   LegendarySummonConscripts
-   LegendaryTrailblazer
-   LegendaryUnearthlyMight
-   LegendaryUnexpectedAid
-   LegendaryUnstoppable
-   LegendaryUnstoppableArrows
-   LegendaryWalkAir
-   LegendaryWallFighting
-   LegendaryWalkWater
-   LowlanderStatPenalty
-   LowlanderStatBonus
-   MasterArcanisLPL1
-   MasterArcanisLPL2
-   MasterArcanisLPL3
-   MasterArcanisLPL4
-   MasterArcanisLPL5
-   MechanicalAptitude
-   MoveReputationOne
-   MoveReputationTwo
-   MoveReputationThree
-   MysteryManAbility
-   MysticAbility
-   NeedForSpeed
-   NewsHoundAbility
-   NightHunterGift
-   Operator
-   OperatorAbility
-   Precision
-   Prodigy
-   RaceAbility
-   RacialTraitCost
-   RadiantEnlightenment
-   Rage
-   Research
-   RelicHunterAbility
-   ScientistAbility
-   SecretEnlightenment
-   ScoundrelHP
-   ShalraekuZarakku
-   ShadowyAvengerAbility
-   ShamanElementalForm
-   ShaperDivineFocus
-   ShaperSpecialty
-   SidekickBonus
-   SignatureKitChoice
-   SmartTalent
-   Soldiery
-   Special
-   SpecialAttack
-   SpecialQuality
-   SpiritAdeptPowers
-   SpyAbility
-   StrongTalent
-   Subclass
-   Supernatural
-   Survivalist
-   TeutonicKnightCombat
-   TLS
-   ToughTalent
-   UnbrokenResistance
-   UncannyDodge
-   UnsufferingLPL1
-   UnsufferingLPL2
-   UnsufferingLPL3
-   UnsufferingLPL4
-   UnsufferingLPL5
-   VelinGuardianSwornEnemy
-   WeirdInventorAbility
-   WildernessGuideGift
-   WordLaw
-   X-Training

**<span id="feats_mod"></span> Group Name:** -- feats\_mod.lst

-   Adventurer
-   AirRunner
-   Ambassador
-   Antiques\_Dealer
-   Athlete
-   Athlete
-   BarterJack
-   Brawler
-   Bureaucrat
-   Circus\_Performer
-   ColonialLeader
-   CombatAce
-   Craftsperson
-   Criminal
-   Daredevil
-   Detective
-   Dissident
-   Driver
-   Fortuneteller
-   Explorer
-   Escape\_Artist
-   G\_Man
-   Gangster
-   General
-   Gunhand
-   HumanSurvivor
-   Hunter
-   Investigative
-   Law\_Enforcement
-   Lawman
-   Military
-   Mystery\_Man
-   Mystic\_PF
-   Nomad
-   Operator
-   Pilot
-   Politician
-   Rancher
-   RanchHand
-   Rebuilder
-   Relic\_Hunter
-   Rural
-   Scientist
-   Shadowy\_Avenger
-   Soldier
-   Spacer
-   Stage\_Magician
-   Terraformer
-   TribalLeader
-   VelinChief
-   VelinGuardian
-   VelinHunter
-   World\_Traveller
-   XenoExpert

**<span id="feats_occupations"></span> Group Name:** --
feats\_occupations.lst

-   Academic\_Skills
-   Adventurer\_Skills
-   Antiques\_Dealer\_Skills
-   Artist\_Skills
-   Bureaucrat\_Skills
-   Circus\_Performer\_Skills
-   Craftsperson\_Skills
-   Courtier\_Skills
-   Dissident\_Skills
-   Domestic\_Skills
-   Engineer\_Skills
-   Escape\_Artist\_Skills
-   Explorer\_Skills
-   Fortuneteller\_Skills
-   Heir\_Skills
-   Hunter\_Skills
-   Laborer\_Skills
-   Nomad\_Skills
-   Occupation
-   Occupation\_Skill
-   Outcast\_Skills
-   Pilot\_Skills
-   Politician\_Skills
-   Ranch\_Hand\_Skills
-   Scientst\_Skills
-   Spacer\_Skills
-   Stage\_Magician\_Skills
-   Terraformer\_Skills
-   Tribal\_Leader\_Skills
-   World\_Traveller\_Skills
-   Xeno\_Expert\_Skills

**<span id="feats_races"></span> Group Name:** -- feats\_races.lst

-   AwakeningMagic
-   DawnElfRacialTalent
-   DawnElfRacialTalent1
-   DawnElfRacialTalent3
-   DawnElfRacialTalent5
-   DawnElfRacialTalent7
-   DawnElfRacialTalent9
-   DawnElfRacialTransformation
-   DawnElfRacialTransformation
-   DawnElfRacialTransformation2
-   DawnElfRacialTransformation4
-   DawnElfRacialTransformation6
-   DawnElfRacialTransformation8
-   DawnElfRacialTransformation10
-   DawnElfTalentSkill
-   DawnElfTransfSkill
-   DoppelBaseAltForm
-   DoppelRacialTalent
-   DoppelRacialTalent1
-   DoppelRacialTalent3
-   DoppelRacialTalent5
-   DoppelRacialTalent7
-   DoppelRacialTalent9
-   DoppelRacialTransformation
-   DoppelRacialTransformation
-   DoppelRacialTransformation2
-   DoppelRacialTransformation4
-   DoppelRacialTransformation6
-   DoppelRacialTransformation8
-   DoppelRacialTransformation10
-   DoppelTalentSkill
-   DoppelTransfSkill
-   DwarfRacialTalent
-   DwarfRacialTalent1
-   DwarfRacialTalent3
-   DwarfRacialTalent5
-   DwarfRacialTalent7
-   DwarfRacialTalent9
-   DwarfRacialTransformation
-   DwarfRacialTransformation2
-   DwarfRacialTransformation4
-   DwarfRacialTransformation6
-   DwarfRacialTransformation8
-   DwarfRacialTransformation10
-   DwarfTalentSkill
-   DwarfTransfSkill
-   ForestWightRacialTalent
-   ForestWightRacialTalent1
-   ForestWightRacialTalent3
-   ForestWightRacialTalent5
-   ForestWightRacialTalent7
-   ForestWightRacialTalent9
-   ForestWightRacialTransformation
-   ForestWightRacialTransformation2
-   ForestWightRacialTransformation4
-   ForestWightRacialTransformation6
-   ForestWightRacialTransformation8
-   ForestWightRacialTransformation10
-   ForestWightTalentSkill
-   GhostElfRacialTalent
-   GhostElfRacialTalent1
-   GhostElfRacialTalent3
-   GhostElfRacialTalent5
-   GhostElfRacialTalent7
-   GhostElfRacialTalent9
-   GhostElfRacialTransformation
-   GhostElfRacialTransformation2
-   GhostElfRacialTransformation4
-   GhostElfRacialTransformation6
-   GhostElfRacialTransformation8
-   GhostElfRacialTransformation10
-   GhostElfTalentSkill
-   GnomeRacialTalent
-   GnomeRacialTalent1
-   GnomeRacialTalent3
-   GnomeRacialTalent5
-   GnomeRacialTalent7
-   GnomeRacialTalent9
-   GnomeRacialTransformation
-   GnomeRacialTransformation2
-   GnomeRacialTransformation4
-   GnomeRacialTransformation6
-   GnomeRacialTransformation8
-   GnomeRacialTransformation10
-   GnomeTalentSkill
-   GnomeTransfSkill
-   HalflingRacialTalent
-   HalflRacialTalent
-   HalflRacialTalent1
-   HalflRacialTalent3
-   HalflRacialTalent5
-   HalflRacialTalent7
-   HalflRacialTalent9
-   HalflRacialTransformation
-   HalflRacialTransformation2
-   HalflRacialTransformation4
-   HalflRacialTransformation6
-   HalflRacialTransformation8
-   HalflRacialTransformation10
-   HalflTalentSkill
-   HalflTransfSkill
-   HHighlRacialTalent
-   HHighlRacialTalent1
-   HHighlRacialTalent3
-   HHighlRacialTalent5
-   HHighlRacialTalent7
-   HHighlRacialTalent9
-   HHighlRacialTransformation
-   HHighlRacialTransformation2
-   HHighlRacialTransformation4
-   HHighlRacialTransformation6
-   HHighlRacialTransformation8
-   HHighlRacialTransformation10
-   HHighlTransfSkill
-   HLowlRacialTalent
-   HLowlRacialTalent
-   HLowlRacialTalent1
-   HLowlRacialTalent3
-   HLowlRacialTalent5
-   HLowlRacialTalent7
-   HLowlRacialTalent9
-   HLowlRacialTransformation
-   HLowlRacialTransformation2
-   HLowlRacialTransformation4
-   HLowlRacialTransformation6
-   HLowlRacialTransformation8
-   HLowlRacialTransformation10
-   HLowlTalentSkill
-   HLowlTransfSkill
-   HSaltRacialTalent
-   HSaltRacialTalent1
-   HSaltRacialTalent3
-   HSaltRacialTalent5
-   HSaltRacialTalent7
-   HSaltRacialTalent9
-   HSaltRacialTransformation
-   HSaltRacialTransformation2
-   HSaltRacialTransformation4
-   HSaltRacialTransformation6
-   HSaltRacialTransformation8
-   HSaltRacialTransformation10
-   HSaltRacialTalent
-   HSaltTalentSkill
-   HSaltTransfSkill
-   HTrueCTalentSkill
-   HTrueRacialTalent
-   HTrueRacialTalent
-   HTrueRacialTalent1
-   HTrueRacialTalent3
-   HTrueRacialTalent5
-   HTrueRacialTalent7
-   HTrueRacialTalent9
-   HTrueRacialTransformation
-   HTrueRacialTransformation2
-   HTrueRacialTransformation4
-   HTrueRacialTransformation6
-   HTrueRacialTransformation8
-   HTrueRacialTransformation10
-   HTrueTalentSkill
-   HTrueTransfSkill
-   LizardRacialTalent
-   LizardRacialTalent1
-   LizardRacialTalent3
-   LizardRacialTalent5
-   LizardRacialTalent7
-   LizardRacialTalent9
-   LizardRacialTransformation
-   LizardRacialTransformation2
-   LizardRacialTransformation4
-   LizardRacialTransformation6
-   LizardRacialTransformation8
-   LizardRacialTransformation10
-   LizardfolkTalentSkill
-   LizardfolkTransfSkill
-   MinotaurRacialTalent
-   MinotaurRacialTalent1
-   MinotaurRacialTalent3
-   MinotaurRacialTalent5
-   MinotaurRacialTalent7
-   MinotaurRacialTalent9
-   MinotaurRacialTransformation
-   MinotaurRacialTransformation2
-   MinotaurRacialTransformation4
-   MinotaurRacialTransformation6
-   MinotaurRacialTransformation8
-   MinotaurRacialTransformation10
-   MinotaurTalentSkill
-   MinotaurTransfSkill
-   MoonElfRacialTalent
-   MoonElfRacialTalent1
-   MoonElfRacialTalent3
-   MoonElfRacialTalent5
-   MoonElfRacialTalent7
-   MoonElfRacialTalent9
-   MoonElfRacialTransformation
-   MoonElfRacialTransformation2
-   MoonElfRacialTransformation4
-   MoonElfRacialTransformation6
-   MoonElfRacialTransformation8
-   MoonElfRacialTransformation10
-   NightElfRacialTalent
-   NightElfRacialTalent
-   NightElfRacialTalent1
-   NightElfRacialTalent3
-   NightElfRacialTalent5
-   NightElfRacialTalent7
-   NightElfRacialTalent9
-   NightElfRacialTransformation
-   NightElfRacialTransformation2
-   NightElfRacialTransformation4
-   NightElfRacialTransformation6
-   NightElfRacialTransformation8
-   NightElfRacialTransformation10
-   NightElfTalentSkill
-   NightElfTransfSkill
-   OgreRacialTalent
-   OgreRacialTalent1
-   OgreRacialTalent3
-   OgreRacialTalent5
-   OgreRacialTalent7
-   OgreRacialTalent9
-   OgreRacialTransformation
-   OgreRacialTransformation2
-   OgreRacialTransformation4
-   OgreRacialTransformation6
-   OgreRacialTransformation8
-   OgreRacialTransformation10
-   OgreTalentSkill
-   OgreTransfSkill
-   OgreRacialTransformation
-   OrcRacialTalent
-   OrcRacialTalent1
-   OrcRacialTalent3
-   OrcRacialTalent5
-   OrcRacialTalent7
-   OrcRacialTalent9
-   OrcRacialTransformation
-   OrcRacialTransformation2
-   OrcRacialTransformation4
-   OrcRacialTransformation6
-   OrcRacialTransformation8
-   OrcRacialTransformation10
-   OrcTransfSkill
-   OrcRacialTransformation
-   RacialTalent
-   RacialTransformation
-   Special
-   TalentCraftSkill
-   TalentKnowSkill
-   TalentProfSkill
-   TalentSkill
-   ThinbloodgRacialTransformation
-   ThinbloodRacialTalent
-   ThinbloodRacialTalent1
-   ThinbloodRacialTalent3
-   ThinbloodRacialTalent5
-   ThinbloodRacialTalent7
-   ThinbloodRacialTalent9
-   ThinbloodRacialTransformation
-   ThinbloodRacialTransformation2
-   ThinbloodRacialTransformation4
-   ThinbloodRacialTransformation6
-   ThinbloodRacialTransformation8
-   ThinbloodRacialTransformation10
-   ThinbloodTalentSkill
-   ThinbloodTransfSkill
-   TieflingRacialTalent
-   TieflingRacialTalent1
-   TieflingRacialTalent3
-   TieflingRacialTalent5
-   TieflingRacialTalent7
-   TieflingRacialTalent9
-   TieflingRacialTransformation
-   TieflingRacialTransformation2
-   TieflingRacialTransformation4
-   TieflingRacialTransformation6
-   TieflingRacialTransformation8
-   TieflingRacialTransformation10
-   TieflingTalentSkill
-   TieflingTransfSkill
-   TransfSkill
-   WoodElfRacialTalent
-   WoodElfRacialTalent1
-   WoodElfRacialTalent3
-   WoodElfRacialTalent5
-   WoodElfRacialTalent7
-   WoodElfRacialTalent9
-   WoodElfRacialTransformation
-   WoodElfRacialTransformation2
-   WoodElfRacialTransformation4
-   WoodElfRacialTransformation6
-   WoodElfRacialTransformation8
-   WoodElfRacialTransformation10

**<span id="feats_talents"></span> Group Name:** -- feats\_talents.lst

-   AnimalAffinity
-   AnimalFriendship
-   AnimalHusbandry
-   Brute
-   CharismaticPlus
-   CharismaticTalent
-   Command
-   DedicatedPlus
-   DedicatedTalent
-   Diplomatic
-   Efficacious
-   Elusive
-   Facetious
-   FastLearner
-   FastTalent
-   FastPlus
-   Footwork
-   Finesse
-   FXResistance
-   HeavyGravityResistance
-   HeavyLoad
-   Hurling
-   Intimidating
-   Investigation
-   LikeRock
-   Mercantile
-   Might
-   Navigation
-   NeedSpeed
-   Oracle
-   Pulchritudinous
-   QuickerThanEye
-   QuickThinking
-   RadiationResistnace
-   RebuilderSwornEnemy
-   Selfless
-   Scholar
-   Sharpshooter
-   SmartPlus
-   SmartTalent
-   StrongPlus
-   StrongRage
-   StrongTalent
-   StunResistance
-   Survival
-   SwornEnemy
-   Tactician
-   Talent
-   ThrowingArm
-   ToughPlus
-   ToughRage
-   ToughTalent
-   ToxinResistance
-   Virtue
-   Xenotech

**<span id="languages"></span> Group Name:** -- languages.lst

-   Braille
-   Caddoan
-   Iroquoian
-   Muskogean
-   Read
-   Sahaptian
-   Signaling
-   Siouian
-   Spoken
-   Uto-Aztecan
-   Written

**<span id="races"></span> Group Name:** -- races.lst

-   Aberration
-   Animal
-   Humanoid
-   Magical Beast
-   Monstrous Humanoid
-   Plant
-   Vermin

**<span id="races_base"></span> Group Name:** -- races\_base.lst

-   Humanoid

**<span id="races_monsters"></span> Group Name:** -- races\_monsters.lst

-   Animal
-   Humanoid
-   Plant
-   Undead
-   Vermin

**<span id="skills"></span> Group Name:** -- skills.lst

-   Arcane
-   Charisma
-   Craft
-   HearthMagic
-   Intelligence
-   Knowledge
-   None
-   Perform
-   Profession
-   Science
-   Wisdom

**<span id="spells"></span> Group Name:** -- spells.lst

-   Arcane
-   Divine

**<span id="talent"></span> Group Name:** -- talents.lst

-   CharismaticTalent.Efficacious.Facetious.Intimidating.Pulchritudinous
-   CharismaticTalent.AnimalHusbandry.Command.Diplomatic.Mercantile.CharismaticPlus
-   DedicatedTalent.AnimalAffinity.AnimalFriendship.Oracle.Selfless.Virtue
-   DedicatedTalent.Survival.SwornEnemy.RebuilderSwornEnemy.Treatment.DedicatedPlus
-   Efficacious
-   FastTalent.Elusive.Finesse.NeedSpeed.QuickerThanEye
-   FastTalent.Footwork.Sharpshooter.FastPlus
-   SmartTalent.FastLearner.QuickThinking.Tactician
-   SmartTalent.Investigation.Navigation.Scholar.Xenotech.SmartPlus
-   StrongTalent.Brute.HeavyLoad.Hurling.LikeRock.Might
-   StrongTalent.HeavyGravityResistance.StrongRage.ThrowingArm.StrongPlus
-   ToughTalent.FXResistance.ToxinResistance
-   ToughTalent.ToughRage.RadiationResistnace.StunResistance.ToughPlus

**<span id="templates"></span> Group Name:** -- templates.lst

-   KnighthoodAPG
-   Magical Beast
-   Undead

**<span id="templates_focus"></span> Group Name:** --
templates\_focus.lst

-   Fey
-   Giant
-   Humanoid

**<span id="templates_hidden"></span> Group Name:** --
templates\_hidden.lst

-   Giant
-   Monstrous Humanoid
-   Outsider

**<span id="weaponprofs"></span> Group Name:** -- weaponprofs.lst

-   Archaic
-   Arquebus
-   Cannon
-   Exotic
-   ExoticFirearms
-   PersonalFirearm
-   Simple

**<span id="weaponprofs_natural"></span> Group Name:** --
weaponprofs\_natural.lst

-   Natural

**<span id="weapons"></span> Group Name:** -- weapons.lst

-   Arquebus
-   Cannon
-   Ranged
-   Projectile
-   Weapon


