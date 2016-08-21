+++
date = "2016-08-01"
title = "Introduction to FreeMarker"
original_url = "/freemarker/intro.html"

[menu.main]
    identifier = "freemarker_intro"
    name = "Introduction to FreeMarker"
    parent = "freemarker"
    
+++
[FreeMarker](http://freemarker.org/) is a template engine that has now
been incorporated into PCGen's export system as an alternative to our
venerable export syntax. The FreeMarker engine brings some important
benefits:

-   Industry standard syntax
-   Support for macros to output parameterised blocks
-   Improved flow-control and logic instructions
-   Support for including other files, e.g. macro libraries or common
    blocks
-   Calculations and state within the output template
-   Built-in syntax support in [many text
    editors](http://freemarker.org/editors.html)

Here's a simple example FreeMarker PCGen template

``` {.code}
<!-- Produced on ${.now?date} at ${.now?time} using template ${.template_name} -->
<h1>Freemarker Sheet for <@pcstring tag="NAME"/> - ${.now?date}</h1>

<p> Character Name: <@pcstring tag="NAME"/> </p>
<p> Player Name: <@pcstring tag="PLAYERNAME"/> </p>

<p> Fighter: ${pcvar("CL=Fighter")} </p>
<p> Rogue: ${pcvar("CL=Rogue")} </p>

<p><@loop from=0 to=pcvar('countdistinct("CLASSES")')-1 ; class , class_has_next >
        <@pcstring tag="CLASSABB.${class}"/> <#t>
        <@pcstring tag="CLASS.${class}.LEVEL"/><#if class_has_next>,</#if><#t>
</@loop></p>
```

which produces the output

``` {.code}
<!-- Produced on 29/10/2013 at 9:44:47 PM using template csheet_test-html.ftl -->
<h1>Freemarker Sheet for Ronald 'Surefingers' Millbridge - 29/10/2013</h1>

<p> Character Name: Ronald 'Surefingers' Millbridge </p>
<p> Player Name: James </p>

<p> Fighter: 0 </p>
<p> Rogue: 11 </p>

<p>Rog 11,Wiz 2</p>
```



