---
title: Neueste Analytics-Versionshinweise
description: Hier finden Sie die aktuellen Versionshinweise zu Adobe Analytics.
feature: Release Notes
exl-id: 97d16d5c-a8b3-48f3-8acb-96033cc691dc
source-git-commit: 8666c32ffe907ad486778fa382404807459be03c
workflow-type: tm+mt
source-wordcount: '826'
ht-degree: 62%

---

# Aktuelle Adobe Analytics-Versionshinweise (Mai 2022)

**Letzte Aktualisierung**: 8. Juni 2022

## Verwandte Ressourcen

* [Frühere Versionshinweise für 2022](/help/release-notes/2022.md)
* [Versionshinweise zu Customer Journey Analytics](https://experienceleague.adobe.com/docs/analytics-platform/using/releases/latest.html?lang=de)
* [Versionshinweise zu Media Analytics](https://experienceleague.adobe.com/docs/media-analytics/using/additional-resources/release-notes.html?lang=de)
* Die neuesten Versions-Updates für [Adobe Experience Cloud-Produkte](https://business.adobe.com/de/products/adobe-experience-cloud-products.html)

## Neue Funktionen in Adobe Analytics

| Funktion | Beschreibung | [Zieldatum](releases.md) |
| ----------- | ---------- | ------- |
| Auffüllen von Lebenszyklusdimensionen und Metriken über Experience Edge | Mobile Lebenszyklusdaten, die über Experience Edge gesendet werden, werden jetzt in Analytics-Berichten angezeigt. Weitere Informationen dazu, welche Lebenszyklusdaten über Experience Edge erfasst werden und wie sie vorhandenen Lebenszyklusberichten entsprechen, finden Sie in der Dokumentation. [Weitere Informationen](https://experienceleague.adobe.com/docs/analytics/implementation/aep-edge/variable-mapping.html) | 27. Mai 2022 |

{style=&quot;table-layout:auto&quot;}

### Fehlerbehebungen in Adobe Analytics

(Fehlerbehebungen für mehrere Kunden)

Nicht angegeben

### Weitere Fehlerbehebungen in Adobe Analytics

(Fehlerbehebungen für einzelne Kunden)

AN-274429; AN-279640; AN-280918; AN-280945; AN-282884; AN-283565; AN-284785; AN-284814; AN-284854; AN-284989; AN-285244; AN-285253; AN-285432; AN-285528; AN-285535; AN-285710; AN-286255; AN-286340; AN-286434; AN-286454; AN-286630; AN-286716; AN-286854; AN-286911

### Wichtige Hinweise für Adobe Analytics-Administratoren

| Hinweis | Hinzugefügt oder aktualisiert am | Beschreibung |
| ----------- | ---------- | ---------- |
| Anhalten geplanter Berichte in Reports &amp; Analytics | 8. Juni 2022 | Am 21. April 2022 haben wir angekündigt, dass einige Funktionen für terminierte Berichte eingestellt wurden, um die zuvor angekündigte [Abschaffung der Unterstützung für Reports &amp; Analytics](https://express.adobe.com/page/6WnF8JK6IRDhf/). Zu diesen Funktionen gehörte die Möglichkeit, neue Berichte sowie neue Datenextraktionen zu planen.<p>Als Reaktion auf Kundenanfragen, die eine Erweiterung anstreben und den Übergang von Reports and Analytics aus erleichtern möchten, haben wir beschlossen, den Zugriff auf diese Funktionen zu verlängern, bis **31. Januar 2023**. Bitte beachten Sie, dass das Ablauffenster für Berichte und Datenextrakte weiterhin auf neun Monate begrenzt ist. Die Bereitstellung von Berichten und Datenextraktionen wird am Ende dieses Zeitraums ausgesetzt, es sei denn, der Zeitplan wird reaktiviert. <p>Diese Funktionen werden am 31. Januar 2023 eingestellt. Danach müssen Sie Ihre terminierten Berichte auf einen der anderen Mechanismen migrieren, die Ihnen in Adobe Analytics zur Verfügung stehen. Bei weiteren Fragen oder bezüglich Support wenden Sie sich bitte an die Kundenunterstützung von Adobe. |
| Anhalten geplanter Aufgaben in Report Builder | 8. Juni 2022 | Am 21. April 2022 haben wir im Rahmen unserer Leistungs- und Versandoptimierungsbemühungen im Report Builder Änderungen an geplanten Aufgaben durchgeführt. Zu diesen Änderungen gehörte auch das Entfernen der Möglichkeit, dass geplante Sendungen &quot;nach x Vorfällen enden&quot;. Als Reaktion auf mehrere Kundenanfragen, die mehr Zeit für die Erforschung und Implementierung von Alternativen benötigen, haben wir beschlossen, diese Option in begrenztem Umfang wiederherzustellen, bis **31. Januar 2023**.<p>Sie können weiterhin stündliche Report Builder-Aufgaben planen und diese nach maximal 99 Vorkommen beenden. Beachten Sie, dass das Rollback nur für stündliche Aufgaben gilt. das &quot;Nach x Vorkommen beenden&quot;bleibt für alle anderen Versandintervalle (täglich, wöchentlich, monatlich und jährlich) nicht verfügbar. Bitte beachten Sie, dass diese Option ab dem 31. Januar 2023 nicht mehr unterstützt wird. Weitere Fragen oder Support erhalten Sie bei der Kundenunterstützung von Adobe. |
| **SFTP-Upgrade** | 9. Mai 2022 | Zuvor hatten wir mitgeteilt, dass Adobe im Mai 2022 seine Secure File Transfer Protocol (SFTP)-Services aktualisieren würde, um die Sicherheit für die Dateiübertragung zu verbessern. Wir haben dieses Upgrade auf die **Sommer 2022**. Nach dieser Änderung werden bestimmte SFTP-Client-Konfigurationen nicht mehr unterstützt. Dies wirkt sich nur auf Daten aus, die per SFTP an Adobe Analytics gesendet oder von Adobe Analytics abgerufen werden. Das FTP-Protokoll ist nicht betroffen. Um Service-Unterbrechungen zu vermeiden, stellen Sie bitte sicher, dass Ihre SFTP-Clients (Code, Tools, Services) die [hier](https://experienceleague.adobe.com/docs/analytics/export/ftp-and-sftp/secure-file-transfer-protocol/sftp-upgrade.html?lang=de) beschriebenen Anforderungen erfüllen. |
| **Aktualisierung der Browser-Verschlüsselungsmethoden für bestimmte Kunden** | 28. März 2022 | Adobe bietet zwei Chiffrier-Sicherheitsstufen an, die den unterschiedlichen Sicherheitsanforderungen bei der Erfassung von First-Party-Daten gerecht werden. Am **23. Juni 2022** entfernen wir die Unterstützung für bestimmte HTTPS-Verschlüsselungsalgorithmen, so genannte Chiffren, für Kunden, deren Sicherheitsstufe auf „Hoch“ eingestellt ist. Dies bedeutet, dass einige ältere Betriebssysteme dann keine Daten mehr an Analytics senden können, da sie keine modernen Verschlüsselungsmethoden unterstützen. Kunden, die die standardmäßigen Chiffrier-Sicherheitseinstellungen „Standard“ verwenden, sind davon nicht betroffen. Alle Kunden, die derzeit die Einstellung „Hoch“ verwenden, wurden bereits direkt kontaktiert. Eine detaillierte Liste der von dieser Änderung betroffenen Chiffren finden Sie hier. |
| **Aktualisierungen der ISO-Region 2022** | 11. März 2021 | Adobe plant, am **10. Juni 2022** Aktualisierungen für die ISO-Region für 2022 durchzuführen. Nach diesem Release erfolgen kleinere Aktualisierungen zu Geodaten. |
| **EOL für [!DNL Reports & Analytics]** | 4. Januar 2022 | Adobe beabsichtigt, [!DNL Reports & Analytics] und die zugehörigen Berichte und Funktionen zum **31. Dezember 2023** einzustellen. Die Berichte, Visualisierungen und zugrunde liegenden Technologien von [!DNL Reports & Analytics] entsprechen nicht mehr den technologischen Standards von Adobe. Die meisten Funktionen von [!DNL Reports & Analytics] sind in [Analysis Workspace](https://experienceleague.adobe.com/docs/analytics/analyze/analysis-workspace/home.html?lang=de) verfügbar. Seit der Veröffentlichung von Analysis Workspace im Jahr 2015 wurden die Funktionen von [!DNL Reports & Analytics] nach Analysis Workspace verschoben, und es wurde ein Schwellenwert für die Workflow-Parität erreicht. In [dieser Mitteilung](https://spark.adobe.com/page/6WnF8JK6IRDhf/) wird der Ablauf der Produktlebensdauer erläutert. |

{style=&quot;table-layout:auto&quot;}

### AppMeasurement

Die neuesten Aktualisierungen zu AppMeasurement-Versionen (Version 2.22.4) finden Sie in den [Versionshinweisen zu AppMeasurement für JavaScript](https://experienceleague.adobe.com/docs/analytics/implementation/appmeasurement-updates.html?lang=de).

