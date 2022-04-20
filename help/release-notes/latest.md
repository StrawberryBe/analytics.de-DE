---
title: Neueste Analytics-Versionshinweise
description: Hier finden Sie die aktuellen Versionshinweise zu Adobe Analytics.
feature: Release Notes
exl-id: 97d16d5c-a8b3-48f3-8acb-96033cc691dc
source-git-commit: b93b27fac0a9e3364512bb8a27ad64c7eb379dd1
workflow-type: tm+mt
source-wordcount: '1021'
ht-degree: 32%

---

# Aktuelle Adobe Analytics-Versionshinweise (April 2022)

**Letzte Aktualisierung**: 19. April 2022

* Versionshinweise für März 2022 finden Sie unter [here](/help/release-notes/2022.md).

* Versionshinweise zu Customer Journey Analytics finden Sie unter [here](https://experienceleague.adobe.com/docs/analytics-platform/using/releases/latest.html?lang=de).

* For Media Analytics release notes, go [here](https://experienceleague.adobe.com/docs/media-analytics/using/additional-resources/release-notes.html?lang=en).

* Erfahren Sie mehr über die neuesten Versions-Updates für [Adobe Experience Cloud-Produkte](https://business.adobe.com/de/products/adobe-experience-cloud-products.html). Hier finden Sie die aktuelle Dokumentation, Tutorials und Kurse zu Experience League.

| Funktion | Beschreibung | [Zieldatum](releases.md) |
| ----------- | ---------- | ------- |
| Adobe Analytics landing page updates | Aktualisierungen der gemeinsamen Landingpage für Workspace/Reports &amp; Analytics, die die Benutzerfreundlichkeit und die einfache Navigation verbessern. [Weitere Informationen](/help/analyze/landing.md) | 20. April 2022 |
| [!UICONTROL Next item] or [!UICONTROL Previous item] Workspace panel | The [!UICONTROL Next or Previous item] panel allows you to explore items that follow or precede a dimension item of your choice. Verwenden Sie sie beispielsweise, wenn Sie die nächsten oder vorherigen Seiten zu einer bestimmten Produktseite, einem Marketingkanal oder sogar Gerätetyp anzeigen möchten. This panel goes beyond legacy next/previous reporting because it allows you to look at any dimension and does not require any new implementation to get insights. [Weitere Informationen](/help/analyze/analysis-workspace/c-panels/next-previous.md) | 20. April 2022 |
| [!UICONTROL Seitenzusammenfassung] Arbeitsbereich | Die [!UICONTROL Seitenzusammenfassung] -Bedienfeld bietet eine Tiefenanalyse für eine Seite Ihrer Wahl. It provides the same details as the legacy Reports &amp; Analytics [!UICONTROL Page Summary] report, plus much more. [Weitere Informationen](/help/analyze/analysis-workspace/c-panels/page-summary.md) | 20. April 2022 |
| Die Anforderung von `x-proxy-global-company-id` -Kopfzeile für 2.0-API-Aufrufe | The Adobe Analytics 2.0 APIs no longer require the `x-proxy-global-company-id` header, as this information is part of the endpoint URL. Sie können diese Kopfzeile zwar weiterhin einbeziehen, aber kein Fehler mehr ausgeben, wenn sie fehlt. | 20. April 2022 |

{style=&quot;table-layout:auto&quot;}

## Fehlerbehebungen in Adobe Analytics

* Es wurde ein Problem in Daten-Feeds behoben, bei dem Start- und Enddaten nach dem Speichern des Daten-Feeds beim Erstellen über die Daten-Feed-Benutzeroberfläche automatisch geändert wurden. The dates were updating themselves by 1 day. (AN-281262)

* Fixed an issue that prevented the renewal of scheduled projects via e-mail link. (AN-283622)

### Weitere Fehlerbehebungen in Adobe Analytics

AN-274486; AN-279258; AN-279995; AN-280918; AN-281423; AN-282084; AN-282435; AN-283508; AN-283517; AN-283706; AN-283762; AN-283921; AN-284195; AN-284663; AN-284573; AN-284721; AN-284790; AN-284867; AN-284870; AN-284872; AN-284884; AN-284914; AN-284930; AN-284933; AN-284967; AN-284970; AN-285187; AN-285328; AN-285337; AN-285375; AN-285447; AN-285724; AN-285753; AN-285761;

## Important notices for Adobe Analytics administrators

| Hinweis | Hinzugefügt oder aktualisiert am | Beschreibung |
| ----------- | ---------- | ---------- |
| **Berechtigung für geräteübergreifende Analyse (CDA)** | April 13, 2022 | effektiv **1. Mai 2022** bei jeder neuen Implementierung von [CDA](/help/components/cda/overview.md) sind auf maximal drei Report Suite-IDs (RSIDs) pro Kunde beschränkt. |
| **Änderung der Verarbeitung von A4T-Daten durch Adobe Analytics, die über Experience Edge erfasst wurden** | 31. März 2022 | Am 7. März 2022 hat Analytics die Art und Weise geändert, wie es einige Aufrufe aus Experience Edge verarbeitet, die Target-Inhalte für die Berichterstellung für Analytics for Target (A4T) enthalten. Starting March 7, all hits with A4T reporting content are modified so they are not treated as Page View or Link events. Start **31. März 2022**, ist die Logik selektiver, sodass die standardmäßigen Seitenansichts- und Klickereignisse nicht geändert werden. Going forward, the only events that are modified are personalization-only calls that only have A4T content. |
| **Aktualisierung der Browserverschlüsselungsmethoden, die von bestimmten Kunden unterstützt werden** | March 28, 2022 | Adobe bietet zwei Sicherheitsstufen, die den unterschiedlichen Kundenanforderungen an die Sicherheit bei der Erstanbieter-Datenerfassung gerecht werden. On **June 23, 2022** support is removed for certain HTTPS encryption algorithms, known as ciphers, for customers with their security level set to “High”. Diese Aktion bedeutet, dass einige ältere Betriebssysteme keine Daten mehr an Analytics senden können, da sie keine modernen Verschlüsselungsmethoden unterstützen. Customers using the default “Standard” cipher security settings are not impacted. Alle Kunden, die derzeit die Einstellung &quot;Hoch&quot;verwenden, wurden bereits direkt kontaktiert. A detailed list of the ciphers affected by this change can be found here. |
| **Anhalten älterer terminierter Berichte** | 12. April 2022 | effektiv **20. April 2022** Adobe beabsichtigt, alle terminierten Berichte anzuhalten, deren Erstellungsdatum mehr als zwei Jahre beträgt (die vor dem 31. Januar 2020 erstellt wurden). Es werden keine Berichte oder Daten gelöscht. Nur Berichte, die älter als zwei Jahre sind, werden angehalten und keine weiteren terminierten Berichte werden gesendet. Weitere Informationen |
| **Aktualisierung der ISO-Region 2022** | 11. März 2021 | Adobe plans to perform 2022 ISO region updates on **June 10, 2022**. Expect to see minor geo information updates following this release. |
| **Anhalten älterer geplanter Report Builder-Aufgaben** | 12. April 2022 | Effective **April 20, 2022**, Adobe intends to pause all scheduled Report Builder tasks that were created more than two years ago. Diese Pausierung gilt insbesondere für alle Aufgaben, die vor dem 31. Januar 2020 erstellt wurden. Es werden keine Aufgaben, Arbeitsmappen oder Daten gelöscht. Aufgaben, die älter als zwei Jahre sind, werden jedoch ausgesetzt und es werden keine weiteren geplanten Aufgaben gesendet. Weitere Informationen |
| **Ablauf der Zulassungslisten-Verlängerung für das Ende der Nutzungsdauer für veraltete Analytics-OAuth-/JWT-Integrationen** | 14. Januar 2022 | On **May 25, 2022**, the [Analytics 1.3 API, 1.4 SOAP API, and Legacy Analytics OAuth/JWT EOL](https://github.com/AdobeDocs/analytics-1.4-apis/blob/master/docs/APIEOL.md) allowlist extension expires. Sie wurde angeboten, um Kunden, die noch die veralteten OAuth/JWT-Anmeldeinformationen für [!DNL Adobe Analytics] verwenden, zusätzliche Zeit für die Migration ihrer Client-Integrationen auf die [Adobe IMS-Anmeldeinformationen](https://developer.adobe.com/console) zu geben. Dieser Gültigkeitsablauf betrifft (ist jedoch nicht auf beschränkt auf) Kunden von [!DNL Adobe Analytics Livestream] und [!DNL Adobe Campaign], die die erforderlichen IMS-Migrationen nicht abgeschlossen haben. Kunden, die derzeit ältere [!DNL Analytics] OAuth-/JWT-Anmeldeinformationen über die Zulassungsliste-Erweiterung und die ihre Migration zu IMS-Anmeldeinformationen nicht bis zum 25. Mai 2022 abgeschlossen haben, verlieren den Zugriff auf Adobe-Dienste. Livestream-Kunden können im Hinblick auf die Umstellung ihrer Client-Programme auf IMS-Anmeldeinformationen diese [Anweisungen](https://github.com/AdobeDocs/analytics-1.4-apis/blob/master/docs/live-stream-api/getting_started.md) zurate ziehen. [!DNL Campaign]-Kunden können sich zwecks Upgrade auf die neueste Version von [!DNL Campaign] an ihr Adobe-Account-Team wenden. |
| **EOL für[!DNL Reports & Analytics]** | 4. Januar 2022 | Adobe beabsichtigt, [!DNL Reports & Analytics] und die zugehörigen Berichte und Funktionen zum **31. Dezember 2023** einzustellen. Die Berichte, Visualisierungen und zugrunde liegenden Technologien von [!DNL Reports & Analytics] entsprechen nicht mehr den technologischen Standards von Adobe. Die meisten Funktionen von [!DNL Reports & Analytics] sind in [Analysis Workspace](https://experienceleague.adobe.com/docs/analytics/analyze/analysis-workspace/home.html?lang=de) verfügbar. Seit der Veröffentlichung von Analysis Workspace im Jahr 2015 wurden die Funktionen von [!DNL Reports & Analytics] nach Analysis Workspace verschoben, und es wurde ein Schwellenwert für die Workflow-Parität erreicht. In [dieser Mitteilung](https://spark.adobe.com/page/6WnF8JK6IRDhf/) wird der Ablauf der Produktlebensdauer erläutert. |

{style=&quot;table-layout:auto&quot;}

## AppMeasurement {#appm}

Die neuesten Aktualisierungen zu AppMeasurement-Versionen (Version 2.22.4) finden Sie in den [Versionshinweisen zu AppMeasurement für JavaScript](https://experienceleague.adobe.com/docs/analytics/implementation/appmeasurement-updates.html?lang=de).

>[!MORELIKETHIS]
>[[!DNL Customer Journey Analytics] Versionshinweise](https://experienceleague.adobe.com/docs/analytics-platform/using/releases/latest.html?lang=en)
