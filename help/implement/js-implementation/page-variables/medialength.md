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


# mediaLength

Die Variable gibt die Gesamtlänge des Mediums an, das abgespielt wird.


<!-- 

mediaLength.xml

 -->

<table id="table_B1AE8A9DF9D545C2965CDB2DB6C2969B"> 
 <thead> 
  <tr> 
   <th class="entry"> Maximale Größe </th> 
   <th class="entry"> Debug-Parameter </th> 
   <th class="entry"> Ausgefüllte Berichte </th> 
   <th class="entry"> Standardwert </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td> Für die gesamte pev3-Anforderung gibt es keine Größenbeschränkung – stattdessen gilt die Längenbeschränkung des jeweiligen Browsers für URLs. </td> 
   <td> pev3 </td> 
   <td> Besuchszeit für Video; <p>Angezeigte Videosegmente </p> </td> 
   <td> Keine </td> 
  </tr> 
 </tbody> 
</table>

**Syntax und mögliche Werte** {#section_FEC1B01FDD234ACEB63C0558BEEB5CBC}

**Bei Einsatz von autoTrack:**

Bei Verwendung von [!UICONTROL s.Media.autoTrack] muss die Variable [!UICONTROL mediaLength] nicht explizit implementiert werden. Sie wird vom AppMeasurement für JavaScript-Code automatisch ermittelt.

**Manuelle Verfolgung:**

Syntax:

```js
s.Media.open(mediaName,mediaLength,mediaPlayerName)
```

Mögliche Werte:

```js
s.Media.open("de_bofr_1045Making_400k", "414","Windows Media Player 11.0.5721.5230")
```

**Beispiele** {#section_048B2D31BB584647A5D335AE94E5A599}

```js
s.Media.open("de_bofr_1045Making_400k", "414","Windows Media Player 11.0.5721.5230")
```

```js
Resulting pev3 parameter syntax: pev3= [Asset Name]--**--[Total length of asset]--**--[Player name]--**--[Total seconds consumed]--**--[Timestamp]--**--[Chronological record of all starts and stops along with accompanying markers]  
  
```

```js
Possible pev3 values: pev3=de_bofr_1045Making_400k--**--414--**--Windows Media Player 11.0.5721.5230--**--288--**--1207893838--**--S0E0S0E256S0E32
```

**Probleme, Fragen und Tipps** {#section_1CEDC78FEF4940E9BC02A2AF1EE2FB01}

* Sie müssen die Methoden für die Medienverfolgung nur dann aufrufen, wenn der Player nicht mittels „[!UICONTROL s.Media.autoTrack] = true“ verfolgt werden kann.
* Beim Verfolgen von Medien ohne den Einsatz von [!UICONTROL autoTrack] müssen Sie daran denken, die Länge in Sekunden festzulegen.

