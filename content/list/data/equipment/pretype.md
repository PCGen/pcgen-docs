+++
date = "2016-08-01"
title = "PRETYPE (Data: equipment.lst)"
original_url = "/list/data/equipment.html#pretype"
categories = [ "all-tag", "equipment-tag" ]
[menu.main]
    name = "PRETYPE"
    parent = "data_equipment"
+++

## Status

None

## Syntax

`PRETYPE:x,y,y`

## Parameters

-   x: Number (The number of types that must match the
    specified requirements).
-   y: Text (Equipment type).
-   y: EQMODTYPE=Text (Equipment Modifier type).
-   y: EQMOD=Text (Equipment Modifier KEY).
-   y: Same as above.



What it does
------------

-   Make specific Types or Equipment Modifiers a prerequisite.
-   `EQMODTYPE` checks for the **TYPE** in the applied Equipment
    Modifiers, not Equipment type.
-   `EQMOD` checks for the specified **EQMOD** by name or key.
-   `EQMOD` can take an optional parameter of the form
    `EQMOD=<key>(<choice>)` , where the "choice" represents an item
    previously selected by an internal chooser for the specified
    **EQMOD** .

<span class="alpha"> Note </span> : `PRETYPE` has a different use
outside of Equipment and Equipment Modifier files, it checks for race
types. See the [Global PRETYPE](/list/global/pre/pretype.html) entry for
usage outside of Equipment and Equipment Modifier files.

Examples
--------

`PRETYPE:1,Magic <tab> PRETYPE:1,Piercing,Slashing`

Type must be magic and piercing or slashing

`PREMULT:2,[PRETYPE:1,Magic],[PRETYPE:1,Piercing,Slashing]`

This example, utilizing the PREMULT tag, accomplishes the same thing as
the example above it but as it is one statement it can be attached to a
BONUS statement.

`!PRETYPE:1,Heavy`

Type must NOT be Heavy

`PRETYPE:1,EQMODTYPE=Mundane`

Use to test for any modifier with "Mundane" type.

`PRETYPE:1,EQMOD=IRONWOOD`

Use to test for the "Ironwood" Equipment Modifier.

**Secondary Syntax:** PRETYPE:y,y|y

What it does
------------

-   PRETYPE has a second older syntax which is still in use in the
    release files.
-   The comma (,) represents a logical **AND** function, indicating that
    all types listed are required to pass.
-   The pipe (|) represents the logical **OR** function, indicating that
    only one of the types listed are required to pass.
-   Pipes (|) and commas (,) can be combined with the logical **OR**
    being processed first and then the logical **AND** . As an example,
    `PRETYPE:Heavy,Armor|Shield` translates to: Must have "Heavy" AND
    either "Armor" OR "Shield" types.

Examples of secondary syntax
----------------------------

`PRETYPE:Magic,Piercing,Slashing`

Type must be Magic, Piercing and Slashing.

`PRETYPE:Magic,Armor|Shield,Piercing,Slashing`

Type must be Magic, Piercing, Slashing and (Armor OR Shield).

