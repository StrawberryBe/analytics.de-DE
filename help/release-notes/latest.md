---
title: Aktuelle Adobe Analytics-Versionshinweise
description: Aktuelle Versionshinweise zu Adobe Analytics anzeigen
feature: Release Notes
exl-id: 97d16d5c-a8b3-48f3-8acb-96033cc691dc
source-git-commit: 00c6915275c4730413aa8505094886ae56649ec4
workflow-type: tm+mt
source-wordcount: '1167'
ht-degree: 98%

---

# Aktuelle Adobe Analytics-Versionshinweise (Oktober/November 2023)

**Letztes Update**: Donnerstag, 13. Dezember 2023

Diese Versionshinweise beziehen sich auf den Veröffentlichungszeitraum vom 23. Oktober 2023 bis Ende November 2023. Die Versionen von Adobe Analytics basieren auf einem [kontinuierlichen Bereitstellungsmodell](releases.md), das eine besser skalierbare, schrittweise Implementierung von Funktionen ermöglicht. Dementsprechend werden diese Versionshinweise mehrmals im Monat aktualisiert. Bitte überprüfen Sie sie regelmäßig.

## Neue Funktionen oder Verbesserungen {#features}

| Funktion | Beschreibung | [Rollout-Beginn](releases.md) | [Allgemeine Verfügbarkeit](releases.md) |
| ----------- | ---------- | ------- | ---- |
| **Verbesserungen für Reporting Activity Manager** | Reporting Activity Manager zeigt die Berichtskapazität für jede Report Suite in Ihrer Organisation an.  Er bietet Admins detaillierte Einblicke in die Berichtsnutzung und hilft ihnen, Kapazitätsprobleme bei Spitzen während der Berichterstellung mühelos zu diagnostizieren und zu beheben. Im Folgenden finden Sie einige der Verbesserungen, die jetzt in Reporting Activity Manager verfügbar sind: <ul><li>Admins können nicht nur aktuelle Anfragen abbrechen, sondern auch Anfragen für einen bestimmten Zeitraum einschränken. Admins können Anfragen nach Anfrage, Projekt oder Benutzerin bzw. Benutzer einschränken.</li><li>Zusätzlich zu den Metriken „Nutzung“ und „Kapazität“ enthält Reporting Activity Manager jetzt weitere Daten zur Berichtsaktivität: die Spalten „Komplexität“, „Benutzerin bzw. Benutzer“ und „Verbindung“.</li><li>Alle Abbrüche und Einschränkungen, die in Reporting Activity Manager vorgenommen wurden, sind jetzt im Administratorprotokoll sichtbar. Admins können das Administratorprotokoll verwenden, um anzuzeigen, was derzeit abgebrochen wird. Abbrüche können in Reporting Activity Manager oder im Administratorprotokoll nicht rückgängig gemacht werden.</li></ul><p>Weitere Informationen finden Sie unter [Reporting Activity Manager – Übersicht](/help/admin/admin/reporting-activity-manager/reporting-activity-overview.md)</p> | 17. Oktober 2023 | 24. Oktober 2023 |
| **Verbesserungen bei Data Warehouse** | Beim Erstellen einer Data Warehouse-Anfrage können Sie jetzt ein Cloud-Konto für die Verwendung als Berichtsziel konfigurieren. Die folgenden Cloud-Kontotypen sind für das Senden von Daten verfügbar:<ul><li>Amazon S3</li><li>Google Cloud Platform</li><li>Azure SAS</li><li>Azure RBAC</li><li>E-Mail (diese Option war zuvor bereits verfügbar)</li></ul>FTP, SFTP, Azure Blob und S3 sind weiterhin als Berichtsziele verfügbar, werden aber nicht mehr empfohlen.<p>Das Benutzererlebnis beim Erstellen und Verwalten von Data Warehouse-Anfragen wurde ebenfalls verbessert. Weitere Informationen finden Sie unter [Erstellen einer Data Warehouse-Anfrage](/help/export/data-warehouse/create-request/t-dw-create-request.md) und [Verwalten von Data Warehouse-Anfragen](https://experienceleague.adobe.com/docs/analytics/export/data-warehouse/data-warehouse-requests-manage.html?lang=de). | 12. September 2023 | TBD |

{style="table-layout:auto"}

## Fehlerbehebungen in Adobe Analytics

* Diese Änderungen an der Verarbeitungs- und Berichterstellungs-Engine von Analytics werden in der letzten Oktoberwoche bereitgestellt: Wir werden ein Problem beheben, bei dem die Beschriftungen für die Seiten- oder Link-Dimensionen fälschlicherweise als `Unknown` angezeigt wurden. Vor der Korrektur wurden die `Unknown`-Beschriftungen möglicherweise falsch angezeigt, wenn ein Seitenname oder Link-Name bei einem Treffer nicht übergeben wurde. Die Standardeinstellung ist [!UICONTROL Seiten-URL] bzw. [!UICONTROL Link-URL]. Diese Dimensionen wurden so konfiguriert, dass nicht zwischen Groß- und Kleinschreibung unterschieden wird. Mit dieser Fehlerbehebung werden Berichte in Zukunft korrekt sein. Bei Berichten zu historischen Daten sind einige Berichtsergebnisse jedoch möglicherweise noch fälschlicherweise als `Unknown` beschriftet. (AN-328030)

### Weitere Fehlerbehebungen

AN-315676; AN-323398; AN-326209; AN-328178; AN-328261; AN-328395; AN-328671; AN-329282; AN-329330; AN-329355; AN-329506; AN-329516; AN-329738; AN-329769; AN-329771; AN-329816; AN-329877; AN-329928; AN-329957; AN-329962; AN-329966; AN-330023; AN-330081; AN-330083; AN-330105; AN-330138; AN-330140; AN-330165; AN-330241; AN-330359; AN-330366; AN-330427; AN-330438; AN-330442; AN-330534; AN-330616; AN-330654; AN-330783; AN-330879; AN-330881; AN-330883; AN-330887; AN-330888; AN-330955; AN-330979; AN-331031; AN-331053; AN-331068; AN-331071; AN-331074; AN-331075; AN-331076; AN-331078; AN-331085; AN-331093; AN-331167; AN-331171; AN-331181; AN-331196; AN-331226; AN-331258; AN-331260; AN-331279; AN-331286; AN-331290; AN-331365; AN-331375; AN-331376; AN-331454; AN-331519; AN-331570; AN-331590; AN-331593; AN-331603; AN-331751; AN-331816; AN-331897; AN-331900; AN-331906; AN-331926; AN-331929; AN-332031; AN-332067; AN-332101; AN-332114; AN-332156; AN-332201; AN-332225; AN-332253; AN-332277; AN-332361; AN-332370; AN-332386

## Wichtige Hinweise für Adobe Analytics-Administratoren {#admin}

| Hinweis | Datum hinzugefügt oder aktualisiert | Beschreibung |
| ----------- | ---------- | ---------- |
| **Vollständige IP-Verschleierung für Adobe Experience Edge-Treffer** | 27. September 2023 | Die IP-Verschleierung für Treffer aus Experience Edge wird Ende Oktober 2023 aktualisiert. Im April 2023 wurde bei Experience Edge die Möglichkeit hinzugefügt, IP-Adressen zu verschleiern. Damals unterstützte Adobe Analytics nur eine partielle Verschleierung von IPs, aufgrund der Art, wie Analytics Treffer aus Experience Edge verarbeitet. Auch wenn Kundinnen und Kunden die vollständige Verschleierung für Experience Edge ausgewählt haben, erhielt Analytics nur teilweise verschleierte IPs. Wenn diese Änderung implementiert ist, erhält Analytics die vollständig verschleierte IP. |
| **Adobe Analytics-Livestream – Analytics 2.0-APIs** | 27. September 2023 | Kundinnen und Kunden können jetzt auf den [Endpunkt-Leitfaden für den Adobe Analytics-Livestream](https://developer.adobe.com/analytics-apis/docs/2.0/guides/endpoints/livestream/) zugreifen, der bei den Adobe Analytics 2.0-APIs und nicht mehr bei den 1.4-APIs zu finden ist. Kundinnen und Kunden, die Anmeldeinformationen von Adobe I/O JWT verwenden, müssen vor dem 1. Januar 2025 zu Anmeldeinformationen von Adobe I/O OAuth Server-to-Server migrieren. (Einzelheiten dazu finden Sie im Folgenden unter „Mitteilungen über das Ende der Nutzungsdauer (EOL)“.) |

{style="table-layout:auto"}

## Mitteilungen über das Ende der Nutzungsdauer (EOL) {#eol}

| Ende der Nutzungsdauer eines Produkts oder einer Funktion | Datum hinzugefügt oder aktualisiert | Beschreibung |
| --- | --- | --- |
| **EOL für [!DNL Reports & Analytics]** | Donnerstag, 13. Dezember 2023 | Adobe beabsichtigt, [!DNL Reports & Analytics] und die zugehörigen Berichte und Funktionen zum **Donnerstag, 17. Januar 2024** einzustellen. Die Berichte, Visualisierungen und zugrunde liegenden Technologien, die [!DNL Reports & Analytics] unterstützen, entsprechen nicht mehr den technologischen Standards von Adobe. Die meisten Funktionen von [!DNL Reports & Analytics] sind in [Analysis Workspace](https://experienceleague.adobe.com/docs/analytics/analyze/analysis-workspace/home.html?lang=de) verfügbar. Seit der Veröffentlichung von Analysis Workspace im Jahr 2015 wurden die Funktionen von [!DNL Reports & Analytics] nach Analysis Workspace verschoben, und es wurde ein Schwellenwert für die Workflow-Parität erreicht. In [dieser Mitteilung](https://spark.adobe.com/page/6WnF8JK6IRDhf/) wird der Ablauf der Produktlebensdauer erläutert.<p>Am 31. Dezember 2023 werden wir viele der zugehörigen Reports &amp; Analytics-Funktionen einstellen, insbesondere: Terminierte Berichte, Datenextraktionen und DL-Berichte. Nach dem 31. Dezember 2023 werden terminierte Berichte nicht mehr gesendet. Im **April 2023** wurden alle Berichte, die erst nach dem 31. Dezember 2023 ablaufen sollten, automatisch aktualisiert und das Datum auf den 31. Dezember 2023 gesetzt. Darüber hinaus können Sie nach dem 31. Dezember 2023 keine zukünftigen Berichte mehr planen. |
| **EOL für die [!UICONTROL Veröffentlichungslisten]-Funktion** | Donnerstag, 13. Dezember 2023 | Als Teil der EOL von Reports &amp; Analytics [!UICONTROL Veröffentlichungslisten] werden so eingestellt, dass sie das Ende des Lebenszyklus erreichen **17. Januar 2024**. Sie werden keine neuen [!UICONTROL Veröffentlichungslisten] erstellen oder auf bestehende [!UICONTROL Analysis Workspace]-Projekte zugreifen können, um diese zu senden oder zu planen. |
| **Migration auf OAuth Server-zu-Server-Anmeldeinformationen für Adobe I/O** | 11. Mai 2023 | Kundinnen und Kunden von Adobe Analytics-API und Livestream, die JWT-Anmeldeinformationen für Adobe I/O verwenden, müssen bis zum **1. Januar 2025** auf OAuth Server-zu-Server-Anmeldeinformationen für Adobe I/O migrieren. Adobe I/O lässt die Erstellung neuer JWT-Anmeldeinformationen ab dem 1. Mai 2024 nicht mehr zu. Kunden und Kundinnen, die JWT verwenden, müssen neue OAuth Server-zu-Server-Anmeldeinformationen erstellen oder ihre bestehende JWT-Anmeldeinformationen zu OAuth Server-zu-Server-Anmeldeinformationen migrieren. Kunden und Kundinnen müssen außerdem ihre Client-Anwendungen aktualisieren, um die neuen OAuth Server-to-Server-Anmeldeinformationen zu verwenden. <ul><li>[Migration von Dienstkonto-Anmeldeinformationen (JWT)](https://developer.adobe.com/developer-console/docs/guides/authentication/ServerToServerAuthentication/migration/)</li><li>[Implementierungshandbuch für neue und alte Programme mit OAuth](https://developer.adobe.com/developer-console/docs/guides/authentication/ServerToServerAuthentication/implementation/)<li>[Verwenden der neuen OAuth Server-zu-Server-Anmeldeinformationen](https://developer.adobe.com/developer-console/docs/guides/authentication/ServerToServerAuthentication/implementation/)</li><li>[Häufig gestellte Fragen (FAQ)](https://developer.adobe.com/developer-console/docs/guides/authentication/ServerToServerAuthentication/faqs/)</li></ul> |
| **EOL für Data Workbench** | 14. September 2022 | Adobe beabsichtigt, Data Workbench ab **31. Dezember 2023** einzustellen. Weitere Informationen finden Sie in der [Mitteilung zum Ende der Nutzungsdauer von Data Workbench](https://experienceleague.adobe.com/docs/data-workbench/using/eol.html?lang=de). Wenden Sie sich bei Fragen an den für Ihre Organisation zuständigen Adobe-Kundenbetreuer. |

{style="table-layout:auto"}

## AppMeasurement

Die neuesten Aktualisierungen zu AppMeasurement-Versionen (Version 2.25.0) finden Sie in den [Versionshinweisen zu AppMeasurement für JavaScript](https://experienceleague.adobe.com/docs/analytics/implementation/appmeasurement-updates.html?lang=de).


## Verwandte Ressourcen

* [Frühere Versionshinweise für 2022](/help/release-notes/2022.md)
* [Versionshinweise zu Customer Journey Analytics](https://experienceleague.adobe.com/docs/analytics-platform/using/releases/latest.html?lang=de)
* [Versionshinweise zu Media Analytics](https://experienceleague.adobe.com/docs/media-analytics/using/additional-resources/release-notes.html?lang=de)
* Die neuesten Versions-Updates für [Adobe Experience Cloud-Produkte](https://business.adobe.com/de/products/adobe-experience-cloud-products.html)
