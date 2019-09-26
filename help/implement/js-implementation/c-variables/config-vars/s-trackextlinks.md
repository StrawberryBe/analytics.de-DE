---
description: Mit dynamischen Variablen können Sie Werte von einer Variablen in eine andere kopieren, ohne die vollständigen Werte mehrfach in die Bildanforderung auf Ihrer Site eingeben zu müssen.
keywords: Analytics-Implementierung
seo-description: Mit dynamischen Variablen können Sie Werte von einer Variablen in eine andere kopieren, ohne die vollständigen Werte mehrfach in die Bildanforderung auf Ihrer Site eingeben zu müssen.
solution: null
title: Dynamische Variablen
translation-type: tm+mt
source-git-commit: b38ba4222951d957c607cd764224028527835c7e

---


# s.trackExternalLinks

Wenn "true"ist, wird ermittelt, ob ein angeklickter Link ein Exitlink ist.

| Maximale Größe | Debug-Parameter | Ausgefüllte Berichte | Standardwert |
|---|---|---|---|
| Keine | Keine | Keine | True |

Die Variable *`trackExternalLinks`* ist nur dann auf „false“ zu setzen, wenn Ihre Site keine Exitlinks enthält oder wenn Sie nicht daran interessiert sind, dass die Anzahl der Klicks auf Exitlinks verfolgt wird. Jeder Link, der einen Besucher weg von Ihrer Site führt, gilt als Exitlink. Wenn *`trackExternalLinks`* is 'true,' then when you click an exit link, tracking data is immediately sent. Dazu gehören die URL des Exitlinks, der Linkname und Daten zur Benutzerklickzuordnung für den Link. Wenn *`trackExternalLinks`* is 'false,' then visitor click map data for exit links on your site is likely to be under reported.

## Syntax und mögliche Werte

Die Variable *`trackExternalLinks`kann entweder „true“ oder „false“ sein.*

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

–

## Probleme, Fragen und Tipps

* When *`trackExternalLinks`* is 'false,' links that take people away from your site are likely to be under reported in visitor click map.

* When *`trackExternalLinks`* is 'true,' data is sent each time a visitor clicks on an exit link (before link target loads).
