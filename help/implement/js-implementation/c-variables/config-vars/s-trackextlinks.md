---
description: Mit dynamischen Variablen können Sie Werte von einer Variablen in eine andere kopieren, ohne die vollständigen Werte mehrfach in die Bildanforderung auf Ihrer Site eingeben zu müssen.
keywords: Analytics-Implementierung
seo-description: Mit dynamischen Variablen können Sie Werte von einer Variablen in eine andere kopieren, ohne die vollständigen Werte mehrfach in die Bildanforderung auf Ihrer Site eingeben zu müssen.
solution: null
title: Dynamische Variablen
translation-type: tm+mt
source-git-commit: a2c38c2cf3a2c1451e2c60e003ebe1fa9bfd145d

---


# s.trackExternalLinks

Wenn „“ auf „true“ eingestellt ist, wird über „“ und „“ bestimmt, ob ein angeklickter Link ein Exitlink ist.

| Maximale Größe | Debug-Parameter | Ausgefüllte Berichte | Standardwert |
|---|---|---|---|
| Keine | Keine | Keine | True |

Die Variable *`trackExternalLinks`* ist nur dann auf „false“ zu setzen, wenn Ihre Site keine Exitlinks enthält oder wenn Sie nicht daran interessiert sind, dass die Anzahl der Klicks auf Exitlinks verfolgt wird. Jeder Link, der einen Besucher weg von Ihrer Site führt, gilt als Exitlink. Wenn *`trackExternalLinks`* auf „true“ eingestellt ist, werden bei jedem Klick auf einen Exitlink unverzüglich Trackingdaten gesendet. Dazu gehören die URL des Exitlinks, der Linkname und Daten zur Benutzerklickzuordnung für den Link. Wenn *`trackExternalLinks`* auf „false“ eingestellt ist, sind die Daten zur Besucherklickzuordnung für Exitlinks, die zu herunterladbaren Dateien gehören, wahrscheinlich in Berichten enthalten.

## Syntax und mögliche Werte

Die Variable *`trackExternalLinks`* kann entweder „true“ oder „false“ sein.

```
js
s.trackExternalLinks=true|false
```

## Beispiele

```
js
s.trackExternalLinks=true 
```

```
js
s.trackExternalLinks=false
```

## Konfigurationseinstellungen

Keine

## Probleme, Fragen und Tipps

* Wenn *`trackExternalLinks`* auf „false“ gesetzt ist, sind Links, über die Besucher Ihre Site verlassen, in Berichten zur Besucherklickzuordnung wahrscheinlich enthalten.

* Wenn *`trackExternalLinks`* „true“ ist, werden die Daten bei jedem Klick auf einen Exitlink (bevor das Linkziel geladen wird) gesendet.
