+++
date = "2016-08-01"
title = "CLASS (Data: classes.lst)"
original_url = "list/data/classes.html#class"
categories = [ "all-tag", "classes-tag" ]
+++

## Status

None

## Syntax

`CLASS:x`

## Parameters

-   x: Text



<span id="class"></span> \*\*\* Updated 5.13.6

What it does
------------

-   This tells PCgen the class name and sets up the relationships with
    skills and spells.
-   This line can be entered twice in a single class entry (appear on 2
    separate lines) for purposes of making the lines easier to read in
    an editor (so as to not have to scroll forever to reach the end of
    the class line).
-   THIS <span class="underline"> **MUST** </span> BE THE FIRST TAG!!!
-   Symbols that should not be used: , / - + & If you need to use those
    symbols, put them in an OUTPUTNAME tag.
-   For class variants from other sources, the norm seen is 'Base Class
    Name (Source)' ex. Cleric (Fey).

Example
-------

`CLASS:Ranger`

The full class name is "Ranger".

`CLASS:Defender.MOD <tab> TEMPLATE:Maximum Spell Level`

Adds the TEMPLATE:Maximum Spell Level to the class "Defender".

`CLASS:Rogue.COPY=Rogueless`

Copies the Class "Rogue" and renames to "Rogueless".

`CLASS:Fighter.FORGET`

Removes the Class "Fighter" from the dataset.

Where it is used
----------------

Beginning of Class Line.

