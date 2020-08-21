---
title: Gesamtbesuchszeit in Sekunden
description: Die aggregierte Gesamtdauer der auf das Dimensionselement verbrachten Sekunden.
translation-type: tm+mt
source-git-commit: d3f92d72207f027d35f81a4ccf70d01569c3557f
workflow-type: tm+mt
source-wordcount: '201'
ht-degree: 64%

---


# Gesamtbesuchszeit in Sekunden

Die Metrik &quot;Gesamtbesuchszeit&quot;zeigt die aggregierte Anzahl der Sekunden, die ein Besucher für ein bestimmtes Dimensionselement verbracht hat. Diese Metrik ist hilfreich, wenn Sie die Rohzeit für ein bestimmtes Dimensionselement und nicht wie andere Besuchszeitmetriken-Angebot ermitteln möchten.

In Report Builder heißt diese Metrik „Gesamtbesuchszeit“.

## Berechnung dieser Metrik

Diese Metrik verwendet die folgenden Schritte zur Berechnung:

1. Sehen Sie sich für einen bestimmten Treffer den Zeitstempel an.
2. Vergleichen Sie diesen Treffer mit dem Zeitstempel des nächsten Treffers im Besuch. Sowohl Seitenansichts- als auch Linktracking-Treffer werden gezählt.
3. Die Zeit in Sekunden, die zwischen den beiden Treffern vergangen ist, trägt zum Dimensionselement bei.

Beständige Variablen wie [eVars](../dimensions/evar.md) werden auf die Gesamtbesuchszeit in Sekunden angerechnet. Zu den Traffic-Variablen, wie [Props](../dimensions/prop.md), gehören Sekunden, die mit nachfolgenden Linktracking-Aufrufe verbracht werden.

>[!TIP]
>
>Die Besuchszeit wird beim letzten Treffer des Besuchs nicht gemessen, da keine nachfolgende Bildanforderung zur Messung der verstrichenen Zeit vorliegt. Dieses Konzept gilt auch für Besuche, die aus einem einzelnen Treffer (einem Absprung) bestehen.

Allgemeine Informationen zur Besuchszeit finden Sie unter [Besuchszeit – Übersicht](time-spent.md).
