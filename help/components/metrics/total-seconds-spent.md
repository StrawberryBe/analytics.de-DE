---
title: Gesamtbesuchszeit in Sekunden
description: Die aggregierte Gesamtanzahl der Sekunden, die für den Dimensionswert verbracht wurden.
translation-type: tm+mt
source-git-commit: c4833525816d81175a3446215eb92310ee4021dd
workflow-type: tm+mt
source-wordcount: '201'
ht-degree: 9%

---


# Gesamtbesuchszeit in Sekunden

Die Metrik &quot;Gesamtbesuchszeit&quot;zeigt die aggregierte Anzahl der Sekunden an, die ein Besucher für einen bestimmten Dimensionswert verbracht hat. Diese Metrik ist hilfreich, wenn Sie die Rohzeit für einen bestimmten Dimensionswert und nicht wie andere Angebot für Besuchszeitmetriken ermitteln möchten.

In ReportBuilder heißt diese Metrik &quot;Gesamtbesuchszeit&quot;.

## Berechnung dieser Metrik

Diese Metrik verwendet die folgenden Schritte zur Berechnung:

1. Sehen Sie sich für einen bestimmten Treffer den Zeitstempel an.
2. Vergleichen Sie diesen Treffer mit dem Zeitstempel des nächsten Treffers im Besuch. Sowohl die Ansicht als auch die Linktracking-Treffer werden gezählt.
3. Die Zeit in Sekunden, die zwischen den beiden Treffern vergangen ist, trägt zum Dimensionswert bei.

Beständige Variablen wie [eVars](../dimensions/evar.md)werden als Gesamtdauer in Sekunden gezählt. Traffic-Variablen wie [Props](../dimensions/prop.md)enthalten Sekunden, die über nachfolgende Linkverfolgungsaufrufe verbracht wurden.

>[!TIP]
>
>Die Besuchszeit wird nicht für den letzten Treffer des Besuchs gemessen, da es keine nachfolgende Bildanforderung zur Messung der verstrichenen Zeit gibt. Dieses Konzept gilt auch für Besuche, die aus einem einzelnen Treffer (einem Absprung) bestehen.

Allgemeine Informationen zur Besuchszeit finden Sie unter Übersicht über die [Besuchszeit](time-spent.md) .
