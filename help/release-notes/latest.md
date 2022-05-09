---
title: Neueste Analytics-Versionshinweise
description: Hier finden Sie die aktuellen Versionshinweise zu Adobe Analytics.
feature: Release Notes
exl-id: 97d16d5c-a8b3-48f3-8acb-96033cc691dc
source-git-commit: 43869c683ca30c94157c6822b53f02a917f6e3ff
workflow-type: tm+mt
source-wordcount: '1170'
ht-degree: 95%

---

# Aktuelle Adobe Analytics-Versionshinweise (April 2022)

**Letzte Aktualisierung**: 9. Mai 2022

## Verwandte Ressourcen

* [Frühere Versionshinweise für 2022](/help/release-notes/2022.md)
* [Versionshinweise zu Customer Journey Analytics](https://experienceleague.adobe.com/docs/analytics-platform/using/releases/latest.html?lang=de)
* [Versionshinweise zu Media Analytics](https://experienceleague.adobe.com/docs/media-analytics/using/additional-resources/release-notes.html?lang=de)
* Die neuesten Versions-Updates für [Adobe Experience Cloud-Produkte](https://business.adobe.com/de/products/adobe-experience-cloud-products.html)

## Neue Funktionen in Adobe Analytics

| Funktion | Beschreibung | [Zieldatum](releases.md) |
| ----------- | ---------- | ------- |
| Aktualisierungen der Landingpage von Adobe Analytics | Aktualisierungen der gemeinsamen Landingpage für Analysis Workspace/Reports &amp; Analytics, die die Benutzerfreundlichkeit verbessern und die Navigation vereinfachen. [Weitere Informationen](/help/analyze/landing.md) | 20. April 2022 |
| Analysis Workspace-Bedienfeld [!UICONTROL Nächstes Element] oder [!UICONTROL Vorheriges Element] | Das Bedienfeld [!UICONTROL Nächstes oder vorheriges Element] ermöglicht es Ihnen, Elemente zu untersuchen, die einem von Ihnen ausgewählten Dimensionselement folgen oder vorausgehen. Sie können es beispielsweise verwenden, wenn Sie die nächsten oder vorherigen Seiten zu einer bestimmten Produktseite, einem Marketing-Kanal oder sogar einem Gerätetyp anzeigen möchten. Dieses Bedienfeld geht über die alte nächste/vorherige Berichterstellung hinaus, da es Ihnen ermöglicht, eine beliebige Dimension anzuzeigen, wobei keine neue Implementierung erforderlich ist, um Einblicke zu erhalten. [Weitere Informationen](/help/analyze/analysis-workspace/c-panels/next-previous.md) | 20. April 2022 |
| Analysis Workspace-Bedienfeld [!UICONTROL Seitenzusammenfassung] | Das Bedienfeld [!UICONTROL Seitenzusammenfassung] bietet eine umfassende Analyse für eine von Ihnen ausgewählte Seite. Es enthält dieselben Details wie der Bericht [!UICONTROL Seitenzusammenfassung] im alten Reports &amp; Analytics-Tool sowie viele weitere Informationen. [Weitere Informationen](/help/analyze/analysis-workspace/c-panels/page-summary.md) | 20. April 2022 |
| Erfordernis der `x-proxy-global-company-id`-Kopfzeile für 2.0-API-Aufrufe entfällt | Die Adobe Analytics 2.0-APIs erfordern jetzt nicht mehr die `x-proxy-global-company-id`-Kopfzeile, da diese Informationen Teil der Endpunkt-URL sind. Sie können diese Kopfzeile nach wie vor einbeziehen, erhalten jedoch keinen Fehler mehr, wenn sie fehlt. | 20. April 2022 |

{style=&quot;table-layout:auto&quot;}

## Fehlerbehebungen in Adobe Analytics

* Es wurde ein Problem bei Daten-Feeds behoben, bei dem das Start- und Enddatum nach dem Speichern des Daten-Feeds beim Erstellen über die Daten-Feed-Benutzeroberfläche automatisch geändert wurden. Das Datum wurde um 1 Tag aktualisiert. (AN-281262)
* Fehlerkorrektur – Die Verlängerung von terminierten Projekten kann jetzt über einen E-Mail-Link durchgeführt werden. (AN-283622)
* Es wurde ein Fehler behoben, der dazu führte, dass aktuelle Versionen von Apple Safari und Microsoft Edge in der Adobe-Suchtabelle des Browser-Typs nicht korrekt identifiziert wurden. Ähnlich wie beim [Aktualisieren von Browser-Versionen](/help/components/dimensions/browser.md) werden bei Aktualisierungen der Suchtabellen des Browser-Typs nur Daten korrigiert, die in Zukunft berücksichtigt werden. Die Suchtabellen für die Browser-Version wurden am 20. April aktualisiert und die Suchtabellen für den Browser-Typ am 28. April. (AN-284872; AN-285753; AN-286257)

### Weitere Fehlerbehebungen in Adobe Analytics

AN-274486; AN-279258; AN-279995; AN-280918; AN-281423; AN-282084; AN-282435; AN-283508; AN-283517; AN-283706; AN-283762; AN-283921; AN-284195; AN-284663; AN-284573; AN-284721; AN-284790; AN-284867; AN-284870; AN-284872; AN-284884; AN-284914; AN-284930; AN-284933; AN-284967; AN-284970; AN-285187; AN-285328; AN-285337; AN-285375; AN-285447; AN-285724; AN-285753; AN-285761

## Wichtige Hinweise für Adobe Analytics-Administratoren

| Hinweis | Hinzugefügt oder aktualisiert am | Beschreibung |
| ----------- | ---------- | ---------- |
| **SFTP-Upgrade** | 9. Mai 2022 | Zuvor hatten wir mitgeteilt, dass die Adobe im Mai 2022 ihre Secure File Transfer Protocol (SFTP)-Dienste aktualisieren würde, um die Sicherheit für die Dateiübertragung zu verbessern. Wir haben diese Aktualisierung auf den Sommer 2022 verschoben. When this change takes place, certain SFTP client configurations will no longer be supported. Dies wirkt sich nur auf Daten aus, die per SFTP an Adobe Analytics gesendet oder von Adobe Analytics abgerufen werden. Das FTP-Protokoll ist nicht betroffen. Um Service-Unterbrechungen zu vermeiden, stellen Sie bitte sicher, dass Ihre SFTP-Clients (Code, Tools, Services) die [hier](https://experienceleague.adobe.com/docs/analytics/export/ftp-and-sftp/secure-file-transfer-protocol/sftp-upgrade.html?lang=de) beschriebenen Anforderungen erfüllen. |
| **Berechtigung für geräteübergreifende Analyse (CDA)** | 13. April 2022 | Mit Wirkung vom **1. Mai 2022** wird jede neue Implementierung von [CDA](/help/components/cda/overview.md) auf maximal drei Report Suite IDs (RSIDs) pro Kunde beschränkt. |
| **Geänderte Verarbeitung von über Experience Edge erfassten A4T-Daten durch Adobe Analytics** | 31. März 2022 | Am 7. März 2022 wurde in Analytics die Art und Weise der Behandlung einiger von Experience Edge kommender Aufrufe geändert, die Target-Inhalte für die Berichterstellung von Analytics for Target (A4T) enthalten. Seit dem 7. März werden alle Treffer mit A4T-Berichtsinhalten so geändert, dass sie nicht als Seitenansichts- oder Link-Ereignisse gezählt werden. Seit dem **31. März 2022** ist die Logik selektiver, sodass die standardmäßigen Seitenansichts- und Klickereignisse nicht geändert werden. Künftig werden nur noch reine Personalisierungsaufrufe geändert, die nur A4T-Inhalte aufweisen. |
| **Aktualisierung der Browser-Verschlüsselungsmethoden für bestimmte Kunden** | 28. März 2022 | Adobe bietet zwei Chiffrier-Sicherheitsstufen an, die den unterschiedlichen Sicherheitsanforderungen bei der Erfassung von First-Party-Daten gerecht werden. Am **23. Juni 2022** entfernen wir die Unterstützung für bestimmte HTTPS-Verschlüsselungsalgorithmen, so genannte Chiffren, für Kunden, deren Sicherheitsstufe auf „Hoch“ eingestellt ist. Dies bedeutet, dass einige ältere Betriebssysteme dann keine Daten mehr an Analytics senden können, da sie keine modernen Verschlüsselungsmethoden unterstützen. Kunden, die die standardmäßigen Chiffrier-Sicherheitseinstellungen „Standard“ verwenden, sind davon nicht betroffen. Alle Kunden, die derzeit die Einstellung „Hoch“ verwenden, wurden bereits direkt kontaktiert. Eine detaillierte Liste der von dieser Änderung betroffenen Chiffren finden Sie hier. |
| **Pausieren älterer terminierter Berichte** | 12. April 2022 | Ab **20. April 2022** pausiert Adobe alle terminierten Berichte, deren Erstellungsdatum mehr als zwei Jahre zurückliegt (erstellt vor dem 31. Januar 2020). Es werden keine Berichte oder Daten gelöscht. Nur Berichte, die älter als zwei Jahre sind, werden pausiert. In diesem Fall werden keine weiteren terminierten Berichte gesendet. Weitere Informationen |
| **Aktualisierungen der ISO-Region 2022** | 11. März 2021 | Adobe plant, am **10. Juni 2022** Aktualisierungen für die ISO-Region für 2022 durchzuführen. Nach diesem Release erfolgen kleinere Aktualisierungen zu Geodaten. |
| **Pausieren älterer terminierter Report Builder-Aufgaben** | 12. April 2022 | Ab **20. April 2022** pausiert Adobe alle terminierten Report Builder-Aufgaben, die vor mehr als zwei Jahren erstellt wurden. Diese Pausierung gilt insbesondere für alle Aufgaben, die vor dem 31. Januar 2020 erstellt wurden. Es werden keine Aufgaben, Arbeitsmappen oder Daten gelöscht. Aufgaben, die älter als zwei Jahre sind, werden jedoch pausiert, und es werden keine weiteren terminierten Aufgaben gesendet. Weitere Informationen |
| **Ablauf der Zulassungslisten-Verlängerung für das Ende der Nutzungsdauer für veraltete Analytics-OAuth-/JWT-Integrationen** | 14. Januar 2022 | Am **25. Mai 2022** läuft die Erweiterung der Zulassungsliste für [Analytics 1.3 API, 1.4 SOAP API und Legacy Analytics OAuth/JWT EOL](https://github.com/AdobeDocs/analytics-1.4-apis/blob/master/docs/APIEOL.md) ab. Sie wurde angeboten, um Kunden, die noch die veralteten OAuth/JWT-Anmeldeinformationen für [!DNL Adobe Analytics] verwenden, zusätzliche Zeit für die Migration ihrer Client-Integrationen auf die [Adobe IMS-Anmeldeinformationen](https://developer.adobe.com/console) zu geben. Dieser Gültigkeitsablauf betrifft (ist jedoch nicht auf beschränkt auf) Kunden von [!DNL Adobe Analytics Livestream] und [!DNL Adobe Campaign], die die erforderlichen IMS-Migrationen nicht abgeschlossen haben. Kunden, die derzeit veraltete [!DNL Analytics] OAuth/JWT-Anmeldeinformationen über die Erweiterung der Zulassungsliste verwenden und die Migration zu IMS-Anmeldeinformationen nicht bis zum 25. Mai 2022 abschließen, verlieren den Zugriff auf Adobe-Services. Livestream-Kunden können im Hinblick auf die Umstellung ihrer Client-Programme auf IMS-Anmeldeinformationen diese [Anweisungen](https://github.com/AdobeDocs/analytics-1.4-apis/blob/master/docs/live-stream-api/getting_started.md) zurate ziehen. [!DNL Campaign]-Kunden können sich zwecks Upgrade auf die neueste Version von [!DNL Campaign] an ihr Adobe-Account-Team wenden. |
| **EOL für [!DNL Reports & Analytics]** | 4. Januar 2022 | Adobe beabsichtigt, [!DNL Reports & Analytics] und die zugehörigen Berichte und Funktionen zum **31. Dezember 2023** einzustellen. Die Berichte, Visualisierungen und zugrunde liegenden Technologien von [!DNL Reports & Analytics] entsprechen nicht mehr den technologischen Standards von Adobe. Die meisten Funktionen von [!DNL Reports & Analytics] sind in [Analysis Workspace](https://experienceleague.adobe.com/docs/analytics/analyze/analysis-workspace/home.html?lang=de) verfügbar. Seit der Veröffentlichung von Analysis Workspace im Jahr 2015 wurden die Funktionen von [!DNL Reports & Analytics] nach Analysis Workspace verschoben, und es wurde ein Schwellenwert für die Workflow-Parität erreicht. In [dieser Mitteilung](https://spark.adobe.com/page/6WnF8JK6IRDhf/) wird der Ablauf der Produktlebensdauer erläutert. |

{style=&quot;table-layout:auto&quot;}

## AppMeasurement {#appm}

Die neuesten Aktualisierungen zu AppMeasurement-Versionen (Version 2.22.4) finden Sie in den [Versionshinweisen zu AppMeasurement für JavaScript](https://experienceleague.adobe.com/docs/analytics/implementation/appmeasurement-updates.html?lang=de).

>[!MORELIKETHIS]
>[[!DNL Customer Journey Analytics] Versionshinweise](https://experienceleague.adobe.com/docs/analytics-platform/using/releases/latest.html?lang=de)
