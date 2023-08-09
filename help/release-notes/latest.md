---
title: Aktuelle Adobe Analytics-Versionshinweise
description: Hier finden Sie die aktuellen Versionshinweise zu Adobe Analytics.
feature: Release Notes
exl-id: 97d16d5c-a8b3-48f3-8acb-96033cc691dc
source-git-commit: d1b9ef79a456fc52b7fa644d088f7089c9b654e4
workflow-type: tm+mt
source-wordcount: '899'
ht-degree: 79%

---

# Aktuelle Adobe Analytics-Versionshinweise (August 2023)

**Letzte Aktualisierung**: 9. August 2023

Diese Versionshinweise beziehen sich auf den Veröffentlichungszeitraum vom 9. August bis 13. September 2023. Die Versionen von Adobe Analytics basieren auf einem [kontinuierlichen Bereitstellungsmodell](releases.md), das eine besser skalierbare, schrittweise Implementierung von Funktionen ermöglicht. Dementsprechend werden diese Versionshinweise mehrmals im Monat aktualisiert. Bitte überprüfen Sie sie regelmäßig.

## Neue Funktionen oder Verbesserungen zwischen 9. August und 12. September 2023 {#features}

| Funktion | Beschreibung | [Rollout-Beginn](releases.md) | [Allgemeine Verfügbarkeit](releases.md) |
| ----------- | ---------- | ------- | ---- |
| **Klassifizierungssätze in API 2.0** | Bietet Adobe Analytics API 2.0-Methoden zum Speichern, Löschen, Abrufen, Importieren und Exportieren von Classification-Set-Daten. | Nicht angegeben | 31. August 2023 |
| **Reporting Activity Manager** | Der Reporting-Aktivitäts-Manager bietet Administratoren detaillierte Einblicke in den Berichtsverbrauch für jede Report Suite, sodass sie während Spitzenzeiten der Berichterstellung mühelos Kapazitätsprobleme diagnostizieren und beheben können. [Weitere Informationen](/help/admin/admin/reporting-activity.md) | Nicht angegeben | 6. September 2023 |

{style="table-layout:auto"}

## Fehlerbehebungen in Adobe Analytics

* Es wurde ein Problem behoben, durch das benutzerspezifische Ereignisse nicht geladen wurden. (AN-324163)
* Es wurde ein Problem behoben, durch das Beschriftungen für Legenden in einer Visualisierung nicht bearbeitet werden konnten. (AN-323246)

AN-315605; AN-316306; AN-317494; AN-317844; AN-320424; AN-320597; AN-320680; AN 320869; AN-321624; AN-321693; AN-322009; AN-32244; AN-322380; AN-322432; AN-3 22466; AN-322556; AN-322669; AN-322735; AN-323151; AN-323220; AN-32380; AN-32 3492; AN-323595; AN-323755; AN-323854; AN-323916; AN-324044; AN-324200; AN-324 213; AN-324238; AN-324347; AN-323598; AN-323625; AN-323631; AN-323638; AN-3236 41; AN-323755; AN-323767; AN-323777; AN-323825; AN-323846; AN-323972; AN-3241 3; AN-324170; AN-324197; AN-324273; AN-324275; AN-324345; AN-324384; AN-32443; AN-324511; AN-324513; AN-324521; AN-324524; AN-324531; AN-324532; AN-324534; AN 324537; AN-324569; AN-324618; AN-324635; AN-324688; AN-324704; AN-324712; AN-3 24721; AN-324745; AN-324792; AN-324793; AN-324794; AN-324795; AN-324824; AN-32 4905; AN-324918; AN-324932; AN-324934; AN-324947; AN-325003; AN-325073; AN-325 143; AN-325148; AN-325153; AN-325177; AN-325187; AN-325252; AN-325305; AN-3253 63; AN-325401; AN-325439; AN-325431; AN-325491; AN-325495; AN-325508; AN-3259 4; AN-325601; AN-325660; AN-325779; AN-325857; AN-325883; AN-325885; AN-32586


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
