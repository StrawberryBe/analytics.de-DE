---
description: Mit dynamischen Variablen können Sie Werte von einer Variablen in eine andere kopieren, ohne die vollständigen Werte mehrfach in die Bildanforderung auf Ihrer Site eingeben zu müssen.
keywords: Analytics Implementation
solution: null
title: Dynamische Variablen
translation-type: ht
source-git-commit: 16ba0b12e0f70112f4c10804d0a13c278388ecc2

---


# s.linkExternalFilters

Wenn Ihre Site viele Links zu externen Sites enthält und Sie nicht sämtliche Exitlinks verfolgen möchten, setzen Sie „“ so ein, dass nur eine bestimmte Untermenge der Ausstiegs-Links im Bericht aufgeführt wird.

| Maximale Größe | Debug-Parameter | Ausgefüllte Berichte | Standardwert |
|---|---|---|---|
| nicht angegeben | nicht angegeben | Pfade &gt; Einstiege und Ausstiege &gt; Exitlinks | "" |

*`linkExternalFilters`* ist eine optionale Variable, die in Verbindung mit *`linkInternalFilters`* verwendet wird, um festzustellen, ob ein Link ein Exitlink ist. Jeder Link, der einen Besucher weg von Ihrer Site führt, gilt als Exitlink. Ob ein Exitlink in ein Popupfenster oder in das vorhandene Fenster führt, spielt keine Rolle, damit ein Link in Berichten als Exitlink aufgeführt wird. Exitlinks werden nur verfolgt, wenn *`trackExternalLinks`* auf „True“ festgelegt ist. Bei den Filtern in *`linkExternalFilters`* und *`linkInternalFilters`* sind die Groß- und Kleinschreibung nicht zu beachten.

> [!NOTE]Wenn Sie *`linkExternalFilters`* nicht verwenden möchten, löschen Sie sie oder setzen Sie sie auf „“.

Die Filterliste in *`linkExternalFilters`* und *`linkInternalFilters`* gilt standardmäßig für die Domäne und den Pfad jedes Links. Wenn *`linkLeaveQueryString`* auf „true“ gesetzt ist, werden die Filter auf die gesamte URL angewendet (Domäne, Pfad und Abfragezeichenfolge). Diese Filter werden immer auf den absoluten Pfad der URL angewendet, auch wenn ein relativer Pfad als href-Wert verwendet wird.

Mit *`linkInternalFilters`* haben die meisten Firmen genug Kontrolle über Exitlinks, sodass sie *`linkExternalFilters`* nicht benötigen. Bei Verwendung von *`linkExternalFilters`* sinkt lediglich die Wahrscheinlichkeit, dass ein Exitlink als extern betrachtet wird. Wenn *`linkExternalFilters`* über einen Wert verfügt, wird ein Link nur dann als extern angesehen, wenn er mit *`linkInternalFilters`* nicht übereinstimmt und mit *`linkExternalFilters`* übereinstimmt.

Das folgende Beispiel zeigt, wie diese Variable verwendet wird. In diesem Beispiel lautet die URL der Seite `https://www.mysite.com/index.html`.

```js
s.trackExternalLinks=true 
s.linkInternalFilters="javascript:,mysite.com" 
s.linkExternalFilters="site1.com,site2.com,site3.com/partners" 
s.linkLeaveQueryString=false 
...
<a href="https://www.mysite.com">Not an Exit Link</a> 
<a href="/careers/job_list.html">Not an Exit Link</a> 
<a href="https://www2.site3.com">Not an Exit Link</a> 
<a href="https://www.site1.com">Exit Link</a> 
<a href="https://www2.site3.com/partners/offer.asp">Exit Link</a> 
```

## Syntax und mögliche Werte

Die Variable *`linkExternalFilters`* ist eine durch Kommas getrennte Liste von ASCII-Zeichen. Leerzeichen sind nicht erlaubt.

```js
s.linkExternalFilters="site1.com[,site2.com[,site3.net[...]]]"
```

Jeder beliebige Teil einer URL kann in *`linkExternalFilters`* – durch Kommas getrennt – aufgeführt sein.

## Beispiele

```js
s.linkExternalFilters="partnersite.com,partnertwo.net/path/"
```

```js
s.linkExternalFilters=""
```

## Konfigurationseinstellungen

Keine

## Probleme, Fragen und Tipps

* Das Verwenden von *`linkExternalFilters`* kann dazu führen, dass weniger Links in einer Site Exitlinks sind. Verwenden Sie diese Variable nicht anstelle von *`linkInternalFilters`*, um interne Links zu zwingen, Exitlinks zu werden.

* Wenn *`linkLeaveQueryString`* auf die Abfragezeichenfolge eines Links angewendet werden soll, stellen Sie sicher, dass *`linkExternalFilters`* auf „true“ eingestellt ist. Siehe [linkLeaveQueryString](https://docs.adobe.com/content/help/de-DE/analytics/implementation/javascript-implementation/variables-analytics-reporting/config-var/s-account.html), bevor Sie `"true"` einstellen.

* Um Exitlinktracking zu deaktivieren, legen Sie *`trackExternalLinks`* auf `"false"` fest.
