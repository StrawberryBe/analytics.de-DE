---
title: Identifizierter Status
description: Eine Markierung, die die Erkennung durch das Gerätediagramm bestimmt.
translation-type: tm+mt
source-git-commit: 12c026fec44f2e66e2997e8b338823f2c7d790e4
workflow-type: tm+mt
source-wordcount: '120'
ht-degree: 12%

---


# Identifizierter Status

Die Dimension &quot;Identifizierter Status&quot;ist spezifisch für [Geräteübergreifende Analysen](../cda/overview.md) Virtual Report Suites. Er meldet, ob die Experience Cloud-ID vom Gerätediagramm zum Zeitpunkt der Ausführung des Berichts erkannt wird. Diese Dimension ist hilfreich, um zu verstehen, wie gut CDA Daten zusammenfügt oder &quot;komprimiert&quot;.

## Füllen dieser Dimension mit Daten

Solange [Geräteübergreifende Analysen](../cda/overview.md) für eine Virtual Report Suite konfiguriert sind, funktioniert diese Dimension standardmäßig.

## Dimensionselemente

Zu den Dimensionselementen gehören `"Identified"` und `"Unidentified"`.

* **`"Identified"`**: Das Gerätediagramm erkennt die mit dem Treffer verbundene Experience Cloud-ID.
* **`"Unidentified"`**: Das Gerätediagramm erkennt die Experience Cloud-ID nicht oder der Treffer hat keine Experience Cloud-ID.
