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


# mediaSession

Diese Variable gibt an, welche Segmente eines Video- oder Medienelements abgespielt wurden.


<!-- 

mediaSession.xml

 -->

<table id="table_8681473270FE44DFBBCCC0FBA6737104"> 
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
   <td> 255 Byte </td> 
   <td> pev3 </td> 
   <td> Besuchszeit für Video <p>Angezeigte Videosegmente </p> </td> 
   <td> Keine </td> 
  </tr> 
 </tbody> 
</table>

**Syntax und mögliche Werte** {#section_9A63266633C4427CB4A6549E4D887B85}

**Bei Einsatz von autoTrack:**

Bei Verwendung von [!UICONTROL s.Media.autoTrack] muss die *`mediaName`*-Variable nicht explizit implementiert werden. Sie wird vom AppMeasurement für JavaScript-Code automatisch ermittelt.

**Manuelle Verfolgung:**

Syntax:

```js
s.Media.open(mediaName,mediaLength,mediaPlayerName) 
```

```js
s.Media.play(mediaName,mediaOffset)
```

```js
s.Media.stop(mediaName,mediaOffset)
```

Mögliche Werte:

```js
s.Media.open("de_bofr_1045Making_400k", "414","Windows Media Player 11.0.5721.5230") 
```

```js
s.Media.play("de_bofr_1045Making_400k", "0")
```

```js
s.Media.play("de_bofr_1045Making_400k", "414")
```

**Beispiele** {#section_3446EC37E017407FA3F43C9BDAEA0B85}

```js
s.Media.open("de_bofr_1045Making_400k", "414","Windows Media Player 11.0.5721.5230") 
```

```js
s.Media.play("de_bofr_1045Making_400k", "0")
```

```js
s.Media.play("de_bofr_1045Making_400k", "414")
```

```js
Resulting pev3 parameter syntax: pev3=[Asset Name]--**--[Total length of asset]--**--[Player name]--**--[Total seconds consumed]--**--[Timestamp]--**--[Chronological record of all starts and stops along with accompanying markers]
```

```js
Possible pev3 Values: pev3=de_bofr_1045Making_400k--**--414--**--Windows Media Player 11.0.5721.5230--**--288--**--1207893838--**--S0E0S0E256S0E32 
```

**Probleme, Fragen und Tipps** {#section_1BCEB037AB724B6EBE87420BD3604B88}

Sie müssen die Methoden für die Medienverfolgung nur dann aufrufen, wenn der Player nicht mittels „[!UICONTROL s.Media.autoTrack] = true“ verfolgt werden kann.
