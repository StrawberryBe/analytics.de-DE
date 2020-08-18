---
title: Stunde des Tages
description: Die numerische Stunde des Tages, unabhängig vom Tag.
translation-type: tm+mt
source-git-commit: e758c070f402113b6d8a9069437b53633974a3e9
workflow-type: tm+mt
source-wordcount: '356'
ht-degree: 8%

---


# Stunde des Tages

Die Dimension &quot;Stunde des Tages&quot;erfasst die numerische Stunde eines Tages als Dimensionselement. Wenn Sie z. B. einen Bericht vom 1. Januar bis 7. Januar haben, gruppiert sich die erste Stunde jedes Tages in demselben Dimensionselement. Dieser Bericht ist nützlich, wenn Sie möchten, dass ein Bericht nach der relativen Tageszeit aufgeschlüsselt wird, aber keine statischen Stunden als Dimensionselemente wünschen. Es ist besonders nützlich als Dimension in eingeplanten Berichten, da diese Dimension mit dem ausgewählten Datumsbereich rolliert.

Diese Dimension basiert auf der Zeitzone der Report Suite und nicht auf der Zeitzone des Besuchers. Wenn Ihre Report Suite beispielsweise in Mountain Time liegt und ein Besucher in Kalifornien Ihre Site um 10:00 Uhr Pacific-Zeit besucht, werden die Treffergruppen unter dem `11:00 AM` Dimensionselement angezeigt. Wenn Sie eine Dimension wünschen, die die Zeit des lokalen Besuchers aufzeichnet, empfiehlt Adobe die Verwendung des Plug-Ins [getTimeParting](/help/implement/vars/plugins/gettimeparting.md) .

## Füllen dieser Dimension mit Daten

Diese Dimension ist bei allen Implementierungen vorkonfiguriert. Wenn eine Report Suite Daten enthält, funktioniert diese Dimension.

## Dimensionen

Zu den Elementen der Dimension zählen `12:00 AM` - `11:00 PM`, die die Stunde des Treffers (abgerundet) darstellen. Wenn beispielsweise um 15:58 Uhr ein Treffer generiert wurde, gruppiert er sich unter dem Dimensionselement `3:00 PM`.

## Sommerzeit

Die Sommerzeit ist eine Praxis, bei der Uhren eine Stunde vor dem Frühling und im Herbst eine Stunde zurückgestellt werden. Wenn die Zeitzone einer Report Suite DST verwendet, passt die Adobe die Daten für diese Stunde entsprechend an.

* **Wenn die Sommerzeit beginnt**: Im März zeigen Berichte in der Regel eine Stundenlücke in den Daten an, bei denen die Sommerzeit Beginn einspart. Die Stunde war nicht vorhanden, daher ist sie nicht Teil der Datenerfassung. Beachten Sie, dass eine kleine Datenmenge in diese Stunde hineinreichen kann. Die Berücksichtigung von DST-Anpassungen dauert bei den Datenerfassungsservern in der Adobe mehrere Sekunden (bis zu einer Minute).
* **Wenn die Sommerzeit endet**: Im November zeigt der Bericht in der Regel eine gestapelte Dublette an, in der die Sommerzeit endet. Die Stunde ist zweimal passiert, sodass beide Stunden in Berichten zusammengefasst werden.
