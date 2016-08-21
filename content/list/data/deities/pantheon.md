+++
date = "2016-08-01"
title = "PANTHEON (Data: deities.lst)"
original_url = "list/data/deities.html#pantheon"
categories = [ "all-tag", "deities-tag" ]
+++

## Status

Deprecated 6.05.1 - use FACTSET

## Syntax

`PANTHEON:x|x`

## Parameters

-   x: Text (Pantheon Name)
-   x: .CLEAR



What it does
------------

-   To specify what pantheon the deity belongs to.
-   This is a pipe (|) delimited list.
-   The deity belongs to all pantheons if this tag is not present.
-   Using `.CLEAR` will clear the pantheon from the deities profile.

Examples
--------

`PANTHEON:Celtic`

The deity belongs to the "Celtic" pantheon.

`PANTHEON:Celtic|Elf (Sun)`

The deity belongs to the "Celtic" or "Sun Elf" pantheon.

**.MOD Example (Appending):**

Initial Deity: `<deity name> <tab> PANTHEON:Celtic`

Modified By: `<deity name>.MOD <tab> PANTHEON:Elf`

Is Equivalent To: `<deity name> <tab> PANTHEON:Celtic|Elf`

