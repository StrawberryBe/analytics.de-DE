---
title: Identifizierter Status
description: Eine Markierung, die die Erkennung durch das Gerätediagramm bestimmt.
translation-type: tm+mt
source-git-commit: 12c026fec44f2e66e2997e8b338823f2c7d790e4
workflow-type: tm+mt
source-wordcount: '120'
ht-degree: 100%

---


# Identifizierter Status

Die Dimension „Identifizierter Status“ ist spezifisch für Virtual Report Suites in [Cross-Device Analytics](../cda/overview.md). Sie vermerkt, ob die Experience Cloud ID vom Gerätediagramm zum Zeitpunkt der Ausführung des Berichts erkannt wird. Diese Dimension ist hilfreich, um zu verstehen, wie gut CDA Daten zusammenfügt oder „komprimiert“.

## Füllen dieser Dimension mit Daten

Solange [Cross-Device Analytics](../cda/overview.md) für Virtual Report Suite konfiguriert ist, funktioniert diese Dimension standardmäßig.

## Dimensionselemente

Zu den Dimensionselementen gehören `"Identified"` und `"Unidentified"`.

* **`"Identified"`**: Das Gerätediagramm erkennt die mit dem Treffer verbundene Experience Cloud ID.
* **`"Unidentified"`**: Das Gerätediagramm erkennt die Experience Cloud ID nicht oder der Treffer hat keine Experience Cloud ID.
