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


# colorDepth

In der Variablen „“ ist angegeben, mit wie vielen Bit die Farbe jedes Pixels dargestellt wird.


<!-- 

colordepth.xml

 -->

So würde zum Beispiel der Wert 32 bedeuten, dass die Farbtiefe des Bildschirms 32 Bit beträgt. Diese Variable erhält ihren Wert nach dem Seiten-Code und bevor *`doPlugins`* ausgeführt wird.

> [!NOTE] Diese Variable sollte nur gelesen und nie geschrieben werden.

Sie dürfen diese Werte lesen und in `props/eVars` kopieren, jedoch nie ändern. Diese Variable wird mit der Version H.11 der JavaScript-Datei neu eingeführt.

| Abfrageparameter | Wert | Beispiel | Betroffene Berichte |
|---|---|---|---|
| c | 8,16 und 32 | 32 | „Datenverkehr“ &gt; „Technologie“ &gt; „Bildschirmfarbtiefe“ |
