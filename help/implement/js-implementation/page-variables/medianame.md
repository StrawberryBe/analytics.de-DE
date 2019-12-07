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


# mediaName

Diese Variable gibt den Namen des Video- oder Medienelements an.


<!-- 

mediaName.xml

 -->

Sie ist nur über die [!UICONTROL Dateneinfüge-API] und [!UICONTROL Vollständige Verarbeitung von Datenquelle] verfügbar.

| Maximale Größe | Debug-Parameter | Ausgefüllte Berichte | Standardwert |
|---|---|---|---|
| 64 KB | pev3 | Videos, Nächster Videofluss, Vorheriger Videofluss, Angezeigte Videosegmente, Besuchszeit für Video | Keine |

**Syntax und mögliche Werte** {#section_F97A2253BBD24FEBBC225F233A319F5D}

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

```js
s.Media.close(mediaName)
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

```js
s.Media.close("de_bofr_1045Making_400k")
```

**Beispiele** {#section_4B9584265B1A47289818141B2A88021D}

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
s.Media.close("de_bofr_1045Making_400k")
```

```js
Resulting pev3 parameter syntax: pev3=[Asset Name]--**--[Total length of asset]--**--[Player name]--**--[Total seconds consumed]--**--[Timestamp]--**--[Chronological record of all starts and stops along with accompanying markers]  
  
```

```js
Possible pev3 Values: 
  pev3=de_bofr_1045Making_400k--**--414--**--Windows Media Player 
  11.0.5721.5230--**--288--**--1207893838--**--S0E0S0E256S0E32  
  
```

**Probleme, Fragen und Tipps** {#section_941A445BB52E4063B0F6920E61BB90DE}

* Sie müssen die Methoden für die Medienverfolgung nur dann aufrufen, wenn der Player nicht mittels „[!UICONTROL s.Media.autoTrack] = true“ verfolgt werden kann.
* Diese Variable wird als mySQL TEXT-Variable im Gegensatz zu VARCHAR(100) gespeichert.
