---
title: Neueste Analytics-Versionshinweise
description: Hier finden Sie die aktuellen Versionshinweise zu Adobe Analytics.
feature: Release Notes
exl-id: 97d16d5c-a8b3-48f3-8acb-96033cc691dc
source-git-commit: 611477ef794464de0b05b45e8445ed8fdd32b154
workflow-type: tm+mt
source-wordcount: '0'
ht-degree: 0%

---

# Aktuelle Adobe Analytics-Versionshinweise (April 2023)

**Letzte Aktualisierung**: 12. April 2023

Die Versionen von Adobe Analytics basieren auf einem [kontinuierlichen Bereitstellungsmodell](releases.md), das eine besser skalierbare, schrittweise Implementierung von Funktionen ermöglicht. Dementsprechend werden diese Versionshinweise mehrmals im Monat aktualisiert. Bitte überprüfen Sie sie regelmäßig.

## Neue oder aktualisierte Funktionen in Adobe Analytics {#features}

| Funktion | Beschreibung | [Rollout-Beginn](releases.md) | [Allgemeine Verfügbarkeit](releases.md) |
| ----------- | ---------- | ------- | ---- |
| **Zeilen-/Spaltenfilter für Analytics-Source-Connector-Streaming** | Der Analytics-Source-Connector in Adobe Experience Platform ermöglicht jetzt das Filtern von Analytics-Daten, mit denen Profile in [Echtzeit-Kundenprofil](https://experienceleague.adobe.com/docs/experience-platform/profile/home.html?lang=de) gefüllt werden. Die Filterung auf Zeilenebene hilft, die Anzahl der mit Profilen verknüpften Ereignisse zu reduzieren. Die Filterung auf Spaltenebene hilft, die Vielfalt der Ereignisse selbst zu reduzieren, und ermöglicht es Ihnen so, die Nutzung von Profilberechtigungen zu optimieren. Diese Filterung gilt nur für Daten, die an das Echtzeit-Kundenprofil und an [Identity Service](https://experienceleague.adobe.com/docs/experience-platform/identity/home.html?lang=de) gesendet werden. **Die Filterung wirkt sich nicht auf die Daten aus, die zur Verwendung in Anwendungen wie Customer Journey Analytics an Data Lake gesendet werden**. [Weitere Informationen](https://experienceleague.adobe.com/docs/experience-platform/sources/ui-tutorials/create/adobe-applications/analytics.html?lang=de#filtering-for-profile) | Nicht angegeben | 29. März 2023 |
| **Teilweise Unterstützung für Activity Map mit Web SDK** | Ab Web SDK-Version 2.15.0 beginnen wir mit dem Ausfüllen von Activity Map-Daten, wenn das Linktracking aktiviert ist. Dies ermöglicht es Web SDK-Benutzern, Activity Map-Berichte zu erhalten, wenn das Linktracking mit dem Web SDK und der in Analytics konfigurierten Activity Map aktiviert ist.<p>Durch die Aktivierung des Linktrackings mit dem Web SDK werden derzeit Linkereignisse gesendet, wenn ein Kunde von einer Seite zur nächsten navigiert. Dies unterscheidet sich von der Funktionsweise von AppMeasurement und kann möglicherweise zu zusätzlichen abrechnungsfähigen Treffern führen, die an Adobe gesendet werden. Weitere Infos [here](https://experienceleague.adobe.com/docs/experience-platform/edge/data-collection/track-links.html?lang=de) und [here](/help/analyze/activity-map/activitymap-getting-started/activitymap-getting-started-admins/activitymap-enable.md) | Nicht angegeben | 31. März 2023 |
| **IP-Verschleierung für Experience Edge** | Experience Edge unterstützt die IP-Verschleierung für Daten, die direkt an Adobe Experience Platform gesendet werden. Dies kommt Kunden zugute, die Daten zur Verwendung in CJA- oder anderen Platform-Lösungen direkt an Platform senden. Die IP-Verschleierung wird auf Datenstream-Ebene konfiguriert. Es unterstützt das Entfernen des letzten Oktetts oder der gesamten IP-Adresse.<p>**Hinweis**: Die Verschleierung gilt NICHT für Daten, die an Adobe Analytics gesendet werden. Analytics erhält weiterhin die vollständige IP-Adresse. Die IP-Verarbeitung erfolgt weiterhin separat in Analytics. In Zukunft planen wir, die Verschleierung von Analytics-Daten an der Edge zuzulassen. | Nicht angegeben | AEP-Version vom 26. April 2023 |
| **Datenwörterbuch in Analysis Workspace** | Das Datenwörterbuch hilft Benutzenden und Admins, die Komponenten (Dimensionen, Metriken) in ihrer Analytics-Umgebung zu verfolgen, zu verwalten und besser zu verstehen. [Weitere Informationen](/help/analyze/analysis-workspace/components/data-dictionary/data-dictionary-overview.md) | 15. März 2023 | 29. März 2023 |
| **Link-Freigabe für Projekte (keine Anmeldung erforderlich)** – Nur privater Beta-Zugriff | <p>Sie können jetzt schreibgeschützte Links zu Analysis Workspace-Projekten für Personen freigeben, die keinen Zugriff auf Adobe Analytics haben. Sie können Projekt-Links für Personen außerhalb Ihrer Organisation oder für Personen innerhalb Ihrer Organisation freigeben, die nicht für Adobe Analytics vorgesehen sind. [Weitere Informationen](/help/analyze/analysis-workspace/curate-share/share-projects.md)</p> <p>Um an der privaten Beta-Version teilzunehmen, wenden Sie sich an Ihr Adobe Account Team.</p> | 26. April 2023 | Juni 2023 |

{style="table-layout:auto"}

## Fehlerbehebungen in Adobe Analytics

* Fehlerkorrektur - Die Lookup-Dateien von Betriebssystem.tsv im Daten-Feed funktionieren jetzt einwandfrei.
* Es wurde ein Problem behoben, durch das sich die Metrikwerte zwischen Reports &amp; Analytics und Workspace unterscheiden (AN-315965).
* Es wurde ein Problem behoben, durch das partielle Classifications nicht importiert werden konnten. (AN-315854)
* Es wurde ein Problem mit der Analytics-API 1.4 behoben. (AN-316475)
* Es wurde ein Fehler behoben, der verhinderte, dass einige Kunden Classifications für die Dimension Seite über Report Builder und Report &amp; Analytics erhalten. (AN-314445)
* Es wurde ein Problem behoben, durch das Warnhinweise nicht übertragen werden konnten. (AN-306457)

### Weitere Fehlerbehebungen

AN-288373; AN-305144; AN-309023; AN-310466; AN-311686; AN-311705; AN-312018; AN-312105 AN-312116; AN-312191; AN-312502; AN-312737; AN-312854; AN-312991; AN-313253; AN-313275; AN-313278; AN-313282; AN-313365; AN-313390; AN-313547; AN-313549; AN-313818; AN-313986; AN-314080; AN-314248; AN-314251; AN-314262; AN-314300; AN-314309; AN-314448; AN-314643; AN-314564; AN-314645; AN-314705; AN-314761; AN-314831; AN-314919; AN-314948; AN-315032; AN-315115; AN-315154; AN-315158; AN-315321; AN-315375; AN-315379; AN-315392; AN-315407; AN-315427; AN-315582; AN-315591; AN-315699; AN-315700; AN-315704; AN-315705; AN-315777; AN-315923; AN-316237; AN-316243; AN-316324; AN-316415; AN-316474; AN-316493; AN-316596; AN-316864;

## Wichtige Hinweise für Adobe Analytics-Administratoren {#admin}

| Hinweis | Hinzugefügt oder aktualisiert am | Beschreibung |
| ----------- | ---------- | ---------- |
| **Gerätesuchvorgänge verwenden jetzt einen Drittanbieter für alle Gerätesuchen.** | 3. März 2023 | Am 2. März 2023 haben wir im Rahmen des Support-Rollouts für Client-Hinweise unsere Gerätesuchvorgänge so aktualisiert, dass für alle Gerätesuchen ein Drittanbieter verwendet wird. Zuvor hatten wir den Drittanbieter nur für die Suche nach Mobilgeräten verwendet. Im Zuge dieses Rollouts wurden einige Desktop-Betriebssysteme fälschlicherweise mit dem Text „Mobile“ gekennzeichnet (z. B. „Mobile OS X 10.15.7“ anstelle von „OS X 10.15.7“).<p>Bei der Adobe-Aprilversion werden wir diese Namen korrigieren. Die Analytics- und CJA-Berichte werden rückwirkend aktualisiert, da die zugehörigen Berichtsfunktionen den Betriebssystemnamen basierend auf einer ID nachschlagen, die als Teil der Ereignisdaten aufgezeichnet wird. Sobald der Suchwert, der einer ID entspricht, aktualisiert wird, werden alle Berichte korrigiert, einschließlich historischer Daten. Für Kunden und -Kundinnen von [!UICONTROL Daten-Feeds] ist die Änderung rückwirkend, wenn zum Berichtszeitpunkt ein ähnlicher Suchvorgang verwendet wird. Wenn Sie den Betriebssystemwert jedoch in Ihren Ereignisdaten speichern, werden nur die Berichte in der Zukunft aktualisiert. Weitere Informationen dazu finden Sie unter [Betriebssystem](/help/components/dimensions/operating-systems.md). |
| **Aktualisierung der Gerätesuche aufgrund von Google-Client-Hinweisen** | 27. Februar 2023 | Die für den 16. Februar 2023 geplante Verwendung von Client-Hinweisen wurde verschoben, um die Qualität der Gerätesuche mithilfe von Hinweisen besser gewährleisten zu können. Die erste Phase der Freigabe für die Unterstützung von Client-Hinweisen wurde am 27. Februar 2023 durchgeführt. Die zweite und letzte Phase der Freigabe wurde am Donnerstag, 2. März 2023 abgeschlossen. [Weitere Informationen](/help/technotes/client-hints.md) |
| **Automatische Migration zur Klassifizierungssatzarchitektur** | 8. Februar 2023 | In den nächsten Monaten plant Adobe, alle Klassifizierungen organisationsübergreifend auf die neueste Klassifizierungsarchitektur zu migrieren. Die letzten Kundinnen und Kunden werden schätzungsweise im Mai 2023 migriert. Es ist keine Kundenaktion erforderlich, und es wird keine Ausfallzeit erwartet. Diese neue Architektur bietet viele Vorteile, darunter:<ul><li>deutlich verkürzte Verarbeitungszeit (72 Stunden → 24 Stunden)</li><li>die Möglichkeit, die Benutzeroberfläche für [Klassifizierungssätze](/help/components/classifications/sets/overview.md) zu verwenden</li><li>die Option, Klassifizierungsdaten in Adobe Experience Platform künftig über den [Adobe Analytics-Source-Connector für Klassifizierungsdaten](https://experienceleague.adobe.com/docs/experience-platform/sources/connectors/adobe-applications/classifications.html?lang=de) zu verwenden</li></ul>Beachten Sie die folgenden Änderungen, die sich möglicherweise auf den Workflow Ihrer Organisation auswirken können:<ul><li>Bei Verwendung des Browser- oder FTP-Imports ist „[!UICONTROL Bei Konflikt überschreiben]“ immer aktiviert.</li><li>Bei Verwendung des Browser- oder FTP-Imports wird die Option zum sofortigen Export nach dem Import nicht mehr unterstützt.</li><li>Der `GetDimensions`-Endpunkt der Analytics 2.0-API gibt jetzt Zeichenfolgenkennungen für Klassifizierungen anstelle numerischer Kennungen zurück. Numerische Kennungen können zwar weiterhin verwendet werden, Adobe empfiehlt jedoch, nach Möglichkeit die neuen Zeichenfolgenkennungen zu verwenden. Numerische Kennungen können mithilfe des Abfragezeichenfolgen-Parameters `?expansion=hidden` abgerufen werden.</li></ul>Wenden Sie sich an die Kundenunterstützung von Adobe, wenn Sie einen spezifischeren Migrationsplan für Ihre Organisation wünschen oder Fragen/Bedenken zu dieser Migration haben. [Weitere Informationen](/help/components/classifications/sets/overview.md) |

{style="table-layout:auto"}

## Mitteilungen über das Ende der Nutzungsdauer (EOL) {#eol}

| Ende der Nutzungsdauer eines Produkts oder einer Funktion | Datum hinzugefügt oder aktualisiert | Beschreibung |
| --- | --- | --- |
| **EOL des japanischen Feature Phone-Tracking-Dienstes** | 21. März 2023 | Nur für unsere japanischen Kunden: Im **Ende Mai 2023**, wird der japanische Feature Phone-Tracking-Dienst (mod_ktrack) eingestellt. Wir entschuldigen uns für die Unannehmlichkeiten, bitten jedoch darum, die auf Ihrem Apache-Server installierten Module zu deinstallieren oder zu deaktivieren. Siehe Seiten 27 und 28 in [diesem Dokument](/help/release-notes/mod_ktrackforSiteCatalyst_ver1.40.pdf).. |
| **EOL für [!DNL Reports & Analytics]** | 7. März 2023 | Adobe beabsichtigt, [!DNL Reports & Analytics] und die zugehörigen Berichte und Funktionen zum **31. Dezember 2023** einzustellen. Die Berichte, Visualisierungen und zugrunde liegenden Technologien, die [!DNL Reports & Analytics] unterstützen, entsprechen nicht mehr den technologischen Standards von Adobe. Die meisten Funktionen von [!DNL Reports & Analytics] sind in [Analysis Workspace](https://experienceleague.adobe.com/docs/analytics/analyze/analysis-workspace/home.html?lang=de) verfügbar. Seit der Veröffentlichung von Analysis Workspace im Jahr 2015 wurden die Funktionen von [!DNL Reports & Analytics] nach Analysis Workspace verschoben, und es wurde ein Schwellenwert für die Workflow-Parität erreicht. In [dieser Mitteilung](https://spark.adobe.com/page/6WnF8JK6IRDhf/) wird der Ablauf der Produktlebensdauer erläutert.<p>Am 31. Dezember 2023 werden wir viele der zugehörigen Reports &amp; Analytics-Funktionen einstellen, insbesondere: Terminierte Berichte, Datenextraktionen und DL-Berichte. Nach dem 31. Dezember 2023 werden terminierte Berichte nicht mehr gesendet. Im **April 2023** werden alle Berichte, die nach dem 31. Dezember 2023 ablaufen sollten, automatisch aktualisiert und auf den 31. Dezember 2023 zurückgesetzt. Darüber hinaus können Sie nach dem 31. Dezember 2023 keine zukünftigen Berichte mehr planen. |
| **Ende der Nutzungsdauer der [!UICONTROL Personen]-Metrik** | 9. März 2023 | Mit der Einstellung der [[!DNL Device Co-op]](https://experienceleague.adobe.com/docs/discontinued/using/device-co-op.html?lang=de) ist die Metrik „Personen“, die sich auf die Gerätekooperation bezieht, nicht mehr relevant. Am 8. Mai 2023 werden wir die Metrik [!UICONTROL Personen] entfernen. An diesem Punkt werden wir diese Daten an die [!UICONTROL Unique Visitor]-Metrik umleiten, um zu verhindern, dass Projekte, Segmente und berechnete Metriken beschädigt werden.<p>**Hinweis**: Die [[!UICONTROL Personen]-Metrik, die mit der geräteübergreifenden Analyse verknüpft ist](/help/components/metrics/people.md), ist von dieser Ankündigung nicht betroffen. |
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
