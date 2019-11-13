---
description: Mit dynamischen Variablen können Sie Werte von einer Variablen in eine andere kopieren, ohne die vollständigen Werte mehrfach in die Bildanforderung auf Ihrer Site eingeben zu müssen.
keywords: Analytics-Implementierung
solution: null
title: Dynamische Variablen
translation-type: tm+mt
source-git-commit: 8c06a54ccd652f3f915af3af040e9cc69f01d0c1

---


# s.linkType

Enthält den automatisch ermittelten Linktyp (wenn vorhanden). Kann auf einen der folgenden Werte eingestellt werden:

    * `d` (Download)
    * `e` (Ausstieg)
    * `o` (benutzerspezifisch/sonstige)

Dies ist der Parameter `pe` in der Bildanforderung. Wenn mit `linkURL` oder `linkName` festgelegt, wird ein Server-Aufruf als Downloadlink, Exitlink oder benutzerspezifischer Link gesendet.

*Hinweis: Die Variable[`pageName`](https://docs.adobe.com/content/help/en/analytics/implementation/testing-and-validation/optimize-implementation/page-naming-strategies.html)kann nicht für einen Datei-Download, Exitlink oder benutzerspezifischen Link festgelegt werden, da jeder Linktyp keine Seitenansicht und keinen zugehörigen Seitennamen darstellt.*


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
