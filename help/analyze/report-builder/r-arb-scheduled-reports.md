---
description: Feldbeschreibungen für den Manager für geplante Aufgaben.
title: Manager für geplante Aufgaben
feature: Report Builder
role: User, Admin
exl-id: 8bacd7e4-ab50-4b36-842c-a8b6130a58d9
source-git-commit: 68a8eb3452d3f86bb59140ab5842667094198dee
workflow-type: tm+mt
source-wordcount: '659'
ht-degree: 51%

---

# Manager für geplante Aufgaben

The [!UICONTROL Scheduled Task Manager] lets you see a list of existing scheduled reports, along with their recipients, schedule details, and file formats. Sie können außerdem geplante Arbeitsmappen, deren Ausführung fehlgeschlagen ist, reaktivieren.

## Pausing older scheduled tasks

**Effective April 15, 2022**, Adobe intends to pause all scheduled Report Builder tasks that were created more than two years ago. Diese Pause gilt insbesondere für **vor dem 31. Januar 2020 erstellte Aufgaben**. Es werden keine Aufgaben, Arbeitsmappen oder Daten gelöscht. Tasks that are older than two years will be paused, and no additional scheduled tasks will be sent.

Any tasks that you wish to resume sending can be reactivated. Melden Sie sich bei Report Builder an und starten Sie die [!UICONTROL Manager für geplante Aufgaben]. Klicken **[!UICONTROL Reaktivieren]** für die geplante Aufgabe, mit der Sie den Versand fortsetzen möchten. Any task that gets reactivated will have a default expiration of 18 months - unless a shorter expiration date is chosen.

Darüber hinaus gilt für alle Aufgaben mit einem Erstellungsdatum von weniger als zwei Jahren ohne aktuelles Ablaufdatum (oder mit einem Ablaufdatum von mehr als zwei Jahren) das standardmäßige Ablaufdatum von 18 Monaten. The new expiration date will be October 15, 2023. Sie können dieses Ablaufdatum auf weniger als 18 Monate, jedoch nicht länger ändern. Zum Zeitpunkt des Ablaufs wird die Aufgabe angehalten. Sie können die Aufgabe jedoch mit einem neuen Ablaufdatum von 18 Monaten erneut aktivieren. Es werden keine Aufgaben, Arbeitsmappen oder Daten gelöscht.

The purpose of this pause is to effectively manage and maintain our scheduled tasks database to ensure optimal performance and delivery for needed tasks and workbooks. Dies wird unsere neue Governance-Politik voranbringen. Nach dem 15. April 2022 gilt für alle Aufgaben ein maximales Ablaufdatum von 18 Monaten. After 18 months, expired tasks will be paused and can be reactivated as needed.

## Configure scheduled tasks

| Feld | Beschreibung |
| --- | --- |
| Registerkarte **[!UICONTROL Terminierte Berichte]** |  |
| [!UICONTROL Berichtsname] | Dies ist der Name des terminierten Berichts. |
| [!UICONTROL E-Mail/FTP] | Die E-Mail- oder FTP-Adresse des Empfängers. **Hinweis:** Wenn E-Mail ausgewählt ist, werden Berichte, die größer als 1 MB sind, automatisch als ZIP-Datei an die E-Mail angehängt. Dank dieser Funktion bleibt die Größe des Anhangs gering und Anhänge werden nicht deaktiviert. |
| [!UICONTROL Veröffentlichungsoptionen] | In dieser Spalte wird der Power BI aufgeführt, wenn eine der [Veröffentlichungsoptionen für Power BI](https://experienceleague.adobe.com/docs/analytics/analyze/report-builder/publish-powerbi/power-bi.html) ausgewählt ist. |
| [!UICONTROL Zeitplan] | Der Typ der geplanten Bereitstellung. |
| [!UICONTROL Dateiformat] | Das Bereitstellungsformat des Berichts, z. B. Excel, PDF, HTML usw. |
| [!UICONTROL Reaktivieren] | Wenn eine geplante Arbeitsmappe nicht ausgeführt werden kann, unternimmt Report Builder in jeweils 15 Minuten Abstand zwei weitere Ausführungsversuche. Nach drei fehlgeschlagenen Versuchen deaktiviert Report Builder den Plan und zeigt die Schaltfläche Reaktivieren an. Wenn Sie eine Arbeitsmappe reaktivieren, wird die geplante Bereitstellung ab dem Zeitpunkt wiederaufgenommen, an dem die Deaktivierung erfolgte.  Wenn eine geplante Arbeitsmappe beispielsweise vor 14 Tagen deaktiviert wurde und Sie sie heute reaktivieren, wird sie für jeden fehlenden Tag, also 14-mal ausgeliefert. Wenn die Arbeitsmappe für die fehlenden Tage nicht ausgeliefert werden soll, können Sie die geplante Arbeitsmappe löschen und eine neue geplante Arbeitsmappe unter Verwendung derselben Planungsparameter erstellen.   Hinweis: Sie sollten eine Arbeitsmappe erst reaktivieren, wenn Sie die Ursache der Deaktivierung durch das System kennen. Eine Möglichkeit der Fehlerbehebung besteht darin, die deaktivierte Arbeitsmappe herunterzuladen und sie auf der Clientseite aktualisieren. Wenn keine Fehlermeldung erfolgt, sollte die Arbeitsmappe reaktiviert werden können. |
| [!UICONTROL Zuletzt gesendet] | Das Datum und die Uhrzeit, an denen der Bericht zuletzt gesendet wurde. |
| Registerkarte **Empfänger** |  |
| [!UICONTROL E-Mail-Adresse des Empfängers] | Die E-Mail-Adresse des Berichtempfängers. |
| [!UICONTROL Berichte] | Die Berichte, die an jeden Empfänger gesendet wurden. |
| Registerkarte **Berichte – Verlauf** |  |
| [!UICONTROL Dateiname] | Dies ist der Name des terminierten Berichts. |
| [!UICONTROL Datum] | Das Datum und die Uhrzeit, an denen der Bericht zuletzt gesendet wurde. |
| [!UICONTROL Status] | Der Status gibt an, ob der Bericht gesendet oder nicht gesendet wurde. |
| [!UICONTROL E-Mail/FTP] | Die E-Mail- oder FTP-Adresse für den Empfänger des Berichts. |
| [!UICONTROL Dateiformat] | Das Bereitstellungsformat des Berichts, z. B. Excel, PDF, HTML usw. |
