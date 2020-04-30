---
description: Wenn Sie einen Bericht planen, können Sie eine Veröffentlichungsliste auswählen, die für die Verteilung verwendet werden soll.
title: Veröffentlichungsliste darf außer Kraft gesetzt werden
topic: Report builder
uuid: f2cc9878-ab54-4c6f-8a88-3f3b579955e3
translation-type: tm+mt
source-git-commit: 3fe3442eae1bdd8b90acffc9c25d184714613c16

---


# Veröffentlichungsliste darf außer Kraft gesetzt werden

Wenn Sie einen Bericht planen, können Sie eine Veröffentlichungsliste auswählen, die für die Verteilung verwendet werden soll.

Veröffentlichungslisten werden in den Admin Tools von Analytics eingerichtet.

Siehe [Veröffentlichungslisten-Manager](https://docs.adobe.com/content/help/en/analytics/admin/admin-tools/publishing-list.html) in der Analytics-Referenz.

Um diese Funktion zu aktivieren, navigieren Sie zum [!UICONTROL Request Wizard: Step 1] Fenster.

If you enable [!UICONTROL Allow Publishing List Override], the report suite assigned to each recipient in the publishing list replaces the report suite for this request. Falls die Arbeitsmappe mehrere Report Suites enthält, wird darüber hinaus die Report Suite ID verwendet, die mit der Veröffentlichungsliste verknüpft ist.

Diese Option ist nicht für Report Suites verfügbar, die Sie aus Zellen auswählen.

>[!NOTE] Wenn Sie den terminierten Bericht an mehrere Veröffentlichungslisten gleichzeitig senden, wird der Bericht jeweils einmal pro Liste ausgeführt. Variable Report Suites werden durch die Report Suite ersetzt, die der Veröffentlichungsliste zugeordnet ist.

