---
description: Mit dynamischen Variablen können Sie Werte von einer Variablen in eine andere kopieren, ohne die vollständigen Werte mehrfach in die Bildanforderung auf Ihrer Site eingeben zu müssen.
keywords: Analytics Implementation
solution: null
title: Dynamische Variablen
translation-type: ht
source-git-commit: f1ebe5e89f62957c8bcc829be4b1a97463210f93

---


# s.trackDownLoadLinks

Legen Sie „“ auf „true“ fest, wenn Sie Links für herunterladbare Dateien auf Ihrer Site verfolgen möchten.

Wenn „True“ für *`trackDownloadLinks`* angegeben ist, wird *`linkDownloadFileTypes`* verwendet, um zu bestimmen, welche Links herunterladbare Dateien sind.

| Maximale Größe | Debug-Parameter | Ausgefüllte Berichte | Standardwert |
|---|---|---|---|
| nicht angegeben | nicht angegeben | nicht angegeben | True |

Die Variable *`trackDownloadLinks`* ist nur dann auf „false“ zu setzen, wenn die Site keine herunterladbaren Dateien enthält oder wenn Sie nicht daran interessiert sind, dass die Anzahl der Klicks auf herunterladbare Dateien verfolgt wird. Wenn *`trackDownloadLinks`* auf „True“ gesetzt ist und ein Link für einen Datei-Download angeklickt wird, werden die Daten unverzüglich an [!DNL Analytics] übermittelt. Zu den gesendeten Daten gehören die Download-URL des Links sowie Daten zur Besucherklickzuordnung für diesen Link. Wenn *`trackDownloadLinks`* auf „False“ gesetzt ist, sind die Daten zur Besucherklickzuordnung für Exitlinks, die zu herunterladbaren Dateien gehören, wahrscheinlich in Berichten enthalten.

## Syntax und mögliche Werte

Die Variable *`trackDownloadLinks`* kann entweder „true“ oder „false“ sein.

## Beispiele

```
js
s.trackDownloadLinks=true 
```

```
js
s.trackDownloadLinks=false
```

## Konfigurationseinstellungen

Keine

## Probleme, Fragen und Tipps

* den *`trackDownloadLinks`* Wert „false“ hat, sind Links, die zu herunterladbaren Dateien auf Ihrer Site gehören, wahrscheinlich in Berichten zur Besucherklickzuordnung enthalten.

* Wenn *`trackDownloadLinks`* „true“ ist, werden, sobald ein Besucher auf einen Link für einen Datei-Download klickt, Daten gesendet.

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