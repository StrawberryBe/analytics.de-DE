---
title: Aktuelle Adobe Analytics-Versionshinweise anzeigen
description: Neueste Analytics-Versionshinweise
exl-id: 97d16d5c-a8b3-48f3-8acb-96033cc691dc
source-git-commit: 44bbcabf0bdc74b560a650ce1892a52b4d98052c
workflow-type: tm+mt
source-wordcount: '649'
ht-degree: 61%

---

# Aktuelle Adobe Analytics-Versionshinweise (Februar 2022)

>[!IMPORTANT]
>
>Diese Versionshinweise enthalten Informationen zur Vorabversion, die geändert werden können.

**Letzte Aktualisierung**: 10. Februar 2022

Erfahren Sie mehr über die neuesten Versions-Updates für [Adobe Experience Cloud-Produkte](https://business.adobe.com/de/products/adobe-experience-cloud-products.html). Hier finden Sie die aktuelle Dokumentation, Tutorials und Kurse zu Experience League.

## Neue Funktionen in Adobe Analytics {#aa-features}

| Funktion | Beschreibung | [Zieldatum](https://experienceleague.adobe.com/docs/analytics/technotes/releases.html?lang=de) |
| ----------- | ---------- | ------- |
| Vorschaumodus für Mobile Scorecard-Projekte | Starten Sie eine Vorschau Ihrer mobilen Scorecard in der Analytics-Dashboards-App, direkt vom Scorecard-Builder aus. Im Vorschaumodus können Benutzer auf die gleiche Weise mit Filtern und Diagrammen wie in der App interagieren, sodass sie eine Vorschau des Erlebnisses anzeigen können, bevor sie die Scorecard speichern und freigeben. Benutzer können die Geräteauswahl auch im Vorschaumodus verwenden, um zu sehen, wie ihre Scorecard auf verschiedenen Geräten aussieht. | 16. Februar 2022 |

{style=&quot;table-layout:auto&quot;}

## Fehlerbehebungen in Adobe Analytics

* Korrektur einer Reihe von Problemen mit [!UICONTROL Nutzung von Server-Aufrufen]. (AN-279134, AN-279878, AN-280802, AN-279097, AN-191284, AN-269720)
* Es wurde ein Fehler behoben, der dazu führte, dass Data Warehouse leere CSV-Dateien exportierte. (AN-280291)
* Es wurde ein Fehler behoben, der dazu führte, dass Zielgruppennamen nicht für aktuelle Segmente ausgefüllt wurden. (AN-279715)
* Es wurde ein Problem mit langsamen Berichtszeiten behoben. (AN-280055)
* Es wurden Probleme behoben, durch die Klassifizierungen nicht alle Dimensionselemente klassifizieren konnten. (AN-280031)


### Weitere Fehlerbehebungen in Adobe Analytics

AN-268093, AN-273820, AN-274435, AN-274904, AN-275356, AN-275947, AN-276160, AN 276258, AN-276705, AN-277051, AN-277957, AN-278693, AN-278882, AN-27900, AN-2 79046, AN-279362, AN-279460, AN-279488, AN-279554, AN-279572, AN-279663, AN-27 9755, AN-279825, AN-280002, AN-280013, AN-280019, AN-280033, AN-280086, AN-280 232, AN-280264, AN-280288, AN-280342, AN-280347, AN-280360, AN-280370, AN-2807 24, AN-280830, AN-280941, AN-281353, AN-281424, AN-281533


## Wichtige Hinweise für [!DNL Analytics]-Administratoren

| Hinweis | Hinzugefügt oder aktualisiert am | Beschreibung |
| ----------- | ---------- | ---------- |
| Ablauf der Zulassungslisten-Verlängerung für das Ende der Nutzungsdauer für veraltete Analytics-OAuth-/JWT-Integrationen | 14. Januar 2022 | Am **25. Mai 2022** läuft die Erweiterung der Zulassungsliste für [Analytics 1.3 API, 1.4 SOAP API und Legacy Analytics OAuth/JWT EOL](https://github.com/AdobeDocs/analytics-1.4-apis/blob/master/docs/APIEOL.md) ab. Sie wurde angeboten, um Kunden, die noch die veralteten OAuth/JWT-Anmeldeinformationen für [!DNL Adobe Analytics] verwenden, zusätzliche Zeit für die Migration ihrer Client-Integrationen auf die [Adobe IMS-Anmeldeinformationen](https://developer.adobe.com/console) zu geben. Dieser Gültigkeitsablauf betrifft (ist jedoch nicht auf beschränkt auf) Kunden von [!DNL Adobe Analytics Livestream] und [!DNL Adobe Campaign], die die erforderlichen IMS-Migrationen nicht abgeschlossen haben. Kunden, die derzeit veraltete [!DNL Analytics]-OAuth-/JWT-Anmeldeinformationen über die Zulassungsliste-Verlängerung verwenden und die ihre Migration zu IMS-Anmeldeinformationen nicht bis zum 25. Mai 2022 abgeschlossen haben, verlieren den Zugriff auf Adobe-Services. Livestream-Kunden können im Hinblick auf die Umstellung ihrer Client-Programme auf IMS-Anmeldeinformationen diese [Anweisungen](https://github.com/AdobeDocs/analytics-1.4-apis/blob/master/docs/live-stream-api/getting_started.md) zurate ziehen. [!DNL Campaign]-Kunden können sich zwecks Upgrade auf die neueste Version von [!DNL Campaign] an ihr Adobe-Account-Team wenden. |
| EOL für [!DNL Reports & Analytics] | 4. Januar 2022 | Adobe beabsichtigt,  und die zugehörigen Berichte und Funktionen zum **31. Dezember 2023** einzustellen. [!DNL Reports & Analytics] Die Berichte, Visualisierungen und zugrunde liegenden Technologien von [!DNL Reports & Analytics] entsprechen nicht mehr den technologischen Standards von Adobe. Die meisten Funktionen von [!DNL Reports & Analytics] sind in [Analysis Workspace](https://experienceleague.adobe.com/docs/analytics/analyze/analysis-workspace/home.html?lang=de) verfügbar. Seit der Veröffentlichung von Analysis Workspace im Jahr 2015 wurden die Funktionen von [!DNL Reports & Analytics] nach Analysis Workspace verschoben, und es wurde ein Schwellenwert für die Workflow-Parität erreicht. [In dieser Mitteilung wird der End-of-Life-Prozess erläutert.](https://spark.adobe.com/page/6WnF8JK6IRDhf/) |
| Aktualisierung der Secure File Transfer Protocol (SFTP)-Services | 13. Januar 2022 | Am **2. Mai 2022** werden die SFTP-Services (Secure File Transfer Protocol) von [!DNL Adobe Analytics] aktualisiert, um die Sicherheit für Dateiübertragungen zu verbessern. Mit dieser Änderung werden einige SFTP-Client-Konfigurationen nicht mehr unterstützt. Wir werden auch einige Verbindungsoptionen hinzufügen, die am **1. März 2022** verfügbar sein werden. Dies wirkt sich nur auf Daten aus, die über SFTP an Adobe Analytics gesendet oder von dort abgerufen wurden. Das FTP-Protokoll ist nicht betroffen. Um Dienstunterbrechungen zu vermeiden, stellen Sie sicher, dass Ihre SFTP-Clients (Code, Tools, Dienste) den detaillierten Änderungen entsprechen [here](https://experienceleague.adobe.com/docs/analytics/export/ftp-and-sftp/secure-file-transfer-protocol/sftp-upgrade.html?lang=de). |

## AppMeasurement {#appm}

Die neuesten Aktualisierungen zu AppMeasurement-Versionen (Version 2.22.4) finden Sie in den [Versionshinweisen zu AppMeasurement für JavaScript](https://experienceleague.adobe.com/docs/analytics/implementation/appmeasurement-updates.html?lang=de).

>[!MORELIKETHIS]
>[[!DNL Customer Journey Analytics]  Versionshinweise](https://experienceleague.adobe.com/docs/analytics-platform/using/releases/latest.html?lang=en)
