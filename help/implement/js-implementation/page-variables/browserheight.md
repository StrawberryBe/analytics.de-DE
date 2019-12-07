---
description: Seitenvariablen werden direkt in Berichten ausgefüllt, z. B. pageName, List Props, List Variables usw.
keywords: Analytics Implementation
subtopic: Variables
title: Seitenvariablen
topic: null
uuid: null
translation-type: tm+mt
source-git-commit: 99ee24efaa517e8da700c67818c111c4aa90dc02

---


# browserHeight

Die Variable „“ gibt die Höhe des Browser-Fensters an.


<!-- 
browserheight.xml
-->

Diese Variable erhält ihren Wert nach dem Seiten-Code und bevor *`doPlugins`* ausgeführt wird.

> [!NOTE] Diese Variable sollte nur gelesen und nie geschrieben werden.

Sie dürfen diese Werte lesen und in Eigenschaftsvariablen/eVars kopieren, jedoch nie ändern. Diese Variable wird mit der Version H.11 der JavaScript-Datei neu eingeführt.

**Parameter**

<table id="table_94598A2204CF42FF9DD14D353D5C0468"> 
 <thead> 
  <tr> 
   <th class="entry"> Abfrageparameter </th> 
   <th class="entry"> Wert </th> 
   <th class="entry"> Beispiel </th> 
   <th class="entry"> Betroffene Berichte </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td> <p>bh </p> </td> 
   <td> <p>Eine positive Ganzzahl </p> </td> 
   <td> <p>865 </p> </td> 
   <td> <p>„Datenverkehr“ &gt; „Technologie“ &gt; „Browserhöhe“ </p> </td> 
  </tr> 
 </tbody> 
</table>

