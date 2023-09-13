---
title: Aktuelle Adobe Analytics-Versionshinweise
description: Aktuelle Versionshinweise zu Adobe Analytics anzeigen
feature: Release Notes
exl-id: 97d16d5c-a8b3-48f3-8acb-96033cc691dc
source-git-commit: 1bd654eef37ac242cf4076e133e482f6a5990cc9
workflow-type: tm+mt
source-wordcount: '800'
ht-degree: 68%

---

# Aktuelle Adobe Analytics-Versionshinweise (September 2023)

**Letzte Aktualisierung**: 13. September 2023

Die Versionshinweise vom September beziehen sich auf den Veröffentlichungszeitraum vom 13. September 2023 bis zum 3. Oktober 2023. Die Versionen von Adobe Analytics basieren auf einem [kontinuierlichen Bereitstellungsmodell](releases.md), das eine besser skalierbare, schrittweise Implementierung von Funktionen ermöglicht. Dementsprechend werden diese Versionshinweise mehrmals im Monat aktualisiert. Bitte überprüfen Sie sie regelmäßig.

## Neue Funktionen oder Verbesserungen {#features}

| Funktion | Beschreibung | [Rollout-Beginn](releases.md) | [Allgemeine Verfügbarkeit](releases.md) |
| ----------- | ---------- | ------- | ---- |
| **Klassifizierung in API 2.0** | Bietet Adobe Analytics API 2.0 Methoden zum Speichern, Löschen, Abrufen, Importieren und Exportieren von Klassifizierungssatz-Daten. [Weitere Informationen](https://developer.adobe.com/analytics-apis/docs/2.0/guides/endpoints/classifications/) | Nicht angegeben | 13. September 2023 |
| **Unterstützung für neue `correlationID` -Feld für A4T-Classifications** | Die `_experience.decisioning.propositions.scopeDetails.correlationID` ist jetzt im Adobe Analytics-Quell-Connector-Schema verfügbar. Diese ID wird hinzugefügt, um die einfache Verknüpfung von Classification-Daten für Adobe Target-Aktivitäten und Erlebnisereignisse zu ermöglichen. | Nicht angegeben | 13. September 2023 |
| **Data Warehouse-Verbesserungen** | Beim Erstellen einer Data Warehouse-Anfrage können Sie jetzt ein Cloud-Konto für die Verwendung als Berichtsziel konfigurieren. Die folgenden Cloud-Kontotypen sind für das Senden von Daten verfügbar:<ul><li>Amazon S3</li><li>Google Cloud Platform</li><li>Azure SAS</li><li>Azure RBAC</li><li>E-Mail (diese Option war zuvor verfügbar)</li></ul>FTP, SFTP, Azure Blob und S3 sind weiterhin als Berichtsziele verfügbar, werden aber nicht mehr empfohlen.<p>Das Benutzererlebnis beim Erstellen und Verwalten von Data Warehouse-Anforderungen wurde ebenfalls verbessert. Weitere Informationen finden Sie unter [Erstellen einer Data Warehouse-Anfrage](https://experienceleague.adobe.com/docs/analytics/export/data-warehouse/create-request/t-dw-create-request.html) und [Data Warehouse-Anforderungen verwalten](https://experienceleague.adobe.com/docs/analytics/export/data-warehouse/data-warehouse-requests-manage.html?lang=de). | 13. September 2023 | 4. Oktober 2023 |

{style="table-layout:auto"}

## Fehlerbehebungen in Adobe Analytics

* Es wurde ein Fehler behoben, der verhinderte, dass Klassifizierungsdaten in Workspace angezeigt wurden. (AN-326827)

## Weitere Fehlerbehebungen

AN-314882; AN-315591; AN-318165; AN-318559; AN-319031; AN-319244; AN-321657; AN 321759; AN-323099; AN-323596; AN-323640; AN-324442; AN-324921; AN-324953; AN-3 24977; AN-324979; AN-325124; AN-325395; AN-325433; AN-325535; AN-325693. 5720; AN-325835; AN-325880; AN-325957; AN-325984; AN-326054; AN-326065; AN-326 136; AN-326155; AN-326162; AN-326235; AN-326317; AN-326344; AN-326357; AN-3263 59; AN-326433; AN-326438; AN-326440; AN-326461; AN-326464; AN-326523; AN-32655 3; AN-326606; AN-326635; AN-326642; AN-326652; AN-326678; AN-326769; AN-32677; AN-326830; AN-326938; AN-326949; AN-327081; AN-327082; AN-327085; AN-327103; AN 327198; AN-327225; AN-327275; AN-327358; AN-327423; AN-327561; AN-32755; AN-3 27896; AN-327922; AN-328128; AN-328300; AN-328428; AN-328518; AN-32854

## Wichtige Hinweise für Adobe Analytics-Administratoren {#admin}

| Hinweis | Hinzugefügt oder aktualisiert am | Beschreibung |
| ----------- | ---------- | ---------- |
| Nicht angegeben | nicht angegeben | Nicht angegeben |

{style="table-layout:auto"}

## Mitteilungen über das Ende der Nutzungsdauer (EOL) {#eol}

| Ende der Nutzungsdauer eines Produkts oder einer Funktion | Datum hinzugefügt oder aktualisiert | Beschreibung |
| --- | --- | --- |
| **Migration auf OAuth Server-zu-Server-Anmeldeinformationen für Adobe I/O** | 11. Mai 2023 | Kundinnen und Kunden von Adobe Analytics-API und Livestream, die JWT-Anmeldeinformationen für Adobe I/O verwenden, müssen bis zum **1. Januar 2025** auf OAuth Server-zu-Server-Anmeldeinformationen für Adobe I/O migrieren. Adobe I/O lässt die Erstellung neuer JWT-Anmeldeinformationen ab dem 1. Mai 2024 nicht mehr zu. Kunden und Kundinnen, die JWT verwenden, müssen neue OAuth Server-zu-Server-Anmeldeinformationen erstellen oder ihre bestehende JWT-Anmeldeinformationen zu OAuth Server-zu-Server-Anmeldeinformationen migrieren. Kunden und Kundinnen müssen außerdem ihre Client-Anwendungen aktualisieren, um die neuen OAuth Server-to-Server-Anmeldeinformationen zu verwenden. <ul><li>[Migration von Dienstkonto-Anmeldeinformationen (JWT)](https://developer.adobe.com/developer-console/docs/guides/authentication/ServerToServerAuthentication/migration/)</li><li>[Implementierungshandbuch für neue und alte Programme mit OAuth](https://developer.adobe.com/developer-console/docs/guides/authentication/ServerToServerAuthentication/implementation/)<li>[Verwenden der neuen OAuth Server-zu-Server-Anmeldeinformationen](https://developer.adobe.com/developer-console/docs/guides/authentication/ServerToServerAuthentication/implementation/)</li><li>[Häufig gestellte Fragen (FAQ)](https://developer.adobe.com/developer-console/docs/guides/authentication/ServerToServerAuthentication/faqs/)</li></ul> |
| **EOL für [!DNL Reports & Analytics]** | 7. März 2023 | Adobe beabsichtigt, [!DNL Reports & Analytics] und die zugehörigen Berichte und Funktionen zum **31. Dezember 2023** einzustellen. Die Berichte, Visualisierungen und zugrunde liegenden Technologien, die [!DNL Reports & Analytics] unterstützen, entsprechen nicht mehr den technologischen Standards von Adobe. Die meisten Funktionen von [!DNL Reports & Analytics] sind in [Analysis Workspace](https://experienceleague.adobe.com/docs/analytics/analyze/analysis-workspace/home.html?lang=de) verfügbar. Seit der Veröffentlichung von Analysis Workspace im Jahr 2015 wurden die Funktionen von [!DNL Reports & Analytics] nach Analysis Workspace verschoben, und es wurde ein Schwellenwert für die Workflow-Parität erreicht. In [dieser Mitteilung](https://spark.adobe.com/page/6WnF8JK6IRDhf/) wird der Ablauf der Produktlebensdauer erläutert.<p>Am 31. Dezember 2023 werden wir viele der zugehörigen Reports &amp; Analytics-Funktionen einstellen, insbesondere: Terminierte Berichte, Datenextraktionen und DL-Berichte. Nach dem 31. Dezember 2023 werden terminierte Berichte nicht mehr gesendet. In **April 2023**, wurden alle Berichte, die nach dem 31. Dezember 2023 ablaufen sollten, automatisch aktualisiert und auf den 31. Dezember 2023 zurückgesetzt. Darüber hinaus können Sie nach dem 31. Dezember 2023 keine zukünftigen Berichte mehr planen. |
| **EOL für die [!UICONTROL Veröffentlichungslisten]-Funktion** | 29. September 2022 | Im Rahmen des Endes der Nutzungsdauer von Reports &amp; Analytics werden [!UICONTROL Veröffentlichungslisten] voraussichtlich im **Dezember 2023** das Ende der Nutzungsdauer erreichen. Sie werden keine neuen [!UICONTROL Veröffentlichungslisten] erstellen oder auf bestehende [!UICONTROL Analysis Workspace]-Projekte zugreifen können, um diese zu senden oder zu planen. |
| **EOL für Data Workbench** | 14. September 2022 | Adobe beabsichtigt, Data Workbench ab **31. Dezember 2023** einzustellen. Weitere Informationen finden Sie in der [Mitteilung zum Ende der Nutzungsdauer von Data Workbench](https://experienceleague.adobe.com/docs/data-workbench/using/eol.html?lang=de). Wenden Sie sich bei Fragen an den für Ihre Organisation zuständigen Adobe-Kundenbetreuer. |

{style="table-layout:auto"}

## AppMeasurement

Die neuesten Aktualisierungen zu AppMeasurement-Versionen (Version 2.24.0) finden Sie in den [Versionshinweisen zu AppMeasurement für JavaScript](https://experienceleague.adobe.com/docs/analytics/implementation/appmeasurement-updates.html?lang=de).


## Verwandte Ressourcen

* [Frühere Versionshinweise für 2022](/help/release-notes/2022.md)
* [Versionshinweise zu Customer Journey Analytics](https://experienceleague.adobe.com/docs/analytics-platform/using/releases/latest.html?lang=de)
* [Versionshinweise zu Media Analytics](https://experienceleague.adobe.com/docs/media-analytics/using/additional-resources/release-notes.html?lang=de)
* Die neuesten Versions-Updates für [Adobe Experience Cloud-Produkte](https://business.adobe.com/de/products/adobe-experience-cloud-products.html)
