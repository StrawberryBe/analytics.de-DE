---
title: Neueste Analytics-Versionshinweise
description: Hier finden Sie die aktuellen Versionshinweise zu Adobe Analytics.
feature: Release Notes
exl-id: 97d16d5c-a8b3-48f3-8acb-96033cc691dc
source-git-commit: ac9e4934cee0178fb00e4201cc3444d333a74052
workflow-type: tm+mt
source-wordcount: '1422'
ht-degree: 99%

---

# Aktuelle Adobe Analytics-Versionshinweise (Oktober/November 2022)

**Letztes Update**: 28. Oktober 2022

Die Versionen von Adobe Analytics basieren auf einem [kontinuierlichen Bereitstellungsmodell](releases.md), das eine besser skalierbare, schrittweise Implementierung von Funktionen ermöglicht. Dementsprechend werden diese Versionshinweise mehrmals im Monat aktualisiert. Bitte überprüfen Sie sie regelmäßig.

## Neue oder aktualisierte Funktionen in Adobe Analytics

| Funktion | Beschreibung | [Rollout-Beginn](releases.md) | [Allgemeine Verfügbarkeit](releases.md) |
| ----------- | ---------- | ------- | ---- |
| Visualisierung der **[!UICONTROL Zusammenfassung einer Schlüsselmetrik]** | Durch die Visualisierung der [!UICONTROL Zusammenfassung einer Schlüsselmetrik] können Sie sehen, wie sich eine wichtige Metrik innerhalb eines einzigen Zeitraums entwickelt. Außerdem können Sie damit die Leistung von Metriken über zwei Zeiträume hinweg vergleichen. [Weitere Informationen](https://experienceleague.adobe.com/docs/analytics/analyze/analysis-workspace/visualizations/key-metric.html) | 5. Oktober 2022 | 19. Oktober 2023 |
| **Variablen mit mehreren Werten, bei denen nicht zwischen Groß- und Kleinschreibung unterschieden wird** | Bei Mehrwert-Variablen ohne Unterscheidung von Groß- und Kleinschreibung werden die in `mvvar1 - mvvar3` und `post_mvvar1 - post_mvvar3` gespeicherten Werte in Daten-Feeds nicht mehr automatisch kleingeschrieben. Stattdessen spiegeln Daten-Feeds (und Daten, die über den Analytics Source Connector an Adobe Experience Platform und CJA weitergeleitet werden) die ursprüngliche Groß-/Kleinschreibung wider, die von der Seite übermittelt wurde. | Nicht angegeben | 24. Oktober 2022 |

{style=&quot;table-layout:auto&quot;}

## Fehlerbehebungen in Adobe Analytics

* Es wurde ein Problem behoben, bei dem aktuelle macOS-Versionen fälschlicherweise als „Macintosh“ bezeichnet wurden. Ab dieser Fehlerbehebung beginnt die Betriebssystemdimension mit der Nummerierung der macOS-Version, beginnend mit macOS 11. (AN-301834)
* Es wurde ein Problem mit dem Datumsbereich „Feste Datumswerte“ in Report Builder behoben. (AN-303684)
* Es wurden Probleme behoben, die dazu führten, dass die Daten-Feed-Benutzeroberfläche nicht geladen wurde. (AN-303803, AN-303784)

### Weitere Fehlerbehebungen

AN-295574; AN-296354; AN-297143; AN-299501; AN-301755; AN-302054; AN-302304; AN-302631; AN-302811; AN-303090; AN-303372; AN-303428; AN-303429; AN-303432; AN-303434; AN-303437; AN-303438; AN-303519; AN-303610; AN-303656; AN-303659; AN-303663; AN-303664; AN-303818; AN-303823; AN-303837; AN-304036;  AN-304195; AN-304321; AN-304325; AN-304339; AN-304356; AN-304435; AN-304457; AN-304509; AN-304519; AN-304534

## Wichtige Hinweise für Adobe Analytics-Administratoren

| Hinweis | Hinzugefügt oder aktualisiert am | Beschreibung |
| ----------- | ---------- | ---------- |
| **Aktualisierung der Gerätesuche aufgrund von Google-Client-Hinweisen** | 14. Oktober 2022 | Die ursprünglich für den 26. Oktober 2022 geplante Verwendung von Client-Hinweisen bei der Gerätesuche wurde auf **Januar 2023** verschoben. <p> <p>Ab Oktober 2022 ist es möglich, Client-Hinweise entweder mit den Web SDK- oder den AppMeasurement-JavaScript-Bibliotheken zu erfassen. Die Client-Hinweise werden jedoch erst im Januar 2023 in die Gerätesuche integriert. Zu diesem Zeitpunkt wird Adobe bei der Erfassung bestimmter Geräteinformationen für Treffer in Chromium-Browsern wie Google Chrome und Microsoft Edge zusätzlich zum Benutzeragenten auch Client-Hinweise verwenden. Dies ist eine Reaktion auf den Plan von Google, die Informationen, die der Benutzeragenten-Zeichenfolge entnommen werden können, schrittweise zu reduzieren und stattdessen Daten über Client-Hinweise zu übermitteln. <p> <p>Aufgrund dieser Änderung verwendet Adobe künftig Device Atlas für alle Geräte-Suchvorgänge im Zusammenhang mit dem Benutzeragenten. [Weitere Informationen](/help/technotes/client-hints.md) |
| **Standard-Landingpage** | 29. September 2022 | Die [neue Landingpage](/help/analyze/landing.md) wurde Anfang dieses Jahres eingeführt und wird ab **Januar 2023** zum Standarderlebnis für alle Benutzerinnen und Benutzer. Die aktuelle Seite wird eingestellt, sodass nur mehr die neue Seite verwendet wird. |
| Bedingungen für die automatische Ausführung der **[!UICONTROL Anomalieerkennung]** | 29. September 2022 | Die [!UICONTROL Anomalieerkennung] wird automatisch für alle Spalten von Zeitreihen-Freiformtabellen ausgeführt. Um sicherzustellen, dass Daten für die Analyse verfügbar sind und Projekte schneller geladen werden, verändert Adobe die automatische Ausführung der Anomalieerkennung. Ab dem **26. Oktober 2022** wird die [!UICONTROL Anomalieerkennung] nur für die erste Metrikspalte in einer Tabelle automatisch ausgeführt. Sie können die Spalteneinstellungen bei Bedarf so konfigurieren, dass die Anomalieerkennung für andere Spalten ausgeführt wird. |
| **Aktualisierung auf die neue NetAcuity-Provider-Datenbank** | 26. September 2022 | Diese Aktualisierung, die ursprünglich für den 5. Oktober 2022 geplant war, wurde auf **Januar 2023** verschoben. Die im Feld `carrier` in Adobe Analytics Data Warehouse und in Analytics Data Feeds gespeicherten Informationen zum Provider werden sich ändern. Traditionell war das Datenformat in dieser Spalte `<domain>:<ISP>`. Adobe hat eine interne Lookup-Tabelle gepflegt, um diese `<domain>:<ISP>`-Werte Provider-Namen für das Reporting in den Reporting-Tools von Adobe Analytics (Analysis Workspace, Reports &amp; Analytics, Reporting-API, Data Warehouse, LiveStream usw.) zuzuordnen. Die Lookup-Datei (`carrier.tsv`) wird auch mit Daten-Feeds bereitgestellt, damit Sie dieselben Zuordnungen verwenden können.<p>Diese Aktualisierung verbessert unsere Provider-Zuordnung durch die Verwendung einer präziseren Provider-Datenbank von NetAcuity. Das Format der Daten in der Provider-Spalte in Daten-Feeds wird sich in Zukunft ändern. Anstelle von `<domain>:<ISP>` wird dort ein Provider-Name enthalten sein. Adobe wird weiterhin die Lookup-Tabelle verwenden, um im Hinblick auf bereits erfolgtes Reporting so viel Kontinuität wie möglich aufrechtzuerhalten. Reporting-Tools, bei denen die Suchen von Adobe angewendet werden (Analysis Workspace, Reports &amp; Analytics, Reporting-API, Data Warehouse, LiveStream usw.), profitieren von präziseren Zuordnungen. Einige Zuordnungen – insbesondere für internationale Domains und ISPs – werden sich stärker verändern als andere, sobald Adobe die neue Datenbank anwendet. Die Provider-Lookup-Datei der Daten-Feeds (`carrier.tsv`) verwaltet die alten Zuordnungen und fügt die neuen Zuordnungen hinzu.<p>Der Analytics-Quell-Connector ordnet derzeit das Provider-Feld nicht zu, weshalb derzeit in Experience Platform, CJA usw. kein Reporting zu Providern verfügbar ist. Daher hat die Verwendung der neuen Provider-Datenbank keinerlei Auswirkungen auf Daten in Experience Platform, die auf den vom Analytics-Quell-Connector bereitgestellten Daten basieren. |
| **Verbesserte Geolokalisierung von IPs** | 26. September 2022 | Unser Anbieter für IP-Lookups, Digital Element, aktualisiert für die Geolokalisierung von IPs auf einen neuen verbesserten Datensatz (NetAcuity Pulse). Ursprünglich für Oktober 2022 geplant, wird Adobe Analytics diesen neuen Datensatz im **Januar 2023** übernehmen. Die neue Datenbank wird genauer sein als frühere Versionen. Einige Geolokalisierungen von IPs werden sich ändern/verbessern, wenn die neue Datenbank übernommen wurde.<p>Alle Adobe Analytics-Tools (Analysis Workspace, Reports &amp; Analytics, Reporting-API, Data Warehouse, LiveStream, Daten-Feeds usw.) nutzen automatisch die neuen verbesserten Zuordnungen. Das Format der Daten in Daten-Feeds wird sich nicht ändern. CJA-Daten, die über den Analytics-Quell-Connector bereitgestellt werden, nutzen ebenfalls automatisch die neuen Zuordnungen. |
| **Anhalten geplanter Berichte in Reports &amp; Analytics** | 8. Juni 2022 | Am 21. April 2022 hat Adobe bekannt gegeben, dass einige Funktionen für terminierte Berichte eingestellt wurden, um die zuvor angekündigte Einstellung von Reports &amp; Analytics vorzubereiten. Zu diesen Funktionen gehörte die Möglichkeit, neue Berichte sowie neue Datenextraktionen zu planen.<p>Als Reaktion auf Kundenanfragen, die um eine Verlängerung baten, und um den Übergang weg von Reports &amp; Analytics zu erleichtern, hat Adobe beschlossen, den Zugriff auf diese Funktionen bis zum **31. Januar 2023** zu verlängern. Bitte beachten Sie, dass das Ablauffenster für Berichte und Datenextrakte weiterhin auf neun Monate begrenzt ist. Die Bereitstellung von Berichten und Datenextraktionen wird am Ende dieses Zeitraums ausgesetzt, es sei denn, der Zeitplan wird reaktiviert.<p>Um es noch einmal zu sagen: Diese Funktionen werden am 31. Januar 2023 eingestellt. Bis zu diesem Datum müssen Sie Ihre terminierten Berichte auf einen der anderen Mechanismen migriert haben, die Ihnen in Adobe Analytics zur Verfügung stehen. Bei weiteren Fragen oder bezüglich Support wenden Sie sich bitte an die Kundenunterstützung von Adobe. [Weitere Informationen](/help/analyze/reports-analytics/scheduled-reports-eol.md) |
| **Anhalten geplanter Aufgaben in Report Builder** | 8. Juni 2022 | Am 21. April 2022 habt Adobe im Rahmen seiner Leistungs- und Versandoptimierungsbemühungen in Report Builder Änderungen an terminierten Aufgaben durchgeführt. Zu diesen Änderungen gehörte auch das Entfernen der Möglichkeit, dass geplante Sendungen „nach x Ereignissen beendet werden“. Als Reaktion auf mehrere Kundenanfragen, die mehr Zeit für die Suche und Implementierung von Alternativen benötigen, hat Adobe beschlossen, diese Option in begrenztem Umfang wieder einzuführen und bis zum **31. Januar 2023** aufrecht zu erhalten.<p>Sie können weiterhin stündliche Report Builder-Aufgaben planen und diese nach maximal 99 Vorfällen beenden lassen. Bitte beachten Sie, dass das Rollback nur für stündliche Aufgaben gilt. Die Option „Nach x Ereignissen beenden“ bleibt für alle anderen Versandintervalle (täglich, wöchentlich, monatlich und jährlich) weiterhin nicht verfügbar. Bitte beachten Sie, dass diese Option ab dem 31. Januar 2023 nicht mehr unterstützt wird. Bei weiteren Fragen oder bezüglich Support wenden Sie sich bitte an die Kundenunterstützung von Adobe. [Weitere Informationen](/help/analyze/report-builder/r-arb-scheduled-reports.md) |

{style=&quot;table-layout:auto&quot;}

## Mitteilungen über das Ende der Nutzungsdauer

| Ende der Nutzungsdauer eines Produkts oder einer Funktion | Datum hinzugefügt oder aktualisiert | Beschreibung |
| --- | --- | --- |
| **EOL für die [!UICONTROL Veröffentlichungslisten]-Funktion** | 29. September 2022 | Im Rahmen des EOL von Reports &amp; Analytics ist geplant, dass die Veröffentlichungslisten im **Dezember 2023** das Ende ihrer Lebensdauer erreichen. Sie können keine neuen Veröffentlichungslisten erstellen oder auf vorhandene zugreifen, um Projekte in Analysis Workspace zu senden oder zu planen. [Weitere Informationen](/help/admin/admin/publishing-list.md) |
| **EOL für Data Workbench** | 14. September 2022 | Adobe beabsichtigt, Data Workbench ab **31. Dezember 2023** einzustellen. Weitere Informationen finden Sie in der [Mitteilung zum Ende der Nutzungsdauer von Data Workbench](https://experienceleague.adobe.com/docs/data-workbench/using/eol.html?lang=de). Wenden Sie sich bei Fragen an den für Ihre Organisation zuständigen Adobe-Kundenbetreuer. |
| **EOL für [!DNL Reports & Analytics]** | 4. Januar 2022 | Adobe beabsichtigt, [!DNL Reports & Analytics] und die zugehörigen Berichte und Funktionen zum **31. Dezember 2023** einzustellen. Die Berichte, Visualisierungen und zugrunde liegenden Technologien, die [!DNL Reports & Analytics] unterstützen, entsprechen nicht mehr den technologischen Standards von Adobe. Die meisten Funktionen von [!DNL Reports & Analytics] sind in [Analysis Workspace](https://experienceleague.adobe.com/docs/analytics/analyze/analysis-workspace/home.html) verfügbar. Seit der Veröffentlichung von Analysis Workspace im Jahr 2015 wurden die Funktionen von [!DNL Reports & Analytics] nach Analysis Workspace verschoben, und es wurde ein Schwellenwert für die Workflow-Parität erreicht. In [dieser Mitteilung](https://spark.adobe.com/page/6WnF8JK6IRDhf/) wird der Ablauf der Produktlebensdauer erläutert. |

{style=&quot;table-layout:auto&quot;}

## AppMeasurement

Die neuesten Aktualisierungen zu AppMeasurement-Versionen (Version 2.23.0) finden Sie in den [Versionshinweisen zu AppMeasurement für JavaScript](https://experienceleague.adobe.com/docs/analytics/implementation/appmeasurement-updates.html?lang=de).

## Verwandte Ressourcen

* [Frühere Versionshinweise für 2022](/help/release-notes/2022.md)
* [Versionshinweise zu Customer Journey Analytics](https://experienceleague.adobe.com/docs/analytics-platform/using/releases/latest.html?lang=de)
* [Versionshinweise zu Media Analytics](https://experienceleague.adobe.com/docs/media-analytics/using/additional-resources/release-notes.html?lang=de)
* Die neuesten Versions-Updates für [Adobe Experience Cloud-Produkte](https://business.adobe.com/de/products/adobe-experience-cloud-products.html)
