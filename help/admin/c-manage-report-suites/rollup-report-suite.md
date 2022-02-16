---
description: Beschreibungen der Report Suite-Typen und Vergleich globaler Report Suites und Datenaggregations-Report Suites.
title: Report Suite-Ansätze
feature: Report Suite Settings
exl-id: 97bdc9bd-2212-436b-b3b4-ec518624f9e6
source-git-commit: 72bd67179e003b70233d863d34153fec77548256
workflow-type: tm+mt
source-wordcount: '973'
ht-degree: 27%

---

# Report Suite-Ansätze

<!-- change filename since page name changed? -->

Sie können Ihre Report Suites wie folgt konfigurieren: *globale Report Suites* oder *Datenaggregations-Report Suites*.

## Globale Report Suites

Eine globale Report Suite erfasst Daten aus allen Domänen und Apps, deren Inhaber Ihre Organisation ist. Dazu ist eine Implementierung erforderlich, um alle Bildanforderungen an eine einzelne Report Suite zu senden.

Adobe empfiehlt in den meisten Fällen die Implementierung einer globalen Report Suite. Siehe[Überlegungen zur globalen Report Suite](https://experienceleague.adobe.com/docs/analytics/implementation/prepare/global-rs.html)&quot;, um die Vorteile der Implementierung einer globalen Report Suite zu nutzen.

Sie können mithilfe der Variablen *Multi-Suite-Tagging* und *Virtual Report Suite* Ansätze:

* **Multi-Suite-Tagging**: Mit Multi-Suite-Tagging können Sie Bildanforderungen nicht nur an eine globale Report Suite, sondern auch an einzelne untergeordnete Report Suites senden. Die globalen Berichtsdaten werden in allen Report Suites dedupliziert.

   Sie können beispielsweise alle Daten in einer globalen Report Suite erfassen und auch sekundäre Report Suites basierend auf Marke, Region oder einem anderen Differenzator einrichten. Die verschiedenen Teams in Ihrem Unternehmen können sich dann auf Daten in den Report Suites konzentrieren, die für sie relevant sind.

   Um Multi-Suite-Tagging zu verwenden, implementieren Sie untergeordnete Report Suites und eine globale Report Suite, die alle Daten der untergeordneten Elemente enthält. Der Trackingcode für Ihre Webseiten und Apps enthält die Report Suite-ID (RSID) für die globale Report Suite sowie die RSIDs für die entsprechenden untergeordneten Report Suites.<!-- Wording/be more specific? And include any links? -->

   Für jede Report Suite in der Bildanforderung wird ein separater Server-Aufruf durchgeführt. Bei den Aufrufen an die untergeordneten Report Suites handelt es sich um sekundäre Aufrufe.

* **Virtual Report Suite**: A [Virtual Report Suite](/help/components/vrs/vrs-about.md) ist eine Abfrage zu bestimmten Segmenten, die in einer globalen Report Suite erfasst und für bestimmte Benutzergruppen verfügbar sind. Virtual Report Suites ermöglichen es Ihnen, Berichtselemente für verschiedene Endbenutzer zu kuratieren, ohne Multi-Suite-Tagging zu verwenden, wodurch sekundäre Server-Aufrufe vermieden werden.

   Um Virtual Report Suites zu verwenden, implementieren Sie eine globale Report Suite und analysieren Sie dann die Daten, um Virtual Report Suites mit bestimmten angewendeten Segmenten und mit bestimmten Gruppenberechtigungen zu erstellen. Sie können Virtual Report Suites im Virtual Report Suite Manager ([!UICONTROL Komponenten] > [!UICONTROL Virtual Report Suites]). Siehe[Virtual Report Suite - Workflow](/help/components/vrs/c-workflow-vrs/vrs-workflow.md)&quot;.

Die Verwendung von Virtual Report Suites anstelle von Multi-Suite-Tagging ist häufig eine Best Practice, aber Virtual Report Suites weisen einige Einschränkungen auf. Siehe[Virtual Report Suites und Überlegungen zum Multi-Suite-Tagging](/help/components/vrs/vrs-considerations.md)&quot;, um zu bestimmen, welcher Report Suite-Ansatz für Ihre Geschäftsanforderungen am besten geeignet ist. Einen detaillierten Vergleich der Virtual Report Suites und Multi-Suite-Tagging-Funktionen finden Sie unter[Virtual Report Suites vs. Multisuite-Tagging](/help/components/vrs/vrs-about.md#section_317E4D21CCD74BC38166D2F57D214F78).&quot;

## Datenaggregations-Berichte

>[!NOTE]
>
>[!DNL Reports & Analytics] ist das einzige Tool, das Datenaggregations-Berichte unterstützt und Adobe die Verwendung von Datenaggregationen nicht mehr empfiehlt. Verwenden Sie stattdessen eine globale Report Suite mit Multi-Suite-Tagging oder Virtual Report Suites.

Ein Rollup-Bericht ist eine einfache Aggregation von Daten aus mehreren Report Suites ohne Deduplizierung oder ohne Segment- oder Datenaufschlüsselungen. Datenaggregationen erfordern keine Code-Implementierung. So verwenden Sie Datenaggregationsberichte: [untergeordnete Report Suites implementieren](/help/admin/c-manage-report-suites/c-new-report-suite/t-create-a-report-suite.md) und dann [sie in einem Rollup-Bericht zusammenfassen](/help/admin/c-manage-report-suites/t-rollups.md) using [!UICONTROL Admin Tools].

Datenaggregations-Berichte sind kostenlos: Die untergeordneten Report Suites erhalten eigene Server-Aufrufe, die Datenaggregation führt jedoch nicht zu zusätzlichen Aufrufen. Datenaggregationen sind eine alte Funktion und haben viele Einschränkungen.

### Einschränkungen bei Datenaggregationsberichten {#limitations-rollups}

* Datenaggregationen liefern Gesamtdaten, melden jedoch keine individuellen Werte in Berichten. Beispielsweise sind eVar1-Werte nicht enthalten, aber ihre aggregierte Summe kann sein.
* Daten werden nicht dedupliziert, wenn die Datenaggregation Daten über Report Suites hinweg kombiniert.
* Datenaggregationen werden nachts um Mitternacht ausgeführt.
* Wenn Sie eine Report Suite zu einer vorhandenen Datenaggregation hinzufügen, werden historische Daten nicht in die Datenaggregation einbezogen.
* Alle untergeordneten Report Suites müssen Daten enthalten, damit eine Datenaggregation funktioniert. Wenn neue Report Suites in eine Datenaggregation einbezogen werden, stellen Sie sicher, dass Sie mindestens eine Seitenansicht an jede dieser Report Suites senden.
* Datenaggregations-Report Suites können maximal 40 untergeordnete Report Suites enthalten.
* Datenaggregations-Report Suites können maximal 100 Ereignisse enthalten.
* In Datenaggregations-Report Suites enthaltene Daten unterstützen keine Aufschlüsselungen oder Segmente.
* Der Seitenbericht wird durch den Bericht zu den beliebtesten Sites ersetzt, der Metriken auf der Ebene der untergeordneten Suite enthält.

## Vergleich der globalen Report Suite- und Datenaggregations-Berichtsfunktionen

**Sekundäre Server-Aufrufe**: Bei Datenaggregationen gibt es keine zusätzlichen Server-Aufrufe, die über das hinausgehen, was eine einzelne Report Suite erfasst. Wenn Ihre Organisation Multi-Suite-Tagging verwendet, werden für jede zusätzliche Report Suite, die in einer Bildanforderung enthalten ist, sekundäre Server-Aufrufe durchgeführt.

>[!TIP]
>
>Wenn Sie nur eine globale Report Suite mit [Virtual Report Suites](/help/components/vrs/vrs-considerations.md) verwenden, sind keine sekundären Server-Aufrufe erforderlich.

**Implementierungsänderungen**: Bei Datenaggregationen sind keine Implementierungsänderungen erforderlich, bei globalen Report Suites müssen Sie jedoch die globale Report Suite-ID in Ihre Implementierung einbeziehen.

**Duplizierung:** In globalen Report Suites werden doppelte Unique Visitor entfernt, in Aggregationen dagegen nicht. Wenn ein Besucher beispielsweise drei Ihrer Domänen am gleichen Tag besucht, werden in den Aggregationen drei Unique Visitors pro Tag gezählt. In globalen Report Suites wird nur ein einziger Unique Visitor festgehalten.

**Zeitrahmen:** Aggregationen werden lediglich jeden Tag um Mitternacht verarbeitet, globale Report Suites melden Daten dagegen mit einer gewissen Standardlatenz.

**Breite**: Bei Aggregationen gibt es keine Möglichkeit für eine Kommunikation zwischen den Report Suites. Globale Report Suites können Gutschriften für Konversionsvariablen zwischen Report Suites vornehmen und Pfade für alle Report Suites bereitstellen.

**Historische Daten:** In Aggregationen können historische Daten gesammelt werden, globale Report Suites befassen sich nur mit den Daten, die ab dem Zeitpunkt der Implementierung dieser Suites anfallen.

**Berichte:** Globale Report Suites liefern Daten zu allen Dimensionen; Aggregationen stellen die gesammelten Daten lediglich in Übersichtsberichten bereit.

**Unterstützte Produkte:** Datenaggregationen können nur in Reports &amp; Analytics verwendet werden. Sie werden in Analysis Workspace oder Data Warehouse nicht unterstützt. Globale Report Suites können in allen Produkten verwendet werden.

**Anzahl der aggregierten Report Suites:** Datenaggregationen unterstützen nur maximal 40 untergeordnete Report Suites. Globale Report Suites können auf beliebig vielen Domänen oder Apps implementiert werden, deren Inhaber Sie sind.
