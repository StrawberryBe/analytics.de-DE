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


# mediaPlayer

Diese Variable gibt an, mit welchem Player ein Video- oder Medienelement wiedergegeben wird.


<!-- 

mediaPlayer.xml

 -->

| Maximale Größe | Debug-Parameter | Ausgefüllte Berichte | Standardwert |
|---|---|---|---|
| 100 Byte | pev3 | Video-Player | Keine |

**Syntax und mögliche Werte** {#section_EAA55A3A45B5405F903E3BE6ACAB143F}

**Bei Einsatz von autoTrack:**

```js
s.Media.playerName = "My Custom Player Name"  //configure player name in global JavaScript or ActionSource
```

**Manuelle Verfolgung:**

```js
s.Media.open(mediaName,mediaLength,mediaPlayerName)
```

Mögliche Werte:

```js
s.Media.open("de_bofr_1045Making_400k", "414","Windows Media Player 11.0.5721.5230")
```

**Beispiele** {#section_64967E1333D542CCB6CF62F0A1E0EF88}

```js
s.Media.open("de_bofr_1045Making_400k", "414","Windows Media Player 11.0.5721.5230")
```

```js
Resulting pev3 parameter syntax: pev3=[Asset Name]--**--[Total length of asset]--**--[Player name]--**--[Total seconds consumed]--**--[Timestamp]--**--[Chronological record of all starts and stops along with accompanying markers] 
```

```js
Possible pev3 Values: pev3=de_bofr_1045Making_400k--**--414--**--Windows Media Player 11.0.5721.5230--**--288--**--1207893838--**--S0E0S0E256S0E32
```

**Probleme, Fragen und Tipps** {#section_0020E031338F4A4880B9AC5B9A85BEF5}

Sie müssen die Methoden für die Medienverfolgung nur dann aufrufen, wenn der Player nicht mittels „s.Media.autoTrack = true“ verfolgt werden kann.

