+++
date = "2016-08-01"
title = "TEMPLATE (Data: feats.lst)"
original_url = "list/data/feats.html#template"
categories = [ "all-tag", "feats-tag" ]
+++

## Status

Updated 5.17.x

## Syntax

`TEMPLATE:x|x`

## Parameters

-   x: Text (Name of template)



What it does
------------

-   This is a pipe-delimited (|) list of templates that are granted by
    the feat.
-   Supports `%LIST` in conjunction with a `CHOOSE` tag.

Example
-------

`TEMPLATE:Celestial`

Adds the "Celestial" template to the character.

`TEMPLATE:Half Dragon (Red)|Zombie`

Adds the templates "Half Dragon (Red)" and "Zombie" to the character.

