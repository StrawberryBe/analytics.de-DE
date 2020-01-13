---
description: Mit dynamischen Variablen können Sie Werte von einer Variablen in eine andere kopieren, ohne die vollständigen Werte mehrfach in die Bildanforderung auf Ihrer Site eingeben zu müssen.
keywords: Analytics Implementation
solution: null
title: Dynamische Variablen
translation-type: ht
source-git-commit: f1ebe5e89f62957c8bcc829be4b1a97463210f93

---


# s.trackExternalLinks

Wenn „“ auf „true“ eingestellt ist, wird über „“ und „“ bestimmt, ob ein angeklickter Link ein Exitlink ist.

| Maximale Größe | Debug-Parameter | Ausgefüllte Berichte | Standardwert |
|---|---|---|---|
| nicht angegeben | nicht angegeben | nicht angegeben | True |

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

Die Parameter `trackDownloadLinks` und `trackExternalLinks` bestimmen, ob ein automatischer Dateidownload und Exitlinktracking aktiviert sind. Wenn diese Option aktiviert ist, wird jeder Link mit einem Dateityp, der mit einem der Werte unter `linkDownloadFileTypes` übereinstimmt, automatisch als Dateidownload verfolgt. Jeder Link mit einer URL ohne die Werte unter `linkInternalFilters` wird automatisch als Exitlink verfolgt.

In H.25.4 (im Februar 2013 veröffentlicht) wurde das automatische Exitlinktracking so geändert, dass Links mit `HREF`-Attributen, die mit `#`, `about:` oder `javascript:` beginnen, stets ignoriert werden.

### Beispiel 1

Die Dateitypen `.jpg` und `.aspx` sind unter `linkDownloadFileTypes` oben nicht enthalten, daher werden keine Klicks auf sie automatisch verfolgt und als Dateidownloads berichtet.

Der Parameter `linkLeaveQueryString` verändert die Logik zur Bestimmung von Exitlinks. Wenn `linkLeaveQueryString` den Wert „false“ hat, werden Exitlinks nur anhand von Domäne, Pfad und Dateiteil der Link-URL ermittelt. Wenn `linkLeaveQueryString` den Wert „true“ hat, wird auch der Teil der Link-URL mit der Abfragezeichenfolge zur Ermittlung eines Exitlinks verwendet.

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

*Hinweis: Ein einzelner Link kann nur als Dateidownload oder Exitlink verfolgt werden, wobei der Dateidownload Priorität hat. Wenn es sich bei einem Link sowohl um einen Exitlink als auch um einen Dateidownload handelt, der auf den Parametern`linkDownloadFileTypes`und`linkInternalFilters`basiert, wird er als Dateidownload und nicht als Exitlink verfolgt und berichtet.*