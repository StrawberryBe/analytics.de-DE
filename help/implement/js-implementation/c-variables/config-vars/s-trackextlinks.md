---
description: Mit dynamischen Variablen können Sie Werte von einer Variablen in eine andere kopieren, ohne die vollständigen Werte mehrfach in die Bildanforderung auf Ihrer Site eingeben zu müssen.
keywords: Analytics-Implementierung
seo-description: Mit dynamischen Variablen können Sie Werte von einer Variablen in eine andere kopieren, ohne die vollständigen Werte mehrfach in die Bildanforderung auf Ihrer Site eingeben zu müssen.
solution: null
title: Dynamische Variablen
translation-type: tm+mt
source-git-commit: 8c06a54ccd652f3f915af3af040e9cc69f01d0c1

---


# s.trackExternalLinks

Wenn „“ auf „true“ eingestellt ist, wird über „“ und „“ bestimmt, ob ein angeklickter Link ein Exitlink ist.

| Maximale Größe | Debug-Parameter | Ausgefüllte Berichte | Standardwert |
|---|---|---|---|
| Keine | Keine | Keine | True |

Die Variable *`trackExternalLinks`* ist nur dann auf „false“ zu setzen, wenn Ihre Site keine Exitlinks enthält oder wenn Sie nicht daran interessiert sind, dass die Anzahl der Klicks auf Exitlinks verfolgt wird. Jeder Link, der einen Besucher weg von Ihrer Site führt, gilt als Exitlink. Wenn *`trackExternalLinks`* auf „true“ eingestellt ist, werden bei jedem Klick auf einen Exitlink unverzüglich Trackingdaten gesendet. Dazu gehören die URL des Exitlinks, der Linkname und Daten zur Benutzerklickzuordnung für den Link. Wenn *`trackExternalLinks`* auf „false“ eingestellt ist, sind die Daten zur Besucherklickzuordnung für Exitlinks, die zu herunterladbaren Dateien gehören, wahrscheinlich in Berichten enthalten.

## Syntax und mögliche Werte

Die Variable *`trackExternalLinks`* kann entweder „true“ oder „false“ sein.

```
js
s.trackExternalLinks=true|false
```

## Beispiele

```
js
s.trackExternalLinks=true 
```

```
js
s.trackExternalLinks=false
```

## Konfigurationseinstellungen

Keine

## Probleme, Fragen und Tipps

* Wenn *`trackExternalLinks`* auf „false“ gesetzt ist, sind Links, über die Besucher Ihre Site verlassen, in Berichten zur Besucherklickzuordnung wahrscheinlich enthalten.

* Wenn *`trackExternalLinks`* „true“ ist, werden die Daten bei jedem Klick auf einen Exitlink (bevor das Linkziel geladen wird) gesendet.

## Automatische Verfolgung von Exitlinks und Dateidownloads

Die JavaScript-Datei kann auf der Grundlage entsprechender Definitionsparameter für die automatische Verfolgung von Dateidownloads und Exitlinks konfiguriert werden.

Die Parameter zur Kontrolle der automatischen Verfolgung lauten wie folgt:

```
s.trackDownloadLinks=true 
s.trackExternalLinks=true 
s.linkDownloadFileTypes="exe,zip,wav,mp3,mov,mpg,avi,doc,pdf,xls" 
s.linkInternalFilters="javascript:,mysite.com,[more filters here]" 
s.linkLeaveQueryString=false 
```

Die Parameter `trackDownloadLinks` and `trackExternalLinks` determine if automatic file download and exit link tracking are enabled. Wenn diese Option aktiviert ist, wird jeder Link mit einem Dateityp, der mit einem der Werte in übereinstimmt, automatisch als Dateidownload verfolgt. `linkDownloadFileTypes` Jeder Link mit einer URL, der keinen der Werte in enthält, `linkInternalFilters` wird automatisch als Ausstiegslink verfolgt.

In JavaScript H.25.4 (released February 2013), automatic exit link tracking was updated to always ignore links with `HREF` attributes that start with `#`, `about:`, or `javascript:`.

### Beispiel 1

Die Dateitypen `.jpg` und `.aspx` sind in `linkDownloadFileTypes` oben nicht enthalten, daher werden keine Klicks auf sie automatisch verfolgt und als Datei-Downloads gemeldet.

The parameter `linkLeaveQueryString` modifies the logic used to determine exit links. When `linkLeaveQueryString`=false, exit links are determined using only the domain, path, and file portion of the link URL. When `linkLeaveQueryString`=true, the query string portion of the link URL is also used to determine an exit link.

### Beispiel 2

Mit den folgenden Einstellungen wird das unten stehende Beispiel als Exitlink gezählt:

```
//JS file  
s.linkInternalFilters="javascript:,mysite.com" 
s.linkLeaveQueryString=false 
 
//HTML file 
<a href='https://othersite.com/index.html?r=mysite.com'>Visit Other Site!</a> 
```

### Beispiel 3

Mit den folgenden Einstellungen wird der unten angegebene Link nicht als Exitlink gezählt:

```
//JS file  
s.linkInternalFilters="javascript:,mysite.com" 
s.linkLeaveQueryString=true 
 
//HTML  
<a href='https://othersite.com/index.html?r=mysite.com'>Visit Other Site</a> 
```

*Hinweis: Ein einzelner Link kann nur als Dateidownload oder Exitlink verfolgt werden, wobei der Dateidownload die Priorität hat. Wenn es sich bei einem Link sowohl um einen Ausstiegslink als auch um einen Dateidownload handelt, der auf den Parametern basiert,`linkDownloadFileTypes`und`linkInternalFilters`er wird als Datei-Download und nicht als Ausstiegslink verfolgt und berichtet.*