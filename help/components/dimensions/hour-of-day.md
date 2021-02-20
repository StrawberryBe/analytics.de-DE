---
title: Stunde des Tages
description: Die numerische Stunde des Tages, unabhängig vom Tag.
translation-type: tm+mt
source-git-commit: e758c070f402113b6d8a9069437b53633974a3e9
workflow-type: tm+mt
source-wordcount: '356'
ht-degree: 100%

---


# Stunde des Tages

Die Dimension „Stunde des Tages“ erfasst die numerische Stunde eines Tages als Dimensionselement. Wenn Sie beispielsweise einen Bericht haben, der sich vom 1. Januar bis zum 7. Januar erstreckt, wird die erste Stunde jedes Tages in dasselbe Dimensionselement gruppiert. Dieser Bericht ist nützlich, wenn Sie einen Bericht nach relativer Tageszeit aufschlüsseln möchten, aber keine statischen Stunden als Dimensionselemente wünschen. Er ist besonders nützlich als Dimension in terminierten Berichten, da diese Dimension mit dem ausgewählten Datumsbereich rolliert.

Diese Dimension basiert auf der Zeitzone der Report Suite und nicht auf der lokalen Zeitzone des Besuchers. Wenn Ihre Report Suite beispielsweise in der Zeitzone „Mountain Time“ liegt und ein Besucher in Kalifornien Ihre Site um 10:00 Uhr „Pacific-Zeit“ besucht, werden die Treffergruppen unter dem Dimensionselement `11:00 AM` angezeigt. Wenn Sie eine Dimension wünschen, die die Zeit des lokalen Besuchers erfasst, empfiehlt Adobe die Verwendung des Plug-Ins [getTimeParting](/help/implement/vars/plugins/gettimeparting.md).

## Füllen dieser Dimension mit Daten

Diese Dimension ist bei allen Implementierungen vorkonfiguriert. Wenn eine Report Suite Daten enthält, funktioniert diese Dimension.

## Dimensionselemente

Zu den Dimensionselementen gehören `12:00 AM` – `11:00 PM`, die die Stunde des Tages darstellen, in der der Treffer auftrat (abgerundet). Wenn beispielsweise ein Treffer um 15:58 Uhr generiert wurde, wird er unter dem Dimensionselement `3:00 PM` gruppiert.

## Sommerzeit

Die Sommerzeit ist eine Praxis, bei der die Uhren im Frühjahr eine Stunde im Voraus und im Herbst eine Stunde zurückgestellt werden. Wenn die Zeitzone einer Report Suite die Sommerzeit verwendet, passt Adobe die Daten für diese Stunde entsprechend an.

* **Wenn die Sommerzeit beginnt**: Im März zeigen Berichte in der Regel eine Datenlücke von einer Stunde, wenn die Sommerzeit beginnt. Die Stunde existierte nicht, daher ist sie nicht Teil der Datenerfassung. Beachten Sie, dass eine kleine Datenmenge trotzdem in dieser Stunde angezeigt kann. Die Adobe-Datenerfassungs-Server benötigen einige Sekunden (bis zu einer Minute), um die Sommerzeitanpassungen zu berücksichtigen.
* **Wenn die Sommerzeit endet**: Im November wird in Berichten normalerweise eine doppelt gestapelte Stunde angezeigt, wenn die Sommerzeit endet. Die Stunde ist zweimal passiert, daher werden beide Stunden in Berichten zusammengefasst.
