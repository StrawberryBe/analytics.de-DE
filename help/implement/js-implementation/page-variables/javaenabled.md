---
description: Seitenvariablen werden direkt in Berichten ausgefüllt, z. B. pageName, List Props, List Variables usw.
keywords: Analytics Implementation
solution: Analytics
subtopic: Variables
title: Seitenvariablen
topic: null
uuid: null
translation-type: tm+mt
source-git-commit: 45642bdbe18627caa20b1def6443f1e596a41f52

---



# javaEnabled

Die Variable „“ zeigt an, ob im Browser Java aktiviert ist.

<!-- 

javaEnabled.xml

 -->

Diese Variable erhält ihren Wert nach dem Seiten-Code und bevor „doPlugins“ ausgeführt wird.

> [!NOTE] Diese Variable sollte nur gelesen und nie geschrieben werden.

Sie dürfen diese Werte lesen und in Eigenschaftsvariablen/eVars kopieren, jedoch nie ändern. Diese Variable wird mit der Version H.11 der JavaScript-Datei neu eingeführt.

| Abfrageparameter | Wert | Beispiel | Betroffene Berichte |
|---|---|---|---|
| v | J oder N | Y | Datenverkehr &gt; Technologie &gt; Java |
