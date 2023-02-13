---
title: Neueste Analytics-Versionshinweise
description: Hier finden Sie die aktuellen Versionshinweise zu Adobe Analytics.
feature: Release Notes
exl-id: 97d16d5c-a8b3-48f3-8acb-96033cc691dc
source-git-commit: 2ba6ffc7f632975ca16fa02ee79d467d4d53f076
workflow-type: tm+mt
source-wordcount: '1053'
ht-degree: 51%

---

# Aktuelle Adobe Analytics-Versionshinweise (Februar 2023)

**Letzte Aktualisierung**: 9. Februar 2023

Die Versionen von Adobe Analytics basieren auf einem [kontinuierlichen Bereitstellungsmodell](releases.md), das eine besser skalierbare, schrittweise Implementierung von Funktionen ermöglicht. Dementsprechend werden diese Versionshinweise mehrmals im Monat aktualisiert. Bitte überprüfen Sie sie regelmäßig.

## Neue oder aktualisierte Funktionen in Adobe Analytics

| Funktion | Beschreibung | [Rollout-Beginn](releases.md) | [Allgemeine Verfügbarkeit](releases.md) |
| ----------- | ---------- | ------- | ---- |
| **Die Benutzeroberfläche für Datenschutzbezeichnungen wurde aktualisiert** | Die aktualisierte Benutzeroberfläche optimiert den Prozess der Erstellung, Verwaltung und Bearbeitung von Datenschutzbezeichnungen für Report Suite-Komponenten. [Weitere Informationen](https://experienceleague.adobe.com/docs/analytics/admin/data-governance/data-labels/gdpr-setup-reportsuite.html?lang=en) | Nicht angegeben | 8. Februar 2023 |
| **Ausblenden von Datumsbereichen für den Vergleich in mobilen Scorecards** | Mit mobilen Scorecards können Sie die **[!UICONTROL Vergleichsdaten einschließen]** Einstellung zum Anzeigen oder Ausblenden von Vergleichsdaten. | Nicht angegeben | 8. Februar 2023 |
| **Kalenderaktualisierungen in Workspace** | <ul><li>Datumsangaben im Ankerbereich: Sie können die Datumsbereichskomponenten relativ zum Bedienfeldkalender festlegen. [Weitere Informationen](/help/analyze/analysis-workspace/components/calendar-date-ranges/calendar.md#relative-panel-dates)</li><li>Aktualisierungen des Kalenderstils: Die Kalenderstile in der gesamten Benutzeroberfläche wurden aktualisiert, um einen konsistenteren und benutzerfreundlicheren Workflow zu bieten.</li><li>Aktualisierungen der Kalenderformel: Wenn Sie relative Datumswerte verwenden, spiegeln alle Kalenderformeln den Beginn des Datumsbereichs des Bedienfelds wider. [Weitere Informationen](/help/analyze/analysis-workspace/components/calendar-date-ranges/calendar.md#formula-relative-dates)</li></ul> | Nicht angegeben | 8. Februar 2023 |
| **Zeilen-/Spaltenfilter für Adobe Analytics Source Connector-Streaming** | Der Analytics Source Connector in Adobe Experience Platform ermöglicht jetzt das Filtern von Analytics-Daten, mit denen Profile in [Echtzeit-Kundenprofil](https://experienceleague.adobe.com/docs/experience-platform/profile/home.html?lang=de). Die Filterung auf Zeilenebene hilft, die Anzahl der mit Profilen verknüpften Ereignisse zu reduzieren. Die Filterung auf Spaltenebene hilft, den Reichtum der Ereignisse selbst zu reduzieren, und ermöglicht es Ihnen so, die Nutzung von Profilberechtigungen zu optimieren. Diese Filterung gilt nur für Daten, die an das Echtzeit-Kundenprofil gesendet werden, und [Identity Service](https://experienceleague.adobe.com/docs/experience-platform/identity/home.html?lang=de). **Die Filterung wirkt sich nicht auf die Daten aus, die zur Verwendung in Anwendungen wie Customer Journey Analytics an den Data Lake gesendet werden**. [Weitere Informationen](https://experienceleague.adobe.com/docs/experience-platform/sources/ui-tutorials/create/adobe-applications/analytics.html?lang=en#filtering-for-profile) | Nicht angegeben | 22. Februar 2023 |

{style=&quot;table-layout:auto&quot;}

## Fehlerbehebungen in Adobe Analytics 

-302282; AN-303127; AN-303541; AN-303550; AN-305282; AN-306504; AN-307351; AN-307496; AN-307530; AN-307947; AN-308497; AN-; AN-308610; AN-308777; AN-308994; AN-309143; AN-309404; AN-309414; AN-309445; AN-309575; AN-309630; AN-309658; AN-309690; AN-309742; AN-309861; AN-309967; AN-309973; AN-310059; AN-310132; AN-310168; AN-310238; AN-310241; AN-310301; AN-310318; AN-310324; AN-310335; AN-310338; AN-310460; AN-310500; AN-310684; AN-310690; AN-311010; AN-311022; AN-311043; AN-311125; AN-311250; AN-311370; AN-311458;

## Wichtige Hinweise für Adobe Analytics-Administratoren

| Hinweis | Hinzugefügt  oder aktualisiert am | Beschreibung |
| ----------- | ---------- | ---------- |
| **Automatische Migration zur Klassifizierungsset-Architektur** | 8. Februar 2023 | In den nächsten Monaten plant Adobe, alle Klassifizierungen unternehmensübergreifend auf die neueste Klassifizierungsarchitektur zu migrieren. Die letzten Kunden, die migriert werden, werden schätzungsweise im Mai 2023 stattfinden. Es ist keine Kundenaktion erforderlich und es wird keine Ausfallzeit erwartet. Diese neue Architektur bietet viele Vorteile, darunter:<ul><li>Deutlich verkürzte Verarbeitungszeit (72 Stunden → 24 Stunden)</li><li>Die Möglichkeit, die [Klassifizierungssätze](/help/components/classifications/sets/overview.md) Benutzeroberfläche</li><li>Die Option, Classification-Daten in Adobe Experience Platform künftig über die [Adobe Analytics-Quell-Connector für Classification-Daten](https://experienceleague.adobe.com/docs/experience-platform/sources/connectors/adobe-applications/classifications.html)</li></ul>Beachten Sie die folgenden Änderungen, die sich möglicherweise auf den Workflow Ihres Unternehmens auswirken können:<ul><li>Bei Verwendung des Browsers oder FTP-Imports wird[!UICONTROL Bei Konflikt überschreiben]&quot; ist immer aktiviert.</li><li>Bei Verwendung des Browsers oder FTP-Imports wird die Option zum sofortigen Export nach dem Import nicht mehr unterstützt.</li><li>Die Analytics 2.0-API `GetDimensions` -Endpunkt gibt jetzt Zeichenfolgenkennungen für Classifications anstelle numerischer Kennungen zurück. Numerische IDs können weiterhin verwendet werden. Adobe empfiehlt jedoch, nach Möglichkeit die neuen Zeichenfolgen-IDs zu verwenden. Numerische IDs können mithilfe der `?expansion=hidden` Abfragezeichenfolgen-Parameter.</li></ul>Wenden Sie sich an die Kundenunterstützung von Adobe, wenn Sie einen spezifischeren Migrationsplan für Ihr Unternehmen wünschen oder Fragen/Bedenken zu dieser Migration haben. [Weitere Informationen](/help/components/classifications/sets/overview.md) |
| **Aktualisierung der Gerätesuche aufgrund von Google-Client-Hinweisen** | 25. Januar 2023 | Die Verwendung von Client-Hinweisen bei der Gerätesuche ist ab **16. Februar 2023** verfügbar. <p> <p>Ab Oktober 2022 ist es möglich, Client-Hinweise entweder mit den Web SDK- oder den AppMeasurement-JavaScript-Bibliotheken zu erfassen. Die Client-Hinweise werden jedoch erst im Februar 2023 in die Gerätesuche integriert. Zu diesem Zeitpunkt wird Adobe bei der Erfassung bestimmter Geräteinformationen für Treffer in Chromium-Browsern wie Google Chrome und Microsoft Edge zusätzlich zum Benutzeragenten auch Client-Hinweise verwenden. Dies ist eine Reaktion auf den Plan von Google, die Informationen, die der Benutzeragenten-Zeichenfolge entnommen werden können, schrittweise zu reduzieren und stattdessen Daten über Client-Hinweise zu übermitteln. <p> <p>Aufgrund dieser Änderung verwendet Adobe künftig Device Atlas für alle Geräte-Suchvorgänge im Zusammenhang mit dem Benutzeragenten. [Weitere Informationen](/help/technotes/client-hints.md) |

{style=&quot;table-layout:auto&quot;}

## Mitteilungen zur Einstellung der Verwendung (End of Life, EOL)

| Ende der Nutzungsdauer eines Produkts oder einer Funktion | Datum hinzugefügt oder aktualisiert | Beschreibung |
| --- | --- | --- |
| **Entfernung einiger Funktionen für Reports &amp; Analytics und die Planung von Report Buildern** | 9. Februar 2023 | Die folgenden Planungsfunktionen wurden am 31. Januar 2023 eingestellt:<ul><li>Die Option &quot;Nach x Vorkommen beenden&quot;für stündliche Aufgaben in Report Builder</li><li>Möglichkeit, neue Berichte zu planen und Datenextraktionen in Reports and Analytics herunterzuladen</li></ul><p>**Hinweis**: Ursprünglich haben wir diese Funktionen im April 2022 beendet, aber die Änderung rückgängig gemacht. Wir haben außerdem eine Benachrichtigung gesendet, dass diese Funktionen vorübergehend wiederhergestellt wurden und am 31. Januar 2023 erneut beendet werden. |
| **EOL für die [!UICONTROL Veröffentlichungslisten]-Funktion** | 29. September 2022 | Im Rahmen des EOL von Reports &amp; Analytics ist geplant, dass die Veröffentlichungslisten im **Dezember 2023** das Ende ihrer Lebensdauer erreichen. Sie können keine neuen Veröffentlichungslisten erstellen oder auf vorhandene zugreifen, um Projekte in Analysis Workspace zu senden oder zu planen. |
| **EOL für Data Workbench** | 14. September 2022 | Adobe beabsichtigt, Data Workbench ab **31. Dezember 2023** einzustellen. Weitere Informationen finden Sie in der [Mitteilung zum Ende der Nutzungsdauer von Data Workbench](https://experienceleague.adobe.com/docs/data-workbench/using/eol.html?lang=de). Wenden Sie sich bei Fragen an den für Ihre Organisation zuständigen Adobe-Kundenbetreuer. |
| **EOL für [!DNL Reports & Analytics]** | 4. Januar 2022 | Adobe beabsichtigt, [!DNL Reports & Analytics] und die zugehörigen Berichte und Funktionen zum **31. Dezember 2023** einzustellen. Die Berichte, Visualisierungen und zugrunde liegenden Technologien, die [!DNL Reports & Analytics] unterstützen, entsprechen nicht mehr den technologischen Standards von Adobe. Die meisten Funktionen von [!DNL Reports & Analytics] sind in [Analysis Workspace](https://experienceleague.adobe.com/docs/analytics/analyze/analysis-workspace/home.html?lang=de) verfügbar. Seit der Veröffentlichung von Analysis Workspace im Jahr 2015 wurden die Funktionen von [!DNL Reports & Analytics] nach Analysis Workspace verschoben, und es wurde ein Schwellenwert für die Workflow-Parität erreicht. In [dieser Mitteilung](https://spark.adobe.com/page/6WnF8JK6IRDhf/) wird der Ablauf der Produktlebensdauer erläutert. |

{style=&quot;table-layout:auto&quot;}

## AppMeasurement

Die neuesten Aktualisierungen zu AppMeasurement-Versionen (Version 2.23.0) finden Sie in den [Versionshinweisen zu AppMeasurement für JavaScript](https://experienceleague.adobe.com/docs/analytics/implementation/appmeasurement-updates.html?lang=de).


## Verwandte Ressourcen

* [Frühere Versionshinweise für 2022](/help/release-notes/2022.md)
* [Versionshinweise zu Customer Journey Analytics](https://experienceleague.adobe.com/docs/analytics-platform/using/releases/latest.html?lang=de)
* [Versionshinweise zu Media Analytics](https://experienceleague.adobe.com/docs/media-analytics/using/additional-resources/release-notes.html?lang=de)
* Die neuesten Versions-Updates für [Adobe Experience Cloud-Produkte](https://business.adobe.com/de/products/adobe-experience-cloud-products.html)
