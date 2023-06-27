---
title: Neueste Analytics-Versionshinweise
description: Hier finden Sie die aktuellen Versionshinweise zu Adobe Analytics.
feature: Release Notes
exl-id: 97d16d5c-a8b3-48f3-8acb-96033cc691dc
source-git-commit: 8e753a4ab2f86ff1b45d3116e51c5ce03f5b038b
workflow-type: tm+mt
source-wordcount: '1515'
ht-degree: 87%

---

# Aktuelle Adobe Analytics-Versionshinweise (Juni 2023)

**Letzte Aktualisierung**: 21. Juni 2023

Die Versionen von Adobe Analytics basieren auf einem [kontinuierlichen Bereitstellungsmodell](releases.md), das eine besser skalierbare, schrittweise Implementierung von Funktionen ermöglicht. Dementsprechend werden diese Versionshinweise mehrmals im Monat aktualisiert. Bitte überprüfen Sie sie regelmäßig.

## Die Highlights der Version {#highlights}

| Funktion | Beschreibung | [Rollout-Beginn](releases.md) | [Allgemeine Verfügbarkeit](releases.md) |
| ----------- | ---------- | ------- | ---- |
| **Verbesserungen bei Datenreparaturfiltern** | Zur Datenreparatur wurden drei Filterverbesserungen hinzugefügt:<ul><li>Filtern Sie nach einer Variablen, um eine zweite Variable zu ändern. Wenn beispielsweise `eVar2` enthält &quot;@&quot;und dann löschen `eVar3`.</li><li>Nach numerischen oder nicht numerischen Werten filtern</li><li>Anwenden mehrerer Filter mit einem AND. Beispiel: wobei `eVar2="a"` UND `eVar3="b"`</li></ul>[Weitere Informationen](https://developer.adobe.com/analytics-apis/docs/2.0/guides/endpoints/data-repair/) | 21. Juni 2023 | 12. Juli 2023 |
| **Link-Freigabe für Projekte (keine Anmeldung erforderlich)** | Sie können jetzt schreibgeschützte Links zu Analysis Workspace-Projekten für Personen freigeben, die keinen Zugriff auf Adobe Analytics haben. Sie können Dinge mit Personen außerhalb Ihrer Organisation oder mit Personen innerhalb Ihrer Organisation teilen, die nicht für Adobe Analytics vorgesehen sind. [Weitere Informationen](../analyze/analysis-workspace/curate-share/share-projects.md#share-a-project-with-anyone-no-login-required)<p>Diese Funktion ist standardmäßig aktiviert und kann von Systemadmins deaktiviert werden. [Weitere Informationen](../analyze/analysis-workspace/user-preferences.md#company-preferences)</p> | 3. Mai 2023 | 7. Juni 2023 |
| **Neue Funktionen für Classification-Sets** | [Klassifizierungssätze](/help/components/classifications/sets/overview.md) wurden mit verschiedenen neuen Funktionen aktualisiert:<ul><li>**Konsolidierung**: Kombinieren Sie Classification-Sets zu einem einzigen konsolidierten Classification-Satz. Der konsolidierte Classification-Satz kann wie andere Classification-Sets oder als Lookup-Datensatz in Customer Journey Analytics verwendet werden. [Weitere Informationen](../components/classifications/sets/consolidations/manage.md)</li><li>**Regeln**: Klassifizieren Sie Werte automatisch anhand von Regeln im Classification-Satz. [Weitere Informationen](../components/classifications/sets/manage/rules.md)</li><li>**Automatisierter Import**: Automatisches Importieren von Classification-Daten aus Cloud-Speicher-Zielen. [Weitere Informationen](../components/classifications/sets/manage/schema.md)</li></ul> | | 7. Juni 2023 |
| **Neue AppMeasurement-Variable** | Die Variable `doubleEncodeLinkParameters` ist für Fälle gedacht, in denen Implementierungen Multi-Byte-Zeichen in Linktracking-Variablen codieren. Die meisten Implementierungen müssen diese Variable nicht festlegen. [Weitere Informationen](../implement/vars/config-vars/doubleencodelinkparameters.md) |  | 7. Juni 2023 |
| **Sichere Ziele für den Export von Daten-Feeds** | Daten-Feeds können jetzt an die folgenden Cloud-Speicher-Ziele gesendet werden:<ul><li>Amazon S3</li><li>Azure RBAC</li><li>Azure SAS</li><li>Google Cloud Platform</li></ul>Ziele, die zuvor verfügbar waren (FTP, SFTP, S3 und Azure Blob), werden nicht mehr empfohlen. [Weitere Informationen](https://experienceleague.adobe.com/docs/analytics/export/analytics-data-feed/create-feed.html?lang=de) | 12. Juni 2023 | 15. Juli 2023 |
| **Bot-Berichte in Workspace** | Bot-Berichte sind jetzt in Analysis Workspace verfügbar. Diese Funktion ist mit mehreren Ergänzungen versehen:<ul><li>Eine neue Dimension: [Bot-Name](/help/components/dimensions/bot-name.md)</li><li>Zwei neue Metriken: [Bot-Seitenaufrufe](/help/components/metrics/bot-page-views.md) und [Bot-Vorfälle](/help/components/metrics/bot-occurrences.md).</li><li>Eine neue Vorlage für berechnete Metriken: [Verhältnis der Bot-Seitenaufrufe](/help/components/c-calcmetrics/cm-reference/default-calcmetrics.md)</li><li>Ein neuer Workspace-Bericht: Bot-Berichte</li></ul>Die neue Dimension und die neuen Metriken enthalten Daten, die ab März 2023 aufgestockt werden. |  | 7. Juni 2023 |

{style="table-layout:auto"}

## Andere neue oder aktualisierte Funktionen {#other}

| Funktion | Beschreibung | [Rollout-Beginn](releases.md) | [Allgemeine Verfügbarkeit](releases.md) |
| ----------- | ---------- | ------- | ---- |
| **Löschen von Zeilen, die dynamische Dimensionen enthalten, aus einer Freiformtabelle** | In einer Freiformtabelle in Analysis Workspace können Sie jetzt mithilfe des Symbols „x“ schnell bestimmte Zeilen löschen, die dynamische Dimensionen enthalten. Dabei wird automatisch die Filterregel „Elemente immer ausschließen“ angewendet.<p>Zuvor bestand die einzige Möglichkeit zum Löschen von Zeilen, die dynamische Dimensionen enthielten, darin, manuell eine Regel im Filterdialogfeld zu erstellen. [Weitere Informationen](/help/analyze/analysis-workspace/visualizations/freeform-table/filter-and-sort.md)</p> | Nicht angegeben | 17. Mai 2023 |
| **Neue Schaltfläche zum Hinzufügen einer Visualisierung in einem Bedienfeld** | Unten in jedem Bedienfeld in Analysis Workspace ist jetzt eine neue Schaltfläche verfügbar, mit der Sie schnell eine Visualisierung hinzufügen können. <p>Zuvor bestand die einzige Methode zum Hinzufügen einer Visualisierung zu einem Bedienfeld darin, eine Visualisierung aus der linken Leiste zu ziehen, eine vorhandene Visualisierung zu duplizieren oder zu kopieren oder ein leeres Bedienfeld zu erstellen. [Weitere Informationen](/help/analyze/analysis-workspace/visualizations/freeform-analysis-visualizations.md)</p> | Nicht angegeben | 17. Mai 2023 |
| **Deep-Linking (Mobile App)** | Ermöglicht Benutzenden das Senden von Links zu Scorecards, die sie direkt zum Scorecard-Projekt in der App führen. Dies erleichtert die Freigabe von Projekten und eine stärkere Interaktion mit weniger technischen Zielgruppen. [Weitere Informationen](https://experienceleague.adobe.com/docs/analytics/analyze/mobapp/create-scorecard.html?lang=de#share-scorecards-using-a-shareable-link) | Nicht angegeben | 17. Mai 2023 |
| **Dynamische Dropdown-Filter** | Wir führen einen neuen Typ von Dropdown-Filtern ein, der verfügbare Werte basierend auf Daten innerhalb des Berichtsbereichs des Bedienfelds und Werte in anderen Dropdown-Filtern bestimmt. Sie können dynamische Dropdown-Filter verwenden, indem Sie eine Dimension in die Dropzone des Bedienfelds ziehen, während Sie die [!UICONTROL Umschalt]-Taste gedrückt halten. Statische Dropdown-Filter bleiben unverändert, indem Sie eine Gruppe von Dimensions-Elementen in die Dropzone des Bedienfelds ziehen, während Sie die [!UICONTROL Umschalt]-Taste gedrückt halten. [Weitere Informationen](/help/analyze/analysis-workspace/c-panels/panels.md) |  | 14. Juni 2023 |
| **Aktualisierte Lernseite für Analytics** | Die Registerkarte „Lernen“ auf der Adobe Analytics-Landingpage enthält jetzt die folgenden Verbesserungen:<ul><li>Verbessertes Design, das mehr Lerninhalte auf einer Seite mit verbesserter Navigation anzeigt</li><li>Möglichkeit zur Personalisierung von Lerninhalten nach Erlebnisebene (Anfängerinnen und Anfänger, Fortgeschrittene und Expertinnen und Experten)</li></ul>[Weitere Informationen](/help/analyze/landing.md) | 27. Juni 2023 | 30. Juni 2023 |
| **Sortieren von Komponenten in Analysis Workspace** | Bei der Anzeige von Komponenten in der linken Leiste oder im Datenwörterbuch in Analysis Workspace ist jetzt eine neue Sortieroption verfügbar. Sie können Komponenten nach „Empfohlen“ (die am häufigsten verwendeten), „Alphabetisch“ oder „Kategorie“ (Typ) sortieren.<p>Zuvor war es nur möglich, Komponenten zu suchen oder zu filtern. [Weitere Informationen](/help/analyze/analysis-workspace/components/analysis-workspace-components.md)</p> | Nicht angegeben | TBD |

{style="table-layout:auto"}

## Fehlerbehebungen in Adobe Analytics

-311878; AN-313968; AN-314130; AN-315701; AN-315761; AN-316613; AN-317563; AN-318829; AN-319009; AN-319043; AN-319066; AN-; AN-319166; AN-319245; AN-319271; AN-319381; AN-319391; AN-319482; AN-319621; AN-319637; AN-319676; AN-320176; AN-320221; AN-320225; AN-320286; AN-320312; AN-320316; AN-320449; AN-320477; AN-320492; AN-320538; AN-320556; AN-320569; AN-320679; AN-320684; AN-320786; AN-320802; AN-320811; AN-320812; AN-320815; AN-321032; AN-321033; AN-321070; AN-321096; AN-321105; AN-321122; AN-321337;

## Wichtige Hinweise für Adobe Analytics-Administratoren {#admin}

| Hinweis | Hinzugefügt oder aktualisiert am | Beschreibung |
| ----------- | ---------- | ---------- |
| **37-monatige Gültigkeit von Kauf-IDs und Ereignis-IDs (Ereignis-Serialisierung)** | 25. Mai 2023 | Eine bevorstehende Version der Analytics-Trefferverarbeitungs-Engine, die für **Ende Juni 2023 oder Anfang Juli 2023** geplant ist, wird damit beginnen, eine 37-monatige Gültigkeit für Kauf-IDs und Ereignis-IDs (Ereignis-Serialisierung) durchzusetzen. Derzeit laufen Kauf-IDs und Ereignis-IDs in Adobe Analytics nie ab. Sobald eine Kauf-ID oder Ereignis-ID gesehen/verwendet wird, wird jeder zukünftige Treffer, unabhängig vom Zeitraum, als Duplikat dieses Kaufs oder Ereignisses markiert. Mit der neuen Version der Verarbeitungs-Engine gilt Folgendes:<ul><li>Kauf-IDs und Ereignis-IDs laufen nach 37 Monaten immer ab.</li><li>Wenn die Kauf-ID oder Ereignis-ID seit 37 Monaten angezeigt wurde, wird sie nicht mehr als doppelter Kauf oder Ereignis betrachtet.</li><li> Wenn Sie Kauf-IDs oder Ereignis-IDs aus mehr als 37 Monaten „wiederverwenden“, werden sie nicht mehr als Duplikate betrachtet.</li></ul> |
| **Migration zu Adobe I/O OAuth Server-zu-Server-Anmeldeinformationen** | 11. Mai 2023 | Adobe Analytics-API- und Livestream-Kunden, die Adobe I/O-JWT-Anmeldeinformationen verwenden, müssen zu Adobe I/O OAuth Server-zu-Server-Anmeldeinformationen migrieren, indem Sie **1. Januar 2025**. Weitere Informationen und Zeitpläne finden Sie in der unten stehenden Tabelle unter dem Hinweis zum Ende der Nutzungsdauer. |
| **Neue IPs, die von Adobe Analytics Daten-Feeds und Data Warehouse Egress im London Data Center verwendet werden** | 27. April 2023 | Dies betrifft Kunden und Kundinnen im London Data Center, die Daten-Feed-Anfragen und/oder Data Warehouse-Berichte an einen FTP-/SFTP-Dienst senden. Die folgenden IP-Adressbereiche sollten Ihrer Firewall-Konfiguration hinzugefügt werden, um den Zugriff zu ermöglichen: <ul><li>130.248.244.32/29</li><li>130.248.244.40/29</li></ul> |

{style="table-layout:auto"}

## Mitteilungen über das Ende der Nutzungsdauer (EOL) {#eol}

| Ende der Nutzungsdauer eines Produkts oder einer Funktion | Datum hinzugefügt oder aktualisiert | Beschreibung |
| --- | --- | --- |
| **Migration zu Adobe I/O OAuth Server-zu-Server-Anmeldeinformationen** | 11. Mai 2023 | Adobe Analytics-API- und Livestream-Kunden, die Adobe I/O-JWT-Anmeldeinformationen verwenden, müssen zu Adobe I/O OAuth Server-zu-Server-Anmeldeinformationen migrieren, indem Sie **1. Januar 2025**. Adobe I/O lässt die Erstellung neuer JWT-Anmeldeinformationen ab dem 1. Mai 2024 nicht zu. Kunden und Kundinnen, die JWT verwenden, müssen neue OAuth Server-zu-Server-Anmeldeinformationen erstellen oder ihre bestehende JWT-Anmeldeinformationen zu OAuth Server-zu-Server-Anmeldeinformationen migrieren. Kunden und Kundinnen müssen außerdem ihre Client-Anwendungen aktualisieren, um die neuen OAuth Server-to-Server-Anmeldeinformationen zu verwenden. <ul><li>[Migration von Dienstkonto-Anmeldeinformationen (JWT)](https://developer.adobe.com/developer-console/docs/guides/authentication/ServerToServerAuthentication/migration/)</li><li>[Implementierungshandbuch für neue und alte Anwendungen mit OAuth](https://developer.adobe.com/developer-console/docs/guides/authentication/ServerToServerAuthentication/implementation/)<li>[Verwenden der neuen OAuth Server-zu-Server-Anmeldeinformationen](https://developer.adobe.com/developer-console/docs/guides/authentication/ServerToServerAuthentication/implementation/)</li><li>[Häufig gestellte Fragen (FAQ)](https://developer.adobe.com/developer-console/docs/guides/authentication/ServerToServerAuthentication/faqs/)</li></ul> |
| **EOL für [!DNL Reports & Analytics]** | 7. März 2023 | Adobe beabsichtigt, [!DNL Reports & Analytics] und die zugehörigen Berichte und Funktionen zum **31. Dezember 2023** einzustellen. Die Berichte, Visualisierungen und zugrunde liegenden Technologien, die [!DNL Reports & Analytics] unterstützen, entsprechen nicht mehr den technologischen Standards von Adobe. Die meisten Funktionen von [!DNL Reports & Analytics] sind in [Analysis Workspace](https://experienceleague.adobe.com/docs/analytics/analyze/analysis-workspace/home.html?lang=de) verfügbar. Seit der Veröffentlichung von Analysis Workspace im Jahr 2015 wurden die Funktionen von [!DNL Reports & Analytics] nach Analysis Workspace verschoben, und es wurde ein Schwellenwert für die Workflow-Parität erreicht. In [dieser Mitteilung](https://spark.adobe.com/page/6WnF8JK6IRDhf/) wird der Ablauf der Produktlebensdauer erläutert.<p>Am 31. Dezember 2023 werden wir viele der zugehörigen Reports &amp; Analytics-Funktionen einstellen, insbesondere: Terminierte Berichte, Datenextraktionen und DL-Berichte. Nach dem 31. Dezember 2023 werden terminierte Berichte nicht mehr gesendet. Im **April 2023** werden alle Berichte, die nach dem 31. Dezember 2023 ablaufen sollten, automatisch aktualisiert und auf den 31. Dezember 2023 zurückgesetzt. Darüber hinaus können Sie nach dem 31. Dezember 2023 keine zukünftigen Berichte mehr planen. |
| **EOL für die [!UICONTROL Veröffentlichungslisten]-Funktion** | 29. September 2022 | Im Rahmen des Endes der Nutzungsdauer von Reports &amp; Analytics werden [!UICONTROL Veröffentlichungslisten] voraussichtlich im **Dezember 2023** das Ende der Nutzungsdauer erreichen. Sie werden keine neuen [!UICONTROL Veröffentlichungslisten] erstellen oder auf bestehende [!UICONTROL Analysis Workspace]-Projekte zugreifen können, um diese zu senden oder zu planen. |
| **EOL für Data Workbench** | 14. September 2022 | Adobe beabsichtigt, Data Workbench ab **31. Dezember 2023** einzustellen. Weitere Informationen finden Sie in der [Mitteilung zum Ende der Nutzungsdauer von Data Workbench](https://experienceleague.adobe.com/docs/data-workbench/using/eol.html?lang=de). Wenden Sie sich bei Fragen an den für Ihre Organisation zuständigen Adobe-Kundenbetreuer. |

{style="table-layout:auto"}

## AppMeasurement

Die neuesten Aktualisierungen zu AppMeasurement-Versionen (Version 2.23.0) finden Sie in den [Versionshinweisen zu AppMeasurement für JavaScript](https://experienceleague.adobe.com/docs/analytics/implementation/appmeasurement-updates.html?lang=de).


## Verwandte Ressourcen

* [Frühere Versionshinweise für 2022](/help/release-notes/2022.md)
* [Versionshinweise zu Customer Journey Analytics](https://experienceleague.adobe.com/docs/analytics-platform/using/releases/latest.html?lang=de)
* [Versionshinweise zu Media Analytics](https://experienceleague.adobe.com/docs/media-analytics/using/additional-resources/release-notes.html?lang=de)
* Die neuesten Versions-Updates für [Adobe Experience Cloud-Produkte](https://business.adobe.com/de/products/adobe-experience-cloud-products.html)
