---
description: Mit dynamischen Variablen können Sie Werte von einer Variablen in eine andere kopieren, ohne die vollständigen Werte mehrfach in die Bildanforderung auf Ihrer Site eingeben zu müssen.
keywords: Analytics-Implementierung
seo-description: Mit dynamischen Variablen können Sie Werte von einer Variablen in eine andere kopieren, ohne die vollständigen Werte mehrfach in die Bildanforderung auf Ihrer Site eingeben zu müssen.
solution: null
title: Dynamische Variablen
translation-type: tm+mt
source-git-commit: b38ba4222951d957c607cd764224028527835c7e

---


# s.linkExternalFilters

Wenn Ihre Site viele Links zu externen Sites enthält und Sie nicht sämtliche Exitlinks verfolgen möchten, setzen Sie „“ so ein, dass nur eine bestimmte Untermenge der Ausstiegs-Links im Bericht aufgeführt wird.

| Maximale Größe | Debug-Parameter | Ausgefüllte Berichte | Standardwert |
|---|---|---|---|
| Keine | Keine | Pfade &gt; Einstiege und Ausstiege &gt; Exitlinks | "" |

Die Variable Bei *`linkExternalFilters`* einer Variablen handelt es sich um eine optionale Variable, mit der *`linkInternalFilters`* ermittelt wird, ob ein Link ein Exitlink ist. Jeder Link, der einen Besucher weg von Ihrer Site führt, gilt als Exitlink. Ob ein Exitlink in ein Popupfenster oder in das vorhandene Fenster führt, spielt keine Rolle, damit ein Link in Berichten als Exitlink aufgeführt wird. Exitlinks werden nur verfolgt, wenn *`trackExternalLinks`* is set to 'true.' Bei den Filtern in *`linkExternalFilters`* und *`linkInternalFilters`* sind die Groß- und Kleinschreibung nicht zu beachten.

>[!NOTE]
>
>Wenn Sie diese nicht verwenden möchten, löschen Sie sie *`linkExternalFilters`* oder setzen Sie sie auf "".

Die Filter werden standardmäßig in der Liste angezeigt *`linkExternalFilters`* und *`linkInternalFilters`* gelten für die Domäne und den Pfad jedes Links. Wenn "true"festgelegt *`linkLeaveQueryString`* ist, gelten die Filter für die gesamte URL (Domäne, Pfad und Abfragezeichenfolge). Diese Filter werden immer auf den absoluten Pfad der URL angewendet, auch wenn ein relativer Pfad als href-Wert verwendet wird.

Mit *`linkInternalFilters`* haben die meisten Firmen genug Kontrolle über Exitlinks, sodass sie *`linkExternalFilters`*. Using *`linkExternalFilters`* simply decreases the likelihood that an exit link is considered external. If *`linkExternalFilters`* has a value, then a link is considered only external if it does not match *`linkInternalFilters`* and does match *`linkExternalFilters`*.

Das folgende Beispiel zeigt, wie diese Variable verwendet wird. In this example, the URL of the page is `https://www.mysite.com/index.html`.

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

The *`linkExternalFilters`* variable is a comma-separated list of ASCII characters. Leerzeichen sind nicht erlaubt.

```js
s.linkExternalFilters="site1.com[,site2.com[,site3.net[...]]]"
```

Jeder beliebige Teil einer URL kann in *`linkExternalFilters`*, separated by commas.

## Beispiele

```js
s.linkExternalFilters="partnersite.com,partnertwo.net/path/"
```

```js
s.linkExternalFilters=""
```

## Konfigurationseinstellungen

–

## Probleme, Fragen und Tipps

* Using *`linkExternalFilters`* can result in fewer links on your site being exit links. Verwenden Sie diese Variable nicht anstelle von, *`linkInternalFilters`* um zu erzwingen, dass interne Links zu Ausstiegslinks werden.

* Wenn Sie auf die Abfragezeichenfolge eines Links angewendet werden *`linkExternalFilters`* sollten, stellen Sie sicher, dass auf "true"festgelegt *`linkLeaveQueryString`* ist. See [linkLeaveQueryString](https://docs.adobe.com/content/help/en/analytics/implementation/javascript-implementation/variables-analytics-reporting/config-var/s-account.html) before setting to `"true"`.

* To disable exit link tracking, set *`trackExternalLinks`* to `"false"`.
