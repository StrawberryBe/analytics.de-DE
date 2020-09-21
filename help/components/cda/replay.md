---
title: Funktionsweise der Wiederholung
description: Verstehen Sie das Konzept der „Wiederholung“ in der geräteübergreifenden Analyse.
translation-type: ht
source-git-commit: 2230fa2c48358346d1d449f2db335ff75c6b1631
workflow-type: ht
source-wordcount: '624'
ht-degree: 100%

---


# Funktionsweise der Wiederholung

Die geräteübergreifende Analyse läuft in einer Virtual Report Suite zweimal über die Daten:

* **Live-Stitching**: die geräteübergreifende Analyse versucht, jeden Treffer beim Eintreten zu zuzuordnen. Neue Geräte in der Report Suite, die sich noch nie angemeldet haben, werden in der Regel nicht auf dieser Ebene zugeordnet. Bereits erkannte Geräte werden sofort zugeordnet.
* **Wiederholung**: Ungefähr einmal pro Woche „wiederholt“ die geräteübergreifende Analyse die Daten anhand der gelernten eindeutigen Kennungen. In dieser Phase werden neue Geräte in der Report Suite zugeordnet.

## Beispieltabelle

Die folgenden Tabellen veranschaulichen, wie beide CDA-Methoden ([Feldbasiertes Stitching](field-based-stitching.md) und [Gerätediagramm](device-graph.md)) die Anzahl der eindeutigen Personen berechnen: 

### Live-Stitching

Sobald ein Treffer erfasst wird, versucht die geräteübergreifende Analyse, ihn bekannten Geräten zuzuordnen. Betrachten wir das folgende Beispiel, in dem Bob zwei Geräte verwendet.

*Daten, wie sie am Tag der Erfassung erscheinen:*

| Zeitstempel | ECID | eVar1 oder CustomerID | Erläuterung des Treffers | Metrik „Personen“ (kumulativ) mit Gerätediagramm | Metrik „Personen“ (kumulativ) mit feldbasiertem Stitching |
| --- | --- | --- | --- | --- | --- |
| `1` | `246` | – | Bob auf seinem Desktop-Computer, nicht authentifiziert | `1` (246) | `1` (246) |
| `2` | `246` | `Bob` | Bob meldet sich auf seinem Desktop an. | `1` (246) | `2` (246 und Bob) |
| `3` | `3579` | – | Bob auf seinem Mobilgerät, nicht authentifiziert | `2` (246 und 3579) | `3` (246, Bob und 3579) |
| `4` | `3579` | `Bob` | Bob meldet sich auf einem Mobilgerät an | `2` (246 und 3579) | `3` (246, Bob und 3579) |
| `5` | `246` | – | Bob greift erneut auf Ihre Site auf dem Desktop zu, nicht authentifiziert | `2` (246 und 3579) | `3` (246, Bob und 3579) |
| `6` | `246` | `Bob` | Bob meldet sich erneut auf seinem Desktop an | `2` (246 und 3579) | `3` (246, Bob und 3579) |
| `7` | `3579` | – | Bob ruft Ihre Site erneut auf einem Mobilgerät auf | `2` (246 und 3579) | `3` (246, Bob und 3579) |
| `8` | `3579` | `Bob` | Bob meldet sich erneut auf einem Mobilgerät an | `2` (246 und 3579) | `3` (246, Bob und 3579) |

Sowohl nicht authentifizierte als auch authentifizierte Treffer auf neuen Geräten werden (vorübergehend) als separate Personen gezählt.

