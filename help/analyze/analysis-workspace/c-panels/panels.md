---
description: 'null'
title: Übersicht über Bedienfelder
translation-type: ht
source-git-commit: 8e8a6672b95da56bba4af0fbf66981f85cb36415
workflow-type: ht
source-wordcount: '481'
ht-degree: 100%

---


# Übersicht über Bedienfelder

Ein Bedienfeld ist eine Sammlung von Tabellen und Visualisierungen. Sie können auf Bedienfelder über das Symbol oben links in Workspace zugreifen. Bedienfelder sind hilfreich, wenn Sie Ihre Projekte anhand von Zeiträumen, Geschäftsbereichen, Standorten usw. organisieren möchten. In Analysis Workspace gibt es diese sechs Arten von Bedienfeldern:

* [Leeres Bedienfeld](blank-panel.md)
* [Bedienfeld „Quick Insights“](quickinsight.md)
* [Bedienfeld „Analytics for Target“](a4t-panel.md) (in Kürze verfügbar)
* [Attributionsbedienfeld](attribution.md)
* [Freiform-Bedienfeld](freeform-panel.md)
* [Bedienfeld „Segmentvergleich“](c-segment-comparison/segment-comparison.md)

Quick Insight-, leere und Freiform-Bedienfelder eignen sich hervorragend als Ausgangspunkt für Ihre Analyse, während sich die Bedienfelder für Analytics for Target, Attribution IQ und Segmentvergleich für fortgeschrittenere Analysen eignen. In Projekten steht eine `"+"`-Schaltfläche zur Verfügung, mit der Sie jederzeit leere Bedienfelder hinzufügen können.

Das standardmäßige Startbedienfeld ist das Freiform-Bedienfeld. Sie können jedoch auch das [leere Bedienfeld](/help/analyze/analysis-workspace/c-panels/blank-panel.md) als Ihren Standard festlegen.

## Dropdown-Filter in Bedienfeldern {#section_D2828EEDD52944528E87F470EAB581CF}

Die Dropzone für Bedienfelder verfügt über Dropdown-Filterfunktionen. Mit diesen Filtern können Sie kontrolliert mit den Projektdaten interagieren und somit tiefgreifende Analysen durchführen, Ihre Projekte vereinfachen und/oder Erkenntnisse mit anderen teilen.

Beispiel für ein vereinfachtes Projekt: Angenommen, Sie haben für länderspezifisches Reporting mehrere Versionen eines Projekts/Bedienfelds. Jetzt können Sie diese Projekte/Bedienfelder zu einem einzigen Projekt komprimieren und stattdessen ein Dropdown für Länder hinzufügen, um verschiedene Datensätze herauszufiltern.

![](assets/dropdowns.png)

Beachten Sie:

* Sie können mehrere Komponenten (oder Dimensionselemente) miteinbeziehen und dann in einem Dropdown zwischen ihnen wechseln, um den Bedienfeldinhalt zu filtern.
* Sie können außerdem mehrere Dropdown-Listen auf demselben Bedienfeld erstellen.
* Sie können den Titel der Dropdown-Liste anpassen, indem Sie auf den Titel klicken und ihn ändern, oder den Titel ganz entfernen, indem Sie auf das „x“ daneben klicken.
* Sie können Dropdown-Filter mit jedem Komponententyp erstellen: Dimensionen, Datumsbereichen, Segmenten und Metriken. Beachten Sie, dass Dropdown-Datumsbereiche immer die Datumsbereiche des Bedienfelds überschreiben.
* Wir behalten die Komponentenfarben von der linken Leiste bei: Gelb für Dimensionen, Grün für Metriken, Blau für Segmente und Violett für Datumsbereiche.
* Die Dropzone erstellt weiterhin Hit-Segmente für Elemente, die als Segmente hineingezogen werden. Sie können sie wie gewohnt ändern, indem Sie auf das Informationssymbol (i) neben dem Segment klicken, dann das stiftförmige Bearbeitungssymbol auswählen und die Bearbeitung im Segment Builder durchführen.

**So erstellen und verwenden Sie Dropdown-Filter:**

1. Wählen Sie beliebige Elemente aus der linken Leiste aus und legen Sie sie **bei gedrückter -Taste** in der Dropzone des Bedienfelds ab.

   ![](assets/create_dropdown.png)

   Dadurch werden die Komponenten in eine Dropdown-Liste und nicht in ein Segment umgewandelt. (Sie können auch weitere Segmente hinzufügen, indem Sie die -Taste nicht gedrückt halten.)

   ![](assets/dropdown.png)

1. Wählen Sie eine der Optionen aus der Dropdown-Liste aus, um die Daten im unteren Bedienfeld zu ändern. (Sie können auch auf die Filterung von Bedienfelddaten verzichten, indem Sie **[!UICONTROL Kein Filter]** auswählen.)
1. Wenn Sie beispielsweise die Daten auch nach Marketing-Kanälen aufteilen möchten, können Sie ein weiteres Dropdown namens „Marketing-Kanal“ hinzufügen:

   ![](assets/mc_dropdown.png)

