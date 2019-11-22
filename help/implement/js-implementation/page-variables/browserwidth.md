---
description: Seitenvariablen werden direkt in Berichten ausgefüllt, z. B. pageName, List Props, List Variables usw.
keywords: Analytics Implementation
solution: Analytics
subtopic: Variables
title: Seitenvariablen
topic: null
uuid: null
translation-type: tm+mt
source-git-commit: 47291fb3d55ab3eb5ef181770bf2078c7ea55bc4

---



# browserWidth

Die Variable „“ gibt die Breite des Browser-Fensters an.


<!-- 

browserwidth.xml

 -->

Diese Variable erhält ihren Wert nach dem Seiten-Code und bevor *`doPlugins`* ausgeführt wird.

> [!NOTE] Diese Variable sollte nur gelesen und nie geschrieben werden.

Sie dürfen diese Werte lesen und in Eigenschaftsvariablen/eVars kopieren, jedoch nie ändern. Diese Variable wird mit der Version H.11 der JavaScript-Datei neu eingeführt.

**Parameter**

<table id="table_B70F279A8CD240328520E5BD889806BD"> 
 <tbody> 
  <tr> 
   <td> <p> <b>Abfrageparameter</b> </p> </td> 
   <td> <p> <b>Wert</b> </p> </td> 
   <td> <p> <b>Beispiel</b> </p> </td> 
   <td> <p> <b>Betroffene Berichte</b> </p> </td> 
  </tr> 
  <tr> 
   <td> <p>bw </p> </td> 
   <td> <p>Eine positive Ganzzahl </p> </td> 
   <td> <p>1179 </p> </td> 
   <td> <p>„Datenverkehr“ &gt; „Technologie“ &gt; „Browserbreite“ </p> </td> 
  </tr> 
 </tbody> 
</table>
