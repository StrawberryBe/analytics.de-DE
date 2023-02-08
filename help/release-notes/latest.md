---
title: Neueste Analytics-Versionshinweise
description: Hier finden Sie die aktuellen Versionshinweise zu Adobe Analytics.
feature: Release Notes
exl-id: 97d16d5c-a8b3-48f3-8acb-96033cc691dc
source-git-commit: e7140b78b7b2c6c63cb93f1341581cc83af7b33b
workflow-type: tm+mt
source-wordcount: '954'
ht-degree: 62%

---

# Aktuelle Adobe Analytics-Versionshinweise (Februar 2023)

**Letzte Aktualisierung**: 2. Februar 2023

Die Versionen von Adobe Analytics basieren auf einem [kontinuierlichen Bereitstellungsmodell](releases.md), das eine besser skalierbare, schrittweise Implementierung von Funktionen ermöglicht. Dementsprechend werden diese Versionshinweise mehrmals im Monat aktualisiert. Bitte überprüfen Sie sie regelmäßig.

## Neue oder aktualisierte Funktionen in Adobe Analytics

| Funktion | Beschreibung | [Rollout-Beginn](releases.md) | [Allgemeine Verfügbarkeit](releases.md) |
| ----------- | ---------- | ------- | ---- |
| **Die Benutzeroberfläche für Datenschutzbezeichnungen wurde aktualisiert** | Die aktualisierte Benutzeroberfläche optimiert den Prozess der Erstellung, Verwaltung und Bearbeitung von Datenschutzbezeichnungen für Report Suite-Komponenten. [Weitere Informationen](https://experienceleague.adobe.com/docs/analytics/admin/data-governance/data-labels/gdpr-setup-reportsuite.html?lang=en) | Nicht angegeben | 8. Februar 2023 |
| **Vergleichsdatumsbereiche in mobilen Scorecards** | Mit mobilen Scorecards können Sie die **[!UICONTROL Vergleichsdaten einschließen]** Einstellung zum Anzeigen oder Ausblenden von Vergleichsdaten. | Nicht angegeben | 8. Februar 2023 |
| **Kalenderaktualisierungen in Workspace** | <ul><li>Datumsangaben im Ankerbereich: Sie können die Datumsbereichskomponenten relativ zum Bedienfeldkalender festlegen. [Weitere Informationen](/help/analyze/analysis-workspace/components/calendar-date-ranges/calendar.md#relative-panel-dates)</li><li>Aktualisierungen des Kalenderstils: Die Kalenderstile in der gesamten Benutzeroberfläche wurden aktualisiert, um einen konsistenteren und benutzerfreundlicheren Workflow zu bieten.</li><li>Aktualisierungen der Kalenderformel: Wenn Sie relative Datumswerte verwenden, spiegeln alle Kalenderformeln den Beginn des Datumsbereichs des Bedienfelds wider. [Weitere Informationen](/help/analyze/analysis-workspace/components/calendar-date-ranges/calendar.md#formula-relative-dates)</li></ul> | Nicht angegeben | 8. Februar 2023 |
| **Zeilen-/Spaltenfilter für Adobe Analytics Source Connector-Streaming** | Der Analytics Source Connector in Adobe Experience Platform ermöglicht jetzt das Filtern von Analytics-Daten, mit denen Profile in [Echtzeit-Kundenprofil](https://experienceleague.adobe.com/docs/experience-platform/profile/home.html?lang=de). Die Filterung auf Zeilenebene hilft, die Anzahl der mit Profilen verknüpften Ereignisse zu reduzieren. Die Filterung auf Spaltenebene hilft, den Reichtum der Ereignisse selbst zu reduzieren, und ermöglicht es Ihnen so, die Nutzung von Profilberechtigungen zu optimieren. Diese Filterung gilt nur für Daten, die an das Echtzeit-Kundenprofil gesendet werden, und [Identity Service](https://experienceleague.adobe.com/docs/experience-platform/identity/home.html?lang=de). **Die Filterung wirkt sich nicht auf die Daten aus, die zur Verwendung in Anwendungen wie Customer Journey Analytics an den Data Lake gesendet werden**. [Weitere Informationen](https://experienceleague.adobe.com/docs/experience-platform/sources/ui-tutorials/create/adobe-applications/analytics.html?lang=en#filtering-for-profile) | Nicht angegeben | 22. Februar 2023 |

{style=&quot;table-layout:auto&quot;}

## Fehlerbehebungen in Adobe Analytics

-302282; AN-303127; AN-303541; AN-303550; AN-305282; AN-306504; AN-307351; AN-307496; AN-307530; AN-307947; AN-308497; AN-; AN-308610; AN-308777; AN-308994; AN-309143; AN-309404; AN-309414; AN-309445; AN-309575; AN-309630; AN-309658; AN-309690; AN-309742; AN-309861; AN-309967; AN-309973; AN-310059; AN-310132; AN-310168; AN-310238; AN-310241; AN-310301; AN-310318; AN-310324; AN-310335; AN-310338; AN-310460; AN-310500; AN-310684; AN-310690; AN-311010; AN-311022; AN-311043; AN-311125; AN-311250; AN-311370; AN-311458;

## Wichtige Hinweise für Adobe Analytics-Administratoren

| Hinweis | Hinzugefügt oder aktualisiert am | Beschreibung |
| ----------- | ---------- | ---------- |
| **Aktualisierung der Gerätesuche aufgrund von Google-Client-Hinweisen** | 25. Januar 2023 | Die Verwendung von Client-Hinweisen bei der Gerätesuche beginnt am **16. Februar 2023**. <p> <p>Ab Oktober 2022 ist es möglich, Client-Hinweise entweder mit den Web SDK- oder AppMeasurement-JavaScript-Bibliotheken zu erfassen. Client-Hinweise werden jedoch erst im Februar 2023 in die Gerätesuche integriert. Zu diesem Zeitpunkt beginnt Adobe mit der Verwendung von Client-Hinweisen zusätzlich zum User-Agent, wenn bestimmte Geräteinformationen für Treffer von Chrome-Browsern abgeleitet werden, z. B. Google Chrome und Microsoft Edge. Dies ist eine Reaktion auf den Plan von Google, die Informationen, die der Benutzeragenten-Zeichenfolge entnommen werden können, schrittweise zu reduzieren und stattdessen Daten über Client-Hinweise zu übermitteln. <p> <p>Aufgrund dieser Änderung verwendet Adobe künftig Device Atlas für alle Geräte-Suchvorgänge im Zusammenhang mit dem Benutzeragenten. [Weitere Informationen](/help/technotes/client-hints.md) |
| **Anhalten geplanter Berichte in Reports &amp; Analytics** | 6. Januar 2023 | Diese Funktionen werden von Adobe nicht mehr unterstützt in **31. Januar 2023**. Bitte beachten Sie, dass das Ablauffenster für Berichte und Datenextrakte weiterhin auf neun Monate begrenzt ist. Die Bereitstellung von Berichten und Datenextraktionen wird am Ende dieses Zeitraums ausgesetzt, es sei denn, der Zeitplan wird reaktiviert.<p>Vor dem 31. Januar 2023 mussten Sie Ihre terminierten Berichte auf einen der anderen Mechanismen migrieren, die Ihnen in Adobe Analytics zur Verfügung standen. Bei weiteren Fragen oder bezüglich Support wenden Sie sich bitte an die Kundenunterstützung von Adobe. [Weitere Informationen](/help/analyze/reports-analytics/scheduled-reports-eol.md) |
| **Anhalten geplanter Aufgaben in Report Builder** | 6. Januar 2023 | on **31. Januar 2023**, führte Adobe im Rahmen unserer Leistungs- und Versandoptimierungsbemühungen Änderungen an geplanten Aufgaben in Report Builder durch. Zu diesen Änderungen gehörte auch das Entfernen der Möglichkeit, dass geplante Sendungen „nach x Ereignissen beendet werden“. <p>Sie können weiterhin stündliche Report Builder-Aufgaben planen und diese nach maximal 99 Vorfällen beenden lassen. Bitte beachten Sie, dass das Rollback nur für stündliche Aufgaben gilt. Die Option „Nach x Ereignissen beenden“ bleibt für alle anderen Versandintervalle (täglich, wöchentlich, monatlich und jährlich) weiterhin nicht verfügbar. Bei weiteren Fragen oder bezüglich Support wenden Sie sich bitte an die Kundenunterstützung von Adobe. [Weitere Informationen](/help/analyze/report-builder/r-arb-scheduled-reports.md) |

{style=&quot;table-layout:auto&quot;}

## Mitteilungen über das Ende der Nutzungsdauer

| Ende der Nutzungsdauer eines Produkts oder einer Funktion | Datum hinzugefügt oder aktualisiert | Beschreibung |
| --- | --- | --- |
| **EOL für Data Workbench** | 14. September 2022 | Adobe beabsichtigt, Data Workbench ab **31. Dezember 2023** einzustellen. Weitere Informationen finden Sie in der [Mitteilung zum Ende der Nutzungsdauer von Data Workbench](https://experienceleague.adobe.com/docs/data-workbench/using/eol.html?lang=de). Wenden Sie sich bei Fragen an den für Ihre Organisation zuständigen Adobe-Kundenbetreuer. |
| **EOL für [!DNL Reports & Analytics]** | 4. Januar 2022 | Adobe beabsichtigt, [!DNL Reports & Analytics] und die zugehörigen Berichte und Funktionen zum **31. Dezember 2023** einzustellen. Die Berichte, Visualisierungen und zugrunde liegenden Technologien, die [!DNL Reports & Analytics] unterstützen, entsprechen nicht mehr den technologischen Standards von Adobe. Die meisten Funktionen von [!DNL Reports & Analytics] sind in [Analysis Workspace](https://experienceleague.adobe.com/docs/analytics/analyze/analysis-workspace/home.html?lang=de) verfügbar. Seit der Veröffentlichung von Analysis Workspace im Jahr 2015 wurden die Funktionen von [!DNL Reports & Analytics] nach Analysis Workspace verschoben, und es wurde ein Schwellenwert für die Workflow-Parität erreicht. In [dieser Mitteilung](https://spark.adobe.com/page/6WnF8JK6IRDhf/) wird der Ablauf der Produktlebensdauer erläutert. |
| **EOL für die [!UICONTROL Veröffentlichungslisten]-Funktion** | 29. September 2022 | Im Rahmen des EOL von Reports &amp; Analytics ist geplant, dass die Veröffentlichungslisten im **Dezember 2023** das Ende ihrer Lebensdauer erreichen. Sie können keine neuen Veröffentlichungslisten erstellen oder auf vorhandene zugreifen, um Projekte in Analysis Workspace zu senden oder zu planen. |

{style=&quot;table-layout:auto&quot;}

## AppMeasurement

Die neuesten Aktualisierungen zu AppMeasurement-Versionen (Version 2.23.0) finden Sie in den [Versionshinweisen zu AppMeasurement für JavaScript](https://experienceleague.adobe.com/docs/analytics/implementation/appmeasurement-updates.html?lang=de).


## Verwandte Ressourcen

* [Frühere Versionshinweise für 2022](/help/release-notes/2022.md)
* [Versionshinweise zu Customer Journey Analytics](https://experienceleague.adobe.com/docs/analytics-platform/using/releases/latest.html?lang=de)
* [Versionshinweise zu Media Analytics](https://experienceleague.adobe.com/docs/media-analytics/using/additional-resources/release-notes.html?lang=de)
* Die neuesten Versions-Updates für [Adobe Experience Cloud-Produkte](https://business.adobe.com/de/products/adobe-experience-cloud-products.html)
