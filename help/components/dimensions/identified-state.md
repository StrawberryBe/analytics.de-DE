---
title: Identifizierter Status
description: Eine Markierung, die die Erkennung durch das Gerätediagramm bestimmt.
exl-id: 8c6e9003-96f8-460f-a490-203f67be6337
translation-type: ht
source-git-commit: 4c726cc78e4d6c15db70ab04b0319b0602a51be6
workflow-type: ht
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
