---
description: Behebung von Fehlern und Erkennen von Problemen im Zusammenhang mit Segmenten.
title: Fehlerbehebung bei der Segmentierung
feature: Segmentation
exl-id: ca51110e-1ba7-4182-b5b2-baf9b0c017af
source-git-commit: 7a47d837eeae65f2e98123aca78029bfeb7ffe9d
workflow-type: ht
source-wordcount: '227'
ht-degree: 100%

---

# Fehlerbehebung bei der Segmentierung

## Fehler: „Inkompatible Elemente in diesem Segment“  {#incompatible}

Dieser Fehler wird angezeigt, wenn Sie versuchen, ein Segment im Data Warehouse-Ordner zu speichern und das Segment Elemente enthält, die mit Data Warehouse nicht kompatibel sind. Um den Fehler zu beheben, befolgen Sie eine der beiden folgenden Möglichkeiten:

* Speichern Sie das Segment in einem anderen Ordner.
* Entfernen oder ändern Sie die inkompatiblen Segmentbestandteile.

## Warum gibt mein Segment überhaupt keine Daten zurück? {#no-data}

Mögliche Gründe:

* Inverse Verschachtelung – beispielsweise die Verschachtelung eines Containers für Besucher in einem Container für Besuche.
* Der Bericht unterstützt keine Segmentierung.
* Es stimmen keine Daten mit den Segmentierungskriterien überein.

## Warum sehe ich das Segment, das ich erstellt habe, nicht im Segment-Manager? {#invisible}

Mögliche Gründe:

* Einige Dimensionen sind nur in Data Warehouse und nicht im Segment-Manager verfügbar.
* Das Segment ist mit Reports &amp; Analytics nicht kompatibel.
* Das Segment ist nur für eine bestimmte Report Suite aktiviert.
* Ein freigegebenes Segment wurde möglicherweise von einem anderen Benutzer gelöscht.
* Segmente konnten aufgrund eines Problems mit dem Datencenter oder dem Browser-Cache nicht geladen werden.
* Das Segment wurde nicht gespeichert.
* Die IP-Adresse ist möglicherweise auf Seiten des Benutzers gesperrt.

## Warum sind die Seitendaten, die nach dem Anwenden eines Segments angezeigt werden, falsch? {#page-data}

Mögliche Gründe:

* Die Regeln/Operatoren sind für das erforderliche Ergebnis inkorrekt.
* Container wurden falsch auf das Segment angewendet.
* Traffic-Variablen, die zur Segmentierung verwendet werden, sind nicht richtig eingestellt oder abgelaufen.
