---
title: Bot-Seitenansichten
description: Die Anzahl der Seitenansichten, die mit Bot-Regeln übereinstimmten.
exl-id: 9b1efcb1-10ca-40fb-8f20-e6da105366d9
source-git-commit: 5ba12c243a8013c52b487d048c54461ebdf7bd85
workflow-type: tm+mt
source-wordcount: '124'
ht-degree: 4%

---

# Bot-Seitenansichten

Die Metrik &quot;Bot-Seitenansichten&quot;gibt die Anzahl der übereinstimmenden Seitentreffer an [Bot-Regeln](/help/admin/admin/c-manage-report-suites/c-edit-report-suites/general/bot-removal/bot-rules.md).

Da Bot-Berichte vom Rest Ihrer Report Suite-Daten getrennt sind, funktioniert diese Metrik nur mit den folgenden Dimensionen:

* [Bot name](../dimensions/bot-name.md)
* [Seite](../dimensions/page.md)
* Zeitbasierte Dimensionen (z. B. [Tag](../dimensions/day.md), [Woche](../dimensions/week.md)oder [Monat](../dimensions/month.md))

Die Verwendung einer anderen Dimension mit dieser Metrik gibt keine Daten zurück.

## Berechnung dieser Metrik

Adobe überprüft jeden Seitentreffer, um festzustellen, ob er mit den von Ihrem Unternehmen konfigurierten Bot-Regeln übereinstimmt. Wenn ein bestimmter Treffer mit einer Bot-Regel übereinstimmt, wird der Seitentreffer aus dem Bericht ausgeschlossen und diese Metrik erhöht sich um 1. Diese Metrik enthält keine Linktracking-Treffer ([`tl()`](/help/implement/vars/functions/tl-method.md)).
