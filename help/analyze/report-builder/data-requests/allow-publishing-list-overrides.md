---
description: Wenn Sie einen Bericht planen, können Sie eine Veröffentlichungsliste auswählen, die für die Verteilung verwendet werden soll.
title: Veröffentlichungsliste darf außer Kraft gesetzt werden
uuid: f2cc9878-ab54-4c6f-8a88-3f3b579955e3
feature: Report Builder
role: User, Admin
exl-id: a7bd6cdb-397a-45ba-88ff-c3b3c7062005
source-git-commit: 7226b4c77371b486006671d72efa9e0f0d9eb1ea
workflow-type: tm+mt
source-wordcount: '164'
ht-degree: 95%

---

# Veröffentlichungsliste darf außer Kraft gesetzt werden

Wenn Sie einen Bericht planen, können Sie eine Veröffentlichungsliste auswählen, die für die Verteilung verwendet werden soll.

Veröffentlichungslisten werden in den Admin Tools von Analytics eingerichtet.

Siehe [Veröffentlichungslisten-Manager](https://experienceleague.adobe.com/docs/analytics/admin/admin-tools/publishing-list.html) in der Analytics-Referenz.

Um diese Funktion zu aktivieren, navigieren Sie zum Fenster [!UICONTROL Anforderungs-Assistent: Schritt 1].

Wenn Sie [!UICONTROL Veröffentlichungsliste darf außer Kraft gesetzt werden] aktivieren, wird die Report Suite der betreffenden Anforderung durch die den einzelnen Empfängern in der Veröffentlichungsliste zugeordnete Report Suite ersetzt. Falls die Arbeitsmappe mehrere Report Suites enthält, wird darüber hinaus die Report Suite ID verwendet, die mit der Veröffentlichungsliste verknüpft ist.

Diese Option ist nicht für Report Suites verfügbar, die Sie aus Zellen auswählen.

>[!NOTE]
>
>Wenn Sie den terminierten Bericht an mehrere Veröffentlichungslisten gleichzeitig senden, wird der Bericht jeweils einmal pro Liste ausgeführt. Variable Report Suites werden durch die Report Suite ersetzt, die der Veröffentlichungsliste zugeordnet ist.
