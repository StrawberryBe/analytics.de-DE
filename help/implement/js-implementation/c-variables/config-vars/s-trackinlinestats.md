---
description: Mit dynamischen Variablen können Sie Werte von einer Variablen in eine andere kopieren, ohne die vollständigen Werte mehrfach in die Bildanforderung auf Ihrer Site eingeben zu müssen.
keywords: Analytics-Implementierung
seo-description: Mit dynamischen Variablen können Sie Werte von einer Variablen in eine andere kopieren, ohne die vollständigen Werte mehrfach in die Bildanforderung auf Ihrer Site eingeben zu müssen.
solution: null
title: Dynamische Variablen
translation-type: tm+mt
source-git-commit: 8c4c368a84ba5499d85f0b7512c99de47ddb14c2

---


# s.trackInlineStats

Die Variable bestimmt, ob ClickMap-Daten gesammelt werden.

Wenn *`trackInlineStats`* auf „true“ gesetzt ist, werden Daten zur Seite und zum angeklickten Link in einem Cookie namens „s_sq“ gespeichert. Wenn „false“, hat „s_sq“ den Wert „[[B]]“, was als null angesehen wird.

| Maximale Größe | Debug-Parameter | Ausgefüllte Berichte | Standardwert |
|---|---|---|---|
| Keine | Keine | ClickMap | False |

## Syntax und mögliche Werte

```
js
s.trackInlineStats=true|false
```

Die Variable *`trackInlineStats`* kann entweder „true“ oder „false“ sein.

## Beispiele

```js
s.trackInlineStats=true
```

```js
s.trackInlineStats=false
```

## Konfigurationseinstellungen

Keine
