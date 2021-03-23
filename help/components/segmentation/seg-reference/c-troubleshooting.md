---
description: Behebung von Fehlern und Erkennen von Problemen im Zusammenhang mit Segmenten.
title: Fehlerbehebung bei der Segmentierung
uuid: 8476d617-4b44-4ff2-9b3a-02685f666afc
translation-type: ht
source-git-commit: 5d8032a9806836e7d0ecbd7fa3652ed1fd137e89
workflow-type: ht
source-wordcount: '227'
ht-degree: 100%

---


# Fehlerbehebung bei der Segmentierung

## Fehler: „Inkompatible Elemente in diesem Segment“ {#section_B167EE10A0844E649DD7E14D0BAEDA17}

Dieser Fehler wird angezeigt, wenn Sie versuchen, ein Segment im Data Warehouse-Ordner zu speichern und das Segment Elemente enthält, die mit Data Warehouse nicht kompatibel sind. Um den Fehler zu beheben, befolgen Sie eine der beiden folgenden Möglichkeiten:

* Speichern Sie das Segment in einem anderen Ordner.
* Entfernen oder ändern Sie die inkompatiblen Segmentbestandteile.

## Warum gibt mein Segment überhaupt keine Daten zurück? {#section_999749CBBE984142AEA49A6E68E6730A}

Mögliche Gründe:

* Inverse Verschachtelung – beispielsweise die Verschachtelung eines Containers für Besucher in einem Container für Besuche.
* Der Bericht unterstützt keine Segmentierung.
* Es stimmen keine Daten mit den Segmentierungskriterien überein.

## Warum sehe ich das Segment, das ich erstellt habe, nicht im Segment-Manager? {#section_BE0A0930A2694A23BB32DA71696D52CE}

Mögliche Gründe:

* Einige Dimensionen sind nur in Data Warehouse und nicht im Segment-Manager verfügbar.
* Das Segment ist mit Reports &amp; Analytics nicht kompatibel.
* Das Segment ist nur für eine bestimmte Report Suite aktiviert.
* Ein freigegebenes Segment wurde möglicherweise von einem anderen Benutzer gelöscht.
* Segmente konnten aufgrund eines Problems mit dem Datencenter oder dem Browser-Cache nicht geladen werden.
* Das Segment wurde nicht gespeichert.
* Die IP-Adresse ist möglicherweise auf Seiten des Benutzers gesperrt.

## Warum sind die Seitendaten, die nach dem Anwenden eines Segments angezeigt werden, falsch? {#section_B226AF69FE06463A8BC5337FDA8D4949}

Mögliche Gründe:

* Die Regeln/Operatoren sind für das erforderliche Ergebnis inkorrekt.
* Container wurden falsch auf das Segment angewendet.
* Traffic-Variablen, die zur Segmentierung verwendet werden, sind nicht richtig eingestellt oder abgelaufen.

