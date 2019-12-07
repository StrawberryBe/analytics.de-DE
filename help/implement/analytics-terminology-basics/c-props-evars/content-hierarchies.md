---
description: Inhaltshierarchien werden meist eingesetzt, um zu zeigen, welche verschiedenen Pfade Besucher von einer bestimmten Seite, Ebene usw. aus eingeschlagen haben.
keywords: Analytics Implementation;content hierachies;hier
title: Zählen von Inhaltshierarchien
topic: Developer and implementation
uuid: d41df92d-65fb-44de-bf46-8fac24303dad
translation-type: tm+mt
source-git-commit: 99ee24efaa517e8da700c67818c111c4aa90dc02

---


# Zählen von Inhaltshierarchien

Inhaltshierarchien werden meist eingesetzt, um zu zeigen, welche verschiedenen Pfade Besucher von einer bestimmten Seite, Ebene usw. aus eingeschlagen haben.

**Wie soll ich meine[!UICONTROL Inhaltshierarchie nachverfolgen]?**

Zuerst müssen Sie wissen, welche Anforderungen es hinsichtlich der Berichterstellung beim Nachverfolgen von [!UICONTROL Inhaltshierarchien] gibt. Wenn die Anforderungen für das Nachverfolgen der Hierarchie sehr detailliert sind, empfiehlt sich meist der Einsatz der Hierarchievariable ( *`hier`*). Bei Hierarchien ist für gewöhnlich eine strenge, vordefinierte Strukturierung erforderlich, bei der ein untergeordneter Knoten nur in den seltensten Fällen mehrere übergeordnete Knoten besitzt. Siehe folgendes Beispiel:

[!UICONTROL Globale Hierarchie]

„Alle Sites“ &gt; „Regionen“ &gt; „Länder“ &gt; „Sprache“ &gt; „Kategorie“

In diesem Beispiel wird die Hierarchie bis hinunter auf die Sprachenebene aufgeschlüsselt. Wenn eine Anforderung lautet, dass der gesamte „englische“ Datenverkehr in einem Bericht gemeldet werden soll, kann es zu Problemen kommen, wenn sowohl unter den USA als auch unter Großbritannien, Australien usw. eine Sprache namens „Englisch“ aufgeführt ist. Hierarchien können nur abwärts weiter aufgeschlüsselt werden. Best Practice für Analysen in horizontaler Richtung über mehrere Hierarchien hinweg ist der Einsatz einer [!UICONTROL benutzerspezifischen Traffic-Variablen] (Eigenschaftsvariablen).

Wenn Benutzer in der Lage sein sollen, sich in der Site weiter abwärts zu bewegen (ähnlich wie beim Durchsuchen einer Site) und Sie einen Bericht über [!UICONTROL Unique Visitors] auf den einzelnen Ebenen der Site haben möchten, empfiehlt sich die Verwendung der Hierarchievariablen.

In einigen Fällen ist die Verwendung von Props und der Variable *`hier`* sinnvoll. Nachfolgend ist aufgeführt, in welchen Fällen beide Variablentypen kombiniert werden können:

<table id="table_E960D100DA0F433A94A4B246D6EF0D0A"> 
 <thead> 
  <tr> 
   <th class="entry"> </th> 
   <th class="entry"> Props </th> 
   <th class="entry"> Hierarchie </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td> Korrelationen </td> 
   <td> <p><img  src="assets/check-mark.png" id="image_2832E346D220429DA643B908EC10260D" /> </p> </td> 
   <td> <p><img  src="assets/check-mark.png" id="image_2A70A61A78024204B6CEE4FFF9A0851E" /> </p> </td> 
  </tr> 
  <tr> 
   <td> Pathing </td> 
   <td> <p><img  src="assets/check-mark.png" id="image_EE5ED36AC75F4D648F54858D796F82BD" /> </p> </td> 
   <td> </td> 
  </tr> 
  <tr> 
   <td> Seitenansicht </td> 
   <td> <p><img  src="assets/check-mark.png" id="image_5BB82776D41642E78C2ECFD71DD33164" /> </p> </td> 
   <td> <p><img  src="assets/check-mark.png" id="image_18F34EE8957946AF9D6C2C9B492CEDB7" /> </p> </td> 
  </tr> 
  <tr> 
   <td> Unique Visitors </td> 
   <td> <p><img  src="assets/check-mark.png" id="image_A475267547B94DB4A1EEFD903B2CA1EB" /> </p> </td> 
   <td> <p><img  src="assets/check-mark.png" id="image_1E9E302D999146128CDBCE13E52BC38C" /> </p> </td> 
  </tr> 
  <tr> 
   <td> Classifications </td> 
   <td> <p><img  src="assets/check-mark.png" id="image_FC5FEFE7BA8C4475BA4F31D57302BE6B" /> </p> </td> 
   <td> </td> 
  </tr> 
 </tbody> 
</table>

