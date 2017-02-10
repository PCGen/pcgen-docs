+++
date = "2016-08-01"
title = "CHANGEPROF (Global: OTHER)"
original_url = "/list/global/other.html#changeprof"
categories = [ "all-tag", "other-tag" ]
[menu.main]
    name = "CHANGEPROF"
    parent = "global_other"
+++

## Status

New 5.3.13

## Syntax

`CHANGEPROF:x,x=y|x,x=y`

## Parameters

-   x: Text (Name of weapon)
-   x: TYPE.Text (weapon type)
-   y: Text (Category of Proficiency to change to)



What it does
------------

-   Changes named or types of weapons to new Proficiency category.
-   Valid everywhere.

Examples
--------

`CHANGEPROF:Urgrosh (Dwarven),Waraxe (Dwarven)=Martial`

Changes the above weapons to be Martial weapons for proficiency
purposes.

`CHANGEPROF:TYPE.Hammer=Simple`

Changes all weapons of TYPE Hammer to be Simple weapons for proficiency
purposes.

