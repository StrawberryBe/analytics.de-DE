---
description: Mit dynamischen Variablen können Sie Werte von einer Variablen in eine andere kopieren, ohne die vollständigen Werte mehrfach in die Bildanforderung auf Ihrer Site eingeben zu müssen.
keywords: Analytics Implementation
solution: null
title: Dynamische Variablen
translation-type: ht
source-git-commit: f1ebe5e89f62957c8bcc829be4b1a97463210f93

---



# s.linkInternalFilters

Mithilfe der „“-Variablen wird bestimmt, welche Links auf der Site Exitlinks sind.

Die Variable enthält eine kommagetrennte Liste mit Filtern, die die Links darstellen, die zu Ihrer Site gehören.

| Maximale Größe | Debug-Parameter | Ausgefüllte Berichte | Standardwert |
|---|---|---|---|
| nicht angegeben | nicht angegeben | Pfade &gt; Einstiege und Ausstiege &gt; Exitlinks |  |

> [!NOTE]Zuvor wurde vorgeschlagen, „linkInternalFilters“ auf „javascript:“ festzulegen. Dies führte jedoch dazu, dass alle Domänen als extern betrachtet wurden, einschließlich der aktuellen Domäne, in der sich das Tag befindet. Wenn mehrere Domänen als intern betrachtet werden sollen, können Sie sie wie in den folgenden Beispielen hinzufügen.

Die Variable *`linkInternalFilters`* bestimmt, ob ein Link ein Exitlink ist. Zu Exitlinks gehören alle Links, über die Besucher von Ihrer Site weg geleitet werden. Ob ein Exitlink in ein Popupfenster oder in das vorhandene Fenster führt, spielt keine Rolle, damit ein Link in Berichten als Exitlink aufgeführt wird. Exitlinks werden nur verfolgt, wenn *`trackExternalLinks`* den Wert `"true"` hat. (Informationen zur Verarbeitung von Exitlinks durch DTM finden Sie unter [Linktracking](https://marketing.adobe.com/resources/help/de_DE/dtm/link_tracking.html) in der Dokumentation für Dynamic Tag Management.) Bei den Filtern in *`linkInternalFilters`* wird nicht zwischen Groß- und Kleinschreibung unterschieden.

Die Liste der Filter in *`linkInternalFilters`* gilt standardmäßig für die Domäne und den Pfad jedes Links. Wenn *`linkLeaveQueryString`* auf `"true"` gesetzt ist, werden die Filter auf die gesamte URL angewendet (Domäne, Pfad und Abfragezeichenfolge). Die Filter werden immer auf den absoluten Pfad der URL angewendet, auch wenn ein relativer Pfad als href-Wert verwendet wird.

Stellen Sie sicher, dass alle Domänen Ihrer Site (und aller Partnersites, die Ihre JavaScript-Datei verwenden) in *`linkInternalFilters`* enthalten sind. Wenn nicht sämtliche Domänen in der Liste enthalten sind, werden Links auf und zu diesen Domänen als Exitlinks betrachtet, wodurch die Zahl der gesendeten Server-Aufrufe zunimmt. Wenn Sie möchten, dass mehrere Domänen oder Unternehmen eine einzelne [!DNL AppMeasurement] für JavaScript-Dateien verwenden, sollten Sie erwägen, *`linkInternalFilters`* auf der Seite auszufüllen und dabei den in der JavaScript-Datei angegebenen Wert zu überschreiben. Wenn Vanitydomänen vorhanden sind, die sofort zu Ihrer Hauptdomäne umgeleitet werden, müssen diese nicht in die Liste aufgenommen werden.

Das folgende Beispiel zeigt, wie diese Variable verwendet wird. In diesem Beispiel lautet die URL der Seite `https://www.mysite.com/index.html`.

```js
s.trackExternalLinks=true 
s.linkInternalFilters="mysite.com" 
s.linkExternalFilters="" 
s.linkLeaveQueryString=false 
...
<a href="https://www.mysite.com">Not an Exit Link</a> 
<a href="/careers/job_list.html">Not an Exit Link</a> 
<a href="https://www2.site3.com">Exit Link</a> 
<a href="https://www2.site1.com/partners/">Exit Link</a> 
```

## Syntax und mögliche Werte

Die Variable *`linkInternalFilters`* ist eine durch Kommas getrennte Liste von ASCII-Zeichen. Leerzeichen sind nicht erlaubt.

```js
s.linkInternalFilters="site1.com[,site2.com[,site3.net[...]]]"
```

## Beispiele

```js
s.linkInternalFilters="mysite.com"
```

```js
s.linkInternalFilters="mysite.com,mysite.net,vanity1.com"
```

## Konfigurationseinstellungen

Keine

## Probleme, Fragen und Tipps

* Tragen Sie alle Domänen, unter denen die [!DNL AppMeasurement] für JavaScript-Datei möglicherweise bereitgestellt wird, in die Filterliste ein.
* Überprüfen Sie in regelmäßigen Abständen, ob der Bericht [!UICONTROL Pfade] &gt; [!UICONTROL Einstiege und Ausstiege] &gt; [!UICONTROL Exitlinks] nur korrekte Einträge enthält.

* Überprüfen Sie in regelmäßigen Abständen Ihre Partnerverträge auf Einschränkungen bei der Linktracking. So kann es Ihnen zum Beispiel untersagt sein, Links nachzuverfolgen, die in Display-Anzeigen des Partners stehen. Filtern Sie Partnerlinks, indem Sie deren Domäne zu *`linkInternalFilters`* hinzufügen:

```js
s.linkInternalFilters="mysite.com,mysite.net,mypartner.net/adclick"
```

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
