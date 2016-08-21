+++
date = "2016-08-01"
title = "PCGen Functions"
original_url = "/freemarker/pcgen-functions.html"

[menu.main]
    identifier = "freemarker_pcgen-functions"
    name = "PCGen Functions"
    parent = "freemarker"
    
+++
To provide output of PCGen characters we need to be able to access the
character data and the output tags. In the FreeMarker documentation they
talk about the data model, plus directives and functions. At this time,
PCGen does not provide a data model, but instead provides a number of
directives and functions that allow access to the character data.
Current work is examining the provision of a data model to access
characters.

A **directive** produces output to the output file, or controls the flow
of the output process. FreeMarker directives start with &lt;\# while
PCGen directives start with &lt;@

A **function** allows a value to be extracting into a variable (or
directly output). Both PCGen and FreeMarker functions are enclosed in
\${ } . Functions may also be referred to directly wherever a formula or
variable is used.

### pcstring

This tag evaluates a PCGen export token for the current character and
returns the value as a string. It may be called as a directive (with a
single parameter named 'tag') or as a function (with a single unnamed
parameter).

*Examples*

``` {.code}
<@pcstring tag="PLAYERNAME"/>
<@pcstring tag="CLASSABB.${class}"/>
${pcstring('CLASSABB.${class}')}
<#if (pcstring('SPELLLISTCLASS.${class}')?length > 0)>present</#if>
        
```

### pcvar

This function allows character variable values to be exported to a
FreeMarker template. It evaluates a variable for the current character
and returns the value as a number.

*Examples*

``` {.code}
<#assign numClasses=pcvar('countdistinct("CLASSES")')/>
${pcvar('count("ABILITIES","CATEGORY=FEAT","TYPE=Metamagic",
        "VISIBILITY=DEFAULT[or]VISIBILITY=OUTPUT_ONLY")')}
${pcvar("CL=Fighter")}

        
```

### pcboolean

The pcboolean function allows character boolean values to be exported to
a FreeMarker template. It evaluates an export token for the current
character and returns the value as a boolean.

*Examples*

``` {.code}
<#if pcboolean('WEAPON.${weap}.ISTYPE.Double')>
<#if (pcboolean('VAR.HASFEAT:CMB Output')) >
        
```

### pchasvar

The pchasvar function allows the presence of variables to be tested in
the output sheet.

*Examples*

``` {.code}
<#if pchasvar('Foo')>
<#if (pchasvar("Manifester") || pchasvar('PsychicWarriorManifester')) >
        
```

### loop

The loop directive provides a way to repeat content a certain number of
times. Unlike the inbuilt list directive it can loop zero times.

**Parameters**

-   from (optional) - The starting value, defaults to 0.
-   to - The ending value (inclusive). If this is less than from then
    the contents will not be output.
-   step (optional) - The amount to increment b each loop, defaults
    to 1.

In addition up to two loopvars may be specified. The first will be
populated with the current index value of the loop and the second will
be a boolean indicating if there are more iterations of the loop to go.
We recommend that the second variable, if present, is named after the
first variable with \_has\_next added. e.g. class, class\_has\_next.
This is in order to match the list directive, which provides a similarly
named variable automatically.

*Example*

``` {.code}
<@loop from=0 to=pcvar('countdistinct("CLASSES")')-1 ; class , class_has_next >
        <@pcstring tag="CLASSABB.${class}"/>
        <@pcstring tag="CLASS.${class}.LEVEL"/><#if class_has_next>,</#if>
</@loop>
        
```

might produce

    Rog 11, Wiz 5
            

### equipsetloop

The equipsetloop directive provides a way to repeat content for each of
a character's equipment sets.

**Parameters**

None

*Example*

``` {.code}
<@equipsetloop>
  <b>Equipment Set : </b> ${pcstring("EQSET.NAME")}. Equipment:
  <@loop from=0 to=pcvar('COUNT[EQUIPMENT.MERGELOC]')-1 ; equip , equip_has_next >
    ${pcstring("EQ.MERGELOC.${equip}.NAME")}<#if equip_has_next>, </#if>
  </@loop><#lt><#-- Equipment -->
  </equipmentset><br/>
</@equipsetloop>
        
```

might produce

``` {.code}
<b>Equipment Set : </b> Travelling Gear. Equipment: Backpack, Longsword, Traveller's Outfit<br/>
<b>Equipment Set : </b> Council. Equipment: Coin purse, Noble's Outfit, Rapier<br/>
        
```

\

FreeMarker Variables
--------------------

PCGen also provides some in built variables which can be used in
FreeMarker. These are referred to in the same way as any user defined
variables.

### gameodename

This is the name of the current game mode.

*Example*

``` {.code}
<#if (gamemodename = "Modern" || gamemodename = "Darwins_World_2" || gamemodename = "Sidewinder") >
  ${gamemodename}
</#if>
        
```

\

------------------------------------------------------------------------



