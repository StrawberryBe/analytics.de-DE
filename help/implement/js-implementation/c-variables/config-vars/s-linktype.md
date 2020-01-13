---
description: Mit dynamischen Variablen können Sie Werte von einer Variablen in eine andere kopieren, ohne die vollständigen Werte mehrfach in die Bildanforderung auf Ihrer Site eingeben zu müssen.
keywords: Analytics Implementation
solution: null
title: Dynamische Variablen
translation-type: ht
source-git-commit: 21f278017472ae39c6066ca7694a5cdbbfde41f3

---


# s.linkType

Enthält den automatisch ermittelten Linktyp (wenn vorhanden). Kann auf einen der folgenden Werte eingestellt werden:

    * `d` (Herunterladen)
    * `e` (Beenden)
    * `o` (Benutzerdefiniert/Sonstiges)

Dies ist der Parameter `pe` in der Bildanforderung. Wenn mit [`linkURL`](https://docs.adobe.com/content/help/de-DE/analytics/implementation/javascript-implementation/variables-analytics-reporting/config-var/s-linkURL.html) oder [`linkName`](https://docs.adobe.com/content/help/de-DE/analytics/implementation/javascript-implementation/variables-analytics-reporting/config-var/s-linkname.html) festgelegt, wird ein Server-Aufruf als Downloadlink, Exitlink oder benutzerspezifischer Link gesendet.

*Hinweis: Die Variable[`pageName`](https://docs.adobe.com/content/help/de-DE/analytics/implementation/testing-and-validation/optimize-implementation/page-naming-strategies.html)kann nicht für Dateidownloads, Exitlinks oder benutzerspezifische Links festgelegt werden, da Links dieser Typen keine Seitenansichten sind und somit keinen zugehörigen Seitennamen haben.*


**Beispiel**

```js
function s_doPlugins(s) { 
    if (s.linkType == "d" && s.linkURL.indexOf(".aspx?f=") { 
        //special tracking for .aspx file download script 
        s.eVar11 = s.linkURL.substring(s.linkURL.lastIndexOf("?f=") + 3, s.linkURL.length); 
    } 
  
    else if (s.linkType == "o" ) { 
        // note: linkType is set to "o" only if you make a custom call 
        // to s.tl() and set the link type to "o". Automatically tracked 
        // links are set to "d" or "e" only. 
        s.eVar10 = s.LinkURL; 
    } 
}
```
