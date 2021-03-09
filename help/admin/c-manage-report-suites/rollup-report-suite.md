---
description: Beschreibungen der Report Suite-Typen und Vergleich globaler Report Suites und Datenaggregations-Report Suites.
title: Report Suite-Ansätze
topic: Admin Tools
uuid: c90b8e38-2c95-4318-8165-a362106b6142
translation-type: tm+mt
source-git-commit: 9bc2e0425fa99efb32561ad1f80605e078eb7650
workflow-type: tm+mt
source-wordcount: '975'
ht-degree: 27%

---


# Report Suite-Ansätze

<!-- change filename since page name changed? -->

Sie können Ihre Report Suites entweder als *globale Report Suites* oder *Datenaggregations-Report Suites* konfigurieren.

## Globale Report Suites

Eine globale Report Suite sammelt Daten aus allen Domänen und Apps, deren Eigentümer Ihre Organisation ist. Es ist eine Implementierung erforderlich, um alle Bildanforderungen an eine einzelne Report Suite zu senden.

Adobe empfiehlt in den meisten Fällen die Implementierung einer globalen Report Suite. Die Vorteile der Implementierung einer globalen Report Suite finden Sie unter &quot;[Überlegungen zur globalen Report Suite](https://experienceleague.adobe.com/docs/analytics/implementation/prepare/global-rs.html)&quot;.

Mithilfe der Ansätze *Multi-Suite Tagging* und *Virtual Report Suite* können Sie Untergruppen der globalen Report Suite-Daten Ihrer Firma für verschiedene Endbenutzer bereitstellen:

* **Multi-Suite-Tagging**: Mit Multi-Suite-Tagging können Sie Bildanforderungen nicht nur an eine globale Report Suite, sondern auch an einzelne untergeordnete Report Suites senden. Die globalen Berichtsdaten werden in allen Report Suites dedupliziert.

   Sie können beispielsweise alle Daten in einer globalen Report Suite erfassen und auch sekundäre Report Suites einrichten, die auf der Marke, der Region oder einem anderen Differenzierungsfaktor basieren. Die verschiedenen Teams in Ihrer Firma könnten sich dann auf die für sie relevanten Daten in den Report Suites konzentrieren.

   Um Multi-Suite-Tagging zu verwenden, implementieren Sie untergeordnete Report Suites und eine globale Report Suite, die alle Daten der untergeordneten Report Suites enthält. Der Rückverfolgungscode für Ihre Webseiten und Apps enthält die Report Suite-ID (RSID) für die globale Report Suite sowie die RSIDs für die entsprechenden untergeordneten Report Suites.<!-- Wording/be more specific? And include any links? -->

   Für jede Report Suite in der Bildanforderung wird ein separater Server-Aufruf durchgeführt. Die Aufrufe an die untergeordneten Report Suites sind sekundäre Aufrufe.

* **Virtual Report Suite**: Eine  [Virtual Report Suite ](/help/components/vrs/vrs-about.md) enthält eine Abfrage zu bestimmten Segmenten, die in einer globalen Report Suite erfasst wurden und für bestimmte Benutzergruppen verfügbar sind. Virtual Report Suites ermöglichen es Ihnen, Berichtselemente für verschiedene Endbenutzer zu kuratieren, ohne Multi-Suite-Tagging zu verwenden, wodurch sekundäre Server-Aufrufe vermieden werden.

   Um Virtual Report Suites zu verwenden, implementieren Sie eine globale Report Suite und analysieren Sie dann die Daten, um Virtual Report Suites mit bestimmten angewendeten Segmenten und mit bestimmten Gruppenberechtigungen zu erstellen. Virtual Report Suites können im Virtual Report Suite Manager ([!UICONTROL Komponenten] > [!UICONTROL Virtual Report Suites]) erstellt werden. Weitere Informationen finden Sie unter &quot;[Arbeitsablauf für Virtual Report Suites](/help/components/vrs/c-workflow-vrs/vrs-workflow.md)&quot;.

Die Verwendung von Virtual Report Suites anstelle von Multi-Suite-Tagging ist häufig eine Best Practice, Virtual Report Suites weisen jedoch einige Einschränkungen auf. Siehe &quot;[Überlegungen zu Virtual Report Suites und Multi-Suite-Tagging](/help/components/vrs/vrs-considerations.md)&quot;, um festzustellen, welcher Report Suite-Ansatz für Ihre geschäftlichen Anforderungen am besten geeignet ist. Einen ausführlichen Vergleich der Virtual Report Suites mit der Multi-Suite-Tagging-Funktion finden Sie unter &quot;[Virtual Report Suites vs. Multisuite-Tagging](/help/components/vrs/vrs-about.md#section_317E4D21CCD74BC38166D2F57D214F78)&quot;.

## Datenaggregationsberichte

>[!NOTE]
>
>[!DNL Reports & Analytics] ist das einzige Tool, das Datenaggregationsberichte unterstützt. Die Verwendung von Datenaggregationen wird in Adobe nicht mehr empfohlen. Verwenden Sie stattdessen eine globale Report Suite mit Multi-Suite-Tagging oder Virtual Report Suites.

Ein Datenaggregationsbericht ist eine einfache Aggregation von Daten aus mehreren Report Suites ohne Deduplizierung-Duplikate- oder Segmentaufschlüsselungen oder Datenaufschlüsselungen. Datenaggregationen erfordern keine Codeimplementierung. Um Datenaggregations-Berichte zu verwenden, implementieren Sie untergeordnete Report Suites](/help/admin/c-manage-report-suites/c-new-report-suite/t-create-a-report-suite.md) und [kombinieren Sie diese dann mit [!UICONTROL Admin Tools] in einen Datenaggregations-Bericht](/help/admin/c-manage-report-suites/t-rollups.md).[

Datenaggregationsberichte sind kostenlos: Die untergeordneten Report Suites werden mit eigenen Serveraufrufen versehen, die Datenaggregation führt jedoch nicht zu zusätzlichen Aufrufen. Datenaggregationen sind eine alte Funktion und haben viele Einschränkungen.

### Einschränkungen bei Datenaggregationsberichten {#limitations-rollups}

* Datenaggregationen liefern Gesamtdaten, aber keine einzelnen Werte in Berichten. eVar1-Werte werden beispielsweise nicht einbezogen, aber ihr Aggregat insgesamt kann sein.
* Daten werden nicht dedupliziert, wenn die Datenaggregation Daten aus Report Suites zusammenfasst.
* Datenaggregationen werden nachts um Mitternacht ausgeführt.
* Wenn Sie einer vorhandenen Datenaggregation eine Report Suite hinzufügen, werden historische Daten nicht in die Datenaggregation einbezogen.
* Alle untergeordneten Report Suites müssen Daten enthalten, damit eine Datenaggregation funktioniert. Wenn neue Report Suites in eine Datenaggregation einbezogen werden, stellen Sie sicher, dass Sie mindestens eine Ansicht an jede dieser Report Suites senden.
* Datenaggregations-Report Suites können maximal 40 untergeordnete Report Suites enthalten.
* Datenaggregations-Report Suites können maximal 100 Ereignis enthalten.
* Daten in Datenaggregations-Report Suites unterstützen keine Aufschlüsselungen oder Segmente.
* Der Seitenbericht wird durch den Bericht zu den beliebtesten Sites ersetzt, der Metriken auf der Ebene der untergeordneten Suite enthält.

## Vergleich der Funktionen der globalen Report Suite und der Datenaggregations-Report

**Sekundäre Server-Aufrufe**: Bei Datenaggregationen gibt es keine zusätzlichen Server-Aufrufe, die über das hinausgehen, was eine einzelne Report Suite erfasst. Wenn Ihre Organisation Multi-Suite-Tagging verwendet, werden für jede zusätzliche Report Suite, die in einer Bildanforderung enthalten ist, sekundäre Server-Aufrufe durchgeführt.

>[!TIP]
>
>Wenn Sie nur eine globale Report Suite mit [Virtual Report Suites](/help/components/vrs/vrs-considerations.md) verwenden, sind keine sekundären Server-Aufrufe erforderlich.

**Implementierungsänderungen**: Bei Datenaggregationen sind keine Implementierungsänderungen erforderlich, bei globalen Report Suites müssen Sie jedoch die globale Report Suite-ID in Ihre Implementierung einbeziehen.

**Duplizierung:** In globalen Report Suites werden doppelte Unique Visitor entfernt, in Aggregationen dagegen nicht. Wenn ein Besucher beispielsweise drei Ihrer Domänen am gleichen Tag besucht, werden in den Aggregationen drei Unique Visitors pro Tag gezählt. In globalen Report Suites wird nur ein einziger Unique Visitor festgehalten.

**Zeitrahmen:** Aggregationen werden lediglich jeden Tag um Mitternacht verarbeitet, globale Report Suites melden Daten dagegen mit einer gewissen Standardlatenz.

**Breite**: Bei Aggregationen gibt es keine Möglichkeit für eine Kommunikation zwischen den Report Suites. Globale Report Suites können Konversionsvariablen zwischen Report Suites Gutschriften zuweisen und Pfade für alle Report Suites bereitstellen.

**Historische Daten:** In Aggregationen können historische Daten gesammelt werden, globale Report Suites befassen sich nur mit den Daten, die ab dem Zeitpunkt der Implementierung dieser Suites anfallen.

**Berichte:** Globale Report Suites liefern Daten zu allen Dimensionen; Aggregationen stellen die gesammelten Daten lediglich in Übersichtsberichten bereit.

**Unterstützte Produkte:** Datenaggregationen können nur in Reports &amp; Analytics verwendet werden. Sie werden in Analysis Workspace oder Data Warehouse nicht unterstützt. Globale Report Suites können in allen Produkten verwendet werden.

**Anzahl der aggregierten Report Suites:** Datenaggregationen unterstützen nur maximal 40 untergeordnete Report Suites. Globale Report Suites können auf beliebig vielen Domänen oder Apps implementiert werden, deren Inhaber Sie sind.
