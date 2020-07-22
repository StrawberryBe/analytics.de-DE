---
title: Funktionsweise
description: Verstehen Sie das Konzept der "Wiederholung"im geräteübergreifenden Analytics.
translation-type: tm+mt
source-git-commit: 2230fa2c48358346d1d449f2db335ff75c6b1631
workflow-type: tm+mt
source-wordcount: '624'
ht-degree: 1%

---


# Funktionsweise

Das geräteübergreifende Analytics gibt zwei Daten in einer Virtual Report Suite weiter:

* **Live-Heften**: CDA versucht, jeden Treffer beim Eintreten zu verbinden. Netto-neue Geräte an die Report Suite, die noch nie angemeldet sind, werden normalerweise nicht auf dieser Ebene verknüpft. Bereits erkannte Geräte werden sofort fixiert.
* **Wiederholen**: Etwa einmal pro Woche werden Daten von CDA auf der Grundlage von eindeutigen Bezeichnern, die sie gelernt hat, &quot;wiedergegeben&quot;. In dieser Phase werden neue Geräte an die Report Suite angeschlossen.

## Beispieltabelle

Die folgende Tabelle zeigt, wie die Anzahl der individuellen Personen sowohl mit den CDA-Methoden ([Feldbasierte Heften](field-based-stitching.md) und [Gerätediagramm](device-graph.md)) berechnet wird:

### Live-Heften

Sobald ein Treffer erfasst wird, versucht CDA, ihn mit bekannten Geräten zu verbinden. Betrachten wir das folgende Beispiel, in dem Bob zwei Geräte verwendet.

*Daten, die am Tag der Erfassung erscheinen:*

| Zeitstempel | ECID | eVar1 oder CustomerID | Erläuterung des Treffers | Metrik &quot;Personen&quot;(kumulativ) mit Gerätediagramm | Metrik &quot;Personen&quot;(kumulativ) mithilfe der feldbasierten Suche |
| --- | --- | --- | --- | --- | --- |
| `1` | `246` | – | Bob auf seinem Desktop-Computer, nicht authentifiziert | `1` (246) | `1` (246) |
| `2` | `246` | `Bob` | Bob meldet sich auf seinem Desktop an | `1` (246) | `2` (246 und Bob) |
| `3` | `3579` | – | Bob auf seinem Mobilgerät, nicht authentifiziert | `2` (246 und 3579) | `3` (246, Bob und 3579) |
| `4` | `3579` | `Bob` | Bob meldet sich auf einem Mobilgerät an | `2` (246 und 3579) | `3` (246, Bob und 3579) |
| `5` | `246` | – | Bob greift erneut auf Ihre Site auf dem Desktop zu, nicht authentifiziert | `2` (246 und 3579) | `3` (246, Bob und 3579) |
| `6` | `246` | `Bob` | Bob meldet sich erneut über den Desktop an | `2` (246 und 3579) | `3` (246, Bob und 3579) |
| `7` | `3579` | – | Bob ruft Ihre Site erneut auf einem Mobilgerät auf | `2` (246 und 3579) | `3` (246, Bob und 3579) |
| `8` | `3579` | `Bob` | Bob meldet sich erneut über Mobilgeräte an | `2` (246 und 3579) | `3` (246, Bob und 3579) |

Sowohl nicht authentifizierte als auch authentifizierte Treffer auf neuen Geräten werden (vorübergehend) als separate Personen gezählt.

