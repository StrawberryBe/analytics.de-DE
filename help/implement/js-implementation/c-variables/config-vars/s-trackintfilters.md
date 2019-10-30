---
description: Mit dynamischen Variablen können Sie Werte von einer Variablen in eine andere kopieren, ohne die vollständigen Werte mehrfach in die Bildanforderung auf Ihrer Site eingeben zu müssen.
keywords: Analytics-Implementierung
seo-description: Mit dynamischen Variablen können Sie Werte von einer Variablen in eine andere kopieren, ohne die vollständigen Werte mehrfach in die Bildanforderung auf Ihrer Site eingeben zu müssen.
solution: null
title: Dynamische Variablen
translation-type: tm+mt
source-git-commit: a2c38c2cf3a2c1451e2c60e003ebe1fa9bfd145d

---



# s.linkInternalFilters

Mithilfe der „“-Variablen wird bestimmt, welche Links auf der Site Exitlinks sind.

Die Variable enthält eine kommagetrennte Liste mit Filtern, die die Links darstellen, die zu Ihrer Site gehören.

| Maximale Größe | Debug-Parameter | Ausgefüllte Berichte | Standardwert |
|---|---|---|---|
| Keine | Keine | Pfade &gt; Einstiege und Ausstiege &gt; Exitlinks |  |

> [!NOTE]Zuvor wurde vorgeschlagen, „linkInternalFilters“ auf „javascript:“ festzulegen. Dies führte jedoch dazu, dass alle Domänen als extern betrachtet wurden, einschließlich der aktuellen Domäne, in der sich das Tag befindet. Wenn mehrere Domänen als intern betrachtet werden sollen, können Sie sie wie in den folgenden Beispielen hinzufügen.

Die Variable *`linkInternalFilters`* bestimmt, ob ein Link ein Exitlink ist. Zu Exitlinks gehören alle Links, über die Besucher von Ihrer Site weg geleitet werden. Ob ein Exitlink in ein Popupfenster oder in das vorhandene Fenster führt, spielt keine Rolle, damit ein Link in Berichten als Exitlink aufgeführt wird. Exitlinks werden nur verfolgt, wenn *`trackExternalLinks`* den Wert `"true"` hat. (Informationen zur Verarbeitung von Exitlinks durch DTM finden Sie unter [Linktracking](https://marketing.adobe.com/resources/help/en_US/dtm/link_tracking.html) in der Dokumentation für Dynamic Tag Management.) Bei den Filtern in *`linkInternalFilters`* wird nicht zwischen Groß- und Kleinschreibung unterschieden.

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
