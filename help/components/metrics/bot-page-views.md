---
title: Bot-Seitenansichten
description: Die Anzahl der Seitenansichten, die mit Bot-Regeln übereinstimmten.
feature: Metrics
exl-id: 9b1efcb1-10ca-40fb-8f20-e6da105366d9
source-git-commit: d095628e94a45221815b1d08e35132de09f5ed8f
workflow-type: tm+mt
source-wordcount: '124'
ht-degree: 11%

---

# Bot-Seitenansichten

Die &quot;Bot-Seitenansichten&quot; [Metrik](overview.md) zeigt die Anzahl der übereinstimmenden Seitentreffer an [Bot-Regeln](/help/admin/admin/c-manage-report-suites/c-edit-report-suites/general/bot-removal/bot-rules.md).

Da Bot-Berichte vom Rest Ihrer Report Suite-Daten getrennt sind, funktioniert diese Metrik nur mit den folgenden Dimensionen:

* [Bot-Name](../dimensions/bot-name.md)
* [Seite](../dimensions/page.md)
* Zeitbasierte Dimensionen (beispielsweise [Tag](../dimensions/day.md), [Woche](../dimensions/week.md)oder [Monat](../dimensions/month.md))

Die Verwendung einer anderen Dimension mit dieser Metrik gibt keine Daten zurück.

## Berechnung dieser Metrik

Adobe überprüft jeden Seitentreffer, um festzustellen, ob er mit den von Ihrem Unternehmen konfigurierten Bot-Regeln übereinstimmt. Wenn ein bestimmter Treffer mit einer Bot-Regel übereinstimmt, wird der Seitentreffer aus dem Bericht ausgeschlossen und diese Metrik erhöht sich um 1. Diese Metrik enthält keine Linktracking-Treffer ([`tl()`](/help/implement/vars/functions/tl-method.md)).
