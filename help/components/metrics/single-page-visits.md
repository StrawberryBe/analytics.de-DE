---
title: Einzelseitenbesuche
description: Die Häufigkeit, mit der sich das Dimensionselement „Seite“ bei einem Besuch nicht geändert hat.
feature: Metrics
exl-id: 086235d0-4542-4e82-96ab-28c47c842ecf
source-git-commit: 7d5383e1ee3bee189d3dd48bc6b899f4108f7ba8
workflow-type: tm+mt
source-wordcount: '190'
ht-degree: 100%

---

# Einzelseitenbesuche

*Auf dieser Hilfeseite wird beschrieben, wie „Einzelseitenbesuche“ als Metrik funktioniert. Weitere Informationen finden Sie unter der Dimension [Einzelseitenbesuche](../dimensions/single-page-visits.md).*

Die Metrik [!UICONTROL Einzelseitenbesuche] gibt die Anzahl der Besuche an, bei denen das Dimensionselement [Seite](../dimensions/page.md) nur einen einzigen, eindeutigen Wert für den gesamten Besuch enthält. Diese Metrik ist hilfreich bei Dimensionen, in denen Sie kurze Besuche anzeigen, aber keine so strengen Regeln wie bei [[!UICONTROL Absprüngen]](bounces.md) verwenden möchten.

## Berechnung dieser Metrik

Diese Metrik zählt die Anzahl der Besuche, bei denen das Dimensionselement [!UICONTROL Seite] nur einen einzigen, eindeutigen Wert für den gesamten Besuch enthält. Wenn ein Besucher die Seite neu lädt oder Linktracking-Aufrufe auslöst, zählt dies immer noch als Einzelseitenbesuch. Sobald die Dimension „Seite“ in einen zweiten eindeutigen Wert geändert wird, gilt der Besuch nicht mehr als ein Einzelseitenbesuch.

Einen Vergleich der Metriken finden Sie unter [Einzelzugriff](single-access.md).

## Wiederholte Instanzen zählen

Diese Einstellung legt fest, ob wiederholte Instanzen in den Berichten gezählt werden. Weitere Informationen finden Sie unter [Wiederholte Instanzen zählen](/help/components/metrics/count-repeat-instances.md).