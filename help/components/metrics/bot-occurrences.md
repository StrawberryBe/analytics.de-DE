---
title: Bot-Vorkommen
description: Die Anzahl der Treffer, die mit Bot-Regeln übereinstimmten.
feature: Metrics
exl-id: 3b6cbe94-98db-4ba4-aab2-ce59cdbc420a
source-git-commit: 811e321ce96aaefaeff691ed5969981a048d2c31
workflow-type: tm+mt
source-wordcount: '129'
ht-degree: 4%

---

# Bot-Vorkommen

Die Metrik &quot;Bot-Vorkommen&quot;zeigt die Anzahl der Treffer an, die übereinstimmen [Bot-Regeln](/help/admin/admin/c-manage-report-suites/c-edit-report-suites/general/bot-removal/bot-rules.md).

Da Bot-Berichte vom Rest Ihrer Report Suite-Daten getrennt sind, funktioniert diese Metrik nur mit den folgenden Dimensionen:

* [Bot name](../dimensions/bot-name.md)
* [Seite](../dimensions/page.md)
* Zeitbasierte Dimensionen (z. B. [Tag](../dimensions/day.md), [Woche](../dimensions/week.md)oder [Monat](../dimensions/month.md))

Die Verwendung einer anderen Dimension mit dieser Metrik gibt keine Daten zurück.

## Berechnung dieser Metrik

Adobe überprüft jeden Treffer, um festzustellen, ob er mit den von Ihrem Unternehmen konfigurierten Bot-Regeln übereinstimmt. Wenn ein bestimmter Treffer mit einer Bot-Regel übereinstimmt, wird der Treffer aus der Berichterstellung ausgeschlossen und diese Metrik erhöht sich um 1. Diese Metrik enthält beide Seitenansichten ([`t()`](/help/implement/vars/functions/t-method.md)) und Linktracking-Treffer ([`tl()`](/help/implement/vars/functions/tl-method.md)), [Bot-Seitenansichten](bot-page-views.md) enthalten keine Linktracking-Treffer.
