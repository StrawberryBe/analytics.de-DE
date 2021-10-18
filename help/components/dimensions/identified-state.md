---
title: Identifizierter Status
description: Eine Markierung, die die Erkennung durch das Gerätediagramm bestimmt.
exl-id: 8c6e9003-96f8-460f-a490-203f67be6337
source-git-commit: 1a58c3e87f5918c91b891faa6027f5ad8b6024b9
workflow-type: ht
source-wordcount: '111'
ht-degree: 100%

---

# Identifizierter Status

Die Dimension „Identifizierter Status“ ist spezifisch für Virtual Report Suites in [Cross-Device Analytics](../cda/overview.md). Mit dieser Dimension wird angegeben, ob Treffer zum Zeitpunkt der Berichterstellung vom System identifiziert (zugeordnet) wurden oder nicht. Diese Dimension ist hilfreich, um zu verstehen, wie gut CDA Daten zusammenfügt oder „komprimiert“.

## Füllen dieser Dimension mit Daten

Solange [Cross-Device Analytics](../cda/overview.md) für Virtual Report Suite konfiguriert ist, funktioniert diese Dimension standardmäßig.

## Dimensionselemente

Zu den Dimensionselementen gehören `"Identified"` und `"Unidentified"`.

* **`"Identified"`**: Der Treffer wird einer Person zugeordnet.
* **`"Unidentified"`**: Der Treffer wird keiner Person zugeordnet und konnte mit keiner Attributionsmethode zugeordnet werden.
