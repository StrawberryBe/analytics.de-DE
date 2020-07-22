---
title: Stunde des Tages
description: Die numerische Stunde des Tages, unabhängig vom Tag.
translation-type: tm+mt
source-git-commit: d3f92d72207f027d35f81a4ccf70d01569c3557f
workflow-type: tm+mt
source-wordcount: '221'
ht-degree: 0%

---


# Stunde des Tages

Die Dimension &quot;Stunde des Tages&quot;erfasst die numerische Stunde eines Tages als Dimensionselement. Wenn Sie z. B. einen Bericht vom 1. Januar bis 7. Januar haben, gruppiert sich die erste Stunde jedes Tages in demselben Dimensionselement. Dieser Bericht ist nützlich, wenn Sie möchten, dass ein Bericht nach der relativen Tageszeit aufgeschlüsselt wird, aber keine statischen Stunden als Dimensionselemente wünschen. Es ist besonders nützlich als Dimension in eingeplanten Berichten, da diese Dimension mit dem ausgewählten Datumsbereich rolliert.

Diese Dimension basiert auf der Zeitzone der Report Suite und nicht auf der Zeitzone des Besuchers. Wenn Ihre Report Suite beispielsweise in Mountain Time liegt und ein Besucher in Kalifornien Ihre Site um 10:00 Uhr Pacific-Zeit besucht, werden die Treffergruppen unter dem `11:00 AM` Dimensionselement angezeigt. Wenn Sie eine Dimension wünschen, die die Zeit des lokalen Besuchers aufzeichnet, empfiehlt Adobe die Verwendung des [getTimeParting](/help/implement/vars/plugins/gettimeparting.md) -Plug-Ins.

## Diese Dimension mit Daten füllen

Diese Dimension funktioniert bei allen Implementierungen standardmäßig. Wenn eine Report Suite Daten enthält, funktioniert diese Dimension.

## Dimensionselemente

Zu den Dimensionselementen zählen `12:00 AM` - `11:00 PM`, die die Stunde des Tages darstellen, an dem der Treffer stattgefunden hat (abgerundet). Wenn beispielsweise um 15:58 Uhr ein Treffer generiert wurde, gruppiert er sich unter dem Dimensionselement `3:00 PM`.
