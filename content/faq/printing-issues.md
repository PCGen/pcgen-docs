+++
date = "2016-08-01"
title = "Output and Printing Issues"
original_url = "/faq/printing-issues.html"

[menu.main]
    identifier = "faq_printing-issues"
    name = "Output and Printing Issues"
    parent = "faq"
    
+++
1.  <span class="underline"> How do I get the character sheets to only
    print out the skills my character has? </span>

    There is a list box in the lower right hand corner of the Skills tab
    that determines which skills show up on the character sheet (called
    "Include skills").

    -   **All** - includes all skills.
    -   **Untrained** - includes skills with ranks and untrained.
    -   **None** - should include only those with ranks.

2.  <span class="underline"> How do I get my familiar's stat-block to
    appear on my wizard's character sheet? </span>

    The OS block for familiars is only activated when both the
    familiar's and the master's files are loaded.

3.  <span class="underline"> How do I get the natural attacks block to
    show up on my character sheet? </span>

    To activate the "Natural Attack" OS block on the character sheet You
    will need to make an **ABILITY** for that attack. Your new ability
    will look something like the following:

    > `Bite`
    >
    > `CATEGORY:Natural Attack`
    >
    > `TYPE:NaturalAttack`
    >
    > `ASPECT:NaturalAttackName|Bite`
    >
    > *This is the name of the Attack that will be displayed.*
    >
    > `ASPECT:NaturalAttackToHit|%1|BAB+STR+BiteAdditional`
    >
    > *Formula to give the correct attack, will need a special set up if
    > you want Weapon Focus or Greater Weapon Focus to work, there is NO
    > proficiency associated with this "attack".*
    >
    > *`ASPECT:NaturalAttackDamage|%1d%2|BiteDamageDice|BiteDamageSize`*
    >
    > *Sets your damage, the nice thing is these are variable, however,
    > these are NOT size dependent. But you can adjust the damage*
    >
    > `ASPECT:NaturalAttackDamageBonus|%1|STR`
    >
    > *Sets your bonus damage*
    >
    > `ASPECT:NaturalAttackReach|%1|REACH.VAL`
    >
    > *Sets your reach - "REACH.VAL" uses the PC's natural Reach value*
    >
    > `ASPECT:NaturalAttackType|Bludgeoning`
    >
    > *Sets your damage type - Bludgeoning, Slashing, Piercing, Energy
    > Type, Element Type*
    >
    > `ASPECT:NaturalAttackThreatRange|%1|BiteThreatRange`
    >
    > *Sets your natural weapon threat range - typically '20'*
    >
    > `ASPECT:NaturalAttackThreatRange|x%1|BiteCritMult`
    >
    > *Sets your Critical Multiplier value*
    >
    > `ASPECT:NaturalAttackNotes|x`
    >
    > *Allows special notes, like a poison attack*
    >
    > `DESC:x`
    >
    > *Allows additional special notes, like a improved poison attack*
    >
    > *These Set the Values. NOTE: they are all variables and you may
    > alter however you wish.*
    >
    > `DEFINE:BiteDamageDice|0`
    >
    > `DEFINE:BiteDamageSize|0`
    >
    > `DEFINE:BiteCritMult|2`
    >
    > `BONUS:VAR|BiteDamageDice|1`
    >
    > `BONUS:VAR|BiteDamageSize|6`
    >
    > `DEFINE:BiteAdditional|0`
    >
    > `DEFINE:BiteThreatRange|0`
    >
    > `BONUS:VAR|BiteThreatRange|20`

    For Special Attack Notes, you may either use `DESC:x` , or
    `ASPECT:NaturalAttackNotes|x` . `ASPECT` is used for just one note
    while `DESC` can take PRExxx tags and are ideal if your attack can
    be given to other creatures whose attacks vary by level
    based increases.

    What this solution will not do is handle iterative attacks unless
    you set up the ability with an `ASPECT` with all the
    iterative attacks. Unfortunately, ASPECT needs work in order to
    fully support any Alternative Iterative Attacks, or partial
    Iterative Attacks.

    Suggested Method to add Bonus to Hit by proficiency would be to do
    `BONUS:VAR|BiteAdditional|1|PREFEAT:1,Weapon Focus(Bite)` *and make
    sure you add **Bite** to the weaponprof.lst file and append
    `AUTO:WEAPONPROF|Bite` to the ability. This will allow the character
    to take the Proficiency in Weapon Focus. Repeat for other methods
    you desire.*

4.  *<span class="underline"> How do I get checkboxes to show up on my
    character sheet for my homebrew abilitiy? </span>*

    *To activate the "Checkboxe" block on your character sheet for your
    homebrew Special Ability you will need to include the following in
    your ability:*

    1.  *Include the "Checklist" type in the abilities list of types.
        **Example:** `TYPE:SpecialAttack.Supernatural.Checklist`*
    2.  *Include the following `ASPECT` tags:*

        *`ASPECT:CheckList|Yes`*

        *`ASPECT:CheckCount|x` \[x can be a number, variable or
        formula.\]*

        `ASPECT:CheckType|y` \[ *y is simple text that is displayed next
        to the Check Boxes.* \]

5.  <span class="underline"> How do I get conditional skill bonuses to
    show up on my character sheet? </span>

    To activate the "Skill Info Block" on your character sheet the
    character must have been granted an ability or feat with the
    following included in it:

    1.  The quot;SkillBonusquot; type included in the type list.
        **Example:** `TYPE:SpecialQuality.RacialBonus.SkillBonus`
    2.  `ASPECT:SkillBonus|x` tag must be included in the granted
        ability or feat. The quot;xquot; is simple text as per the
        `DESC` tag.

    This will display the included aspect text under the skills block.

6.  <span class="underline"> I try to preview a character or bring up
    the Doc, and nothing happens. </span>

    Since PCGen is cross-platform it's hard to assume what browser
    you're using. Click on the menu item Settings-&gt;Preferences and a
    dialog box will appear.

    One of the options under Locations is to set your Browser Path, just
    navigate to the executable of your favourite browser.

7.  <span class="underline"> I click on the print icon and get a warning
    about missing files. </span>

    The pdf\_new.zip library is required if you want to print directly
    from PCGen - otherwise you can view the files in your browser or
    adobe acrobat (pdf files) and print from there. The pdf\_new.zip
    file is located
    [here](http://prdownloads.sourceforge.net/pcgen/pdf_new.zip) , unzip
    it into the lib subdirectory where you installed PCGen. Then you'll
    need to re-launch PCGen for it to find it properly.

8.  <span class="underline"> Does PCGen support any command line
    exporting functionality? </span>

    PCGen does support command line exporting of characters through its
    **Command Line Interface (CLI)** . For a complete description of all
    options available see the [PCGen
    CLI](/walkthrough/initial-startup.html#cli) page.

------------------------------------------------------------------------



