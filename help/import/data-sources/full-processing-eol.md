---
title: Abschaffung der Datenquellen mit vollständiger Verarbeitung
description: Erfahren Sie mehr über die Mitteilung zum Ende des Lebenszyklus für Datenquellen mit vollständiger Verarbeitung.
exl-id: 7dd6d518-156f-4bf5-86cb-04d0acc8ff0c
feature: Data Sources
role: Admin
source-git-commit: 27bcbd638848650c842ad8d8aaa7ab59e27e900e
workflow-type: tm+mt
source-wordcount: '369'
ht-degree: 4%

---

# Abschaffung der Datenquellen mit vollständiger Verarbeitung

Mit Datenquellen mit vollständiger Verarbeitung konnten Unternehmen historisch Daten auf Trefferebene an Adobe Analytics senden. Diese Daten wurden auf die gleiche Weise verarbeitet wie Daten, die mit herkömmlichen Datenerfassungsmethoden wie AppMeasurement erfasst wurden. Im Jahr 2020 veröffentlichte Adobe die [Bulk-Dateneinfüge-API](https://developer.adobe.com/analytics-apis/docs/2.0/guides/endpoints/bulk-data-insertion/), der die gleichen Funktionen wie Datenquellen mit vollständiger Verarbeitung, jedoch mit zusätzlichen Funktionen ausführt. Auf dieser Seite finden Sie Details zu zusätzlichen Funktionen der Bulk Data Insertion API und Unterschiede in den Dateiformaten.

Am 25. März 2021 verhinderte Adobe die Erstellung neuer Datenquellenverbindungen mit vollständiger Verarbeitung. Am 31. Januar 2022 wurden alle Datendienste für die vollständige Verarbeitung deaktiviert.

## Wichtige Unterschiede zwischen Datenquellen mit vollständiger Verarbeitung und der Bulk-Dateneinfüge-API

* Durch das Einfügen von Massendaten können Sie mehrere Dateien zur parallelen Verarbeitung senden. Besuchergruppen sorgen für Besucherkontinuität und eVar.
* Die Masseneinfügung von Daten verfügt über Funktionen zur Datenvalidierung und Fehlerbehandlung, wodurch ein Teil der administrativen Arbeit beim Senden von Trefferdaten entfernt wird.
* Die Masseneinfügung von Daten unterstützt mehrere Besucher-ID-Identifizierungsmethoden.
* Die Masseneinfügung von Daten enthält einige zusätzliche erforderliche Felder: eine Besucheridentifizierungsspalte, eine `pageName` (oder Link-Äquivalent), `reportSuiteID`, `timestamp`, und `userAgent`.
* Um die Besucherkontinuität und -zuordnung sicherzustellen, müssen beim Einfügen von Massendaten Zeilen in Dateien in chronologischer Reihenfolge sortiert werden. Weitere Informationen zur dateiübergreifenden Sortierung von Besucheraktivitäten finden Sie unter [Besuchergruppen](https://developer.adobe.com/analytics-apis/docs/2.0/guides/endpoints/bulk-data-insertion/visitor-groups/).
* Für die Masseneinfügung von Daten müssen Dateien im .csv-Format komprimiert werden.
* BDIA verwendet `timestamp` anstelle von `date`.

## Variablenvergleich zwischen BDIA und Datenquellen mit vollständiger Verarbeitung

Die folgenden Variablen wurden zum Einfügen von Massendaten eingeführt, die zuvor in Datenquellen mit vollständiger Verarbeitung nicht verfügbar waren:

* **`aamlh`**: Adobe Audience Manager-Standorthinweis.
* **`contextData.key`**: [Kontextdatenvariablen](/help/implement/vars/page-vars/contextdata.md).
* **`customerID`**: Experience Cloud ID-Dienstvariablen. Umfasst `id`, `authState` und `isMCSeed`.
* **`hints`**: [Client-Hinweis](https://experienceleague.adobe.com/docs/experience-platform/edge/fundamentals/user-agent-client-hints.html) Variablen. Enthält `bitness`, `brands`, `mobile`, `model`, `platform`, `platformversion`, und `wow64`.
* **`ipaddress`**: Die IP-Adresse des Benutzers.
* **`language`**: Die [Sprache](/help/components/dimensions/language.md) Dimension.
* **`list1`** - **`list3`**: [Listenvariablen](/help/implement/vars/page-vars/list.md).
* **`marketingCloudVisitorID`**: Die Experience Cloud-ID des Besuchers.
* **`tnta`**: In verwendete Target-Daten-Payload [Analytics for Target](https://experienceleague.adobe.com/docs/target/using/integrate/a4t/a4t.html?lang=de) Integrationen.
* **`trackingServer`**: Die [`trackingServer`](/help/implement/vars/config-vars/trackingserver.md) -Variable.
* **`transactionID`**: Die [`transactionID`](/help/implement/vars/page-vars/transactionid.md) -Variable.
* **`userAgent`**: Die Benutzeragenten-Zeichenfolge des Geräts.

Die folgenden Variablen werden durch das Einfügen von Massendaten nicht unterstützt:

* **`charSet`**: Die [`charSet`](/help/implement/vars/config-vars/charset.md) -Variable. Die Masseneinfügung von Daten unterstützt nur UTF-8.
* **`timezone`**: Der Zeitzonenversatz des Besuchers von GMT in Stunden.
* **`clickAction`**, **`clickActionType`**, **`clickContext`**, **`clickContextType`**, **`clickSourceID`**, **`clickTag`**: Bei der Activity Map-Datenerfassung verwendete Variablen.
