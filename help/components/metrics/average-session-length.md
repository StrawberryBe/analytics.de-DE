---
title: Durchschnittliche Sitzungslänge (Mobil)
description: Die durchschnittliche Sitzungslänge für das Mobilgerät.
feature: Metrics
exl-id: e33ac9ca-f1be-4d9c-9247-c5db8fb0102e
source-git-commit: 47d5a532505aff48d43972836c78620870bd8221
workflow-type: tm+mt
source-wordcount: '89'
ht-degree: 65%

---

# Durchschnittliche Sitzungslänge (Mobil)

Die Metrik „Durchschnittliche Sitzungslänge (Mobil)“ zeigt die durchschnittliche Zeit an, die ein bestimmtes Dimensionselement pro Dimensionselement vorhanden ist. Sie ähnelt dem [Zeit pro Besuch [Sekunden]](https://experienceleague.adobe.com/docs/analytics/components/metrics/time-spent-per-visit.html) -Metrik, mit der Ausnahme, dass diese Metrik mobile SDK-spezifische Komponenten als Teil ihrer Berechnung verwendet.

## Berechnung dieser Metrik

Diese Metrik wird mit den [Mobile-Metriken](https://experienceleague.adobe.com/docs/mobile-services/using/get-started-ug/mobile-metrics/metrics-reference.html?lang=de) berechnet`'Total session length' / ('Launches' - 'First launches'`.
