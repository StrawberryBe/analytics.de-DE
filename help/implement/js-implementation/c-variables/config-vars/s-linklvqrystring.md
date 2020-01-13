---
description: Mit dynamischen Variablen können Sie Werte von einer Variablen in eine andere kopieren, ohne die vollständigen Werte mehrfach in die Bildanforderung auf Ihrer Site eingeben zu müssen.
keywords: Analytics Implementation
solution: null
title: Dynamische Variablen
translation-type: ht
source-git-commit: f1ebe5e89f62957c8bcc829be4b1a97463210f93

---


# s.linkLeaveQueryString

Standardmäßig sind Abfragezeichenfolgen in allen Berichten ausgeschlossen.

Bei einigen Exitlinks und Downloadlinks befindet sich der wichtige Teil der URL möglicherweise in der Abfragezeichenfolge (wie in der folgenden Beispiel-URL):

```js
https://www.mycompany.com/download.asp?filename=myfile.exe
```

Der Name der Download-Datei kann in der Abfragezeichenfolge festgelegt sein, sodass die Abfragezeichenfolge erforderlich ist, damit der Bericht [!UICONTROL Dateidownloads] genauer ist.

Die Variable *`linkLeaveQueryString`* bestimmt, ob die Abfragezeichenfolge in den Berichten [!UICONTROL Exitlinks] und [!UICONTROL Datei-Download] enthalten sein soll.

| Maximale Größe | Debug-Parameter | Ausgefüllte Berichte | Standardwert |
|--- |--- |--- |--- |
| nicht angegeben | nicht angegeben | Datei-Downloads für Exitlinks | false |

*Hinweis: Wenn`linkLeaveQueryString=true`festgelegt wird, sind sämtliche Abfragezeichenfolgenparameter für alle Exit- und Downloadlinks eingeschlossen.*

## Syntax

```js
s.linkLeaveQueryString=[false/true]
```

## Beispiele

```js
s.linkLeaveQueryString=false
```

## Mögliche Werte

```js
s.linkLeaveQueryString=false
```

```js
s.linkLeaveQueryString=true
```

## Konfigurationseinstellungen

Bei dieser Variable sind keine Konfigurationen erforderlich.

## Probleme, Fragen und Tipps

* Wenn `s.linkLeaveQueryString=true` eingestellt wird, werden alle Abfragezeichenfolgenparameter für alle Exitlinks und Downloadlinks mit aufgenommen.
* Die `linkLeaveQueryString`-Variable hat keine Auswirkungen auf aufgezeichnete Seiten-URLs, Besucherklickzuordnungen oder [!UICONTROL Pfadberichte].

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