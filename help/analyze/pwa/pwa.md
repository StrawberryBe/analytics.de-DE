---
title: PWAs für Analytics
description: Progressive Web-Apps für Adobe Analytics
translation-type: tm+mt
source-git-commit: b36505c9fd7bf1d2da4d076d6b49298f01ad1cfc

---


# PWAs für Analytics

Auf dieser Seite wird die Verwendung von Adobe Analytics mit progressiven Web-Apps (PWAs) beschrieben.

## Einführung

PWAs können eine native App-Erfahrung sowie Offline-Funktionen für eine Website bereitstellen. Normalerweise umfassen PWAs einen Service Worker, Lösungen zum Zwischenspeichern und eine Manifestdatei. Dies alles kann zu schnelleren Ladezeiten, einfacherer Navigation und responsiverem Verhalten beitragen.

Adobe Analytics funktioniert genauso nahtlos mit PWAs wie mit herkömmlichen Websites. Obwohl PWAs einige zusätzliche Anforderungen haben, um sich progressiv zu verhalten, sind sie im Hinblick auf die Datenerfassung und Berichterstellung durch Adobe Analytics mit den gleichen Hindernissen oder Einschränkungen wie herkömmliche Websites verbunden. Da Analytics bereits Offline-Verfolgungsfunktionen enthält, können PWAs Sie bei der Nutzung dieser integrierten Funktion einfacher unterstützen als bei herkömmlichen Websites.

## PWA-Analysedaten abrufen

Zur Erfassung und Analyse Ihrer PWA-Daten mit Analytics müssen Sie keine Konfigurationsänderungen vornehmen. Analytics bietet automatisch die gleichen Funktionen und Merkmale wie bei einer herkömmlichen Website.

## Offline-Tracking zur Erhöhung der PWA-Effektivität hinzufügen

Sie können die Effektivität Ihrer PWA steigern, indem Sie die Analytics-Funktionen für [Offline-Tracking](https://docs.adobe.com/content/help/de-DE/analytics/implementation/vars/functions/forceoffline.translate.html) verwenden. Standardmäßig ist diese Funktion deaktiviert. Sie können der Datei AppMeasurement.js jedoch die folgende Eigenschaft hinzufügen, um sie zu aktivieren: `s.trackOffline=true;`.

In der folgenden Datei AppMeasurement.js wurde die Eigenschaft beispielsweise am Ende des Abschnitts `CONFIG SECTION` hinzugefügt:

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

Weitere Informationen zum Bearbeiten der Datei AppMeasurement.js finden Sie unter [Einfügen von Code in die Datei AppMeasurement.js](https://docs.adobe.com/content/help/de-DE/analytics/implementation/other/dtm/analytics-tool/t-appmeasurement-code.translate.html).

Beispiele für Konfigurationen in der Datei AppMeasurement.js finden Sie unter [Konfigurieren der Datei AppMeasurement.js](https://docs.adobe.com/content/help/de-DE/analytics/implementation/js/overview.translate.html#section_042412C29CC249E298F19B2BC2F43CE7).

Weitere Informationen zu den Eigenschaften der Datei AppMeasurement.js finden Sie in der [Übersicht über die Javascript-Implementierung](https://docs.adobe.com/content/help/de-DE/analytics/implementation/js/migrate-from-hcode.translate.html).
