+++
date = "2016-08-01"
title = "FUNDS (Data: starting_kits.lst)"
original_url = "/list/data/startingkits.html#funds"
categories = [ "all-tag", "startingkits-tag" ]
[menu.main]
    name = "FUNDS"
    parent = "data_startingkits"
+++

## Status

New 5.8

## Syntax

`FUNDS:x`

## Parameters

-   x: Currency Abbreviation found in miscinfo
    file (i.e. gp, euro, dollars, etc)



What it does
------------

Adds a specified amount of currency to the character's cash pool in the
Gear Sub-tab of the Inventory Tab. The FUNDS tag is paired with a QTY
tag which is used to set the amount granted. When used in a FUNDS line
QTY will take a number or formula with variables. It is possible to
generate a random number with the [roll() JEP
operator](/list/global/formulas.html#randomnumbers) , for example
`roll("1d6")` simulates a 1d6.

Example
-------

`FUNDS:gp <tab> QTY:100`

Adds 100 gp to the Gold pool which the character may now spend on
equipment.

`FUNDS:gp <tab> QTY:10*TL`

Adds 10 times the character's total level of gp to the Gold pool.

`FUNDS:gp <tab> QTY:10*roll("2d4")`

Adds 2d4 times 10 gp to the Gold pool.

