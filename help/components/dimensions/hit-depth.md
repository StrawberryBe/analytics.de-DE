---
title: Treffertiefe
description: Die Anzahl der Treffer im Besuch.
translation-type: tm+mt
source-git-commit: d3f92d72207f027d35f81a4ccf70d01569c3557f
workflow-type: tm+mt
source-wordcount: '261'
ht-degree: 7%

---


# Treffertiefe

Die Dimension &quot;Treffertiefe&quot;zeigt an, wie weit ein Besuch bei einem bestimmten Treffer dauert. Diese Dimension ist ein wertvolles Verständnis dafür, wie weit ein Besuch dauert, an dem Besucher Aktionen auf Ihrer Site durchführen. Die Treffertiefe zählt alle Arten von Treffern, einschließlich Seitenaufrufen ([`t()`](/help/implement/vars/functions/t-method.md))und Linktracking-Treffern ([`tl()`](/help/implement/vars/functions/tl-method.md)).

## Diese Dimension mit Daten füllen

Diese Dimension funktioniert bei allen Implementierungen standardmäßig. Wenn eine Report Suite Daten enthält, funktioniert diese Dimension.

## Dimensionselemente

Dimensionselemente enthalten die Zeichenfolge `"Hit Depth"` gefolgt von einer Zahl, die die Anzahl der Treffer im Besuch darstellt. Das Dimensionselement von `"Hit Depth 1"` stellt den ersten Treffer des Besuchs dar, während das Dimensionselement den achten Treffer des Besuchs `"Hit Depth 8"` darstellt.

## Vergleich mit Besuchstiefe

Die Treffertiefe zählt alle Arten von Treffern, einschließlich der Ansicht von Seiten- und Linktracking-Treffern. Die Besuchstiefe wird nur für Treffer auf der Ansicht der Seite erhöht, _und_ das Dimensionselement &quot; [Seite](page.md) &quot;ist nicht mit dem Wert auf der vorherigen  identisch. Die Besuchstiefe ist auch eine besuchsbasierte Dimension, d. h., sie ist für alle Treffer im Besuch derselbe Wert. In der folgenden Tabelle sind ein Beispielbesuch und die Berücksichtigung der Treffertiefe und Besuchstiefe aufgeführt:

| Seitensequenz | Treffertiefe | Zählt zur Besuchstiefe? | Besuchstiefe |
| --- | --- | --- | --- |
| Startseite | 1 | Ja | 4 |
| Produktseite | 2 | Ja | 4 |
| Startseite | 3 | Ja | 4 |
| Benutzerspezifischer Link | 4 | Nein (benutzerspezifischer Link) | 4 |
| Benutzerspezifischer Link | 5 | Nein (benutzerspezifischer Link) | 4 |
| Produktseite | 6 | Ja | 4 |
| Benutzerspezifischer Link | 7 | Nein (benutzerspezifischer Link) | 4 |
| Produktseite | 8 | Nein (entspricht der vorherigen Seite) | 4 |
