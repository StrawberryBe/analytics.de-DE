---
title: PWAs für Analytics
description: Progressive Web-Apps für Adobe Analytics
role: Business Practitioner, Administrator
exl-id: f28e0bfc-0e3e-4f28-9533-6788a36d37fe
translation-type: tm+mt
source-git-commit: 960274fde798287568ada9e6d8ec96783449dd99
workflow-type: tm+mt
source-wordcount: '291'
ht-degree: 88%

---

# PWAs für Adobe Analytics

Auf dieser Seite wird die Verwendung von Adobe Analytics mit progressiven Web-Apps (PWAs) beschrieben.

## Einführung

PWAs können eine native App-Erfahrung sowie Offline-Funktionen für eine Website bereitstellen. Normalerweise umfassen PWAs einen Service Worker, Lösungen zum Zwischenspeichern und eine Manifestdatei. Dies alles kann zu schnelleren Ladezeiten, einfacherer Navigation und responsiverem Verhalten beitragen.

Adobe Analytics funktioniert genauso nahtlos mit PWAs wie mit herkömmlichen Websites. Obwohl PWAs einige zusätzliche Anforderungen haben, um sich progressiv zu verhalten, sind sie im Hinblick auf die Datenerfassung und Berichterstellung durch Adobe Analytics mit den gleichen Hindernissen oder Einschränkungen wie herkömmliche Websites verbunden. Da Analytics bereits Offline-Tracking-Funktionen enthält, können Sie mit PWAs diese integrierte Funktion einfacher als mit herkömmlichen Websites nutzen.

## PWA-Analytics-Daten abrufen

Zur Erfassung und Analyse Ihrer PWA-Daten mit [!UICONTROL Analytics] müssen Sie keine Konfigurationsänderungen vornehmen. [!UICONTROL Analytics] bietet automatisch die gleichen Funktionen und Merkmale wie bei einer herkömmlichen Website.

## Offline-Tracking zur Erhöhung der PWA-Effektivität hinzufügen

Sie können die Effektivität Ihrer PWA steigern, indem Sie die Adobe Analytics-Funktionen für [Offline-Tracking](/help/implement/vars/config-vars/trackoffline.md) verwenden. Standardmäßig ist diese Funktion deaktiviert. Sie können der Datei AppMeasurement.js jedoch die folgende Eigenschaft hinzufügen, um sie zu aktivieren: `s.trackOffline=true;`.

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

Weitere Informationen zum Bearbeiten der Datei AppMeasurement.js finden Sie unter [Kern-AppMeasurement-Code einfügen](/help/implement/other/dtm/c-aa-tool/t-appmeasurement-code.md).

Weitere Informationen zum Konfigurieren der Datei AppMeasurement.js finden Sie unter [Übersicht über Konfigurationsvariablen](/help/implement/vars/config-vars/configuration-variables.md) und die einzelnen variablenspezifischen Seiten im selben Unterkapitel.

Weitere Informationen zu den Eigenschaften der Datei AppMeasurement.js finden Sie in der [Übersicht über die Javascript-Implementierung](/help/implement/js/overview.md).
