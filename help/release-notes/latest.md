---
title: Neueste Analytics-Versionshinweise
description: Hier finden Sie die aktuellen Versionshinweise zu Adobe Analytics.
feature: Release Notes
exl-id: 97d16d5c-a8b3-48f3-8acb-96033cc691dc
source-git-commit: f996448224ffebd57023c8d8e4eeeccb4d6e2a47
workflow-type: tm+mt
source-wordcount: '920'
ht-degree: 100%

---

# Aktuelle Adobe Analytics-Versionshinweise (Juli 2023)

**Letzte Aktualisierung**: 10. Juli 2023

Die Versionen von Adobe Analytics basieren auf einem [kontinuierlichen Bereitstellungsmodell](releases.md), das eine besser skalierbare, schrittweise Implementierung von Funktionen ermöglicht. Dementsprechend werden diese Versionshinweise mehrmals im Monat aktualisiert. Bitte überprüfen Sie sie regelmäßig.

## Neue Funktionen oder Verbesserungen {#features}

| Funktion | Beschreibung | [Rollout-Beginn](releases.md) | [Allgemeine Verfügbarkeit](releases.md) |
| ----------- | ---------- | ------- | ---- |
| **Konfigurieren von Speicherorten für Cloud-Konten für die Aufnahme von Klassifizierungsdaten** | Sie können jetzt Speicherorte für Cloud-Konten verwalten, die für die Automatisierung von Klassifizierungssätzen verwendet werden. [Weitere Informationen](/help/components/locations/configure-import-accounts.md)<p> | Nicht angegeben | 10. Juli 2023 |
| **Verbesserungen bei Datenreparaturfiltern** | Zur Datenreparatur wurden drei Filterverbesserungen hinzugefügt:<ul><li>Filtern Sie nach einer Variable, um eine zweite Variable zu ändern. Wenn zum Beispiel `eVar2` ein „@“ enthält, dann löschen Sie `eVar3`.</li><li>Filtern nach numerischen oder nicht numerischen Werten</li><li>Wenden Sie mehrere Filter mit einem „UND“ an. Zum Beispiel, wenn `eVar2="a"` UND `eVar3="b"`</li></ul>[Weitere Informationen](https://developer.adobe.com/analytics-apis/docs/2.0/guides/endpoints/data-repair/) | 21. Juni 2023 | 12. Juli 2023 |
| **Sichere Ziele für den Export von Daten-Feeds** | Daten-Feeds können jetzt an die folgenden Cloud-Speicher-Ziele gesendet werden:<ul><li>Amazon S3</li><li>Azure RBAC</li><li>Azure SAS</li><li>Google Cloud Platform</li></ul>Ziele, die zuvor verfügbar waren (FTP, SFTP, S3 und Azure Blob), werden nicht mehr empfohlen. [Weitere Informationen](https://experienceleague.adobe.com/docs/analytics/export/analytics-data-feed/create-feed.html?lang=de) | 12. Juni 2023 | 13. Juli 2023 |
| **Neue AppMeasurement-Variable** | Die Variable `decodeLinkParameters` ist für Fälle gedacht, in denen Implementierungen Multi-Byte-Zeichen in Linktracking-Variablen codieren. Die meisten Implementierungen müssen diese Variable nicht festlegen. [Weitere Informationen](../implement/vars/config-vars/decodelinkparameters.md) |  | 17. Juli 2023 |

{style="table-layout:auto"}

## Fehlerbehebungen in Adobe Analytics

AN-307816; AN-318111; AN-318584; AN-318828; AN-320440; AN-320568; AN-320616; AN-321013; AN-321513; AN-321520; AN-321757; AN-321820; AN-321917; AN-322034; AN-322135; AN-322140; AN-322142; AN-322251; AN-322353; AN-322378; AN-322383; AN-322427; AN-322458; AN-322543; AN-322630; AN-322637; AN-322638; AN-322647; AN-322728; AN-322732; AN-322777; AN-322817; AN-322957; AN-322958; AN-323035; AN-323074; AN-323150; AN-323196; AN-323197; AN-323205; AN-323206; AN-323217; AN-323224; AN-323225; AN-323244; AN-323257; AN-323277; AN-323280; AN-323293; AN-323309; AN-323318; AN-323468; AN-323476; AN-323514; AN-323572; AN-323592; AN-323782; AN-323835

## Wichtige Hinweise für Adobe Analytics-Administratoren {#admin}

| Hinweis | Hinzugefügt oder aktualisiert am | Beschreibung |
| ----------- | ---------- | ---------- |
| **37-monatige Gültigkeit von Kauf-IDs und Ereignis-IDs (Ereignis-Serialisierung)** | 10. Juli 2023 | Eine bevorstehende Version der Analytics-Trefferverarbeitungs-Engine, die für den **13. Juli 2023** geplant ist, wird damit beginnen, eine 37-monatige Gültigkeit für Kauf-IDs und Ereignis-IDs (Ereignis-Serialisierung) durchzusetzen. Derzeit laufen Kauf-IDs und Ereignis-IDs in Adobe Analytics nie ab. Sobald eine Kauf-ID oder Ereignis-ID gesehen/verwendet wird, wird jeder zukünftige Treffer, unabhängig vom Zeitraum, als Duplikat dieses Kaufs oder Ereignisses markiert. Mit der neuen Version der Verarbeitungs-Engine gilt Folgendes:<ul><li>Kauf-IDs und Ereignis-IDs laufen nach 37 Monaten immer ab.</li><li>Wenn die Kauf-ID oder Ereignis-ID seit 37 Monaten angezeigt wurde, wird sie nicht mehr als doppelter Kauf oder Ereignis betrachtet.</li><li> Wenn Sie Kauf-IDs oder Ereignis-IDs aus mehr als 37 Monaten „wiederverwenden“, werden sie nicht mehr als Duplikate betrachtet.</li></ul> |
| **Migration auf OAuth Server-zu-Server-Anmeldeinformationen für Adobe I/O** | 11. Mai 2023 | Kundinnen und Kunden von Adobe Analytics-API und Livestream, die JWT-Anmeldeinformationen für Adobe I/O verwenden, müssen bis zum **1. Januar 2025** auf OAuth Server-zu-Server-Anmeldeinformationen für Adobe I/O migrieren. Weitere Informationen und Zeitpläne finden Sie in der unten stehenden Tabelle unter dem Hinweis zum Ende der Nutzungsdauer. |

{style="table-layout:auto"}

## Mitteilungen über das Ende der Nutzungsdauer (EOL) {#eol}

| Ende der Nutzungsdauer eines Produkts oder einer Funktion | Datum hinzugefügt oder aktualisiert | Beschreibung |
| --- | --- | --- |
| **Migration auf OAuth Server-zu-Server-Anmeldeinformationen für Adobe I/O** | 11. Mai 2023 | Kundinnen und Kunden von Adobe Analytics-API und Livestream, die JWT-Anmeldeinformationen für Adobe I/O verwenden, müssen bis zum **1. Januar 2025** auf OAuth Server-zu-Server-Anmeldeinformationen für Adobe I/O migrieren. Adobe I/O lässt die Erstellung neuer JWT-Anmeldeinformationen ab dem 1. Mai 2024 nicht mehr zu. Kunden und Kundinnen, die JWT verwenden, müssen neue OAuth Server-zu-Server-Anmeldeinformationen erstellen oder ihre bestehende JWT-Anmeldeinformationen zu OAuth Server-zu-Server-Anmeldeinformationen migrieren. Kunden und Kundinnen müssen außerdem ihre Client-Anwendungen aktualisieren, um die neuen OAuth Server-to-Server-Anmeldeinformationen zu verwenden. <ul><li>[Migration von Dienstkonto-Anmeldeinformationen (JWT)](https://developer.adobe.com/developer-console/docs/guides/authentication/ServerToServerAuthentication/migration/)</li><li>[Implementierungshandbuch für neue und alte Programme mit OAuth](https://developer.adobe.com/developer-console/docs/guides/authentication/ServerToServerAuthentication/implementation/)<li>[Verwenden der neuen OAuth Server-zu-Server-Anmeldeinformationen](https://developer.adobe.com/developer-console/docs/guides/authentication/ServerToServerAuthentication/implementation/)</li><li>[Häufig gestellte Fragen (FAQ)](https://developer.adobe.com/developer-console/docs/guides/authentication/ServerToServerAuthentication/faqs/)</li></ul> |
| **EOL für [!DNL Reports & Analytics]** | 7. März 2023 | Adobe beabsichtigt, [!DNL Reports & Analytics] und die zugehörigen Berichte und Funktionen zum **31. Dezember 2023** einzustellen. Die Berichte, Visualisierungen und zugrunde liegenden Technologien, die [!DNL Reports & Analytics] unterstützen, entsprechen nicht mehr den technologischen Standards von Adobe. Die meisten Funktionen von [!DNL Reports & Analytics] sind in [Analysis Workspace](https://experienceleague.adobe.com/docs/analytics/analyze/analysis-workspace/home.html?lang=de) verfügbar. Seit der Veröffentlichung von Analysis Workspace im Jahr 2015 wurden die Funktionen von [!DNL Reports & Analytics] nach Analysis Workspace verschoben, und es wurde ein Schwellenwert für die Workflow-Parität erreicht. In [dieser Mitteilung](https://spark.adobe.com/page/6WnF8JK6IRDhf/) wird der Ablauf der Produktlebensdauer erläutert.<p>Am 31. Dezember 2023 werden wir viele der zugehörigen Reports &amp; Analytics-Funktionen einstellen, insbesondere: Terminierte Berichte, Datenextraktionen und DL-Berichte. Nach dem 31. Dezember 2023 werden terminierte Berichte nicht mehr gesendet. Im **April 2023** werden alle Berichte, die nach dem 31. Dezember 2023 ablaufen sollten, automatisch aktualisiert und auf den 31. Dezember 2023 zurückgesetzt. Darüber hinaus können Sie nach dem 31. Dezember 2023 keine zukünftigen Berichte mehr planen. |
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
