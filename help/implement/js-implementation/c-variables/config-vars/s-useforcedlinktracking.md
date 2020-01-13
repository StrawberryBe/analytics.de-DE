---
description: Mit dynamischen Variablen können Sie Werte von einer Variablen in eine andere kopieren, ohne die vollständigen Werte mehrfach in die Bildanforderung auf Ihrer Site eingeben zu müssen.
keywords: Analytics Implementation
solution: null
title: Dynamische Variablen
translation-type: ht
source-git-commit: 8deec068fcea49f1183633826d5ce8271fb38a14

---



# s.useForcedLinkTracking

Dieses Flag deaktiviert die erzwungene Linktracking für einige Browser. Bei Firefox 20+ und WebKit-Browsern ist die erzwungene Linktracking standardmäßig aktiviert.

Wenn `useForcedLinkTracking` aktiviert ist, übergeht die AppMeasurement-Datei bei einigen Browsern das standardmäßige Link-Verhalten, um zu verhindern, dass der Nachverfolgungslink-Aufruf beim Öffnen der neuen Seite abgebrochen wird. Anstatt die Standard-Browseraktion auszuführen, führt die AppMeasurement-Datei den Nachverfolgungslink-Aufruf aus und übernimmt die Verarbeitung des Navigationsereignisses selbst.

In JavaScript H.25.4 (im Februar 2013 veröffentlicht) wurden die folgenden Einschränkungen beim Umfang von verfolgten Links bei aktiviertem `useForcedLinkTracking` hinzugefügt. Das automatische erzwungene Linktracking gilt nur in folgenden Fällen:

* `<A>`- und `<AREA>`-Tags.
* Das Tag muss über ein `HREF`-Attribut verfügen.
* `HREF` darf nicht mit `about:`, `#` oder `javascript:` beginnen.
* Das `TARGET`-Attribut darf nicht eingestellt sein, oder das `TARGET` muss sich auf das aktuelle Fenster (`_self`, `_top` oder den Wert von `window.name`) beziehen.

Standardwert = `true`

## Beispiel

`s.useForcedLinkTracking = false`
