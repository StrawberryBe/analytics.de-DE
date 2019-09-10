---
title: Pwar für Analytics
seo-title: Pwar für Analytics
description: Progressive Web-Apps für Adobe Analytics
seo-description: Pwar mit Analytics verwenden
translation-type: tm+mt
source-git-commit: f64e5d9977bebd0e9db4af0f7118e9e64978c1c7

---


# Pwar für Analytics

In diesem Handbuch wird beschrieben, wie Sie Adobe Analytics mit progressiven Web-Apps (pwas) verwenden.

## Einführung

Pwar kann eine native App sowie Offline-Funktionen für eine Website bereitstellen. Normalerweise enthalten pwar einen Dienstmitarbeiter, Caching-Regeln und eine Manifestdatei, die für schnellere Ladezeiten, einfachere Navigation und reaktionsfähiges Verhalten hilfreich sein kann.

Adobe Analytics funktioniert genauso nahtlos wie bei herkömmlichen Websites. Pb hat zwar einige Anforderungen, um sich progressiv und selbst zu verhalten, aber es entstehen keine Einschränkungen oder Einschränkungen für die Art und Weise, wie Analytics Daten von ihnen unterscheidet, und zwar anders als herkömmliche Websites. Da Analytics bereits Offline-Verfolgungsfunktionen enthält, kann pwar Ihnen dabei helfen, diese integrierte Funktion leichter zu nutzen als mit herkömmlichen Websites.

## Abrufen der PWA Analytics-Daten

Zur Erfassung und Analyse Ihrer PWA-Daten mit Analytics müssen Sie keine Konfigurationsänderungen vornehmen. Analytics bietet automatisch alle gleichen Funktionen und Funktionen wie bei herkömmlichen Websites.

## Fügen Sie Offline-Verfolgung hinzu, um die PWA-Effektivität zu erhöhen.

Mit der [Offline-Verfolgung von Analytics können Sie die Effektivität Ihrer PWA](https://docs.adobe.com/content/help/en/analytics/implementation/javascript-implementation/offline-tracking.html) verbessern. Standardmäßig ist diese Funktion deaktiviert, aber Sie können die folgende Eigenschaft zur Datei appmeasurement. js hinzufügen, um sie zu aktivieren: `s.trackOffline=true;`.

In der folgenden Datei appmeasurement. js wird die Eigenschaft beispielsweise am Ende der folgenden `CONFIG SECTION`Datei hinzugefügt:

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


Weitere Informationen zum Bearbeiten der Datei appmeasurement. js finden Sie unter [Einfügen von Code in die Datei appmeasurement. js](https://docs.adobe.com/content/help/en/analytics/implementation/implement-analytics-with-dtm/analytics-tool/t-appmeasurement-code.html).

Beispiele für Konfigurationen in der Datei appmeasurement. js finden Sie unter [Appmeasurement. js-Datei](https://docs.adobe.com/content/help/en/analytics/implementation/javascript-implementation/appmeasure-mjs-pagecode.html#section_042412C29CC249E298F19B2BC2F43CE7)konfigurieren.

Weitere Informationen zu den Merkmalen der Datei appmeasurement. js finden Sie in der Übersicht über [die Javascript-Implementierung](https://docs.adobe.com/content/help/en/analytics/implementation/javascript-implementation/appmeasurement-js/appmeasure-mjs.html).
