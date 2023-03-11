---
title: Neueste Analytics-Versionshinweise
description: Hier finden Sie die aktuellen Versionshinweise zu Adobe Analytics.
feature: Release Notes
exl-id: 97d16d5c-a8b3-48f3-8acb-96033cc691dc
source-git-commit: 5739b9bd20d63c51343127832778c4c3836993b3
workflow-type: tm+mt
source-wordcount: '1208'
ht-degree: 50%

---

# Aktuelle Adobe Analytics-Versionshinweise (März 2023)

**Zuletzt aktualisiert**: 10. März 2023

Die Versionen von Adobe Analytics basieren auf einem [kontinuierlichen Bereitstellungsmodell](releases.md), das eine besser skalierbare, schrittweise Implementierung von Funktionen ermöglicht. Dementsprechend werden diese Versionshinweise mehrmals im Monat aktualisiert. Bitte überprüfen Sie sie regelmäßig.

## Neue oder aktualisierte Funktionen in Adobe Analytics {#features}

| Funktion | Beschreibung | [Rollout-Beginn](releases.md) | [Allgemeine Verfügbarkeit](releases.md) |
| ----------- | ---------- | ------- | ---- |
| **Datenwörterbuch in Analysis Workspace** | Das Datenwörterbuch hilft Benutzern und Administratoren, die Komponenten (Dimensionen, Metriken) in ihrer Analytics-Umgebung zu verfolgen, zu verwalten und besser zu verstehen. [Weitere Informationen](/help/analyze/analysis-workspace/components/data-dictionary/data-dictionary-overview.md) | 15. März 2023 | 22. März 2023 |
| **Datenmeldungen in mobilen Dashboards** | Mit Datengeschichten können Sie mehrere anpassbare Detailansichten zu Kacheln in mobilen Scorecard-Projekten hinzufügen. Verwenden Sie Datengeschichten, um tiefer in wichtige Treiber, zugehörige Metriken und verschiedene Schritte entlang der Journey zu tauchen. Sie können diese Ansichten einfach durchwischen, um die gesamte Geschichte hinter Ihren Schlüsselmetriken zu verstehen. [Weitere Informationen](/help/analyze/mobile-app/create-scorecard.md#create-data-story) | Nicht angegeben | 8. März 2023 |
| **Ablaufdaten für geplante Projekte** | Sie können die maximalen Ablaufdaten für geplante Projekte auf bis zu ein Jahr festlegen, unabhängig von der Häufigkeit des Zeitplans. | Nicht angegeben | 8. März 2023 |
| **Linkfreigabe für Projekte (keine Anmeldung erforderlich)** - Nur privaten Beta-Zugriff | <p>Sie können jetzt schreibgeschützte Links zu Analysis Workspace-Projekten für Personen freigeben, die keinen Zugriff auf Adobe Analytics haben. Sie können Projektlinks für Personen außerhalb Ihres Unternehmens oder für Personen in Ihrem Unternehmen freigeben, die nicht für Adobe Analytics bereitgestellt sind. [Weitere Informationen](/help/analyze/analysis-workspace/curate-share/share-projects.md)</p> <p>Wenden Sie sich an Ihr Adobe Account Team, um an die private Betaversion teilzunehmen.</p> | 15. März 2023 (private Beta-Version) | April 2023 |
| **Aktualisierungen des Datumsbereichs des Bedienfelds** | In Workspace wurden die folgenden Verbesserungen hinzugefügt:<ul><li>Ab der Februar-Version basieren Dimensionselemente und Datenvorschauen auf dem Datumsbereich des Bedienfelds und nicht auf den letzten 90 Tagen. </li><li>Alle aufgelisteten Dimensionselemente basieren auf Daten innerhalb des Datumsbereichs des Bedienfelds. Wenn ein Dimensionselement Daten außerhalb des Datumsbereichs enthält, können Sie zusätzliche Daten über den Datumsbereich hinaus am unteren Rand der Liste anzeigen.</li><li>Dimensionen ohne Daten können in der linken Leiste angezeigt werden. Klicken Sie auf die Optionen Weitere Optionen anzeigen , um Dimensionselemente mit Daten außerhalb des Datumsbereichs des Bedienfelds anzuzeigen.</li><li>Die Datenvorschau im Segment und die Generator für berechnete Metriken basieren auf dem Datumsbereich des Bedienfelds, es sei denn, der Zugriff erfolgt über die Komponentenmanager, die kein Bedienfeld haben und weiterhin auf den letzten 90 Tagen basieren.</li><li>Datenvorschau zeigt Daten oder Komponenten basierend auf dem Datumsbereich des Bedienfelds an.</li></ul> | Nicht angegeben | 8. Februar 2023 |

## Fehlerbehebungen in Adobe Analytics 

AN-308177; AN-308727; AN-308846; AN-309591; AN-310614; AN-311544; AN-311570; AN-311665; AN-311948 AN-312108 AN-312114; AN-312142; AN-312143; AN-312389; AN-312391; AN-312431; AN-312453; AN-312454 AN-312458 AN-312503 AN-312533; AN-312682; AN-312698; AN-312714; AN-312738; AN-312807 AN-312829; AN-312849; AN-312875; AN-312980; AN-312997 AN-313059; AN-313077; AN-313110; AN-313195; AN-313196 AN-313258; AN-313554; AN-313580; AN-313702; AN-313820; AN-313844; AN-313859; AN-313879; AN-314273

## Wichtige Hinweise für Adobe Analytics-Administratoren {#admin}

| Hinweis | Hinzugefügt  oder aktualisiert am | Beschreibung |
| ----------- | ---------- | ---------- |
| **Aktualisierung der Gerätesuche aufgrund von Google-Client-Hinweisen** | 27. Februar 2023 | Die Verwendung von Client-Hinweisen, die für den 16. Februar 2023 geplant sind, wurde verschoben, um die Qualität der Gerätesuche mithilfe von Hinweisen besser sicherzustellen. Wir haben am 27. Februar 2023 die erste Phase der Veröffentlichung zur Unterstützung von Client Hints durchgeführt. Die zweite und letzte Phase der Veröffentlichung wurde am Donnerstag, 2. März 2023 abgeschlossen. [Weitere Informationen](/help/technotes/client-hints.md) |
| **Verfügbarkeit von Analytics Source Connector** | 15. Februar 2023 | Am 28. Februar 2023 wurde der Analytics Source Connector im neuen Adobe Experience Platform-Rechenzentrum in Kanada zur Verfügung gestellt. |
| **Automatische Migration zur Klassifizierungssatzarchitektur** | 8. Februar 2023 | In den nächsten Monaten plant Adobe, alle Klassifizierungen organisationsübergreifend auf die neueste Klassifizierungsarchitektur zu migrieren. Die letzten Kundinnen und Kunden werden schätzungsweise im Mai 2023 migriert. Es ist keine Kundenaktion erforderlich, und es wird keine Ausfallzeit erwartet. Diese neue Architektur bietet viele Vorteile, darunter:<ul><li>deutlich verkürzte Verarbeitungszeit (72 Stunden → 24 Stunden)</li><li>die Möglichkeit, die Benutzeroberfläche für [Klassifizierungssätze](/help/components/classifications/sets/overview.md) zu verwenden</li><li>die Option, Klassifizierungsdaten in Adobe Experience Platform künftig über den [Adobe Analytics-Source-Connector für Klassifizierungsdaten](https://experienceleague.adobe.com/docs/experience-platform/sources/connectors/adobe-applications/classifications.html?lang=de) zu verwenden</li></ul>Beachten Sie die folgenden Änderungen, die sich möglicherweise auf den Workflow Ihrer Organisation auswirken können:<ul><li>Bei Verwendung des Browser- oder FTP-Imports ist „[!UICONTROL Bei Konflikt überschreiben]“ immer aktiviert.</li><li>Bei Verwendung des Browser- oder FTP-Imports wird die Option zum sofortigen Export nach dem Import nicht mehr unterstützt.</li><li>Der `GetDimensions`-Endpunkt der Analytics 2.0-API gibt jetzt Zeichenfolgenkennungen für Klassifizierungen anstelle numerischer Kennungen zurück. Numerische Kennungen können zwar weiterhin verwendet werden, Adobe empfiehlt jedoch, nach Möglichkeit die neuen Zeichenfolgenkennungen zu verwenden. Numerische Kennungen können mithilfe des Abfragezeichenfolgen-Parameters `?expansion=hidden` abgerufen werden.</li></ul>Wenden Sie sich an die Kundenunterstützung von Adobe, wenn Sie einen spezifischeren Migrationsplan für Ihre Organisation wünschen oder Fragen/Bedenken zu dieser Migration haben. [Weitere Informationen](/help/components/classifications/sets/overview.md) |

{style="table-layout:auto"}

## Mitteilungen über das Ende der Nutzungsdauer (EOL) {#eol}

| Ende der Nutzungsdauer eines Produkts oder einer Funktion | Datum hinzugefügt oder aktualisiert | Beschreibung |
| --- | --- | --- |
| **EOL für [!DNL Reports & Analytics]** | 7. März 2023 | Adobe beabsichtigt, [!DNL Reports & Analytics] und die zugehörigen Berichte und Funktionen zum **31. Dezember 2023** einzustellen. Die Berichte, Visualisierungen und zugrunde liegenden Technologien, die [!DNL Reports & Analytics] unterstützen, entsprechen nicht mehr den technologischen Standards von Adobe. Die meisten Funktionen von [!DNL Reports & Analytics] sind in [Analysis Workspace](https://experienceleague.adobe.com/docs/analytics/analyze/analysis-workspace/home.html?lang=de) verfügbar. Seit der Veröffentlichung von Analysis Workspace im Jahr 2015 wurden die Funktionen von [!DNL Reports & Analytics] nach Analysis Workspace verschoben, und es wurde ein Schwellenwert für die Workflow-Parität erreicht. In [dieser Mitteilung](https://spark.adobe.com/page/6WnF8JK6IRDhf/) wird der Ablauf der Produktlebensdauer erläutert.<p>Am 31. Dezember 2023 werden wir viele der damit verbundenen Reports &amp; Analytics-Funktionen einstellen, darunter, aber nicht beschränkt auf: Terminierte Berichte, Datenextraktionen und DL-Berichte. Nach dem 31. Dezember 2023 werden terminierte Berichte nicht mehr gesendet. In **April 2023** werden alle Berichte, die nach dem 31. Dezember 2023 ablaufen sollten, automatisch aktualisiert und auf den 31. Dezember 2023 zurückgesetzt. Darüber hinaus können Sie nach dem 31. Dezember 2023 keine zukünftigen Berichte mehr planen. |
| **Ende [!UICONTROL Personen] Metrik** | 9. März 2023 | Mit der Einstellung der [[!DNL Device Co-op]](https://experienceleague.adobe.com/docs/discontinued/using/device-co-op.html), ist die Metrik Personen, die sich auf die Device Co-op bezieht, nicht mehr relevant. Am 8. Mai 2023 werden wir die [!UICONTROL Personen] Metrik. An diesem Punkt werden wir seine Daten an die [!UICONTROL Unique Visitor] -Metrik, um zu verhindern, dass Projekte, Segmente und berechnete Metriken beschädigt werden.<p>**Hinweis**: Die [[!UICONTROL Personen] Metrik, die mit der geräteübergreifenden Analyse verknüpft ist](/help/components/metrics/people.md) von dieser Ankündigung nicht betroffen ist. |
| **EOL für die [!UICONTROL Veröffentlichungslisten]-Funktion** | 29. September 2022 | Als Teil der EOL von Reports &amp; Analytics [!UICONTROL Veröffentlichungslisten] werden so eingestellt, dass sie das Ende der Lebensdauer in **Dezember 2023**. Sie können keine neuen erstellen oder auf vorhandene zugreifen [!UICONTROL Veröffentlichungslisten] zum Senden oder Planen [!UICONTROL Analysis Workspace] Projekte. |
| **EOL für Data Workbench** | 14. September 2022 | Adobe beabsichtigt, Data Workbench ab **31. Dezember 2023** einzustellen. Weitere Informationen finden Sie in der [Mitteilung zum Ende der Nutzungsdauer von Data Workbench](https://experienceleague.adobe.com/docs/data-workbench/using/eol.html?lang=de). Wenden Sie sich bei Fragen an den für Ihre Organisation zuständigen Adobe-Kundenbetreuer. |
| **EOL für [!DNL Reports & Analytics]** | 4. Januar 2022 | Adobe beabsichtigt, [!DNL Reports & Analytics] und die zugehörigen Berichte und Funktionen zum **31. Dezember 2023** einzustellen. Die Berichte, Visualisierungen und zugrunde liegenden Technologien, die [!DNL Reports & Analytics] unterstützen, entsprechen nicht mehr den technologischen Standards von Adobe. Die meisten Funktionen von [!DNL Reports & Analytics] sind in [Analysis Workspace](https://experienceleague.adobe.com/docs/analytics/analyze/analysis-workspace/home.html?lang=de) verfügbar. Seit der Veröffentlichung von Analysis Workspace im Jahr 2015 wurden die Funktionen von [!DNL Reports & Analytics] nach Analysis Workspace verschoben, und es wurde ein Schwellenwert für die Workflow-Parität erreicht. In [dieser Mitteilung](https://spark.adobe.com/page/6WnF8JK6IRDhf/) wird der Ablauf der Produktlebensdauer erläutert. |

{style="table-layout:auto"}

## AppMeasurement

Die neuesten Aktualisierungen zu AppMeasurement-Versionen (Version 2.23.0) finden Sie in den [Versionshinweisen zu AppMeasurement für JavaScript](https://experienceleague.adobe.com/docs/analytics/implementation/appmeasurement-updates.html?lang=de).


## Verwandte Ressourcen

* [Frühere Versionshinweise für 2022](/help/release-notes/2022.md)
* [Versionshinweise zu Customer Journey Analytics](https://experienceleague.adobe.com/docs/analytics-platform/using/releases/latest.html?lang=de)
* [Versionshinweise zu Media Analytics](https://experienceleague.adobe.com/docs/media-analytics/using/additional-resources/release-notes.html?lang=de)
* Die neuesten Versions-Updates für [Adobe Experience Cloud-Produkte](https://business.adobe.com/de/products/adobe-experience-cloud-products.html)
