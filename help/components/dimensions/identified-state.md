---
title: Identifizierter Status
description: Eine Markierung, die die Erkennung durch das Gerätediagramm bestimmt.
feature: Dimensions
exl-id: 8c6e9003-96f8-460f-a490-203f67be6337
source-git-commit: d095628e94a45221815b1d08e35132de09f5ed8f
workflow-type: tm+mt
source-wordcount: '111'
ht-degree: 89%

---

# Identifizierter Status

Der &quot;Identified state&quot; [Dimension](overview.md) ist spezifisch für [Geräteübergreifende Analyse](../cda/overview.md) Virtual Report Suites. Mit dieser Dimension wird angegeben, ob Treffer zum Zeitpunkt der Berichterstellung vom System identifiziert (zugeordnet) wurden oder nicht. Diese Dimension ist hilfreich, um zu verstehen, wie gut CDA Daten zusammenfügt oder „komprimiert“.

## Füllen dieser Dimension mit Daten

Solange [Cross-Device Analytics](../cda/overview.md) für Virtual Report Suite konfiguriert ist, funktioniert diese Dimension standardmäßig.

## Dimensionselemente

Zu den Dimensionselementen gehören `"Identified"` und `"Unidentified"`.

* **`"Identified"`**: Der Treffer wird einer Person zugeordnet.
* **`"Unidentified"`**: Der Treffer wird keiner Person zugeordnet und konnte mit keiner Attributionsmethode zugeordnet werden.
