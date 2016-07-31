+++
date = "2016-08-01"
title = "Companion Modifications File"
original_url = "/list/data/companionmodifiers.html"

[menu.main]
    identifier = "data_companionmodifiers"
    name = "Companion Modifications File"
    parent = "data"
    
+++
These files specify the bonuses that "enhanced companions", such as
familiars and a Paladin's special mount, receive from associating with
the character.

This page is separated into two sections: the [Building a Basic
Companion Mod](/list/data/companionmodifiers.html#howto) and the
[Companion Mod File Tag
Dictionary](/list/data/companionmodifiers.html#tagdictionary) .

------------------------------------------------------------------------

<span id="howto"></span> Building a Basic Companion Mod
-------------------------------------------------------

The Companion Mod file contains two types of lines. The FOLLOWER line
and the MASTERBONUSRACE line. The tags used on each line are listed
below.

FOLLOWER line uses the following tags:

[FOLLOWER](/list/data/companionmodifiers/follower.html) - Begins the
line.

[COPYMASTERBAB](/list/data/companionmodifiers/copymasterbab.html) -
Replaces the follower's Base Attack Bonus (BAB)

[COPYMASTERCHECK](/list/data/companionmodifiers/copymastercheck.html) -
Replaces the follower's check bonuses.

[COPYMASTERHP](/list/data/companionmodifiers/copymasterhp.html) -
Replaces the follower's HP total.

[FOLLOWERADJUSTMENT](/list/data/companionmodifiers.html#followeradjustment)

[HD](/list/data/companionmodifiers/hd.html) - Grants bonus hit dice to
the follower of its normal creature type.

[RACETYPE](/list/data/companionmodifiers/racetype.html) - Changes the
follower's creature type.

[USEMASTERSKILL](/list/data/companionmodifiers/usemasterskill.html) -
Determines whether the follower uses its Master's skill ranks.

Any global tag.

MASTERBONUSRACE line uses the following tags:

[MASTERBONUSRACE](/list/data/companionmodifiers/masterbonusrace.html) -
Begins the line.

The [TYPE](/list/global/type.html#companionmod) tag, any
[BONUS](/list/global/bonus.html) tag and the global
[VFEAT](/list/global/other/vfeat.html) and
[ABILITY](/list/global/other/ability.html) tags.

------------------------------------------------------------------------

<span id="tagdictionary"></span> Companion Mod File Tag Dictionary
------------------------------------------------------------------

------------------------------------------------------------------------

