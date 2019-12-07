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



# javascriptVersion

Die Variable „“ gibt an, welche JavaScript-Version vom Browser unterstützt wird.


<!-- 

javascriptVersion.xml

 -->

Diese Variable erhält ihren Wert nach dem Seiten-Code und bevor *`doPlugins`* ausgeführt wird.

> [!NOTE] Diese Variable sollte nur gelesen und nie geschrieben werden.

Sie dürfen diese Werte lesen und in Eigenschaftsvariablen/eVars kopieren, jedoch nie ändern. Diese Variable wird mit der Version H.11 der JavaScript-Datei neu eingeführt.

| Abfrageparameter | Wert | Beispiel | Betroffene Berichte |
|---|---|---|---|
| j | 1.0, 1.1, 1.2, … 1.7 | 1.7 | Datenverkehr &gt; Technologie &gt; JavaScript Version |

Ab der Version H.10 der JavaScript-Datei werden Versionen bis zu 1.7 genau erkannt (welches die aktuellste Version zum Zeitpunkt der Veröffentlichung von H.10 war). Ältere Versionen der JavaScript-Datei konnten nur bis zu Version 1.3 erkennen.
