+++
date = "2016-08-01"
title = "Output Sheet Example HTML"
original_url = "/outputsheet/example-html.html"

[menu.main]
    identifier = "outputsheet_example-html"
    name = "Output Sheet Example HTML"
    parent = "outputsheet"
    
+++
The following is an example of an HTML Output Sheet Template

------------------------------------------------------------------------

     <html>
      <head>
       <title>|NAME|'s Weapons and Equipment</title>
       <style TYPE="text/css">
        .h { font-size:8pt; vertical-align: bottom; }
        .topline { border-top-width:1px; border-top: 1pt solid black; }
        .border { border: 1px solid black; }
       </style>
      </head>
      <body bgcolor="white">

       <!-- Start Character Info Table -->
       <table cellpadding="0" cellspacing="4" border="0" width="100%">
        <tr>
         <td width="35%" class="h">|NAME|</td>
         <td width="20%" class="h">|CLASSLIST|</td>
         <td width="10%" class="h">|TOTALLEVELS|</td>
         <td width="35%" class="h">|PLAYERNAME|</td>
        </tr>
        <tr>
         <td class="topline"><font style="font-size:6pt">CHARACTER NAME</font></td>
         <td class="topline"><font style="font-size:6pt">CLASS</font></td>
         <td class="topline"><font style="font-size:6pt">LEVEL</font></td>
         <td class="topline"><font style="font-size:6pt">PLAYER</font></td>
        </tr>
       </table>
       <!-- End Character Info Table -->
       <!-- Start Main Sheet Table -->
       <table cellpadding="0" width="100%" cellspacing="5" border="0">
        <tr>
         <td valign="top" width="50%">
          <!-- Start Weapon Table -->
          <table cellpadding="0" width="100%" cellspacing="0" border="0">
           <tr>
            <td bgcolor="black" align="center"><font color="white" style="font-size: 9pt"><b>WEAPONS</b></font></td>
           </tr>
          </table>
    |FOR,%weap,0,COUNT[EQTYPE.WEAPON]-1,1,0|<font style="font-size:2pt"><br /></font>
          <table cellpadding="0" width="100%" cellspacing="0" border="0">
           <tr>
            <td align="center" height="15" bgcolor="black" rowspan="2" width="40%"><font style="font-size:10pt" color="white"><b>|WEAPON%weap.NAME|<br /></b></font></td>
            <td align="center" bgcolor="black" width="20%" height="15"><font style="font-size:6pt" color="white"><b>TOTAL ATTACK BONUS</b></font></td>
            <td align="center" bgcolor="black" width="20%" height="15"><font style="font-size:6pt" color="white"><b>DAMAGE</b></font></td>
            <td align="center" bgcolor="black" width="20%" height="15"><font style="font-size:6pt" color="white"><b>CRITICAL</b></font></td>
           </tr>
           <tr>
            <td align="center" bgcolor="white" class="border"><font style="font-size:8pt" color="black"><b>|WEAPON%weap.TOTALHIT|<br /></b></font></td>
            <td align="center" bgcolor="white" class="border"><font style="font-size:8pt" color="black"><b>|WEAPON%weap.DAMAGE|<br /></b></font></td>
            <td align="center" bgcolor="white" class="border"><font style="font-size:8pt" color="black"><b>|WEAPON%weap.CRIT|/x|WEAPON%weap.MULT|<br /></b></font></td>
           </tr>
          </table>
          <table cellpadding="0" cellspacing="0" border="0" width="100%">
           <tr>
            <td align="center" height="15" bgcolor="black" width="15%"><font style="font-size:6pt" color="white"><b>HAND</b></font></td>
            <td align="center" height="15" bgcolor="black" width="15%"><font style="font-size:6pt" color="white"><b>RANGE</b></font></td>
            <td align="center" bgcolor="black" width="15%" height="15"><font style="font-size:6pt" color="white"><b>TYPE</b></font></td>
            <td align="center" bgcolor="black" width="15%" height="15"><font style="font-size:6pt" color="white"><b>SIZE</b></font></td>
            <td align="center" bgcolor="black" width="40%" height="15"><font style="font-size:6pt" color="white"><b>SPECIAL PROPERTIES</b></font></td>
           </tr>
           <tr>
            <td align="center" bgcolor="white" class="border"><font style="font-size:8pt" color="black"><b>|WEAPON%weap.HAND|<br /></b></font></td>
            <td align="center" bgcolor="white" class="border"><font style="font-size:8pt" color="black"><b>|WEAPON%weap.RANGE|<br /></b></font></td>
            <td align="center" bgcolor="white" class="border"><font style="font-size:8pt" color="black"><b>|WEAPON%weap.TYPE|<br /></b></font></td>
            <td align="center" bgcolor="white" class="border"><font style="font-size:8pt" color="black"><b>|WEAPON%weap.SIZE|<br /></b></font></td>
            <td align="center" bgcolor="white" class="border"><font style="font-size:8pt" color="black"><b>|WEAPON%weap.SPROP|<br /></b></font></td>
           </tr>
          </table>
    |ENDFOR|
          <!-- End Weapon Table -->
         </td>
         <td valign="top" width="50%">
          <!-- START Equipment Table -->
          <table width="100%" cellspacing="0" cellpadding="2" border="0">
           <tr>
            <td bgcolor="black" align="center" colspan="5"><font color="white" style="font-size: 9pt"><b>EQUIPMENT</b></font></td>
           </tr>
           <tr>
            <td valign="top" width="60%" class="border"><font style="font-size: 8pt"><b>ITEM</b></font></td>
            <td valign="top" width="10%" class="border" align="center"><font style="font-size: 8pt"><b>EQUIPPED</b></font></td>
            <td valign="top" width="10%" class="border" align="center"><font style="font-size: 8pt"><b>QTY</b></font></td>
            <td valign="top" width="10%" class="border" align="center"><font style="font-size: 8pt"><b>WT.</b></font></td>
            <td valign="top" width="10%" class="border" align="center"><font style="font-size: 8pt"><b>GP COST</b></font></td>
           </tr>
    |FOR,%eqp,0,COUNT[EQUIPMENT.NOT.Weapon]-1,1,0|
           <tr>
            <td valign="top" class="border"><font style="font-size: 8pt">|EQ.NOT.Weapon.%eqp.NAME.MAGIC~<b>~</b>|</font><font style="font-size: 5pt"><br />|EQ.NOT.Weapon.%eqp.SPROP|</font></td>
            <td valign="top" class="border" align="center"><font style="font-size: 8pt">|EQ.NOT.Weapon.%eqp.EQUIPPED|<br /></font></td>
            <td valign="top" class="border" align="center"><font style="font-size: 8pt">|EQ.NOT.Weapon.%eqp.QTY|<br /></font></td>
            <td valign="top" class="border" align="center"><font style="font-size: 8pt">|EQ.NOT.Weapon.%eqp.WT|<br /></font></td>
            <td valign="top" class="border" align="center"><font style="font-size: 8pt">|EQ.NOT.Weapon.%eqp.COST|<br /></font></td>
           </tr>
    |ENDFOR|
          </table>
          <!-- End Equipment Table -->
         </td>
        </tr>
       </table>
       <!-- End Main Sheet Table -->
      </body>
     </html>

------------------------------------------------------------------------



