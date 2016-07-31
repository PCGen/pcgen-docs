+++
date = "2016-08-01"
title = "Game Mode: rules.lst"
original_url = "/list/system/gamemode-rules.html"

[menu.main]
    identifier = "system_gamemode-rules"
    name = "Game Mode: rules.lst"
    parent = "system"
    
+++
This file contains Rule Checks that the user can turn on/off in the GUI.

**Format is:**

`Name:aName <tab> VAR:/PARM:aKey <tab> DEFAULT:YES/NO <tab> EXCLUDE:aKey <tab> DESC:optional description`

------------------------------------------------------------------------

**<span id="name"></span> Tag Name:** Name:aName

**Variables Used (aName):** Text (Name)

**What it does:**

aName is used to search the Language.properties file for a DESC to
display in the GUI.

------------------------------------------------------------------------

**<span id="var"></span> Tag Name:** VAR:/PARM:aKey

**Variables Used (aKey):** Text (unique key)

**What it does:**

aKey is the unique key used to store and reference this Rule.

VAR:aKey can be referenced in .lst files.

PARM:aKey means it's hardcoded into the Java code.

------------------------------------------------------------------------

**<span id="default"></span> Tag Name:** DEFAULT:x

**Variables Used (x):** Boolean (YES or NO)

**What it does:**

Sets the initial state of the rule. Yes for on, no for off.

------------------------------------------------------------------------

**<span id="exclude"></span> Tag Name:** EXCLUDE:aKey

**Variables Used (aKey):** Text (unique key)

**What it does:**

prevents two rules from being active at the same time. It also creates a
Radio button in the GUI to choose between the two rules.

------------------------------------------------------------------------

**<span id="desc"></span> Tag Name:** DESC:x

**Variables Used (x):** Text (optional description)

**What it does:**

Optional description and is overridden by the Language.properties file
from the java code.



