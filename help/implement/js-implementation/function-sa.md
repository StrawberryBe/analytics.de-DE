---
description: Mithilfe der s.sa()-Funktion können Sie jederzeit eine Report Suite auf der Seite dynamisch ändern, bevor oder nachdem eine Bildanforderung veranlasst wird.
keywords: Analytics Implementation
subtopic: Functions
title: Die s.sa()-Funktion
topic: Developer and implementation
uuid: a6aacd10-2a5b-448b-b3b7-bed5590b71d4
translation-type: tm+mt
source-git-commit: 99ee24efaa517e8da700c67818c111c4aa90dc02

---


# Die s.sa()-Funktion

Mithilfe der s.sa()-Funktion können Sie jederzeit eine Report Suite auf der Seite dynamisch ändern, bevor oder nachdem eine Bildanforderung veranlasst wird.

Wenn Ihre Organisation Daten ohne Seitenneuladung an unterschiedliche Report Suites senden möchte, empfiehlt sich diese Funktion unbedingt.

Diese Informationen sind für fortgeschrittene Benutzer gedacht, die sowohl mit der Berichterstellung als auch der Implementierung gut vertraut sind. Änderungen sollten Sie an Ihrer Implementierung nur dann vornehmen, wenn Sie genau wissen, welche Folgen dies hat. Falls Implementierungsänderungen erforderlich sind, wenden Sie sich an den Account-Manager Ihres Unternehmens.

## Eigenschaften der Funktion {#section_E10CB41A0CF749F4A24C8377958E3671}

Beim Festlegen dieser Funktion können alle bereits definierten Variablen in einer anderen Report Suite verwendet werden.

## Implementierungsbeispiele {#section_14B0B8C853244D5F82B08B995773640C}

Senden von Videodaten zu einer Report Suite, wobei die restlichen Daten zu einer anderen Report Suite gesendet werden:

```js
// Set in the core JS file by default 
var s=s_gi('prodrsid'); 
 
// Define this when a user interacts with a video 
s.sa('videorsid'); 
s.t(); // Sends an image request
```

Verwenden von s.sa() und Multi-Suite-Tagging:

```js
// Set in the core JS file by default 
var s=s_gi('rsid1'); 
 
// Call the function when you wish to change report suites 
s.sa('rsid1,rsid2'); 
s.t();
```

