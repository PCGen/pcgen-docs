+++
date = "2016-08-01"
title = "Game Mode: load.lst"
original_url = "/list/system/gamemode-load.html"

[menu.main]
    identifier = "system_gamemode-load"
    name = "Game Mode: load.lst"
    parent = "gamemode"
    
+++
The first line is a list of Size letters with a pipe-delimiter (|)
separating it from its load limit multiplier.

The second through next-to-last line contain a strength value (must be
incremental starting at 1) and the last line indicates the multiplier
and power escalation for every 10 strength points beyond the end of the
list.

This is to represent the multiplier of 4 for the first 10 beyond the end
of the strength list, 16 for the next 10 (4 to the power of 2), 64 for
the next 10 (4 to the power of 3) and so on.

You can change the multiplier (4) if you wish or add to the list of
strength/capacity lines, but they must be incremental (no skipping
strength scores).

------------------------------------------------------------------------

