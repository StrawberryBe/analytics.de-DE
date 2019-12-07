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


# plugins

Die im Browser installierten werden bei Netscape- und Mozilla-basierten Browsern in der „plugins“-Variablen aufgelistet.


<!-- 

plugins.xml

 -->

Diese Variable erhält ihren Wert nach dem Seiten-Code und bevor *`doPlugins`* ausgeführt wird.

> [!NOTE] Diese Variable sollte nur gelesen und nie geschrieben werden.

Sie dürfen diese Werte lesen und in Eigenschaftsvariablen/eVars kopieren, jedoch nie ändern. Diese Variable wird mit der Version H.11 der JavaScript-Datei neu eingeführt.

| Abfrageparameter | Wert | Beispiel | Betroffene Berichte |
|---|---|---|---|
| p | Erkannte Plug-ins | IE Tab-Plug-in, QuickTime-Plug-in 7.1.6, Mozilla-Standard-Plug-in, iTunes Application Detector, Adobe Acrobat, ActiveTouch General Plugin Container, Shockwave Flash, Microsoft Office 2003, Java(TM) Platform SE 6 U1, Windows Media Player-Plug-in Dynamic Link Library, Microsoft® DRM, | Datenverkehr &gt; Technologie &gt; Plugins |
