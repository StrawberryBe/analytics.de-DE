---
title: Treffertiefe
description: Die Anzahl der Treffer im Besuch.
translation-type: tm+mt
source-git-commit: d3f92d72207f027d35f81a4ccf70d01569c3557f
workflow-type: tm+mt
source-wordcount: '261'
ht-degree: 75%

---


# Treffertiefe

Die Dimension „Treffertiefe“ gibt an, wie weit ein bestimmter Treffer in einem Besuch liegt. Diese Dimension ist hilfreich, um zu verstehen, wie weit innerhalb eines Besuchs die Besucher Aktionen auf Ihrer Site ausführen. Die Treffertiefe zählt alle Arten von Treffern, einschließlich Seitenansicht-Treffern ([`t()`](/help/implement/vars/functions/t-method.md)) und Linktracking-Treffern ([`tl()`](/help/implement/vars/functions/tl-method.md)).

## Füllen dieser Dimension mit Daten

Diese Dimension ist bei allen Implementierungen vorkonfiguriert. Wenn eine Report Suite Daten enthält, funktioniert diese Dimension.

## Dimensionen

Dimension items include the string `"Hit Depth"` followed by a number representing the number of hits into the visit. The dimension item of `"Hit Depth 1"` represents the first hit of the visit, while the dimension item `"Hit Depth 8"` represents the 8th hit of the visit.

## Vergleich mit Besuchstiefe

Die Treffertiefe zählt alle Arten von Treffern, einschließlich Seitenansichts- und Linktracking-Treffern. Visit depth only increments for page view hits, _and_ the [Page](page.md) dimension item is not the same as the value on the previous page. Die Besuchstiefe ist auch eine besuchsbasierte Dimension, d. h., sie hat für alle Treffer im Besuch denselben Wert. In der folgenden Tabelle finden Sie einen Beispielbesuch und wie die Treffertiefe und Besuchstiefe berücksichtigt werden:

| Reihenfolge der Seiten | Treffertiefe | Wird die Besuchstiefe angerechnet? | Besuchstiefe |
| --- | --- | --- | --- |
| Startseite | 1 | Ja | 4 |
| Produktseite | 2 | Ja | 4 |
| Startseite | 3 | Ja | 4 |
| Benutzerspezifischer Link-Klick | 4 | Nein (benutzerspezifischer Link) | 4 |
| Benutzerspezifischer Link-Klick | 5 | Nein (benutzerspezifischer Link) | 4 |
| Produktseite | 6 | Ja | 4 |
| Benutzerspezifischer Link-Klick | 7 | Nein (benutzerspezifischer Link) | 4 |
| Produktseite | 8 | Nein (wie vorherige Seite) | 4 |
