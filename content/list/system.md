+++
date = "2016-08-01"
title = "System List Files"
original_url = "/list/system.html"

[menu.main]
    identifier = "list_system"
    name = "System List Files"
    parent = "list"
    
+++
System list files are used across all of PCGen's abilities and should
not be tampered with lightly, even for an experienced List Monkey!  The
next few sections describe each of the system list files and what they
do.

There are 2 main sections to contend with, Game System files and System
files.

Game System files are specific to the rules for a gaming system, such as
3e, Unisystem, D6, etc. These files define what rules apply for that
system, such as Hit Points, vs Vitality Points, Armor Class vs Damage
Reduction, etc.

System files are just that, files that the PCGen system uses. As such,
these files are more susceptible, to errors, so edit them with care!

Starting in the 5.9 line the remaining system files which have any game
specific bearing are being moved into the gameModes to make them
available for customization. A new directory named "default" has been
added to the gameModes directory which contains default versions of each
of the newly integrated files. If a gameMode is loaded which does not
contain one or more of these files then the files from the default
directory or loaded in their place.

------------------------------------------------------------------------

[![Valid HTML 4.01
Strict](../images/system/valid-html401.png)](http://validator.w3.org/check?uri=referer)

