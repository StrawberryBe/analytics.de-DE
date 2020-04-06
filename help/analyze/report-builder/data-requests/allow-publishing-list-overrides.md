---
description: Wenn Sie einen Bericht planen, können Sie eine Veröffentlichungs-Liste auswählen, die für die Verteilung verwendet werden soll.
title: Veröffentlichungsliste darf außer Kraft gesetzt werden
topic: Report builder
uuid: f2cc9878-ab54-4c6f-8a88-3f3b579955e3
translation-type: tm+mt
source-git-commit: dabaf6247695bc4f3d9bfe668f3ccfca12a52269

---


# Veröffentlichungsliste darf außer Kraft gesetzt werden

Wenn Sie einen Bericht planen, können Sie eine Veröffentlichungs-Liste auswählen, die für die Verteilung verwendet werden soll.

Veröffentlichungs-Listen werden in den Admin Tools von Analytics eingerichtet.

Siehe [Publishing Liste Manager](https://marketing.adobe.com/resources/help/de_DE/reference/publishing_list.html) in der Analytics-Referenz.

Um diese Funktion zu aktivieren, navigieren Sie zum [!UICONTROL Request Wizard: Step 1] Fenster.

Wenn Sie diese Option aktivieren [!UICONTROL Allow Publishing List Override], ersetzt die Report Suite, die jedem Empfänger in der Veröffentlichungs-Liste zugewiesen ist, die Report Suite für diese Anforderung. Wenn die Arbeitsmappe mehrere Report Suites enthält, wird darüber hinaus die Report Suite-ID verwendet, die der Veröffentlichungs-Liste zugeordnet ist.

Diese Option steht nicht für Report Suites zur Verfügung, die Sie aus Zellen auswählen.

>[!NOTE] Wenn Sie den terminierten Bericht an mehrere Veröffentlichungslisten gleichzeitig senden, wird der Bericht jeweils einmal pro Liste ausgeführt. Variable Report Suites werden durch die Report Suite ersetzt, die der Veröffentlichungsliste zugeordnet ist.

