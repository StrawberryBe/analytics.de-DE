---
description: Wenn Sie einen Bericht planen, können Sie eine Veröffentlichungsliste auswählen, die für die Verteilung verwendet werden soll.
title: Zulassen von Überschreibungen der Veröffentlichungsliste
feature: Report Builder
role: User, Admin
exl-id: a7bd6cdb-397a-45ba-88ff-c3b3c7062005
source-git-commit: 1ee50c6a2231795b2ad0015a79e09b7c1c74d850
workflow-type: tm+mt
source-wordcount: '162'
ht-degree: 100%

---

# Zulassen von Überschreibungen der Veröffentlichungsliste

Wenn Sie einen Bericht planen, können Sie eine Veröffentlichungsliste auswählen, die für die Verteilung verwendet werden soll.

Veröffentlichungslisten werden in den Admin Tools von Analytics eingerichtet.

Siehe [Veröffentlichungslisten-Manager](https://experienceleague.adobe.com/docs/analytics/admin/admin-tools/publishing-list.html?lang=de) in der Analytics-Referenz.

Um diese Funktion zu aktivieren, navigieren Sie zum Fenster [!UICONTROL Anforderungs-Assistent: Schritt 1].

Wenn Sie [!UICONTROL Veröffentlichungsliste darf außer Kraft gesetzt werden] aktivieren, wird die Report Suite der betreffenden Anforderung durch die den einzelnen Empfängern in der Veröffentlichungsliste zugeordnete Report Suite ersetzt. Falls die Arbeitsmappe mehrere Report Suites enthält, wird darüber hinaus die Report Suite ID verwendet, die mit der Veröffentlichungsliste verknüpft ist.

Diese Option ist nicht für Report Suites verfügbar, die Sie aus Zellen auswählen.

>[!NOTE]
>
>Wenn Sie den terminierten Bericht an mehrere Veröffentlichungslisten gleichzeitig senden, wird der Bericht jeweils einmal pro Liste ausgeführt. Variable Report Suites werden durch die Report Suite ersetzt, die der Veröffentlichungsliste zugeordnet ist.
