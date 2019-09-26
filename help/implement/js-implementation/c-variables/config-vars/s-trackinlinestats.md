---
description: Mit dynamischen Variablen können Sie Werte von einer Variablen in eine andere kopieren, ohne die vollständigen Werte mehrfach in die Bildanforderung auf Ihrer Site eingeben zu müssen.
keywords: Analytics-Implementierung
seo-description: Mit dynamischen Variablen können Sie Werte von einer Variablen in eine andere kopieren, ohne die vollständigen Werte mehrfach in die Bildanforderung auf Ihrer Site eingeben zu müssen.
solution: null
title: Dynamische Variablen
translation-type: tm+mt
source-git-commit: 60dd1b300035e5149f53870239de85fb3174a77a

---


# s.trackInlineStats

Die Variable bestimmt, ob ClickMap-Daten gesammelt werden.

If *`trackInlineStats`* is 'true,' data about the page and link clicked are stored in a cookie called s_sq. If 'false,' s_sq will have a value of "[[B]]," which is considered null.

| Maximale Größe | Debug-Parameter | Ausgefüllte Berichte | Standardwert |
|---|---|---|---|
| Keine | Keine | ClickMap | False |

## Syntax und mögliche Werte

```
js
s.trackInlineStats=true|false
```

Die Variable *`trackInlineStats`kann entweder „true“ oder „false“ sein.*

## Beispiele

```js
s.trackInlineStats=true
```

```js
s.trackInlineStats=false
```

## Konfigurationseinstellungen

–