+++
date = "2016-08-01"
title = "Game Mode: pointbuymethods_system.lst"
original_url = "/list/system/gamemode-pointbuymethod.html"

[menu.main]
    identifier = "system_gamemode-pointbuymethod"
    name = "Game Mode: pointbuymethods_system.lst"
    parent = "system"
    
+++
The <span class="lstfile"> pointbuymethods\_system.lst </span> file is
where a GameMode defines the "standard" point levels used for that
GameMode when using the **Point Buy Methods** for Character
Statdetermination.

Building a Point Buy Methods File 101
-------------------------------------

PointBuyMethods files have two types of lines: the Stat line and the
Method line.

### The Stat Line Tags

The Stat Line uses the following tags:

------------------------------------------------------------------------

<span id="statcost"></span>

<span id="statcost"></span> **Tag Name:** STAT:x

**Variables Used (x):** Number (Stat value)

**Tag Name:** COST:x

**Variables Used (x):** Number (Stat point cost)

**What it does:**

When using the "Point Buy Method" of determining a characters stats, the
Stat Line defines the `COST` to "buy" a particular `STAT` .

**Stat Line Example:**

`STAT:7 <tab> COST:-4`

Starting with a stat of 10, buying a stat change to 7 will gain 4
points.

`STAT:8 <tab> COST:-2`

Starting with a stat of 10, buying a stat change to 8 will gain 2
points.

`STAT:9 <tab> COST:-1`

Starting with a stat of 10, buying a stat change to 9 will gain 3
points.

`STAT:10 <tab> COST:0`

Starting with a stat of 10, buying a stat change to 10 will cost 0
points.

`STAT:11 <tab> COST:1`

Starting with a stat of 10, buying a stat change to 11 will cost 1
points.

`STAT:12 <tab> COST:2`

Starting with a stat of 10, buying a stat change to 12 will cost 2
points.

`STAT:13 <tab> COST:3`

Starting with a stat of 10, buying a stat change to 13 will cost 3
points.

`STAT:14 <tab> COST:5`

Starting with a stat of 10, buying a stat change to 14 will cost 5
points.

`STAT:15 <tab> COST:7`

Starting with a stat of 10, buying a stat change to 15 will cost 7
points.

`STAT:16 <tab> COST:10`

Starting with a stat of 10, buying a stat change to 16 will cost 10
points.

`STAT:17 <tab> COST:13`

Starting with a stat of 10, buying a stat change to 17 will cost 13
points.

`STAT:18 <tab> COST:17`

Starting with a stat of 10, buying a stat change to 18 will cost 17
points.

------------------------------------------------------------------------

### The Method Line Tags

The Method Line uses the following tags:

------------------------------------------------------------------------

<span id="methodpoints"></span>

<span id="methodpoints"></span> **Tag Name:** METHOD:x

<span id="methodpoints"></span> **Variables Used (x):** Text (Method
name)

<span id="methodpoints"></span> **Tag Name:** POINTS:x

<span id="methodpoints"></span> **Variables Used (x):** Number
(Available points)

<span id="methodpoints"></span> **What it does:**

<span id="methodpoints"></span> When using the "Point Buy Method" of
determining a characters stats, the Method Line defines the total
`POINTS` available to buy stats.

<span id="methodpoints"></span> **Method Line Examples:**

<span id="methodpoints"></span>`METHOD:Low Fantasy <tab> POINTS:10`

<span id="methodpoints"></span> The "Low Fantasy" point buy method
allows 10 total points for purchasing stats.

<span id="methodpoints"></span>`METHOD:Standard Fantasy <tab> POINTS:15`

<span id="methodpoints"></span> The "Standard Fantasy" point buy method
allows 15 total points for purchasing stats.

<span id="methodpoints"></span>`METHOD:High Fantasy <tab> POINTS:20`

<span id="methodpoints"></span> The "High Fantasy" point buy method
allows 20 total points for purchasing stats.

<span id="methodpoints"></span>`METHOD:Epic Fantasy <tab> POINTS:25`

<span id="methodpoints"></span> The "Epic Fantasy" point buy method
allows 25 total points for purchasing stats.

<span id="methodpoints"></span>

------------------------------------------------------------------------

<span id="methodpoints"></span>

