---
title: Treffertiefe
description: Die Anzahl der Treffer im Besuch.
translation-type: ht
source-git-commit: d3f92d72207f027d35f81a4ccf70d01569c3557f
workflow-type: ht
source-wordcount: '261'
ht-degree: 100%

---


# Treffertiefe

Die Dimension „Treffertiefe“ gibt an, wie weit ein bestimmter Treffer in einem Besuch liegt. Diese Dimension ist hilfreich, um zu verstehen, wie weit innerhalb eines Besuchs die Besucher Aktionen auf Ihrer Site ausführen. Die Treffertiefe zählt alle Arten von Treffern, einschließlich Seitenansicht-Treffern ([`t()`](/help/implement/vars/functions/t-method.md)) und Linktracking-Treffern ([`tl()`](/help/implement/vars/functions/tl-method.md)).

## Füllen dieser Dimension mit Daten

Diese Dimension ist bei allen Implementierungen vorkonfiguriert. Wenn eine Report Suite Daten enthält, funktioniert diese Dimension.

## Dimensionselemente

Zu den Dimensionselementen zählen die Zeichenfolge `"Hit Depth"`, gefolgt von einer Zahl, die die Anzahl der Treffer im Besuch darstellt. Das Dimensionselement von `"Hit Depth 1"` steht für den ersten Treffer des Besuchs, während das Dimensionselement `"Hit Depth 8"` den achten Treffer des Besuchs darstellt.

## Vergleich mit Besuchstiefe

Die Treffertiefe zählt alle Arten von Treffern, einschließlich Seitenansichts- und Linktracking-Treffern. Die Besuchstiefe wird nur bei Seitenansicht-Treffern erhöht _und_ das Dimensionselement [Seite](page.md) ist nicht derselbe wie der Wert auf der vorherigen Seite. Die Besuchstiefe ist auch eine besuchsbasierte Dimension, d. h., sie hat für alle Treffer im Besuch denselben Wert. In der folgenden Tabelle finden Sie einen Beispielbesuch und wie die Treffertiefe und Besuchstiefe berücksichtigt werden:

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
