+++
date = "2016-08-01"
title = "DOMAINS (Data: deities.lst)"
original_url = "/list/data/deities.html#domains"
categories = [ "all-tag", "deities-tag" ]
[menu.main]
    name = "DOMAINS (Data: deities.lst)"
    parent = "deities"
+++

## Status

None

## Syntax

`DOMAINS:x,x`

## Parameters

-   x: Text (Domain Name)
-   x: Text ('ALL')
-   x: .CLEAR
-   x: .CLEAR.Text (Domain Name)



What it does
------------

-   This is a comma-delimited list of domains that the deity grants to
    it's divine spell casting followers.
-   The domain name MUST match the domain names listed in the domain
    list file.
-   A domain entry of .CLEAR will remove all previously listed domains
    for the deity.
-   A domain entry of .CLEAR.name will remove the domain called "name"
    from the deity's domain list.
-   A domain entry of ALL will provide access to all domains for the
    deity and makes additional domain designations uncessecary.
-   Multiple DOMAINS tags may be present for a deity. They will all add
    to the list of the deity's domains.
-   PRExxx tags can be added at the end of DOMAINS tags to apply
    restrictions on which divine casters are allowed to select
    the domain.

Examples
--------

`DOMAINS:War,Law,Protection|PREALIGN:LG,NG,TN,CG`

The deity grants two of either the "War", "Law" or "Protection" domains,
but only if the cleric has one of the listed alignments.

`DOMAINS:ALL`

The deity grants two of any domains.

**.MOD Example (Appending):**

Initial Deity: `<deity name> <tab> DOMAINS:Law`

Modified By: `<deity name>.MOD <tab> DOMAINS:Evil`

Is Equivalent To: `<deity name> <tab> DOMAINS:Law,Evil`

