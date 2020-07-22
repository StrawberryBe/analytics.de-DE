---
title: Ausstiege
description: Eine Instanz des letzten Werts bei einem Besuch.
translation-type: tm+mt
source-git-commit: d3f92d72207f027d35f81a4ccf70d01569c3557f
workflow-type: tm+mt
source-wordcount: '186'
ht-degree: 1%

---


# Ausstiege

*Diese Hilfeseite beschreibt, wie Ausstiege als Metrik funktionieren. Informationen dazu, wie Ausstiege als Dimension funktionieren, finden Sie unter[Ausstiegsdimensionen](../dimensions/exit-dimensions.md).*

Die Metrik &quot;Ausstiege&quot;zeigt an, wie oft ein bestimmtes Dimensionselement als letzter Wert bei einem Besuch erfasst wird. Diese Metrik ist hilfreich, wenn Sie mehr über das letzte, was Besucher vor dem Verlassen Ihrer Site sehen, wissen möchten. Die Anzeige der letzten Werte einer Dimension kann Ihnen dabei helfen, das Erlebnis zu verstehen und zu optimieren, das ein Besucher vor dem Verlassen erhält.

## Berechnung dieser Metrik

Wenn ein [Besuch](visits.md) abgeschlossen ist, zeichnen Sie das letzte Dimensionselement als Ausstieg auf. Pro Dimension pro Besuch ist nur ein Ausstieg vorhanden. Es ist nicht unbedingt der letzte Treffer des Besuchs, wenn die Dimension in vorherigen Treffern festgelegt wurde. Es handelt sich um eine besuchsbasierte Metrik; es gilt rückwirkend für alle Treffer im Besuch.

>[!TIP]
>
>Wenn Sie diese Metrik mit einer Dimension, die nicht bei jedem Besuch festgelegt wurde, Ansicht vornehmen, können Sie das Dimensionselement &quot;Nicht angegeben&quot;in Analysis Workspace ausblenden. Klicken Sie auf das Filtersymbol und deaktivieren Sie die Option Nicht angegeben [!UICONTROL einschließen (Keine)].
