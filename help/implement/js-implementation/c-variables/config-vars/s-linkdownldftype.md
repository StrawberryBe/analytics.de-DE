---
description: Mit dynamischen Variablen können Sie Werte von einer Variablen in eine andere kopieren, ohne die vollständigen Werte mehrfach in die Bildanforderung auf Ihrer Site eingeben zu müssen.
keywords: Analytics Implementation
solution: null
title: Dynamische Variablen
translation-type: ht
source-git-commit: f1ebe5e89f62957c8bcc829be4b1a97463210f93

---


# s.linkDownloadFileTypes

Die Variable „“ ist eine kommagetrennte Liste mit Dateierweiterungen.

Wenn die Site Links zu Dateien mit diesen Dateierweiterungen enthält, werden die URLs dieser Links im Bericht [!UICONTROL Dateidownloads] angezeigt.

| Maximale Größe | Debug-Parameter | Ausgefüllte Berichte | Standardwert |
|--- |--- |--- |--- |
| nicht angegeben | nicht angegeben | Traffic &gt; Sitetraffic &gt; Dateidownloads | "exe, zip, wav, mp3, mov, mpg, avi, wmv, doc, pdf, xls" |

Die Variable *`linkDownloadFileTypes`* ist nur relevant, wenn *`trackDownloadLinks`* auf „True“ eingestellt ist.

Im Bericht [!UICONTROL Dateidownloads] werden nur Klicks auf Links gezählt, die mit der linken Maustaste erfolgten. Dateidownloads, die beim Laden einer Seite automatisch gestartet wurden oder die nur nach einer Weiterleitung erfolgten, werden im Bericht [!UICONTROL Dateidownloads] nicht gezählt. Auch Downloads, die über die Kontextmenüoption „Speichern unter“ erfolgen, werden im Bericht [!UICONTROL Dateidownloads] nicht gezählt.

Die Variable *`linkDownloadFileTypes`* kann auch eingesetzt werden, um Klicks zu RSS-Feeds nachzuverfolgen. Wenn Sie Links zu RSS-Feeds mit der Erweiterung .xml oder einer anderen Erweiterung haben, können Sie durch Anhängen von „,xml“ an die *`linkDownloadFileTypes`*-Liste sehen, wie oft auf jeden RSS-Link geklickt wird.

## Syntax und mögliche Werte

Nehmen Sie nur Dateierweiterungen (ohne Leerzeichen) auf.

```js
s.linkDownloadFileTypes="type1[,type2[,type3[...]]]"
```

Jede beliebige Dateierweiterung kann in die Liste eingetragen werden. Achten Sie darauf, keine gängigen Dateierweiterungen (wie HTM oder ASPX) in *`linkDownloadFileTypes`* zu verwenden. Andernfalls wird bei jedem Klick eine weitere Bildanforderung gesendet und als primärer Server-Aufruf gezählt.

## Beispiele

```js
s.linkDownloadFileTypes="exe,zip,wav,mp3,mov,mpg,avi,wmv,doc,pdf,xls"
```

```js
s.linkDownloadFileTypes="exe,zip,wav,mp3,mov,mpg,avi,wmv,doc,pdf,xls,xml"
```

## Konfigurationseinstellungen*

Keine

## Probleme, Fragen und Tipps

* Nur Klicks mit der linken Maustaste oder Dateidownloads führen dazu, dass die URL im Bericht [!UICONTROL Dateidownloads] aufgeführt wird.
* Wenn eine allgemeine Dateierweiterung in *`linkDownloadFileTypes`* aufgenommen wird, kann sich die Gesamtzahl der Server-Aufrufe erheblich erhöhen, die an Server von Adobe gesendet werden.
* Links zu serverseitigen Umleitungen oder HTML-Seiten, die automatisch mit dem Download einer Datei beginnen, werden nur gezählt, wenn die Dateierweiterung in *`linkDownloadFileTypes`*.
* Links, die JavaScript verwenden (wie z. B. „javascript:openLink“), werden bei Dateidownloads nicht gezählt.

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