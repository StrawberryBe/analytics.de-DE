---
description: Ansicht der obersten Werte einer Dimension, bevor sie in einem Projekt verwendet wird.
title: Dimensionsvorschau
feature: Dimensions
role: User, Admin
exl-id: 897edc76-6744-4d8c-ab0e-20672838f7b3
source-git-commit: 10ae8213b8745439ab5968853f655a1176b8c38a
workflow-type: tm+mt
source-wordcount: '192'
ht-degree: 100%

---

# Dimensionsvorschau

Bewegen Sie den Cursor über das Informations-Symbol neben einer Dimension, um die obersten fünf Werte für nicht zeitabhängige Dimensionen (und 15 für zeitabhängige Dimensionen) anzuzeigen. Bisher waren diese Werte statisch (d. h. die fünf ausgewählten Werte blieben unverändert).

![](assets/dimension-preview.png)

Jetzt zeigen wir standardmäßig dynamische Werte anstelle von statischen an, mit der Option, diese in statische Werte umzuwandeln. Wissenswertes:

* Bei einer Aktualisierung Ihrer Daten werden die Spalten der dynamischen Dimension aktualisiert, um die aktuellen 5/15 Dimensionselemente anzuzeigen.
* Eine dynamische Dimensionsspalte, die kopiert oder bewegt wird, wird statisch.
* Wenn Sie mit dem Mauszeiger über eine statische Dimensionsspalte fahren, wird ein Schlosssymbol angezeigt, das angibt, dass es sich bei der Dimension um eine statische handelt.

![](assets/dimension_static.png)

## Anzeige von Dimensionselementen

Wenn Sie auf eine Dimension zeigen und auf den grauen, nach rechts zeigenden Pfeil daneben klicken, wird eine Liste der jeweiligen Dimensionselemente angezeigt. Dimensionselementlisten zeigen normalerweise die Top-Elemente der letzten 30 Tage an.

Am Ende der Liste sehen Sie die Option **[!UICONTROL Top-Elemente der letzten 6 Monate anzeigen]**. Klicken Sie auf diese Option, um die Top-Dimensionselemente der letzten 180 Tage anzuzeigen.
