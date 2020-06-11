---
title: Stunde des Tages
description: Die numerische Stunde des Tages, unabhängig vom Tag.
translation-type: tm+mt
source-git-commit: 226c54b782651ea8c6f4b7bb8030a1513c440a1d
workflow-type: tm+mt
source-wordcount: '221'
ht-degree: 0%

---


# Stunde des Tages

Die Dimension &quot;Stunde des Tages&quot;erfasst die numerische Stunde eines Tages als Dimensionswert. Wenn Sie z. B. einen Bericht vom 1. Januar bis 7. Januar haben, gruppiert sich die erste Stunde jedes Tages in denselben Dimensionswert. Dieser Bericht ist nützlich, wenn Sie möchten, dass ein Bericht nach der relativen Tageszeit aufgeschlüsselt wird, aber keine statischen Stunden als Dimensionswerte wünschen. Es ist besonders nützlich als Dimension in eingeplanten Berichten, da diese Dimension mit dem ausgewählten Datumsbereich rolliert.

Diese Dimension basiert auf der Zeitzone der Report Suite und nicht auf der Zeitzone des Besuchers. Wenn sich Ihre Report Suite beispielsweise in &quot;Berg&quot;befindet und ein Besucher in Kalifornien Ihre Site um 10:00 Uhr PST-Zeit besucht, werden die Treffergruppen unter dem `11:00 AM` Dimensionswert angezeigt. Wenn Sie eine Dimension wünschen, die die Zeit des lokalen Besuchers aufzeichnet, empfiehlt Adobe die Verwendung des [getTimeParting](/help/implement/vars/plugins/gettimeparting.md) -Plug-Ins.

## Diese Dimension mit Daten füllen

Diese Dimension funktioniert bei allen Implementierungen standardmäßig. Wenn eine Report Suite Daten enthält, funktioniert diese Dimension.

## Dimensionswerte

Zu den Dimensionswerten zählen `12:00 AM` - `11:00 PM`, die die Stunde des Tages darstellen, an dem der Treffer stattgefunden hat (abgerundet). Wenn beispielsweise um 15:58 Uhr ein Treffer generiert wurde, wird er unter dem Dimensionswert `3:00 PM`gruppiert.
