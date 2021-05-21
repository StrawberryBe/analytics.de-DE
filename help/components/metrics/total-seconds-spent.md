---
title: Gesamtbesuchszeit in Sekunden
description: Die aggregierte Gesamtanzahl der Sekunden, die mit dem Dimensionselement verbracht wurden.
exl-id: 02302982-ce8c-44e9-9967-0a4f226f5e9e
translation-type: ht
source-git-commit: 549258b0168733c7b0e28cb8b9125e68dffd5df7
workflow-type: ht
source-wordcount: '201'
ht-degree: 100%

---

# Gesamtbesuchszeit in Sekunden

Die Metrik „Gesamtbesuchszeit in Sekunden“ gibt die aggregierte Anzahl der Sekunden an, die ein Besucher mit einem bestimmten Dimensionselement verbracht hat. Diese Metrik ist nützlich, wenn Sie die für ein bestimmtes Dimensionselement aufgewendete Rohzeit und nicht Durchschnittswerte wie bei anderen Besuchszeit-Metriken wünschen.

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
