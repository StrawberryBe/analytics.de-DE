---
description: Mit dynamischen Variablen können Sie Werte von einer Variablen in eine andere kopieren, ohne die vollständigen Werte mehrfach in die Bildanforderung auf Ihrer Site eingeben zu müssen.
keywords: Analytics Implementation
solution: null
title: Dynamische Variablen
translation-type: tm+mt
source-git-commit: 8deec068fcea49f1183633826d5ce8271fb38a14

---



# s.useForcedLinkTracking

Dieses Flag deaktiviert die erzwungene Linktracking für einige Browser. Bei Firefox 20+ und WebKit-Browsern ist die erzwungene Linktracking standardmäßig aktiviert.

When `useForcedLinkTracking` is enabled, the AppMeasurement file overrides the default link behavior on some browsers to prevent the track link call from being canceled when the new page opens. Die AppMeasurement-Datei führt den Nachverfolgungslink-Aufruf aus und verarbeitet das Navigationsereignis manuell, anstatt die standardmäßige Browseraktion zu verwenden.

In JavaScript H.25.4 (im Februar 2013 veröffentlicht) wurden die folgenden Einschränkungen beim Umfang von verfolgten Links bei aktiviertem `useForcedLinkTracking` hinzugefügt. Das automatische erzwungene Linktracking gilt nur in folgenden Fällen:

* `<A>`- und `<AREA>`-Tags.
* Das Tag muss über ein `HREF`-Attribut verfügen.
* The `HREF` can't start with `#`, `about:`, or `javascript:`.
* The `TARGET` attribute must not be set, or the `TARGET` needs to refer to the current window ( `_self`, `_top`, or the value of `window.name`).

Standardwert = `true`

## Beispiel

`s.useForcedLinkTracking = false`
