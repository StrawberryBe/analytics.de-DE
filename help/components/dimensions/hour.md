---
title: Stunde
description: Die Stunde, in der die Metrik aufgetreten ist.
translation-type: tm+mt
source-git-commit: e758c070f402113b6d8a9069437b53633974a3e9
workflow-type: tm+mt
source-wordcount: '242'
ht-degree: 10%

---


# Stunde

Die Dimension &quot;Stunde&quot;gibt die Stunde an, zu der eine bestimmte Metrik aufgetreten ist (abgerundet). Das erste Dimensionselement ist die erste Stunde im Datumsbereich und das letzte Dimensionselement die letzte Stunde im Datumsbereich. Diese Dimension ist für Trendberichte nützlich, da sie Ihnen die Anzeige von Metriken im Zeitverlauf ermöglicht.

## Füllen dieser Dimension mit Daten

Diese Dimension ist bei allen Implementierungen vorkonfiguriert. Wenn eine Report Suite Daten enthält, funktioniert diese Dimension.

## Dimensionen

Dimensionen beinhalten eine bestimmte Stunde innerhalb des Datumsbereichs eines Berichts neben dem Datum. Es ist formatiert wie `HH:HH YYYY-MM-DD`.

## Sommerzeit

Die Sommerzeit ist eine Praxis, bei der Uhren eine Stunde vor dem Frühling und im Herbst eine Stunde zurückgestellt werden. Wenn die Zeitzone einer Report Suite DST verwendet, passt die Adobe die Daten für diese Stunde entsprechend an.

* **Wenn die Sommerzeit beginnt**: Im März zeigen Berichte in der Regel eine Stundenlücke in den Daten an, bei denen die Sommerzeit Beginn einspart. Die Stunde war nicht vorhanden, daher ist sie nicht Teil der Datenerfassung. Beachten Sie, dass eine kleine Datenmenge in diese Stunde hineinreichen kann. Die Berücksichtigung von DST-Anpassungen dauert bei den Datenerfassungsservern in der Adobe mehrere Sekunden (bis zu einer Minute).
* **Wenn die Sommerzeit endet**: Im November zeigt der Bericht in der Regel eine gestapelte Dublette an, in der die Sommerzeit endet. Die Stunde ist zweimal passiert, sodass beide Stunden in Berichten zusammengefasst werden.
