---
title: Bot name
description: Der Name des Bots, der mit den Bot-Regeln übereinstimmte.
exl-id: 668c1dce-c603-477a-9df7-dacb649bbf63
source-git-commit: 5ba12c243a8013c52b487d048c54461ebdf7bd85
workflow-type: tm+mt
source-wordcount: '217'
ht-degree: 3%

---

# Bot name

Die Dimension &quot;Bot name&quot;zeigt die Namen der Bots an, die mithilfe von [Bot-Regeln](/help/admin/admin/c-manage-report-suites/c-edit-report-suites/general/bot-removal/bot-rules.md). Diese Regeln können standardmäßige IAB-Regeln oder benutzerdefinierte Bot-Regeln sein, die Ihr Unternehmen konfiguriert. Dies ist hilfreich in Fällen, in denen Sie mehr darüber erfahren möchten, welche Bots Ihre Site besuchen oder welche Bots den meisten Traffic generieren.

Treffer, die übereinstimmen [!UICONTROL Bot-Regeln] automatisch aus allen Analytics-Berichten mit Ausnahme dieser Dimension herausgefiltert werden, [Bot-Vorkommen](../metrics/bot-occurrences.md)und [Bot-Seitenansichten](../metrics/bot-page-views.md). Sie können diese Dimension und diese beiden Metriken verwenden, um zu sehen, welche Bot-Daten aus dem Rest Ihrer Berichte ausgeschlossen werden.

Da Bot-Berichte vom Rest Ihrer Report Suite-Daten getrennt sind, werden für diese Dimension nur die folgenden Dimensionen und Metriken unterstützt:

* [Seite](page.md)
* Zeitbasierte Dimensionen (z. B. [Tag](day.md), [Woche](week.md)oder [Monat](month.md))
* [Bot-Vorkommen](../metrics/bot-occurrences.md)
* [Bot-Seitenansichten](../metrics/bot-page-views.md)

Die Verwendung einer anderen Dimension oder Metrik mit dieser Dimension gibt keine Daten zurück.

## Füllen dieser Dimension mit Daten

Wenn Sie [Bot-Regeln](/help/admin/admin/c-manage-report-suites/c-edit-report-suites/general/bot-removal/bot-rules.md), erfasst diese Dimension automatisch Daten. Wenn Sie noch nicht aktiviert haben [!UICONTROL Bot-Regeln], wird diese Dimension nicht in Analysis Workspace angezeigt.

## Dimensionselemente

Jedes Dimensionselement listet den Namen des Bots auf, der den IAB- oder benutzerdefinierten Bot-Regelkriterien entsprach.
