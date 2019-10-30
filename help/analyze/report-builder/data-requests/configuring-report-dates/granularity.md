---
description: Im Schritt 1 des Anforderungs-Assistenten können Sie eine Granularitätsstufe auf die Datenanforderung anwenden. Durch die Granularität wird der Detailgrad für die zeitliche Auflösung des Berichts angegeben.
seo-description: Im Schritt 1 des Anforderungs-Assistenten können Sie eine Granularitätsstufe auf die Datenanforderung anwenden. Durch die Granularität wird der Detailgrad für die zeitliche Auflösung des Berichts angegeben.
seo-title: Granularität
solution: Analytics
title: Granularität
topic: ReportBuilder
uuid: 948b3ff2-fcff-45fc-9e8c-8a025ac562b1
translation-type: tm+mt
source-git-commit: a2c38c2cf3a2c1451e2c60e003ebe1fa9bfd145d

---


# Granularität

Im Dialogfeld „Anforderungs-Assistent: Schritt 1“ können Sie angeben, welche Granularität eine Datenanforderung haben soll. Durch die Granularität wird der Detailgrad für die zeitliche Auflösung des Berichts angegeben.

Gültige Werte sind „Stunde“, „Tag“, „Woche“, „Monat“, „Quartal“, „Jahr“ und „Aggregiert“.

## Verarbeitung der Granularität in ReportBuilder

Angenommen, Sie wählen einen Datumsbereich für einen Monat mit einer Granularität des Typs [!UICONTROL Monat]. Die Anforderungen zeigen Gesamtsumme für die Metriken für genau einen Monat von Daten. Wenn der Datumsbereich Ihrer Anforderung ein Quartal umspannt, werden im Bericht drei Abbildungen angezeigt, eine für jede Monatseinheit oder jeden Teil davon. Wenn das aktuelle Datum der 18. März ist, führt die Auswahl des letzten Quartals zu einem Ergebnis mit einer Zahl für den Zeitraum vom 1. bis zum 31. Januar, einer weiteren Zahl für den Zeitraum vom 1. bis zum 28. Februar und einer abschließenden Zahl für den Zeitraum vom 1. bis zum 17. März.
