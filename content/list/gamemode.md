+++
date = "2016-08-01"
title = "Game Mode List Files"
original_url = "/list/gamemode.html"

[menu.main]
    identifier = "gamemode"
    name = "Game Mode"
    parent = "tag_indexes"
+++

## Game Mode files

Game Mode files, found in the `pcgen/system/gameModes/` directory, define the rules of each game system. For example:

* What the statistics are called, i.e. "hit points" or "vitality points"
* What different sizes of creatures exist, and the bonuses / penalties due to size.

These are specific for each game system, i.e. 3rd Edition, Pathfinder, 5th Edition.

Each Game Mode consists of the following files:

  * `bio/biosettings.lst` (optional)
  * `bio/locations.lst` (optional)
  * `bio/traits.lst` (optional)
  * `equipicons.lst` (optional)
  * `equipmentslots.lst`
  * `level.lst`
  * `load.lst`
  * `migration.lst`
  * `miscinfo.lst`
  * `pointbuymethods\_system.lst` (optional)
  * `rules.lst`
  * `sizeAdjustment.lst` (optional)
  * `statsandchecks.lst`
  * `tips.txt` (optional)

Files marked (optional) may be omitted; the defaults from the `pcgen/system/gameModes/default/` directory will be used instead.

