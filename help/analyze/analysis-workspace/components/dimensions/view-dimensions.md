---
description: Ansicht der obersten Werte einer Dimension, bevor sie in einem Projekt verwendet wird.
title: Dimensionsvorschau
uuid: dd1f87de-2d83-4c6b-b8cd-ce81c741d7a3
feature: Grundlagen zu Workspace
role: Business Practitioner, Administrator
exl-id: 897edc76-6744-4d8c-ab0e-20672838f7b3
translation-type: ht
source-git-commit: 549258b0168733c7b0e28cb8b9125e68dffd5df7
workflow-type: ht
source-wordcount: '194'
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
