---
title: Ausstiege
description: Eine Instanz des letzten Werts bei einem Besuch.
feature: Metrics
exl-id: 0997ed1f-29b0-403d-9ed2-644a5ff19aef
source-git-commit: 7d5383e1ee3bee189d3dd48bc6b899f4108f7ba8
workflow-type: ht
source-wordcount: '186'
ht-degree: 100%

---

# Ausstiege

*Auf dieser Hilfeseite wird beschrieben, wie Ausstiege als Metrik funktionieren. Informationen dazu, wie Ausstiege als Dimension funktionieren, finden Sie unter [Ausstiegsdimensionen](../dimensions/exit-dimensions.md).*

Die Metrik „Ausstiege“ gibt an, wie oft ein Dimensionselement als letzter Wert bei einem Besuch erfasst wird. Diese Metrik ist hilfreich, wenn Sie mehr über das Letzte erfahren möchten, was Besucher sehen, bevor sie Ihre Site verlassen. Wenn Sie die letzten Werte einer Dimension anzeigen, können Sie das Erlebnis eines Besuchers vor dem Verlassen besser verstehen und optimieren.

## Berechnung dieser Metrik

Zeichnen Sie nach Abschluss eines [Besuchs](visits.md) das jüngsten Dimensionselement als Ausstieg auf. Pro Dimension und Besuch gibt es nur einen Ausstieg. Dabei handelt es sich nicht unbedingt um den letzten Treffer des Besuchs, wenn die Dimension in vorherigen Treffern festgelegt wurde. Es handelt sich um eine besuchsbasierte Metrik. Sie gilt rückwirkend für alle Treffer im Besuch.

>[!TIP]
>
>Wenn Sie diese Metrik für eine Dimension anzeigen, die nicht immer bei jedem Besuch festgelegt wird, können Sie das Dimensionselement „Nicht angegeben“ in Analysis Workspace ausblenden. Klicken Sie auf das Filtersymbol und deaktivieren Sie die Option [!UICONTROL Nicht angegeben (keine) einschließen].
