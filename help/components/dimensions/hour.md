---
title: Stunde
description: Die Stunde, in der die Metrik aufgetreten ist.
translation-type: ht
source-git-commit: e758c070f402113b6d8a9069437b53633974a3e9
workflow-type: ht
source-wordcount: '242'
ht-degree: 100%

---


# Stunde

Die Dimension „Stunde“ zeigt die Stunde an, in der eine bestimmte Metrik aufgetreten ist (abgerundet). Das erste Dimensionselement ist die erste Stunde im Datumsbereich und das letzte Dimensionselement die letzte Stunde im Datumsbereich. Diese Dimension ist für Trend-Berichte hilfreich, da sie es Ihnen ermöglicht, Metriken im Zeitverlauf anzuzeigen.

## Füllen dieser Dimension mit Daten

Diese Dimension ist bei allen Implementierungen vorkonfiguriert. Wenn eine Report Suite Daten enthält, funktioniert diese Dimension.

## Dimensionselemente

Die Dimensionelemente enthalten eine bestimmte Stunde innerhalb des Datumsbereichs eines Berichts und deren Datum. Sie sind als `HH:HH YYYY-MM-DD` formatiert.

## Sommerzeit

Die Sommerzeit ist eine Praxis, bei der die Uhren im Frühjahr eine Stunde im Voraus und im Herbst eine Stunde zurückgestellt werden. Wenn die Zeitzone einer Report Suite die Sommerzeit verwendet, passt Adobe die Daten für diese Stunde entsprechend an.

* **Wenn die Sommerzeit beginnt**: Im März zeigen Berichte in der Regel eine Datenlücke von einer Stunde, wenn die Sommerzeit beginnt. Die Stunde existierte nicht, daher ist sie nicht Teil der Datenerfassung. Beachten Sie, dass eine kleine Datenmenge trotzdem in dieser Stunde angezeigt kann. Die Adobe-Datenerfassungs-Server benötigen einige Sekunden (bis zu einer Minute), um die Sommerzeitanpassungen zu berücksichtigen.
* **Wenn die Sommerzeit endet**: Im November wird in Berichten normalerweise eine doppelt gestapelte Stunde angezeigt, wenn die Sommerzeit endet. Die Stunde ist zweimal passiert, daher werden beide Stunden in Berichten zusammengefasst.
