+++
date = "2016-08-01"
title = "PCGen Output Options"
original_url = "/menu/settings/pcgen/output.html"

[menu.main]
    identifier = "pcgen_output"
    name = "PCGen Output Options"
    parent = "pcgen"
    
+++
![PCGen Output Options](../../../images/preferences/output.png)

The **Output** option allows the user to select a default **HTML** (Used
by Print Preview), **PDF** (used by Print) and **EquipSet** (generated
from the **Inventory** , **Equipping** Sub-tab) output sheets.

It also allows the user to select the paper type, the ability to delete
temporary files on exit and toggles the weapon proficiency display in
the sheets.

A new addition is the ability to add a command that will be executed
after every export (HTML, PDF or others). If you use a % on the command,
it will be replaced by the fully qualified name of the file just created
by the export.

**Example:**

`cmd /c echo % >> exported_files_list.txt`

This will keep a list of every exported file in
exported\_files\_list.txt in your PCGen directory.

The **Include Skills on Sheet** option allows the user to select which
set of Skills will appear on the exported sheet. The default setting is
**Untrained** which will output all skills the character has ranks in as
well as skills the character may not have ranks in but can be used
untrained. **Skills w/ranks only** will output only those skills the
character has ranks in. **All** will output all skills from the loaded
sources. **Use the option selected on the Skills tab** will default to
the option selected on the Skills tab.



