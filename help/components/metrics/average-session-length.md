---
title: Durchschnittliche Sitzungslänge (Mobil)
description: Die durchschnittliche Sitzungslänge für das Mobilgerät.
feature: Metrics
exl-id: e33ac9ca-f1be-4d9c-9247-c5db8fb0102e
source-git-commit: e32821dd3f30404166554b8437c508172e4764e5
workflow-type: tm+mt
source-wordcount: '80'
ht-degree: 26%

---

# Durchschnittliche Sitzungslänge (Mobil)

Die &quot;durchschnittliche Sitzungslänge (Mobil)&quot; [Metrik](overview.md) zeigt die durchschnittliche Zeit an, die ein bestimmtes Dimensionselement pro Dimensionselement vorhanden ist. Sie ähnelt dem [[!UICONTROL Zeit pro Besuch (Sekunden)]](time-spent-per-visit.md) -Metrik, mit der Ausnahme, dass diese Metrik mobile SDK-spezifische Komponenten als Teil ihrer Berechnung verwendet.

## Berechnung dieser Metrik

Diese Metrik wird mithilfe der [Lebenszyklusmetriken](https://developer.adobe.com/client-sdks/documentation/mobile-core/lifecycle/metrics/) `'Total Session length' / ('Launches' - 'First launches'`.