* **Wenn Sie das Gerätediagramm verwenden**, werden nicht authentifizierte Treffer auf erkannten Geräten live zugeordnet, sobald ein Cluster vom Gerätediagramm veröffentlicht wird. Die Veröffentlichung von Clustern dauert zwischen drei Stunden und zwei Wochen.

   Eine dritte kumulative Person wird ebenfalls hinzugefügt, wenn ein Cluster veröffentlicht wird. Diese dritte Person repräsentiert den Cluster selbst, zusätzlich zu den einzelnen Geräten. Diese dritte „Person“ bleibt bestehen, bis die Daten wiedergegeben werden.

   Die Zuordnung funktioniert geräteübergreifend erst nach der Veröffentlichung eines Clusters, und selbst dann wird erst ab diesem Zeitpunkt live zugeordnet. Im obigen Beispiel werden noch keine Treffer geräteübergreifend zugeordnet. Die geräteübergreifende Attribution bei vorhandenen Treffern funktioniert erst nach der Wiederholungszuordnung.
* **Wenn feldbasiertes Stitching verwendet wird**, werden nicht authentifizierte Treffer auf erkannten Geräten von diesem Punkt an live zugeordnet.

   Die Attribution funktioniert, sobald die identifizierende benutzerdefinierte Variable mit einem Gerät verknüpft ist. Im obigen Beispiel werden alle Treffer mit Ausnahme der Treffer 1 und 3 live zugeordnet (sie verwenden alle die Kennung `Bob`). Die Attribution funktioniert bei Treffern 1 und 3 nach der Wiederholungszuordnung.

### Wiederholungszuordnung

Ungefähr einmal pro Woche berechnet die geräteübergreifende Analyse historische Daten basierend auf Geräten, die sie jetzt erkennt, neu. Wenn ein Gerät Daten anfänglich sendet, ohne authentifiziert zu sein, und sich dann anmeldet, verknüpft die geräteübergreifende Analyse diese nicht authentifizierten Treffer mit der richtigen Person. Die folgende Tabelle stellt dieselben Daten wie oben dar, zeigt jedoch unterschiedliche Zahlen basierend auf der Wiederholung der Daten.

*Dieselben Daten nach der Wiederholung:*

| Zeitstempel | ECID | eVar1 oder CustomerID | Erläuterung des Treffers | Metrik „Personen“ (kumulativ) mit Gerätediagramm | Metrik „Personen“ (kumulativ) mit feldbasiertem Stitching |
| --- | --- | --- | --- | --- | --- |
| `1` | `246` | – | Bob auf seinem Desktop-Computer, nicht authentifiziert | `1` (Cluster1) | `1` (Bob) |
| `2` | `246` | `Bob` | Bob meldet sich auf seinem Desktop an. | `1` (Cluster1) | `1` (Bob) |
| `3` | `3579` | – | Bob auf seinem Mobilgerät, nicht authentifiziert | `1` (Cluster1) | `1` (Bob) |
| `4` | `3579` | `Bob` | Bob meldet sich auf einem Mobilgerät an | `1` (Cluster1) | `1` (Bob) |
| `5` | `246` | – | Bob greift erneut auf Ihre Site auf dem Desktop zu, nicht authentifiziert | `1` (Cluster1) | `1` (Bob) |
| `6` | `246` | `Bob` | Bob meldet sich erneut auf seinem Desktop an | `1` (Cluster1) | `1` (Bob) |
| `7` | `3579` | – | Bob ruft Ihre Site erneut auf einem Mobilgerät auf | `1` (Cluster1) | `1` (Bob) |
| `8` | `3579` | `Bob` | Bob meldet sich erneut auf einem Mobilgerät an | `1` (Cluster1) | `1` (Bob) |

## Zusammenfassung

* **Wenn Sie ein Gerätediagramm verwenden**, werden die Daten bei der Veröffentlichung eines Clusters zugeordnet (normalerweise 3 Stunden bis 2 Wochen).
* **Bei Verwendung von feldbasiertem Stitching** werden Daten, die weniger als eine Woche alt sind, sofort bekannten Geräten zugeordnet, neue oder nicht erkannte Geräte werden jedoch nicht sofort zugeordnet.
* Die Daten werden einmal pro Woche wiederholt und historische Daten in der Virtual Report Suite auf der Grundlage der Geräte geändert, deren Identifizierung gelernt wurde.
