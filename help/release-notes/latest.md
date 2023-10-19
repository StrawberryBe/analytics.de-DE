---
title: Aktuelle Adobe Analytics-Versionshinweise
description: Aktuelle Versionshinweise zu Adobe Analytics anzeigen
feature: Release Notes
exl-id: 97d16d5c-a8b3-48f3-8acb-96033cc691dc
source-git-commit: 69cffe2bc97a81cb9e4b989f2193dc2deb6e8d22
workflow-type: tm+mt
source-wordcount: '1236'
ht-degree: 65%

---

# Aktuelle Adobe Analytics-Versionshinweise (Oktober 2023)

**Letztes Update**: 19. Oktober 2023

Die Versionshinweise vom Oktober beziehen sich auf den Veröffentlichungszeitraum vom 4. Oktober 2023 bis zum 25. Oktober 2023. Die Versionen von Adobe Analytics basieren auf einem [kontinuierlichen Bereitstellungsmodell](releases.md), das eine besser skalierbare, schrittweise Implementierung von Funktionen ermöglicht. Dementsprechend werden diese Versionshinweise mehrmals im Monat aktualisiert. Bitte überprüfen Sie sie regelmäßig.

## Neue Funktionen oder Verbesserungen {#features}

| Funktion | Beschreibung | [Rollout-Beginn](releases.md) | [Allgemeine Verfügbarkeit](releases.md) |
| ----------- | ---------- | ------- | ---- |
| **Neue Spalten verfügbar bei der Verwaltung von Komponenten** | Die folgenden neuen Spalten sind jetzt bei der Verwaltung von Komponenten verfügbar:<ul><li>Verwendet in<p>Diese Spalte ist im Abschnitt [Manager für berechnete Metriken](/help/components/c-calcmetrics/c-workflow/cm-workflow/cm-manager.md) und [Segment-Manager](/help/components/segmentation/segmentation-workflow/seg-manage.md).</p></li><li>Zuletzt verwendet<p>Diese Spalte ist im Abschnitt [Manager für berechnete Metriken](/help/components/c-calcmetrics/c-workflow/cm-workflow/cm-manager.md), die [Segment-Manager](/help/components/segmentation/segmentation-workflow/seg-manage.md)und die [Warnhinweis-Manager](/help/components/c-alerts/alert-manager.md).</p></li></ul><p>Mithilfe dieser Informationen können Sie feststellen, ob eine Komponente für Benutzerinnen und Benutzer in Ihrer Organisation nützlich ist, wo sie verwendet wird und ob sie gelöscht oder geändert werden muss. Sie können das Datenwörterbuch zusammen mit diesen Informationen verwenden, um die Verwendung von Komponenten in Ihrem Unternehmen zu verfolgen und besser zu verstehen.</p> | 20. September 2023 | 4. Oktober 2023 |
| **Verbesserungen bei Reporting Activity Manager** | Reporting Activity Manager zeigt die Berichtskapazität für jede Report Suite in Ihrer Organisation an.  Er bietet Admins detaillierte Einblicke in die Berichtsnutzung und hilft ihnen, Kapazitätsprobleme bei Spitzen während der Berichterstellung mühelos zu diagnostizieren und zu beheben. Im Folgenden finden Sie einige der Verbesserungen, die jetzt im Reporting Activity Manager verfügbar sind: <ul><li>Einschränken nachfolgender Anforderungen: Neben dem Abbrechen aktueller Anforderungen können Administratoren jetzt Anforderungen für einen bestimmten Zeitraum einschränken. Administratoren können Anforderungen nach Anforderung, Projekt und Benutzer einschränken.</li><li>Zusätzlich zu den Metriken &quot;Nutzung&quot;und &quot;Kapazität&quot;enthält der Reporting-Aktivitäts-Manager jetzt weitere Daten zur Berichtsaktivität: Spalte &quot;Komplexität&quot;, Spalte &quot;Benutzer&quot;und Spalte &quot;Verbindung&quot;.</li><li>Alle Stornierungen und Einschränkungen, die im Manager für Berichtsaktivität vorgenommen wurden, sind jetzt im Auditprotokoll sichtbar. Administratoren können das Auditprotokoll verwenden, um anzuzeigen, was derzeit abgebrochen wird. Abbrüche können im Reporting Activity Manager oder im Auditprotokoll nicht rückgängig gemacht werden.</li></ul><p>Weitere Informationen finden Sie unter [Übersicht über die Berichterstellung in Activity Manager](/help/admin/admin/reporting-activity-manager/reporting-activity-overview.md)</p> | 17. Oktober 2023 | 24. Oktober 2023 |
| **Verbesserungen bei Data Warehouse** | Beim Erstellen einer Data Warehouse-Anfrage können Sie jetzt ein Cloud-Konto für die Verwendung als Berichtsziel konfigurieren. Die folgenden Cloud-Kontotypen sind für das Senden von Daten verfügbar:<ul><li>Amazon S3</li><li>Google Cloud Platform</li><li>Azure SAS</li><li>Azure RBAC</li><li>E-Mail (diese Option war zuvor bereits verfügbar)</li></ul>FTP, SFTP, Azure Blob und S3 sind weiterhin als Berichtsziele verfügbar, werden aber nicht mehr empfohlen.<p>Das Benutzererlebnis beim Erstellen und Verwalten von Data Warehouse-Anfragen wurde ebenfalls verbessert. Weitere Informationen finden Sie unter [Erstellen einer Data Warehouse-Anfrage](/help/export/data-warehouse/create-request/t-dw-create-request.md) und [Verwalten von Data Warehouse-Anfragen](https://experienceleague.adobe.com/docs/analytics/export/data-warehouse/data-warehouse-requests-manage.html?lang=de). | 12. September 2023 | Am oder vor dem 8. November 2023 |
| **Migrieren von Adobe Analytics-Projekten und allen enthaltenen Komponenten zu Customer Journey Analytics** | Sie können Ihre Adobe Analytics-Projekte jetzt zu Customer Journey Analytics migrieren. Dadurch wird der Übergang von Adobe Analytics zu Customer Journey Analytics vereinfacht. <p>Wenn Sie Projekte zu Customer Journey Analytics migrieren, werden Assets aus einer Report Suite inAdobe Analytics einer Customer Journey Analytics-Datenansicht zugeordnet.</p> <p>Sie migrieren Projekte über die Adobe Analytics-Benutzeroberfläche zu Customer Journey Analytics. [Weitere Informationen](https://experienceleague.adobe.com/docs/analytics/admin/admin-tools/component-migration/prepare-component-migration.html?lang=de)</p> | Nicht angegeben | 9. Oktober 2023 |

{style="table-layout:auto"}

## Fehlerbehebungen in Adobe Analytics

* Es wurden Probleme behoben, bei denen A4T-Berichte nicht in der Target/Analytics-Benutzeroberfläche angezeigt wurden. (AN-329375, AN-329745, AN-330026)

AN-313983; AN-324189; AN-325095; AN-325677; AN-325886; AN-326068; AN-326360; AN 326458; AN-327290; AN-327315; AN-327353; AN-327505; AN-327589; AN-327609; AN-3 27922; AN-328110; AN-328222; AN-328261; AN-328496; AN-328577; AN-328629; AN-32 8736; AN-328888; AN-328899; AN-328902; AN-328921; AN-328958; AN-329208; AN-329 277; AN-329332; AN-329334; AN-329335; AN-329336; AN-329357; AN-329385; AN-3293 87; AN-329397; AN-329463; AN-329501; AN-329504; AN-329505; AN-329515; AN-32952 4; AN-329526; AN-329534; AN-329539; AN-329541; AN-329543; AN-329545; AN-32956; AN-329570; AN-329623; AN-329624; AN-329636; AN-329646; AN-329647; AN-32968; AN 329701; AN-329737; AN-329741; AN-329751; AN-329812; AN-329813; AN-329821; AN-3 29824; AN-329833; AN-329848; AN-329852; AN-329861; AN-329863; AN-329874; AN-32 9882; AN-329911; AN-329917; AN-329942; AN-329954; AN-329968; AN-329971; AN-329 982; AN-330044; AN-330052; AN-330131; AN-330132; AN-330230; AN-330352; AN-3303 67; AN-330541; AN-330599

## Wichtige Hinweise für Adobe Analytics-Administratoren {#admin}

| Hinweis | Hinzugefügt oder aktualisiert am | Beschreibung |
| ----------- | ---------- | ---------- |
| **Vollständige IP-Verschleierung für Adobe-Experience Edge-Treffer** | 27. September 2023 | Die IP-Verschleierung für Treffer aus Experience Edge wird Ende Oktober 2023 aktualisiert. Im April hat Experience Edge die Möglichkeit hinzugefügt, IP-Adressen zu verschleiern. Damals unterstützte Adobe Analytics nur die teilweise Verschleierung von IPs, da Analytics Treffer aus Experience Edge verarbeitet. Wenn Kunden die vollständige Verschleierung für Experience Edge ausgewählt haben, erhielt Analytics nur teilweise verschleierte IPs. Wenn diese Änderung implementiert ist, erhält Analytics die vollständig verschleierte IP. |
| **Adobe Analytics Livestream - Analytics 2.0-APIs** | 27. September 2023 | Kunden können jetzt auf die [Endpunktleitfaden für Adobe Analytics Livestream](https://developer.adobe.com/analytics-apis/docs/2.0/guides/endpoints/livestream/) unter den Adobe Analytics 2.0-APIs anstelle des vorherigen Speicherorts mit den 1.4-APIs. Beachten Sie, dass Kunden, die Adobe I/O JWT-Anmeldeinformationen verwenden, bis zum 1. Januar 2025 zu Adobe I/O OAuth Server-to-Server-Anmeldeinformationen migrieren müssen. (Siehe Details unter EOL-Benachrichtigungen unten.) |

{style="table-layout:auto"}

## Mitteilungen über das Ende der Nutzungsdauer (EOL) {#eol}

| Ende der Nutzungsdauer eines Produkts oder einer Funktion | Datum hinzugefügt oder aktualisiert | Beschreibung |
| --- | --- | --- |
| **Migration auf OAuth Server-zu-Server-Anmeldeinformationen für Adobe I/O** | 11. Mai 2023 | Kundinnen und Kunden von Adobe Analytics-API und Livestream, die JWT-Anmeldeinformationen für Adobe I/O verwenden, müssen bis zum **1. Januar 2025** auf OAuth Server-zu-Server-Anmeldeinformationen für Adobe I/O migrieren. Adobe I/O lässt die Erstellung neuer JWT-Anmeldeinformationen ab dem 1. Mai 2024 nicht mehr zu. Kunden und Kundinnen, die JWT verwenden, müssen neue OAuth Server-zu-Server-Anmeldeinformationen erstellen oder ihre bestehende JWT-Anmeldeinformationen zu OAuth Server-zu-Server-Anmeldeinformationen migrieren. Kunden und Kundinnen müssen außerdem ihre Client-Anwendungen aktualisieren, um die neuen OAuth Server-to-Server-Anmeldeinformationen zu verwenden. <ul><li>[Migration von Dienstkonto-Anmeldeinformationen (JWT)](https://developer.adobe.com/developer-console/docs/guides/authentication/ServerToServerAuthentication/migration/)</li><li>[Implementierungshandbuch für neue und alte Programme mit OAuth](https://developer.adobe.com/developer-console/docs/guides/authentication/ServerToServerAuthentication/implementation/)<li>[Verwenden der neuen OAuth Server-zu-Server-Anmeldeinformationen](https://developer.adobe.com/developer-console/docs/guides/authentication/ServerToServerAuthentication/implementation/)</li><li>[Häufig gestellte Fragen (FAQ)](https://developer.adobe.com/developer-console/docs/guides/authentication/ServerToServerAuthentication/faqs/)</li></ul> |
| **EOL für [!DNL Reports & Analytics]** | 7. März 2023 | Adobe beabsichtigt, [!DNL Reports & Analytics] und die zugehörigen Berichte und Funktionen zum **31. Dezember 2023** einzustellen. Die Berichte, Visualisierungen und zugrunde liegenden Technologien, die [!DNL Reports & Analytics] unterstützen, entsprechen nicht mehr den technologischen Standards von Adobe. Die meisten Funktionen von [!DNL Reports & Analytics] sind in [Analysis Workspace](https://experienceleague.adobe.com/docs/analytics/analyze/analysis-workspace/home.html?lang=de) verfügbar. Seit der Veröffentlichung von Analysis Workspace im Jahr 2015 wurden die Funktionen von [!DNL Reports & Analytics] nach Analysis Workspace verschoben, und es wurde ein Schwellenwert für die Workflow-Parität erreicht. In [dieser Mitteilung](https://spark.adobe.com/page/6WnF8JK6IRDhf/) wird der Ablauf der Produktlebensdauer erläutert.<p>Am 31. Dezember 2023 werden wir viele der zugehörigen Reports &amp; Analytics-Funktionen einstellen, insbesondere: Terminierte Berichte, Datenextraktionen und DL-Berichte. Nach dem 31. Dezember 2023 werden terminierte Berichte nicht mehr gesendet. Im **April 2023** wurden alle Berichte, die erst nach dem 31. Dezember 2023 ablaufen sollten, automatisch aktualisiert und das Datum auf den 31. Dezember 2023 gesetzt. Darüber hinaus können Sie nach dem 31. Dezember 2023 keine zukünftigen Berichte mehr planen. |
| **EOL für die [!UICONTROL Veröffentlichungslisten]-Funktion** | 29. September 2022 | Im Rahmen des Endes der Nutzungsdauer von Reports &amp; Analytics werden [!UICONTROL Veröffentlichungslisten] voraussichtlich im **Dezember 2023** das Ende der Nutzungsdauer erreichen. Sie werden keine neuen [!UICONTROL Veröffentlichungslisten] erstellen oder auf bestehende [!UICONTROL Analysis Workspace]-Projekte zugreifen können, um diese zu senden oder zu planen. |
| **EOL für Data Workbench** | 14. September 2022 | Adobe beabsichtigt, Data Workbench ab **31. Dezember 2023** einzustellen. Weitere Informationen finden Sie in der [Mitteilung zum Ende der Nutzungsdauer von Data Workbench](https://experienceleague.adobe.com/docs/data-workbench/using/eol.html?lang=de). Wenden Sie sich bei Fragen an den für Ihre Organisation zuständigen Adobe-Kundenbetreuer. |

{style="table-layout:auto"}

## AppMeasurement

Die neuesten Aktualisierungen zu AppMeasurement-Versionen (Version 2.25.0) finden Sie in den [Versionshinweisen zu AppMeasurement für JavaScript](https://experienceleague.adobe.com/docs/analytics/implementation/appmeasurement-updates.html?lang=de).


## Verwandte Ressourcen

* [Frühere Versionshinweise für 2022](/help/release-notes/2022.md)
* [Versionshinweise zu Customer Journey Analytics](https://experienceleague.adobe.com/docs/analytics-platform/using/releases/latest.html?lang=de)
* [Versionshinweise zu Media Analytics](https://experienceleague.adobe.com/docs/media-analytics/using/additional-resources/release-notes.html?lang=de)
* Die neuesten Versions-Updates für [Adobe Experience Cloud-Produkte](https://business.adobe.com/de/products/adobe-experience-cloud-products.html)
