---
title: Aktuelle Adobe Analytics-Versionshinweise anzeigen
description: Neueste Analytics-Versionshinweise
source-git-commit: f8c2d98e49ead838781b175aa9f22712d6802a9d
workflow-type: tm+mt
source-wordcount: '841'
ht-degree: 98%

---


# Neueste Adobe Analytics-Versionshinweise

## Neue Funktionen in Adobe Analytics {#aa-features}

| Funktion | Beschreibung | Zieldatum |
| ----------- | ---------- | ------- |
| Nicht angegeben |  | Siehe [Allgemeine Verfügbarkeit](https://experienceleague.adobe.com/docs/analytics/technotes/releases.html?lang=de) |

{style=&quot;table-layout:auto&quot;}

## Fehlerbehebungen in Adobe Analytics und Customer Journey Analytics {#aa-fixes}

* Es wurde ein Analysis Workspace-Problem behoben, bei dem die Zielgruppen-ID in Dimensionselementen fehlte. (AN-262038; AN-279315)
* Es wurde ein Problem behoben, durch das Benutzer ein gespeichertes [!DNL Target]-Projekt nicht in Arbeitsbereich laden konnten. (AN-277461; AN-275825; AN-266397)
* Es wurde ein Problem behoben, bei dem nicht aktivierte Funktionen in der Benutzeroberfläche sichtbar waren. (AN-262006)
* Es wurde ein Problem behoben, das beim Ändern des Datums mithilfe des Datumsfelds in Arbeitsbereich auftrat. Dies führte dazu, dass die [!UICONTROL Endzeit] von 23:59 Uhr zu 00:00 Uhr wechselte. (AN-277269; AN-277481)
* Es wurde ein Problem behoben, das zu Störungen in der Segment-Benutzeroberfläche beim Hinzufügen neuer Segmente zu einem bereits geladenen Segment führte. (AN-260827)
* Es wurde ein Problem behoben, durch das Benutzer nicht auf freigegebene Arbeitsbereich-Projekte zugreifen können. (AN-267529)
* Es wurde eine Fehlermeldung hinzugefügt, die anzeigt, wenn bei einem rollierenden Datumsbereich das Startdatum nach dem Enddatum liegt. (AN-270488)
* Es wurden verschiedene Probleme mit Daten-Feeds behoben. (AN-275876; AN-270512; AN-277284; AN-277290; AN-274893; AN-274606; AN-269651)
* Es wurde ein Problem behoben, durch das Datumsbereiche in Diagrammen Datumsfilter in Tabellen ignorierten. (AN-263999)
* Es wurde ein Problem behoben, bei dem terminierte Berichte aufgrund der Sommerzeit vorzeitig gesendet wurden. (AN-276410; AN-276305)
* Es wurde ein Problem behoben, bei dem der Projekt-Download im `.csv`-Format in Arbeitsbereich fehlschlug. (AN-275834)

### Weitere Fehlerbehebungen in Adobe Analytics

AN-253294; AN-254976; AN-255377; AN-255561; AN-258550; AN-259336; AN-263935; AN-265094; AN-269441; AN-269486; AN-269855; AN-271166; AN-271588; AN-272088; AN-272249; AN-272859; AN-272873; AN-272885; AN-273229; AN-273913; AN-274237; AN-274472; AN-274491; AN-274619; AN-274766; AN-275248; AN-275259; AN-275271; AN-275315; AN-275388; AN-275418; AN-275597; AN-275643; AN-275650; AN-275651; AN-275675; AN-275682; AN-275704; AN-275711; AN-275796; AN-275834; AN-275923; AN-275941; AN-276044; AN-276125; AN-276157; AN-276397; AN-276597; AN-276789; AN-276834; AN-276861; AN-276870; AN-276963; AN-276975; AN-277000; AN-277044; AN-277093; AN-277200; AN-277215; AN-277271; AN-277281; AN-277362; AN-277419; AN-277492; AN-277498; AN-277533; AN-277619; AN-277675; AN-277681; AN-277767; AN-277805; AN-277810; AN-277818; AN-277875; AN-277933; AN-277988; AN-278105; AN-278115; AN-278122; AN-278192; AN-278407; AN-278437; AN-278559; AN-278604; AN-278610; AN-278709; AN-278835; AN-278849; AN-278881; AN-279067; AN-279103; AN-279111; AN-279219; AN-279237; AN-279312

## Wichtige Hinweise für [!DNL Analytics]-Administratoren {#aa-notices}

| Hinweis | Hinzugefügt oder aktualisiert am | Beschreibung |
| ----------- | ---------- | ---------- |
| Ablauf der Zulassungslisten-Verlängerung für das Ende der Nutzungsdauer für veraltete Analytics-OAuth-/JWT-Integrationen | 14. Januar 2022 | Am **25. Mai 2022** läuft die Erweiterung der Zulassungsliste für [Analytics 1.3 API, 1.4 SOAP API und Legacy Analytics OAuth/JWT EOL](https://github.com/AdobeDocs/analytics-1.4-apis/blob/master/docs/APIEOL.md) ab. Sie wurde angeboten, um Kunden, die noch die veralteten OAuth/JWT-Anmeldeinformationen für [!DNL Adobe Analytics] verwenden, zusätzliche Zeit für die Migration ihrer Client-Integrationen auf die [Adobe IMS-Anmeldeinformationen](https://developer.adobe.com/console) zu geben. Dieser Gültigkeitsablauf betrifft (ist jedoch nicht auf beschränkt auf) Kunden von [!DNL Adobe Analytics Livestream] und [!DNL Adobe Campaign], die die erforderlichen IMS-Migrationen nicht abgeschlossen haben. Kunden, die derzeit veraltete [!DNL Analytics]-OAuth-/JWT-Anmeldeinformationen über die Zulassungsliste-Verlängerung verwenden und die ihre Migration zu IMS-Anmeldeinformationen nicht bis zum 25. Mai 2022 abgeschlossen haben, verlieren den Zugriff auf Adobe-Services. Livestream-Kunden können im Hinblick auf die Umstellung ihrer Client-Programme auf IMS-Anmeldeinformationen diese [Anweisungen](https://github.com/AdobeDocs/analytics-1.4-apis/blob/master/docs/live-stream-api/getting_started.md) zurate ziehen. [!DNL Campaign]-Kunden können sich zwecks Upgrade auf die neueste Version von [!DNL Campaign] an ihr Adobe-Account-Team wenden. |
| EOL für [!DNL Reports & Analytics] | 4. Januar 2022 | Adobe beabsichtigt,  und die zugehörigen Berichte und Funktionen zum **31. Dezember 2023** einzustellen. [!DNL Reports & Analytics] Die Berichte, Visualisierungen und zugrunde liegenden Technologien von [!DNL Reports & Analytics] entsprechen nicht mehr den technologischen Standards von Adobe. Die meisten Funktionen von [!DNL Reports & Analytics] sind in [Analysis Workspace](https://experienceleague.adobe.com/docs/analytics/analyze/analysis-workspace/home.html?lang=de) verfügbar. Seit der Veröffentlichung von Analysis Workspace im Jahr 2015 wurden die Funktionen von [!DNL Reports & Analytics] nach Analysis Workspace verschoben, und es wurde ein Schwellenwert für die Workflow-Parität erreicht. [In dieser Mitteilung wird der End-of-Life-Prozess erläutert.](https://spark.adobe.com/page/6WnF8JK6IRDhf/) |
| Aktualisierung der Secure File Transfer Protocol (SFTP)-Services | 13. Januar 2022 | Am **2. Mai 2022** werden die SFTP-Services (Secure File Transfer Protocol) von [!DNL Adobe Analytics] aktualisiert, um die Sicherheit für Dateiübertragungen zu verbessern. Mit dieser Änderung werden einige SFTP-Client-Konfigurationen nicht mehr unterstützt. Wir werden auch einige Verbindungsoptionen hinzufügen, die am **1. März 2022** verfügbar sein werden. Dies wirkt sich nur auf Daten aus, die über SFTP an Adobe Analytics gesendet oder von dort aus abgerufen werden. Das FTP-Protokoll ist davon nicht betroffen. Um Service-Unterbrechungen zu vermeiden, stellen Sie bitte sicher, dass Ihre SFTP-Clients (Code, Tools, Services) die [hier](https://experienceleague.adobe.com/docs/analytics/export/ftp-and-sftp/secure-file-transfer-protocol/sftp-upgrade.html?lang=de) detailliert beschriebenen neuen Anforderungen erfüllen. |
| RDC-Typ _Global + China_ | 22. November 2021 | _Global + China_ ist ein neuer RDC-Typ (Regional Data Collection), der das Routing von Traffic für globale Kunden mithilfe des [!UICONTROL Add-on-Pakets „China Performance Optimization“] vereinfacht. In der Vergangenheit mussten Sie festlegen, ob Daten an den Sammlungsendpunkt „China“ oder an einen der globalen Sammlungsendpunkte weitergeleitet werden sollten. Jetzt können Sie diesen RDC-*Typ* auswählen, damit Adobe den optimalen Sammlungsendpunkt basierend auf der geografischen Lage des Benutzers bestimmen kann. |
| Ende der Nutzungsdauer (EOL) für die vollständige Verarbeitung in Data Sources | 18. Oktober 2021 | Am **31. Januar 2022** beendet Adobe die vollständige Verarbeitung, mit der Benutzer Offline-Trefferdaten in Analytics aufnehmen können. Diese Funktion ist über die [Bulk Data Insertion-API](https://www.adobe.io/apis/experiencecloud/analytics/docs.html#!AdobeDocs/analytics-2.0-apis/master/bdia.md) verfügbar. [Weitere Infos](https://experienceleague.adobe.com/docs/analytics/import/data-sources/data-types-and-categories/datasrc-fullproc-eol.html?lang=de ) |

{style=&quot;table-layout:auto&quot;}

## AppMeasurement {#appm}

Die neuesten Aktualisierungen zu AppMeasurement-Versionen (Version 2.22.4) finden Sie in den [Versionshinweisen zu AppMeasurement für JavaScript](https://experienceleague.adobe.com/docs/analytics/implementation/appmeasurement-updates.html?lang=de).