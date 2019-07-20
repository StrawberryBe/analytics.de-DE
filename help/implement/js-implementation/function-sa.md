---
description: Mithilfe der s.sa()-Funktion können Sie jederzeit eine Report Suite auf der Seite dynamisch ändern, bevor oder nachdem eine Bildanforderung veranlasst wird.
keywords: Analytics-Implementierung
seo-description: Mithilfe der "s.sa()"-Funktion können Sie jederzeit eine Report Suite auf der Seite dynamisch ändern, bevor oder nachdem eine Bildanforderung veranlasst wird.
seo-title: Die "s.sa()"-Funktion
solution: Analytics
subtopic: Funktionen
title: Die s.sa()-Funktion
topic: Entwickler und Implementierung
uuid: a 6 aacd 10-2 a 5 b -448 b-b 3 b 7-bed 5590 b 71 d 4
translation-type: tm+mt
source-git-commit: 86fe1b3650100a05e52fb2102134fee515c871b1

---


# Die s.sa()-Funktion

Mithilfe der s.sa()-Funktion können Sie jederzeit eine Report Suite auf der Seite dynamisch ändern, bevor oder nachdem eine Bildanforderung veranlasst wird.

Wenn Ihre Organisation Daten ohne Seitenneuladung an unterschiedliche Report Suites senden möchte, empfiehlt sich diese Funktion unbedingt.

Diese Informationen sind für fortgeschrittene Benutzer gedacht, die sowohl mit der Berichterstellung als auch der Implementierung gut vertraut sind. Änderungen sollten Sie an Ihrer Implementierung nur dann vornehmen, wenn Sie genau wissen, welche Folgen dies hat. Falls Implementierungsänderungen erforderlich sind, wenden Sie sich an den Account-Manager Ihres Unternehmens.

## Eigenschaften der Funktion  {#section_E10CB41A0CF749F4A24C8377958E3671}

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

