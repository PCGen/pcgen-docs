+++
date = "2016-08-01"
title = "FEAT (Data: domains.lst)"
original_url = "/list/data/domains.html#feat"
categories = [ "all-tag", "domains-tag" ]
[menu.main]
    name = "FEAT (Data: domains.lst)"
    parent = "domains"
+++

## Status

Updated 6.05.04 (July 2015): JIRA NEWTAG-477 / Github PR #380 The FEAT tag is deprecated. Use ABILITY instead. All FEAT tags have been deprecated and replaced by the ABILITY system, which is more general. The ABILITY system can model feats, racial features, class features, traits, flaws, temporary bonuses, and so on, all using a common format. Updated 5.17.4 Tag Name: FEAT:x,x Variables Used (x): Text (Feat Name) What it does: This is a comma-delimited (,) list of feats granted to a character. The hyphen (-) is used only in the OUTPUTNAME of feats and should NOT be used in the feat list for this tag. (See example below.) When including a feat with an internal chooser, subchoices can be handled one of two ways. Subchoices must be specified within the tag. (e.g. Weapon Focus (Longsword)). or Used in conjunction with the CHOOSE tag, %LIST can be used with this tag to provide the required choice. .MOD Behavior: When modifying a domain with the .MOD tag, given an existing FEAT tag, the data included in a new FEAT tag will be appended to the existing tag data. Example: FEAT:Blind Fight,Alertness The "Blind-Fight" & "Alertness" bonus feats are granted to clerics with this domain. CHOOSE:WEAPONPROFS|LIST <tab> FEAT:Weapon Focus (%LIST) The feat "Weapon Focus" is granted as an automatic feat with the weapon chosen with the CHOOSE tag. .MOD Example: Initial Domain: Space Monkey <tab> FEAT:Alertness Modified By: Space Monkey.MOD <tab> FEAT:Blind Fight Is Equivalent To: Space Monkey <tab> FEAT:Alertness,Blind Fight . The "Alertness" & "Blind-Fight" bonus feats are granted to clerics with this domain.

## Syntax

`None`

## Parameters