* **Wenn Sie das Gerätediagramm verwenden,** werden nicht authentifizierte Treffer auf erkannten Geräten live geheftet, sobald ein Cluster vom Gerätediagramm veröffentlicht wird. Die Veröffentlichung von Clustern dauert zwischen drei Stunden und zwei Wochen.

   Eine dritte kumulative Person wird auch hinzugefügt, wenn ein Cluster veröffentlicht wird. Diese dritte Person repräsentiert den Cluster selbst, zusätzlich zu den einzelnen Geräten. Diese dritte &quot;Person&quot;bleibt bestehen, bis die Daten wiedergegeben werden.

   Die Zuordnung funktioniert erst dann auf allen Geräten, wenn ein Cluster veröffentlicht wurde, und auch dann nur noch live-stitches ab diesem Zeitpunkt. Im obigen Beispiel werden noch keine Treffer auf allen Geräten zugeordnet. Die geräteübergreifende Zuordnung bei vorhandenen Treffern funktioniert erst nach dem erneuten Abspielen von Heften.
* **Bei Verwendung der feldbasierten Heftfunktion werden nicht authentifizierte Treffer auf erkannten Geräten von diesem Zeitpunkt an live geheftet** .

   Die Zuordnung funktioniert, sobald die identifizierende benutzerdefinierte Variable mit einem Gerät verknüpft ist. Im obigen Beispiel werden alle Treffer mit Ausnahme der Treffer 1 und 3 live zugeschnitten (sie verwenden alle den `Bob` Bezeichner). Die Zuordnung funktioniert bei Treffern 1 und 3 nach der Wiederholungszuordnung.

### Wiederholungszuordnung

Etwa einmal pro Woche berechnet CDA historische Daten auf Grundlage von Geräten, die sie jetzt erkennt. Wenn ein Gerät Daten anfänglich sendet, ohne authentifiziert zu sein, und sich dann anmeldet, verknüpft CDA diese nicht authentifizierten Treffer mit der richtigen Person. Die folgende Tabelle stellt dieselben Daten wie oben dar, zeigt jedoch unterschiedliche Zahlen basierend auf der erneuten Wiedergabe der Daten.

*Die gleichen Daten nach der erneuten Wiedergabe:*

| Zeitstempel | ECID | eVar1 oder CustomerID | Erläuterung des Treffers | Metrik &quot;Personen&quot;(kumulativ) mit Gerätediagramm | Metrik &quot;Personen&quot;(kumulativ) mithilfe der feldbasierten Suche |
| --- | --- | --- | --- | --- | --- |
| `1` | `246` | – | Bob auf seinem Desktop-Computer, nicht authentifiziert | `1` (Cluster1) | `1` (Bob) |
| `2` | `246` | `Bob` | Bob meldet sich auf seinem Desktop an | `1` (Cluster1) | `1` (Bob) |
| `3` | `3579` | – | Bob auf seinem Mobilgerät, nicht authentifiziert | `1` (Cluster1) | `1` (Bob) |
| `4` | `3579` | `Bob` | Bob meldet sich auf einem Mobilgerät an | `1` (Cluster1) | `1` (Bob) |
| `5` | `246` | – | Bob greift erneut auf Ihre Site auf dem Desktop zu, nicht authentifiziert | `1` (Cluster1) | `1` (Bob) |
| `6` | `246` | `Bob` | Bob meldet sich erneut über den Desktop an | `1` (Cluster1) | `1` (Bob) |
| `7` | `3579` | – | Bob ruft Ihre Site erneut auf einem Mobilgerät auf | `1` (Cluster1) | `1` (Bob) |
| `8` | `3579` | `Bob` | Bob meldet sich erneut über Mobilgeräte an | `1` (Cluster1) | `1` (Bob) |

## Recap

* **Wenn Sie ein Gerätediagramm verwenden,** werden die Daten beim Veröffentlichen eines Clusters (in der Regel 3 Stunden bis 2 Wochen) zusammengeführt.
* **Bei Verwendung der feldbasierten Heftfunktion werden bei Daten,** die weniger als eine Woche alt sind, bekannte Geräte sofort zugeschnitten, aber keine neuen oder nicht erkannten Geräte sofort zugeschnitten.
* Die Daten werden einmal pro Woche wiedergegeben und ändern historische Daten in der Virtual Report Suite auf der Grundlage der Geräte, die sie identifiziert haben.
