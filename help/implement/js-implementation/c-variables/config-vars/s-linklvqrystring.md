---
description: Mit dynamischen Variablen können Sie Werte von einer Variablen in eine andere kopieren, ohne die vollständigen Werte mehrfach in die Bildanforderung auf Ihrer Site eingeben zu müssen.
keywords: Analytics Implementation
solution: null
title: Dynamische Variablen
translation-type: tm+mt
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
| Keine | Keine | Datei-Downloads für Exitlinks | false |

*Hinweis: Die Einstellung`linkLeaveQueryString=true`umfasst alle Abfragezeichenfolgenparameter für alle Exitlinks und Downloadlinks.*

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

Bei dieser Variablen sind keine Konfigurationen erforderlich.

## Probleme, Fragen und Tipps

* Wenn `s.linkLeaveQueryString=true` eingestellt wird, werden alle Abfragezeichenfolgen-Parameter für alle Exitlinks und Downloadlinks mit aufgenommen.
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