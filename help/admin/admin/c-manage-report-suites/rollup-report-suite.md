---
description: Beschreibungen von Report Suite-Typen und Vergleich globaler Report Suites und Datenaggregations-Report Suites.
title: Report Suite-Ansätze
feature: Report Suite Settings
exl-id: 97bdc9bd-2212-436b-b3b4-ec518624f9e6
source-git-commit: e8cbf24f6e0c829dadb2a6e7db502d0e8ba1f07f
workflow-type: ht
source-wordcount: '973'
ht-degree: 100%

---

# Report Suite-Ansätze

<!-- change filename since page name changed? -->

Sie können Ihre Report Suites als *globale Report Suites* oder als *Datenaggregations-Report Suites* konfigurieren.

## Globale Report Suites

Bei einer globalen Report Suite handelt es sich um eine Report Suite, die Daten aus allen Domains und Programmen sammelt, die Ihr Unternehmen besitzt. Damit alle Bildanfragen an eine einzige Report Suite gesendet werden, ist eine Implementierung erforderlich.

Adobe empfiehlt in den meisten Fällen die Implementierung einer globalen Report Suite. Siehe [Überlegungen zur globalen Report Suite](https://experienceleague.adobe.com/docs/analytics/implementation/prepare/global-rs.html?lang=de) zu den Vorteilen der Implementierung einer globalen Report Suite.

Mit den Methoden *Multi-Suite-Tagging* und *Virtual Report Suite* können Sie Teilmengen der globalen Report Suite Ihres Unternehmens für verschiedene Endbenutzer bereitstellen:

* **Multi-Suite-Tagging**: Mit Multi-Suite-Tagging können Sie Bildanfragen nicht nur an eine globale Report Suite, sondern auch an einzelne untergeordnete Report Suites senden. Die globalen Berichtsdaten werden in allen Report Suites dedupliziert.

   Sie können beispielsweise alle Daten in einer einzigen globalen Report Suite erfassen und auch sekundäre Report Suites basierend auf Marke, Region oder einem anderen Unterscheidungsmerkmal einrichten. Die verschiedenen Teams in Ihrem Unternehmen können sich dann auf Daten in denjenigen Report Suites konzentrieren, die für sie relevant sind.

   Um Multi-Suite-Tagging zu verwenden, implementieren Sie untergeordnete Report Suites und eine globale Report Suite, die alle Daten der untergeordneten Elemente enthält. Der Trackingcode für Ihre Web-Seiten und Programme enthält die Report Suite-ID (RSID) für die globale Report Suite sowie die RSIDs für die entsprechenden untergeordneten Report Suites.<!-- Wording/be more specific? And include any links? -->

   Für jede Report Suite in der Bildanfrage wird ein separater Server-Aufruf durchgeführt. Bei den Aufrufen an die untergeordneten Report Suites handelt es sich um sekundäre Aufrufe.

* **Virtual Report Suite**: Eine [Virtual Report Suite](/help/components/vrs/vrs-about.md) ist eine Abfrage zu bestimmten Segmenten, die in einer globalen Report Suite erfasst und für bestimmte Benutzergruppen verfügbar sind. Virtual Report Suites ermöglichen es Ihnen, Berichtselemente für verschiedene Endbenutzer zu kuratieren, ohne Multi-Suite-Tagging zu verwenden, wodurch sekundäre Server-Aufrufe vermieden werden.

   Um Virtual Report Suites zu verwenden, implementieren Sie eine globale Report Suite und analysieren Sie dann die Daten, um Virtual Report Suites mit bestimmten angewendeten Segmenten und mit bestimmten Gruppenberechtigungen zu erstellen. Sie können Virtual Report Suites in Virtual Report Suite Manager ([!UICONTROL Komponenten] > [!UICONTROL Virtual Report Suites]) erstellen. Weitere Informationen finden Sie unter [Workflow für Virtual Report Suites](/help/components/vrs/c-workflow-vrs/vrs-workflow.md).

Die Verwendung von Virtual Report Suites anstelle von Multi-Suite-Tagging ist oft empfehlenswert, aber Virtual Report Suites weisen einige Einschränkungen auf. Siehe [Virtual Report Suites und Überlegungen zum Multi-Suite-Tagging](/help/components/vrs/vrs-considerations.md), um zu bestimmen, welcher Report Suite-Ansatz für Ihre Geschäftsanforderungen am besten geeignet ist. Einen detaillierten Vergleich der Funktionen von Virtual Report Suites und Multi-Suite-Tagging finden Sie unter [Virtual Report Suites vs. Multi-Suite-Tagging](/help/components/vrs/vrs-about.md#section_317E4D21CCD74BC38166D2F57D214F78).

## Datenaggregationsberichte

>[!NOTE]
>
>[!DNL Reports & Analytics] ist das einzige Tool, das Datenaggregationsberichte unterstützt, und Adobe empfiehlt die Verwendung von Datenaggregationen nicht mehr. Verwenden Sie stattdessen eine globale Report Suite mit Multi-Suite-Tagging oder Virtual Report Suites.

Ein Datenaggregationsbericht ist eine einfache Aggregation von Daten aus mehreren Report Suites ohne Deduplizierung und ohne Segment- oder Datenaufschlüsselungen. Datenaggregationen erfordern keine Implementierung von Code. So verwenden Sie Datenaggregationsberichte: [Implementieren Sie untergeordnete Report Suites](/help/admin/admin/c-manage-report-suites/c-new-report-suite/t-create-a-report-suite.md) und verwenden Sie dann die [!UICONTROL Admin Tools], um sie [zu einem Datenaggregationsbericht zusammenzufassen](/help/admin/admin/c-manage-report-suites/c-new-report-suite/t-rollups.md).

Datenaggregationsberichte sind kostenlos: Die untergeordneten Report Suites beinhalten zwar eigene Server-Aufrufe, die Datenaggregation führt jedoch nicht zu zusätzlichen Aufrufen. Datenaggregationen sind eine alte Funktion und haben viele Einschränkungen.

### Einschränkungen bei Datenaggregationsberichten {#limitations-rollups}

* Datenaggregationen liefern Gesamtdaten und verzeichnen keine Einzelwerte in Berichten. Beispielsweise sind keine eVar1-Werte enthalten, aber ihre aggregierte Summe kann enthalten sein.
* Daten werden beim Zusammenfassen der Daten aus den Report Suites in der Datenaggregation nicht dedupliziert.
* Datenaggregationen werden jede Nacht um Mitternacht ausgeführt.
* Wenn Sie eine Report Suite zu einer vorhandenen Datenaggregation hinzufügen, werden historische Daten nicht einbezogen.
* Alle untergeordneten Report Suites müssen Daten enthalten, damit eine Datenaggregation funktioniert. Wenn in eine Datenaggregation neue Report Suites einbezogen werden, müssen Sie mindestens eine Seitenansicht an jede dieser Report Suites senden.
* Datenaggregations-Report Suites sind auf maximal 40 untergeordnete Report Suites beschränkt.
* Datenaggregations-Report Suites können maximal 100 Ereignisse enthalten.
* Daten in Datenaggregations-Report Suites unterstützen keine Aufschlüsselungen oder Segmente.
* Der Seitenbericht wird durch den Bericht zu den beliebtesten Sites ersetzt, der Metriken auf der Ebene der untergeordneten Suite enthält.

## Vergleich der Funktionen von globalen Report Suites und Datenaggregationsberichten

**Sekundäre Server-Aufrufe**: Bei Datenaggregationen gibt es keine zusätzlichen Server-Aufrufe, die über das hinausgehen, was eine einzelne Report Suite erfasst. Wenn Ihre Organisation Multi-Suite-Tagging verwendet, werden für jede zusätzliche Report Suite, die in einer Bildanforderung enthalten ist, sekundäre Server-Aufrufe durchgeführt.

>[!TIP]
>
>Wenn Sie nur eine globale Report Suite mit [Virtual Report Suites](/help/components/vrs/vrs-considerations.md) verwenden, sind keine sekundären Server-Aufrufe erforderlich.

**Implementierungsänderungen**: Bei Datenaggregationen sind keine Implementierungsänderungen erforderlich, bei globalen Report Suites müssen Sie jedoch die globale Report Suite-ID in Ihre Implementierung einbeziehen.

**Duplizierung:** In globalen Report Suites werden doppelte Unique Visitor entfernt, in Aggregationen dagegen nicht. Wenn ein Besucher beispielsweise drei Ihrer Domänen am gleichen Tag besucht, werden in den Aggregationen drei Unique Visitors pro Tag gezählt. In globalen Report Suites wird nur ein einziger Unique Visitor festgehalten.

**Zeitrahmen:** Aggregationen werden lediglich jeden Tag um Mitternacht verarbeitet, globale Report Suites melden Daten dagegen mit einer gewissen Standardlatenz.

**Breite**: Bei Aggregationen gibt es keine Möglichkeit für eine Kommunikation zwischen den Report Suites. Globale Report Suites können Attributionen zu Konversionsvariablen in verschiedenen Report Suites vornehmen und Pfade zu anderen Report Suites bereitstellen.

**Historische Daten:** In Aggregationen können historische Daten gesammelt werden, globale Report Suites befassen sich nur mit den Daten, die ab dem Zeitpunkt der Implementierung dieser Suites anfallen.

**Berichte:** Globale Report Suites liefern Daten zu allen Dimensionen; Aggregationen stellen die gesammelten Daten lediglich in Übersichtsberichten bereit.

**Unterstützte Produkte:** Datenaggregationen können nur in Reports &amp; Analytics verwendet werden. Sie werden in Analysis Workspace oder Data Warehouse nicht unterstützt. Globale Report Suites können in allen Produkten verwendet werden.

**Anzahl der aggregierten Report Suites:** Datenaggregationen unterstützen nur maximal 40 untergeordnete Report Suites. Globale Report Suites können auf beliebig vielen Domänen oder Apps implementiert werden, deren Inhaber Sie sind.
