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


# media.trackEvents

Die variable „“ gibt an, welche Ereignisse bei einem Medientreffer gesendet werden sollen.


<!-- 

media_trackEvents.xml

 -->

Dies gilt nur bei JavaScript und [!UICONTROL ActionSource].

| Maximale Größe | Debug-Parameter | Ausgefüllte Berichte | Standardwert |
|---|---|---|---|
| nicht angegeben | nicht angegeben | nicht angegeben | s.Media.trackEvents="None" |

**Syntax und mögliche Werte** {#section_66A978EF56914BEAAE73359A268A1B4A}

Ereignisnamen, wie „event1“ oder „purchase“.

**Beispiele** {#section_140A55D80EA24011954F9383CF312237}

```js
s.Media.trackEvents="event1,purchase"
```

**Probleme, Fragen und Tipps** {#section_030B11C64EE84D46A85CA550DB732D28}

Achten Sie darauf, dass in [!UICONTROL trackVars] der Wert „events“ steht, wenn diese Variable einen Wert hat.
