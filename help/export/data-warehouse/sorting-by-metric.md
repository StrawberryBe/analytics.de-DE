---
description: Bietet nach Rang geordnet Detailberichte in Data Warehouse, die nach absteigendem Metrikwert sortiert sind.
title: Nach Metrik sortieren
uuid: 07da2607-b3fd-463b-90d4-6884a93c7e25
translation-type: ht
source-git-commit: 99ee24efaa517e8da700c67818c111c4aa90dc02
workflow-type: ht
source-wordcount: '322'
ht-degree: 100%

---


# Nach Metrik sortieren

Bietet nach Rang geordnet Detailberichte in Data Warehouse, die nach absteigendem Metrikwert sortiert sind.

Die Sortierung nach Metrik erleichtert die Interpretation von Data Warehouse-Berichten und den Vergleich mit anderen Ansichten von Analytics-Aufschlüsselungsberichten.

Im Folgenden sehen Sie, wie die Option „Sortieren von Metriken“ die Zeilen in einem Data Warehouse-Bericht neu sortiert.

Es gibt vier verschiedene Möglichkeiten, um Data Warehouse-Berichte mit „Sortieren von Metriken“ zu organisieren, die darauf basieren, wie die Datengranularität, Berichtsdimensionen oder Metriken konfiguriert sind und ob die maximale Zeilenzahl festgelegt ist:

* **Layout 1**: Zeileneinträge werden in Wörterbuchreihenfolge sortiert (Standard). Wenn die maximale Zeilenzahl festgelegt ist, werden nur die ersten N Zeilen in den Bericht einbezogen.
* **Layout 2**: Data Warehouse wendet eine Metriksortierung auf alle Zeilen im Bericht an. Beziehungen im ersten Metrikwert werden durch die zweite Metrik aufgelöst, dann durch die dritte und so weiter. Wenn alle Metriken verbunden sind, wird die standardmäßige Wörterbuchreihenfolge des aufgeschlüsselten Zeileneintrags angewendet.
* **Layout 3**: Wie Layout 2, jedoch werden nur die ersten N Zeilen (d. h. der für die maximale Zeilenzahl festgelegte Wert) im Bericht ausgegeben.
* **Layout 4**: Wie Layout 2, außer dass Zeileneinträge für die einzelnen Granularitätszeiträume gruppiert und innerhalb des jeweiligen Zeitraums sortiert werden.

In der Spalte „Berichtslayout“ sehen Sie, wie „Sortieren von Metriken“ mit anderen Berichterstellungsoptionen von Data Warehouse interagiert.

| Nach Metrik sortieren? | Metriken vorhanden? | Aufschlüsselungen vorhanden? | Datumsgranularität? | Maximale Zeilenzahl festgelegt? | Berichtslayout |
|---|---|---|---|---|---|
| Nein | Ja oder Nein | Ja oder Nein | Ja oder Nein | Ja oder Nein | 1 |
| Ja | Nein | Ja oder Nein | Ja oder Nein | Ja oder Nein | 1 |
| Ja | Ja | Nein | Nein | nicht angegeben | 1 |
| Ja | Ja | Nein | Ja oder Nein | Nein | 1 |
| Ja | Ja | Ja | Nein | Nein | 2 |
| Ja | Ja | Nein | Ja | Ja | 3 |
| Ja | Ja | Ja | Ja oder Nein | Ja | 3 |
| Ja | Ja | Ja | Ja | Nein | 4 |

