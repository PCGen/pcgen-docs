+++
date = "2016-08-01"
title = "ADDDOMAINS (Data: classes.lst)"
original_url = "list/data/classes.html#adddomains"
categories = [ "all-tag", "classes-tag" ]
+++

## Status

Updated 6.03.x

## Syntax

`ADDDOMAINS:x|x`

## Parameters

-   x: Text (Domain Name)



What it does
------------

-   This grants additional domain choices to the character, it is a
    decimal (.) delimited list of names.
-   It does not add them to the character's domains, but merely adds
    them to the list they can choose from.
-   If the character gets a choice for a bonus domain, it may need to be
    paired with a BONUS:DOMAIN|NUMBER|x tag.
-   If used in the Class Level block it should be put on the third line
    with the SPELLSTAT:and SPELLTYPE: entries.
-   It can contain PRExxx tags, in brackets (\[PRExxx\]), immediately
    after the domain name.

Examples
--------

`CLASS:Foo <tab> ADDDOMAINS:Travel|Sun <tab> SPELLSTAT:CHA <tab> SPELLTYPE:Arcane`

The class gets the Travel and Sun domains as a choice regardless of the
deity selected.

`ADDDOMAINS:Sun`

The class gets the Sun domain as a choice regardless of the deity
selected.

`ADDDOMAINS:Sun|Law`

The class gets the Sun & Law domains as a choice regardless of the deity
selected.

`ADDDOMAINS:Sun[PREDIETY:Ra]|Law`

The class gets to choose between the Sun domain, if the character
follows the diety Ra & the Law domain regardless of the deity selected.

Where it is used
----------------

Class Level and Class Level Line.

**Deprecated Syntax:** <span class="lstdep"> Remove for 6.6 </span>

`ADDDOMAINS:Travel.Sun`

Becomes: `ADDDOMAINS:Travel|Sun`

