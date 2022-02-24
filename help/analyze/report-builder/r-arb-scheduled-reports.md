---
description: Feldbeschreibungen für den Manager für geplante Aufgaben.
title: Manager für geplante Aufgaben
feature: Report Builder
role: User, Admin
exl-id: 8bacd7e4-ab50-4b36-842c-a8b6130a58d9
source-git-commit: 91d94ba33328f0ac5fba09cdafb26f58733b4d58
workflow-type: tm+mt
source-wordcount: '655'
ht-degree: 47%

---

# Manager für geplante Aufgaben

Die [!UICONTROL Manager für geplante Aufgaben] zeigt eine Liste der vorhandenen terminierten Berichte mit ihren Empfängern, Planungsdetails und Dateiformaten an. Sie können außerdem geplante Arbeitsmappen, deren Ausführung fehlgeschlagen ist, reaktivieren.

## Anhalten älterer geplanter Aufgaben

**Wirksam ab 15. April 2022** Adobe beabsichtigt, alle geplanten Report Builder-Aufgaben, die vor mehr als zwei Jahren erstellt wurden, anzuhalten. Diese Pause gilt insbesondere für **vor dem 31. Januar 2020 erstellte Aufgaben**. Es werden keine Aufgaben, Arbeitsmappen oder Daten gelöscht. Aufgaben, die älter als zwei Jahre sind, werden ausgesetzt und es werden keine weiteren geplanten Aufgaben gesendet.

Alle Aufgaben, die zum Fortsetzen des Versands benötigt werden, können reaktiviert werden. Melden Sie sich bei Report Builder an und starten Sie die [!UICONTROL Manager für geplante Aufgaben]. Klicken **[!UICONTROL Reaktivieren]** für die geplante Aufgabe, mit der Sie den Versand fortsetzen möchten. Jede Aufgabe, die reaktiviert wird, hat einen Standardablauf von 18 Monaten - es sei denn, es wird ein kürzeres Ablaufdatum ausgewählt.

Darüber hinaus gilt für alle Aufgaben mit einem Erstellungsdatum von weniger als zwei Jahren ohne aktuelles Ablaufdatum (oder mit einem Ablaufdatum von mehr als zwei Jahren) das standardmäßige Ablaufdatum von 18 Monaten. Das neue Ablaufdatum ist der 15. Oktober 2023. Sie können dieses Ablaufdatum auf weniger als 18 Monate, jedoch nicht länger ändern. Zum Zeitpunkt des Ablaufs wird die Aufgabe angehalten. Sie können die Aufgabe jedoch mit einem neuen Ablaufdatum von 18 Monaten erneut aktivieren. Es werden keine Aufgaben, Arbeitsmappen oder Daten gelöscht.

Ziel dieser Pause ist es, unsere geplante Aufgabendatenbank effektiv zu verwalten und zu verwalten, um eine optimale Leistung und Bereitstellung für benötigte Aufgaben und Arbeitsmappen sicherzustellen. Dies wird unsere neue Governance-Politik voranbringen. Nach dem 15. April 2022 gilt für alle Aufgaben ein maximales Ablaufdatum von 18 Monaten. Nach 18 Monaten werden abgelaufene Aufgaben angehalten und können bei Bedarf reaktiviert werden.

## Geplante Aufgaben konfigurieren

| Feld | Beschreibung |
| --- | --- |
| Registerkarte **[!UICONTROL Terminierte Berichte]** |  |
| [!UICONTROL Berichtsname] | Dies ist der Name des terminierten Berichts. |
| [!UICONTROL E-Mail/FTP] | Die E-Mail- oder FTP-Adresse des Empfängers. **Hinweis:** Wenn E-Mail ausgewählt ist, werden Berichte, die größer als 1 MB sind, automatisch als ZIP-Datei an die E-Mail angehängt. Dank dieser Funktion bleibt die Größe des Anhangs gering und Anhänge werden nicht deaktiviert. |
| [!UICONTROL Veröffentlichungsoptionen] | In dieser Spalte wird der Power BI aufgeführt, wenn eine der [Veröffentlichungsoptionen für Power BI](https://experienceleague.adobe.com/docs/analytics/analyze/report-builder/publish-powerbi/power-bi.html) ausgewählt ist. |
| [!UICONTROL Zeitplan] | Der Typ der geplanten Bereitstellung. |
| [!UICONTROL Dateiformat] | Das Bereitstellungsformat des Berichts, z. B. Excel, PDF, HTML usw. |
| [!UICONTROL Reaktivieren] | Wenn eine geplante Arbeitsmappe nicht ausgeführt werden kann, unternimmt Report Builder in jeweils 15 Minuten Abstand zwei weitere Ausführungsversuche. Nach drei fehlgeschlagenen Versuchen deaktiviert Report Builder den Plan und zeigt die Schaltfläche Reaktivieren an. Wenn Sie eine Arbeitsmappe reaktivieren, wird die geplante Bereitstellung ab dem Zeitpunkt wiederaufgenommen, an dem die Deaktivierung erfolgte.<p>Wenn eine geplante Arbeitsmappe beispielsweise vor 14 Tagen deaktiviert wurde und Sie sie heute reaktivieren, wird sie für jeden fehlenden Tag, also 14-mal ausgeliefert. Wenn die Arbeitsmappe für die fehlenden Tage nicht ausgeliefert werden soll, können Sie die geplante Arbeitsmappe löschen und eine neue geplante Arbeitsmappe unter Verwendung derselben Planungsparameter erstellen.<p>**Hinweis:** Reaktivieren Sie eine Arbeitsmappe nur, wenn Sie den Grund kennen, aus dem sie vom System deaktiviert wurde. Laden Sie zur Fehlerbehebung eine deaktivierte Arbeitsmappe herunter und aktualisieren Sie sie auf der Clientseite. Wenn keine Fehlermeldung erfolgt, sollte die Arbeitsmappe reaktiviert werden können. |
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
