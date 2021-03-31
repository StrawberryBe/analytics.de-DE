---
description: 'Im Dialogfeld „Anforderungs-Assistent: Schritt 1“ können Sie angeben, welche Granularität eine Datenanforderung haben soll. Durch die Granularität wird der Detailgrad für die zeitliche Auflösung des Berichts angegeben.'
title: Granularität
uuid: 948b3ff2-fcff-45fc-9e8c-8a025ac562b1
feature: Report Builder
role: Geschäftspraktiker, Administrator
translation-type: tm+mt
source-git-commit: 894ee7a8f761f7aa2590e06708be82e7ecfa3f6d
workflow-type: tm+mt
source-wordcount: '156'
ht-degree: 98%

---


# Granularität

Im Dialogfeld „Anforderungs-Assistent: Schritt 1“ können Sie angeben, welche Granularität eine Datenanforderung haben soll. Durch die Granularität wird der Detailgrad für die zeitliche Auflösung des Berichts angegeben.

Gültige Werte sind „Stunde“, „Tag“, „Woche“, „Monat“, „Quartal“, „Jahr“ und „Aggregiert“.

## Verarbeitung von Granularität in Report Builder

Angenommen, Sie wählen einen Datumsbereich für einen Monat mit einer Granularität des Typs [!UICONTROL Monat]. Die Anforderungen zeigen Gesamtsumme für die Metriken für genau einen Monat von Daten. Wenn der Datumsbereich Ihrer Anforderung ein Quartal umspannt, werden im Bericht drei Abbildungen angezeigt, eine für jede Monatseinheit oder jeden Teil davon. Wenn das aktuelle Datum der 18. März ist, führt die Auswahl des letzten Quartals zu einem Ergebnis mit einer Zahl für den Zeitraum vom 1. bis zum 31. Januar, einer weiteren Zahl für den Zeitraum vom 1. bis zum 28. Februar und einer abschließenden Zahl für den Zeitraum vom 1. bis zum 17. März.
