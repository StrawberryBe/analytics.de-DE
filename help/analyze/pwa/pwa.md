---
title: PWAs für Analytics
description: Progressive Web-Apps für Adobe Analytics
translation-type: tm+mt
source-git-commit: b36505c9fd7bf1d2da4d076d6b49298f01ad1cfc

---


# PWAs für Analytics

Auf dieser Seite wird die Verwendung von Adobe Analytics mit progressiven Web-Apps (PWAs) beschrieben.

## Einführung

PWAs können eine native App-Erfahrung sowie Offline-Funktionen für eine Website bereitstellen. In der Regel enthalten PWAs einen Servicearbeiter, Cachebedingungen und eine Manifestdatei, die alle bei schnelleren Ladezeiten, einfacherer Navigation und reaktionsfähigem Verhalten helfen können.

Adobe Analytics funktioniert genauso nahtlos mit PWAs wie mit herkömmlichen Websites. Obwohl PWAs einige weitere Anforderungen haben, sich progressiv in sich selbst zu verhalten, schaffen sie keine Hindernisse oder Beschränkungen dafür, wie Analytics Daten von ihnen erfasst oder meldet, anders als herkömmliche Websites. Da Analytics bereits Offline-Verfolgungsfunktionen enthält, können PWAs Sie bei der Nutzung dieser integrierten Funktion einfacher unterstützen als bei herkömmlichen Websites.

## PWA-Analysedaten abrufen

Zur Erfassung und Analyse Ihrer PWA-Daten mit Analytics müssen Sie keine Konfigurationsänderungen vornehmen. Analytics bietet automatisch alle gleichen Funktionen und Funktionen wie bei einer herkömmlichen Website.

## Hinzufügen Offline-Verfolgung zur Erhöhung der PWA-Effektivität

Sie können die Effektivität Ihrer PWA steigern, indem Sie damit Analytics- [Offline-Verfolgungsfunktionen](https://docs.adobe.com/content/help/en/analytics/implementation/javascript-implementation/offline-tracking.html) verwenden. Standardmäßig ist diese Funktion deaktiviert. Sie können der Datei AppMeasurement.js jedoch die folgende Eigenschaft hinzufügen, um sie zu aktivieren: `s.trackOffline=true;`.

In der folgenden Datei AppMeasurement.js wird die Eigenschaft beispielsweise am Ende des `CONFIG SECTION`Berichts hinzugefügt:

```
/************************** CONFIG SECTION **************************/ 
/* You may add or alter any code config here. */ 
/* Link Tracking Config */ 
s.trackDownloadLinks=true 
s.trackExternalLinks=true 
s.trackInlineStats=true 
s.linkDownloadFileTypes="exe,zip,wav,mp3,mov,mpg,avi,wmv,pdf,doc,docx,xls,xlsx,ppt,pptx" 
s.linkInternalFilters="javascript:" //optional: add your internal domain here 
s.linkLeaveQueryString=false 
s.linkTrackVars="None" 
s.linkTrackEvents="None" 
s.trackOffline=true
*** 
```

Weitere Informationen zum Bearbeiten der Datei „AppMeasurement.js“ finden Sie unter [Einfügen von Code in die Datei „AppMeasurement.js“](https://docs.adobe.com/content/help/en/analytics/implementation/implement-analytics-with-dtm/analytics-tool/t-appmeasurement-code.html).

Beispiele für Konfigurationen in der Datei AppMeasurement.js finden Sie unter [Konfigurieren der Datei](https://docs.adobe.com/content/help/en/analytics/implementation/javascript-implementation/appmeasure-mjs-pagecode.html#section_042412C29CC249E298F19B2BC2F43CE7)AppMeasurement.js.

Weitere Informationen zu den Eigenschaften der Datei AppMeasurement.js finden Sie in der Übersicht über die [JavaScript-Implementierung](https://docs.adobe.com/content/help/en/analytics/implementation/javascript-implementation/appmeasurement-js/appmeasure-mjs.html).
