---
title: Neueste Analytics-Versionshinweise
description: Hier finden Sie die aktuellen Versionshinweise zu Adobe Analytics.
feature: Release Notes
exl-id: 97d16d5c-a8b3-48f3-8acb-96033cc691dc
source-git-commit: b9bf373d7d62d7b6df405629cdf304246b80649f
workflow-type: tm+mt
source-wordcount: '905'
ht-degree: 90%

---

# Aktuelle Adobe Analytics-Versionshinweise (Mai 2022)

**Letzte Aktualisierung**: 17. Mai 2022

## Verwandte Ressourcen

* [Frühere Versionshinweise für 2022](/help/release-notes/2022.md)
* [Versionshinweise zu Customer Journey Analytics](https://experienceleague.adobe.com/docs/analytics-platform/using/releases/latest.html?lang=de)
* [Versionshinweise zu Media Analytics](https://experienceleague.adobe.com/docs/media-analytics/using/additional-resources/release-notes.html?lang=de)
* Die neuesten Versions-Updates für [Adobe Experience Cloud-Produkte](https://business.adobe.com/de/products/adobe-experience-cloud-products.html)

## Neue Funktionen in Adobe Analytics

| Funktion | Beschreibung | [Zieldatum](releases.md) |
| ----------- | ---------- | ------- |
| Auffüllen von Lebenszyklusdimensionen und Metriken über Experience Edge | Mobile Lebenszyklusdaten, die über Experience Edge gesendet werden, werden jetzt in Analytics-Berichten angezeigt. Weitere Informationen dazu, welche Lebenszyklusdaten über Experience Edge erfasst werden und wie sie mit vorhandenen Lebenszyklusberichten übereinstimmen, finden Sie in der Dokumentation . [Weitere Informationen - in Kürze verfügbar] | 27. Mai 2022 |

{style=&quot;table-layout:auto&quot;}

### Fehlerbehebungen in Adobe Analytics

(Fehlerbehebungen für mehrere Kunden)

Nicht angegeben

### Weitere Fehlerbehebungen in Adobe Analytics

(Fehlerbehebungen für einzelne Kunden)

AN-274429; AN-279640; AN-280918; AN-280945; AN-282884; AN-283565; AN-284785; AN-284814; AN-284854; AN-284989; AN-285244 AN-285253 AN-285432; AN-285528; AN-285535; AN-285710; AN-286255; AN-286340; AN-286434; AN-286454 AN-286630; AN-286716; AN-286854; AN-286911

### Wichtige Hinweise für Adobe Analytics-Administratoren

| Hinweis | Hinzugefügt oder aktualisiert am | Beschreibung |
| ----------- | ---------- | ---------- |
| **SFTP-Upgrade** | 9. Mai 2022 | Zuvor hatten wir mitgeteilt, dass Adobe im Mai 2022 seine Secure File Transfer Protocol (SFTP)-Services aktualisieren würde, um die Sicherheit für die Dateiübertragung zu verbessern. Wir haben diese Aktualisierung auf den Sommer 2022 verschoben. Nach dieser Änderung werden bestimmte SFTP-Client-Konfigurationen nicht mehr unterstützt. Dies wirkt sich nur auf Daten aus, die per SFTP an Adobe Analytics gesendet oder von Adobe Analytics abgerufen werden. Das FTP-Protokoll ist nicht betroffen. Um Service-Unterbrechungen zu vermeiden, stellen Sie bitte sicher, dass Ihre SFTP-Clients (Code, Tools, Services) die [hier](https://experienceleague.adobe.com/docs/analytics/export/ftp-and-sftp/secure-file-transfer-protocol/sftp-upgrade.html?lang=de) beschriebenen Anforderungen erfüllen. |
| **Berechtigung für geräteübergreifende Analyse (CDA)** | 13. April 2022 | effektiv **1. Mai 2022**, alle neuen Implementierungen von [CDA](/help/components/cda/overview.md) sind auf maximal drei Report Suite-IDs (RSIDs) pro Kunde beschränkt. |
| **Geänderte Verarbeitung von über Experience Edge erfassten A4T-Daten durch Adobe Analytics** | 31. März 2022 | Am 7. März 2022 wurde in Analytics die Art und Weise der Behandlung einiger von Experience Edge kommender Aufrufe geändert, die Target-Inhalte für die Berichterstellung von Analytics for Target (A4T) enthalten. Seit dem 7. März werden alle Treffer mit A4T-Berichtsinhalten so geändert, dass sie nicht als Seitenansichts- oder Link-Ereignisse gezählt werden. Seit dem **31. März 2022** ist die Logik selektiver, sodass die standardmäßigen Seitenansichts- und Klickereignisse nicht geändert werden. Künftig werden nur noch reine Personalisierungsaufrufe geändert, die nur A4T-Inhalte aufweisen. |
| **Aktualisierung der Browser-Verschlüsselungsmethoden für bestimmte Kunden** | 28. März 2022 | Adobe bietet zwei Chiffrier-Sicherheitsstufen an, die den unterschiedlichen Sicherheitsanforderungen bei der Erfassung von First-Party-Daten gerecht werden. Am **23. Juni 2022** entfernen wir die Unterstützung für bestimmte HTTPS-Verschlüsselungsalgorithmen, so genannte Chiffren, für Kunden, deren Sicherheitsstufe auf „Hoch“ eingestellt ist. Dies bedeutet, dass einige ältere Betriebssysteme dann keine Daten mehr an Analytics senden können, da sie keine modernen Verschlüsselungsmethoden unterstützen. Kunden, die die standardmäßigen Chiffrier-Sicherheitseinstellungen „Standard“ verwenden, sind davon nicht betroffen. Alle Kunden, die derzeit die Einstellung „Hoch“ verwenden, wurden bereits direkt kontaktiert. Eine detaillierte Liste der von dieser Änderung betroffenen Chiffren finden Sie hier. |
| **Pausieren älterer terminierter Berichte** | 12. April 2022 | Ab **20. April 2022** pausiert Adobe alle terminierten Berichte, deren Erstellungsdatum mehr als zwei Jahre zurückliegt (erstellt vor dem 31. Januar 2020). Es werden keine Berichte oder Daten gelöscht. Nur Berichte, die älter als zwei Jahre sind, werden pausiert. In diesem Fall werden keine weiteren terminierten Berichte gesendet. Weitere Informationen |
| **Aktualisierungen der ISO-Region 2022** | 11. März 2021 | Adobe plant, am **10. Juni 2022** Aktualisierungen für die ISO-Region für 2022 durchzuführen. Nach diesem Release erfolgen kleinere Aktualisierungen zu Geodaten. |
| **Pausieren älterer terminierter Report Builder-Aufgaben** | 12. April 2022 | Ab **20. April 2022** pausiert Adobe alle terminierten Report Builder-Aufgaben, die vor mehr als zwei Jahren erstellt wurden. Diese Pausierung gilt insbesondere für alle Aufgaben, die vor dem 31. Januar 2020 erstellt wurden. Es werden keine Aufgaben, Arbeitsmappen oder Daten gelöscht. Aufgaben, die älter als zwei Jahre sind, werden jedoch pausiert, und es werden keine weiteren terminierten Aufgaben gesendet. Weitere Informationen |
| **Ablauf der Zulassungslisten-Verlängerung für das Ende der Nutzungsdauer für veraltete Analytics-OAuth-/JWT-Integrationen** | 14. Januar 2022 | Am **25. Mai 2022** läuft die Erweiterung der Zulassungsliste für [Analytics 1.3 API, 1.4 SOAP API und Legacy Analytics OAuth/JWT EOL](https://github.com/AdobeDocs/analytics-1.4-apis/blob/master/docs/APIEOL.md) ab. Sie wurde angeboten, um Kunden, die noch die veralteten OAuth/JWT-Anmeldeinformationen für [!DNL Adobe Analytics] verwenden, zusätzliche Zeit für die Migration ihrer Client-Integrationen auf die [Adobe IMS-Anmeldeinformationen](https://developer.adobe.com/console) zu geben. Dieser Gültigkeitsablauf betrifft (ist jedoch nicht auf beschränkt auf) Kunden von [!DNL Adobe Analytics Livestream] und [!DNL Adobe Campaign], die die erforderlichen IMS-Migrationen nicht abgeschlossen haben. Kunden, die derzeit veraltete [!DNL Analytics] OAuth/JWT-Anmeldeinformationen über die Erweiterung der Zulassungsliste verwenden und die Migration zu IMS-Anmeldeinformationen nicht bis zum 25. Mai 2022 abschließen, verlieren den Zugriff auf Adobe-Services. Livestream-Kunden können im Hinblick auf die Umstellung ihrer Client-Programme auf IMS-Anmeldeinformationen diese [Anweisungen](https://github.com/AdobeDocs/analytics-1.4-apis/blob/master/docs/live-stream-api/getting_started.md) zurate ziehen. [!DNL Campaign]-Kunden können sich zwecks Upgrade auf die neueste Version von [!DNL Campaign] an ihr Adobe-Account-Team wenden. |
| **EOL für [!DNL Reports & Analytics]** | 4. Januar 2022 | Adobe beabsichtigt, [!DNL Reports & Analytics] und die zugehörigen Berichte und Funktionen zum **31. Dezember 2023** einzustellen. Die Berichte, Visualisierungen und zugrunde liegenden Technologien von [!DNL Reports & Analytics] entsprechen nicht mehr den technologischen Standards von Adobe. Die meisten Funktionen von [!DNL Reports & Analytics] sind in [Analysis Workspace](https://experienceleague.adobe.com/docs/analytics/analyze/analysis-workspace/home.html?lang=de) verfügbar. Seit der Veröffentlichung von Analysis Workspace im Jahr 2015 wurden die Funktionen von [!DNL Reports & Analytics] nach Analysis Workspace verschoben, und es wurde ein Schwellenwert für die Workflow-Parität erreicht. In [dieser Mitteilung](https://spark.adobe.com/page/6WnF8JK6IRDhf/) wird der Ablauf der Produktlebensdauer erläutert. |

{style=&quot;table-layout:auto&quot;}

### AppMeasurement

Die neuesten Aktualisierungen zu AppMeasurement-Versionen (Version 2.22.4) finden Sie in den [Versionshinweisen zu AppMeasurement für JavaScript](https://experienceleague.adobe.com/docs/analytics/implementation/appmeasurement-updates.html?lang=de).

