+++
date = "2016-08-01"
title = "PREVAR (Global: PRErequisite)"
original_url = "/list/global/pre.html#prevar"
categories = [ "all-tag", "pre-tag" ]
[menu.main]
    name = "PREVAR"
    parent = "global_pre"
    identifier = "global_pre_PREVAR"
+++

## Status

None

## Syntax

`None`

## Parameters




<span id="prevar"></span>

### PREVAR

Requires that a `VAR` variable has a certain value or range of values.

#### Status

#### Syntax

`PREVARoperator:varname,value`

`operator` is a comparison operator from the list `EQ` , `LT` , `LTEQ` ,
`GT` , `GTEQ` , or `NEQ` . The comparison operator is written as part of
the tag name, i.e. `PREVARLTEQ` . See [comparison
operators](/list/global/pre.html#comparison-operators) for more details.

`varname` is the name of a variable - as used in a `DEFINE:` or
`BONUS:VAR` statement.

`value` is the value the variable is to be compared to.

#### Examples

1.  `PREVARGT:Rage,4`

    Character must have a variable 'Rage' with a value greater
    than four.

2.  `PREVARGT:SneakAttack,5`

    Character must have a variable 'Sneak Attack' with a value greater
    than five.

3.  `PREVARGT:SneakAttack,5,Rage,4`

    Character must have a variable 'SneakAttack' with a value greater
    than five and a variable 'Rage' with a value greater than four.



