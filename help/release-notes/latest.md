---
title: Neueste Analytics-Versionshinweise
description: Aktuelle Versionshinweise zu Adobe Analytics anzeigen.
feature: Release Notes
exl-id: 97d16d5c-a8b3-48f3-8acb-96033cc691dc
source-git-commit: e35e437a61b925625f6dc7fa2344406c5a66e5fe
workflow-type: tm+mt
source-wordcount: '881'
ht-degree: 53%

---

# Aktuelle Adobe Analytics-Versionshinweise (März 2022)

>[!IMPORTANT]
>
>Der folgende Inhalt enthält Informationen zur Vorabversion und kann geändert werden.

* Versionshinweise für Februar 2022 finden Sie unter [here](/help/release-notes/2022.md).
* Erfahren Sie mehr über die neuesten Versions-Updates für [Adobe Experience Cloud-Produkte](https://business.adobe.com/de/products/adobe-experience-cloud-products.html). Hier finden Sie die aktuelle Dokumentation, Tutorials und Kurse zu Experience League.

## Neue Funktionen in Adobe Analytics {#aa-features}

| Funktion | Beschreibung | [Zieldatum](releases.md) |
| ----------- | ---------- | ------- |
| Anmerkungen in Workspace | Mit Anmerkungen in Workspace können Sie Ihrer Organisation kontextbezogene Datennuancen und Einblicke effektiv kommunizieren. [Weitere Informationen](/help/analyze/analysis-workspace/components/annotations/overview.md) | 23. März 2022 |
| Aktualisierungen der Adobe Analytics-Landingpage | Aktualisierungen der gemeinsamen Landingpage von Workspace/Reports &amp; Analytics, die die Benutzerfreundlichkeit verbessern und die Navigation erleichtern. [Weitere Informationen](/help/analyze/landing.md) | 23. März 2022 |

{style=&quot;table-layout:auto&quot;}

## Fehlerbehebungen in Adobe Analytics

* Fehlerkorrektur - Beim Zugriff auf Activity Map tritt jetzt kein Fehler mehr auf. (AN-267177)

* Es wurde ein Problem mit nicht erfolgreichen Benutzer-Asset-Übertragungen behoben. (AN-279813)

* Es wurden Probleme mit dem Bedienfeld &quot;A4T Workspace&quot;behoben. (AN-281594; AN-282418)

* Es wurde ein Problem behoben, durch das einige Benutzer nicht auf Adobe Analytics zugreifen konnten. (AN-282776)

* Es wurden Probleme behoben, die dazu führten, dass einige neu erstellte Report Suites keine Daten sammelten. (AN-283114, AN-283311)

* Es wurden Probleme behoben, die dazu führten, dass Win11 nicht mithilfe der Dimension Betriebssystem erkennen konnte. (AN-275569, AN-275727) AN-280335)

* Es wurden Probleme mit falsch gesendeten Daten-Feeds-E-Mails behoben. (AN-280255; AN-282051)


### Weitere Fehlerbehebungen in Adobe Analytics

AN-256929; AN-270937; AN-272158 AN-275130; AN-277830; AN-278635; AN-279066; AN-279683; AN-279899; AN-280504; AN-280617; AN-280663; AN-281423; AN-281608 AN-281671; AN-281963; AN-282027; AN-282218; AN-282605 AN-282632; AN-282654; AN-282694 AN-282744 AN-282756 AN-282804 AN-282862; AN-282903 AN-282937 AN-282892; AN-283315; AN-283338; AN-283388; AN-283417; AN-283474; AN-283511; AN-283691, AN-283957;

## Wichtige Hinweise für Adobe Analytics-Administratoren

**Aktualisiert am 11. März 2022**

