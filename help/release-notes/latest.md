---
title: Neueste Analytics-Versionshinweise
description: Hier finden Sie die aktuellen Versionshinweise zu Adobe Analytics.
feature: Release Notes
exl-id: 97d16d5c-a8b3-48f3-8acb-96033cc691dc
source-git-commit: a71db2fac9333b70a55da91fe9a94b0cc8434b42
workflow-type: tm+mt
source-wordcount: '1087'
ht-degree: 100%

---

# Aktuelle Adobe Analytics-Versionshinweise (Juli 2022)

**Letzte Aktualisierung**: 13. Juli 2022

## Verwandte Ressourcen

* [Frühere Versionshinweise für 2022](/help/release-notes/2022.md)
* [Versionshinweise zu Customer Journey Analytics](https://experienceleague.adobe.com/docs/analytics-platform/using/releases/latest.html?lang=de)
* [Versionshinweise zu Media Analytics](https://experienceleague.adobe.com/docs/media-analytics/using/additional-resources/release-notes.html?lang=de)
* Die neuesten Versions-Updates für [Adobe Experience Cloud-Produkte](https://business.adobe.com/de/products/adobe-experience-cloud-products.html)

## Neue Funktionen in Adobe Analytics

| Funktion | Beschreibung | [Zieldatum](releases.md) |
| ----------- | ---------- | ------- |
| Unterstützung für Merchandising-Variablen in XDM für Edge-Erfassung | Ermöglicht Kunden, die Daten über Experience Edge/Web SDK erfassen, XDM zur Angabe der verschiedenen Werte für Merchandising-Variablen (eVars) zu verwenden. [Weitere Informationen](https://experienceleague.adobe.com/docs/analytics/implementation/vars/page-vars/evar-merchandising.html?lang=de) | 29. Juni 2022 |

{style=&quot;table-layout:auto&quot;}

## Fehlerbehebungen in Adobe Analytics

* Es wurden einige Fehler bei der Segmentkonversion behoben. (AN-291262, AN-294092)

**Fehlerbehebungen für einzelne Kunden**:

AN-280192; AN-281628; AN-287022; AN-287104; AN-287876; AN-288802; AN-288457; AN-288779; AN-288799; AN-289198; AN-289852; AN-289931; AN-290162; AN-290213; AN-291059; AN-291090; AN-291270; AN-294091; AN-294135; AN-294152; AN-294158; AN-294285; AN-294317; AN-294404; AN-294531; AN-294769; AN-294984; AN-295172; AN-295211; AN-295224; AN-295413; AN-295440; AN-295465; AN-295499; AN-295516;

## Wichtige Hinweise für Adobe Analytics-Administratoren

| Hinweis | Hinzugefügt oder aktualisiert am | Beschreibung |
| ----------- | ---------- | ---------- |
| **Neue Domain für systemgenerierte E-Mails** | 13. Juli 2022 | Am **18. Mai 2022** hat Adobe die Absender-Domain für E-Mails aus Workspace-Projekten, Warnhinweise und Überlastungs-Warnhinweisen von `noreply@omniture.com` in `noreply@adobe.com` geändert. Fügen Sie diese neue E-Mail zu Ihrer Zulassungsliste hinzu, wenn Ihr Unternehmen nur bestimmte Absender zulässt. |
| **Aktualisierung auf die neue NetAcuity-Provider-Datenbank** | 11. Juli 2022 | **Ab Oktober 2022** werden sich die im Feld `carrier` in Adobe Analytics Data Warehouse und Analytics-Daten-Feeds gespeicherten Informationen zum Provider ändern. Traditionell war das Datenformat in dieser Spalte `<domain>:<ISP>`. Adobe hat eine interne Lookup-Tabelle gepflegt, um diese `<domain>:<ISP>`-Werte Provider-Namen für das Reporting in den Reporting-Tools von Adobe Analytics (Analysis Workspace, Reports &amp; Analytics, Reporting-API, Data Warehouse, LiveStream usw.) zuzuordnen. Die Lookup-Datei (carrier.tsv) wird auch mit Daten-Feeds bereitgestellt, damit Daten-Feeds-Kunden dieselben Zuordnungen verwenden können.<p>Diese Aktualisierung verbessert unsere Provider-Zuordnung durch die Verwendung einer präziseren Provider-Datenbank von NetAcuity. Das Format der Daten in der Provider-Spalte in Daten-Feeds wird sich in Zukunft ändern. Anstelle von `<domain>:<ISP>` wird dort ein Provider-Name enthalten sein. Adobe wird weiterhin die Lookup-Tabelle verwenden, um im Hinblick auf bereits erfolgtes Reporting so viel Kontinuität wie möglich aufrechtzuerhalten. Reporting-Tools, bei denen die Suchen von Adobe angewendet werden (Analysis Workspace, Reports &amp; Analytics, Reporting-API, Data Warehouse, LiveStream usw.), profitieren von präziseren Zuordnungen. Einige Zuordnungen – insbesondere für internationale Domains und ISPs – werden sich stärker verändern als andere, sobald wir die neue Datenbank anwenden. Die Nachschlagedatei der Daten-Feeds (carrier.tsv) verwaltet die alten Zuordnungen und fügt die neuen Zuordnungen hinzu.<p>Der Analytics-Quell-Connector ordnet derzeit das Provider-Feld nicht zu, weshalb aktuell in AEP, CJA usw. kein Reporting zu Providern verfügbar ist. Daher hat die Verwendung der neuen Provider-Datenbank keinerlei Auswirkungen auf Daten in AEP, die auf den vom Analytics-Quell-Connector bereitgestellten Daten basieren. |
| **Verbesserte Geolokalisierung von IPs** | 11. Juli 2022 | Unser Anbieter für IP-Lookups, Digital Element, aktualisiert für die Geolokalisierung von IPs auf einen neuen verbesserten Datensatz (NetAcuity Pulse). Adobe Analytics übernimmt diesen neuen Datensatz im Zeitrahmen **Oktober 2022**. Die neue Datenbank wird genauer sein als frühere Versionen. Einige Geolokalisierungen von IPs werden sich ändern/verbessern, wenn die neue Datenbank übernommen wurde.<p>Alle Adobe Analytics-Tools (Analysis Workspace, Reports &amp; Analytics, Reporting-API, Data Warehouse, LiveStream, Daten-Feeds usw.) nutzen automatisch die neuen verbesserten Zuordnungen. Das Format der Daten in Daten-Feeds wird sich nicht ändern. CJA-Daten, die über den Analytics-Quell-Connector bereitgestellt werden, nutzen ebenfalls automatisch die neuen Zuordnungen. |
| **Anhalten geplanter Berichte in Reports &amp; Analytics** | 8. Juni 2022 | Am 21. April 2022 haben wir bekannt gegeben, dass einige Funktionen für terminierte Berichte eingestellt wurden, um die zuvor angekündigte Einstellung von Reports &amp; Analytics vorzubereiten. Zu diesen Funktionen gehörte die Möglichkeit, neue Berichte sowie neue Datenextraktionen zu planen.<p>Als Reaktion auf Kundenanfragen, die um eine Verlängerung baten, und um den Übergang weg von Reports and Analytics zu erleichtern, haben wir beschlossen, den Zugriff auf diese Funktionen bis zum **31. Januar 2023** zu verlängern. Bitte beachten Sie, dass das Ablauffenster für Berichte und Datenextrakte weiterhin auf neun Monate begrenzt ist. Die Bereitstellung von Berichten und Datenextraktionen wird am Ende dieses Zeitraums ausgesetzt, es sei denn, der Zeitplan wird reaktiviert.<p>Um es noch einmal zu sagen: Diese Funktionen werden am 31. Januar 2023 eingestellt. Bis zu diesem Datum müssen Sie Ihre terminierten Berichte auf einen der anderen Mechanismen migriert haben, die Ihnen in Adobe Analytics zur Verfügung stehen. Bei weiteren Fragen oder bezüglich Support wenden Sie sich bitte an die Kundenunterstützung von Adobe. [Weitere Informationen](/help/analyze/reports-analytics/scheduled-reports-eol.md) |
| **Anhalten geplanter Aufgaben in Report Builder** | 8. Juni 2022 | Am 21. April 2022 haben wir im Rahmen unserer Leistungs- und Versandoptimierungsbemühungen in Report Builder Änderungen an terminierten Aufgaben durchgeführt. Zu diesen Änderungen gehörte auch das Entfernen der Möglichkeit, dass geplante Sendungen „nach x Vorfällen beendet werden“. Als Reaktion auf mehrere Kundenanfragen, die mehr Zeit für die Erkundung und Implementierung von Alternativen benötigen, haben wir beschlossen, diese Option in begrenztem Umfang wieder einzuführen und bis zum **31. Januar 2023** aufrecht zu erhalten.<p>Sie können weiterhin stündliche Report Builder-Aufgaben planen und diese nach maximal 99 Vorfällen beenden lassen. Bitte beachten Sie, dass das Rollback nur für stündliche Aufgaben gilt. Die Option „Nach x Vorkommen beenden“ bleibt für alle anderen Versandintervalle (täglich, wöchentlich, monatlich und jährlich) weiterhin nicht verfügbar. Bitte beachten Sie, dass diese Option ab dem 31. Januar 2023 nicht mehr unterstützt wird. Bei weiteren Fragen oder bezüglich Support wenden Sie sich bitte an die Kundenunterstützung von Adobe. [Weitere Informationen](/help/analyze/report-builder/r-arb-scheduled-reports.md) |
| **SFTP-Upgrade** | 9. Mai 2022 | Zuvor hatten wir mitgeteilt, dass Adobe im Mai 2022 seine Secure File Transfer Protocol (SFTP)-Services aktualisieren würde, um die Sicherheit für die Dateiübertragung zu verbessern. Wir haben diese Aktualisierung auf den **Sommer 2022** verschoben. Nach dieser Änderung werden bestimmte SFTP-Client-Konfigurationen nicht mehr unterstützt. Dies wirkt sich nur auf Daten aus, die per SFTP an Adobe Analytics gesendet oder von Adobe Analytics abgerufen werden. Das FTP-Protokoll ist nicht betroffen. Um Service-Unterbrechungen zu vermeiden, stellen Sie bitte sicher, dass Ihre SFTP-Clients (Code, Tools, Services) die [hier](https://experienceleague.adobe.com/docs/analytics/export/ftp-and-sftp/secure-file-transfer-protocol/sftp-upgrade.html?lang=de) beschriebenen Anforderungen erfüllen. |
| **EOL für [!DNL Reports & Analytics]** | 4. Januar 2022 | Adobe beabsichtigt, [!DNL Reports & Analytics] und die zugehörigen Berichte und Funktionen zum **31. Dezember 2023** einzustellen. Die Berichte, Visualisierungen und zugrunde liegenden Technologien von [!DNL Reports & Analytics] entsprechen nicht mehr den technologischen Standards von Adobe. Die meisten Funktionen von [!DNL Reports & Analytics] sind in [Analysis Workspace](https://experienceleague.adobe.com/docs/analytics/analyze/analysis-workspace/home.html?lang=de) verfügbar. Seit der Veröffentlichung von Analysis Workspace im Jahr 2015 wurden die Funktionen von [!DNL Reports & Analytics] nach Analysis Workspace verschoben, und es wurde ein Schwellenwert für die Workflow-Parität erreicht. In [dieser Mitteilung](https://spark.adobe.com/page/6WnF8JK6IRDhf/) wird der Ablauf der Produktlebensdauer erläutert. |

{style=&quot;table-layout:auto&quot;}

## AppMeasurement

Die neuesten Aktualisierungen zu AppMeasurement-Versionen (Version 2.22.4) finden Sie in den [Versionshinweisen zu AppMeasurement für JavaScript](https://experienceleague.adobe.com/docs/analytics/implementation/appmeasurement-updates.html?lang=de).