| Hinweis | Hinzugefügt oder aktualisiert am | Beschreibung |
| ----------- | ---------- | ---------- |
| Anhalten älterer terminierter Berichte | 11. März 2022 | effektiv **15. April 2022** Adobe beabsichtigt, alle terminierten Berichte anzuhalten, deren Erstellungsdatum mehr als zwei Jahre beträgt (die vor dem 31. Januar 2020 erstellt wurden). Es werden keine Berichte oder Daten gelöscht. Nur Berichte, die älter als zwei Jahre sind, werden angehalten und keine weiteren terminierten Berichte werden gesendet. [Weitere Informationen](/help/analyze/reports-analytics/scheduled-reports-eol.md) |
| Aktualisierung der ISO-Region 2022 | 11. März 2021 | Adobe führt 2022 Aktualisierungen der ISO-Region durch **10. Juni 2022**. Nach dieser Version sollten Sie mit kleineren Aktualisierungen rechnen. |
| Ändern der Verarbeitung von A4T-Daten durch Analytics, die über Experience Edge erfasst wurden | 25. Februar 2022 | on **7. März 2022**&#x200B;ändern wir, wie wir mit einigen Target-bezogenen Daten umgehen, die über Experience Edge an Adobe Analytics gesendet werden. Bei Verwendung des Adobe Experience Platform Web SDK mit Analytics und Target wurden einige Personalisierungsereignisse in [!DNL Adobe Analytics] as [!UICONTROL Seitenansichten]. Dies führte zu überhöhten Seitenansichtszahlen und zusätzlichen Server-Aufrufen. Mit der Änderung werden Personalisierungsaufrufe ohne Analytics-Inhalt ignoriert. Personalisierungsaufrufe mit A4T-Daten zeichnen die A4T-Daten auf, werden jedoch nicht als abrechnungsfähige Server-Aufrufe aufgezeichnet und wirken sich auch nicht auf Seitenansichten oder Linkereignismetriken aus. |
| Anhalten älterer geplanter Report Builder-Aufgaben | 24. Februar 2022 | **Wirksam ab 15. April 2022** Adobe beabsichtigt, alle geplanten Report Builder-Aufgaben, die vor mehr als zwei Jahren erstellt wurden, anzuhalten. Diese Pause gilt insbesondere für alle Aufgaben, die vor dem 31. Januar 2020 erstellt wurden. Es werden keine Aufgaben, Arbeitsmappen oder Daten gelöscht. Aufgaben, die älter als zwei Jahre sind, werden jedoch ausgesetzt und es werden keine weiteren geplanten Aufgaben gesendet. [Weitere Informationen](/help/analyze/report-builder/r-arb-scheduled-reports.md) |
| Ablauf der Zulassungslisten-Verlängerung für das Ende der Nutzungsdauer für veraltete Analytics-OAuth-/JWT-Integrationen | 14. Januar 2022 | Am **25. Mai 2022** läuft die Erweiterung der Zulassungsliste für [Analytics 1.3 API, 1.4 SOAP API und Legacy Analytics OAuth/JWT EOL](https://github.com/AdobeDocs/analytics-1.4-apis/blob/master/docs/APIEOL.md) ab. Sie wurde angeboten, um Kunden, die noch die veralteten OAuth/JWT-Anmeldeinformationen für [!DNL Adobe Analytics] verwenden, zusätzliche Zeit für die Migration ihrer Client-Integrationen auf die [Adobe IMS-Anmeldeinformationen](https://developer.adobe.com/console) zu geben. Dieser Gültigkeitsablauf betrifft (ist jedoch nicht auf beschränkt auf) Kunden von [!DNL Adobe Analytics Livestream] und [!DNL Adobe Campaign], die die erforderlichen IMS-Migrationen nicht abgeschlossen haben. Kunden, die derzeit veraltete [!DNL Analytics]-OAuth-/JWT-Anmeldeinformationen über die Zulassungsliste-Verlängerung verwenden und die ihre Migration zu IMS-Anmeldeinformationen nicht bis zum 25. Mai 2022 abgeschlossen haben, verlieren den Zugriff auf Adobe-Services. Livestream-Kunden können im Hinblick auf die Umstellung ihrer Client-Programme auf IMS-Anmeldeinformationen diese [Anweisungen](https://github.com/AdobeDocs/analytics-1.4-apis/blob/master/docs/live-stream-api/getting_started.md) zurate ziehen. [!DNL Campaign]-Kunden können sich zwecks Upgrade auf die neueste Version von [!DNL Campaign] an ihr Adobe-Account-Team wenden. |
| Aktualisierung der Secure File Transfer Protocol (SFTP)-Services | 3. März 2022 | Am **15. Mai 2022** werden die SFTP-Services (Secure File Transfer Protocol) von [!DNL Adobe Analytics] aktualisiert, um die Sicherheit für Dateiübertragungen zu verbessern. Mit dieser Änderung werden einige SFTP-Client-Konfigurationen nicht mehr unterstützt. Wir werden auch einige Verbindungsoptionen hinzufügen, die am **1. März 2022** verfügbar sein werden. Dies wirkt sich nur auf Daten aus, die per SFTP an Adobe Analytics gesendet oder von Adobe Analytics abgerufen werden. Das FTP-Protokoll ist nicht betroffen. Um Service-Unterbrechungen zu vermeiden, stellen Sie bitte sicher, dass Ihre SFTP-Clients (Code, Tools, Services) die [hier](https://experienceleague.adobe.com/docs/analytics/export/ftp-and-sftp/secure-file-transfer-protocol/sftp-upgrade.html?lang=de) beschriebenen Anforderungen erfüllen. |
| EOL für [!DNL Reports & Analytics] | 4. Januar 2022 | Adobe beabsichtigt, [!DNL Reports & Analytics] und die zugehörigen Berichte und Funktionen zum **31. Dezember 2023** einzustellen. Die Berichte, Visualisierungen und zugrunde liegenden Technologien von [!DNL Reports & Analytics] entsprechen nicht mehr den technologischen Standards von Adobe. Die meisten Funktionen von [!DNL Reports & Analytics] sind in [Analysis Workspace](https://experienceleague.adobe.com/docs/analytics/analyze/analysis-workspace/home.html?lang=de) verfügbar. Seit der Veröffentlichung von Analysis Workspace im Jahr 2015 wurden die Funktionen von [!DNL Reports & Analytics] nach Analysis Workspace verschoben, und es wurde ein Schwellenwert für die Workflow-Parität erreicht. In [dieser Mitteilung](https://spark.adobe.com/page/6WnF8JK6IRDhf/) wird der Ablauf der Produktlebensdauer erläutert. |

## AppMeasurement {#appm}

Die neuesten Aktualisierungen zu AppMeasurement-Versionen (Version 2.22.4) finden Sie in den [Versionshinweisen zu AppMeasurement für JavaScript](https://experienceleague.adobe.com/docs/analytics/implementation/appmeasurement-updates.html?lang=de).

>[!MORELIKETHIS]
>[[!DNL Customer Journey Analytics] Versionshinweise](https://experienceleague.adobe.com/docs/analytics-platform/using/releases/latest.html?lang=de)
