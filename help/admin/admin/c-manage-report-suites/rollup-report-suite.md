---
description: Beschreibungen von Report Suite-Typen und Vergleich globaler Report Suites und Datenaggregations-Report Suites.
title: Report Suite-Ansätze
feature: Report Suite Settings
exl-id: 97bdc9bd-2212-436b-b3b4-ec518624f9e6
source-git-commit: 4545c3839586231918ba5ebbf17fcac5a366abab
workflow-type: tm+mt
source-wordcount: '448'
ht-degree: 89%

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

  Um Virtual Report Suites zu verwenden, implementieren Sie eine globale Report Suite und analysieren Sie dann die Daten, um Virtual Report Suites mit bestimmten angewendeten Segmenten und mit bestimmten Gruppenberechtigungen zu erstellen. Sie können Virtual Report Suites im Virtual Report Suites-Manager erstellen ([!UICONTROL Komponenten] > [!UICONTROL Virtual Report Suites]). Weitere Informationen finden Sie unter [Workflow für Virtual Report Suites](/help/components/vrs/c-workflow-vrs/vrs-workflow.md).

Die Verwendung von Virtual Report Suites anstelle von Multi-Suite-Tagging ist oft empfehlenswert, aber Virtual Report Suites weisen einige Einschränkungen auf. Siehe [Virtual Report Suites und Überlegungen zum Multi-Suite-Tagging](/help/components/vrs/vrs-considerations.md), um zu bestimmen, welcher Report Suite-Ansatz für Ihre Geschäftsanforderungen am besten geeignet ist. Einen detaillierten Vergleich der Virtual Report Suites und Multi-Suite-Tagging-Funktionen finden Sie unter[Virtual Report Suites im Vergleich zum Multi-Suite-Tagging](/help/components/vrs/vrs-about.md#section_317E4D21CCD74BC38166D2F57D214F78).&quot;

## Datenaggregationsberichte

>[!NOTE]
>
>[!DNL Reports & Analytics] ist das einzige Tool, das Datenaggregationsberichte unterstützt. Reports &amp; Analytics wurde am 17. Januar 2024 eingestellt.

<!---### Limitations of Rollup Reports {#limitations-rollups}

* Rollups provide total data, but they do not report individual values in reports. For example, eVar1 values are not included, but their aggregate total can be.
* Data is not deduplicated when the rollup combines data across report suites.
* Rollups run nightly at midnight.
* When you add a report suite to an existing rollup, historical data is not included in the rollup.
* All child report suites must have data in them for a rollup to function. If new report suites are included in a rollup, make sure to send at least one page view to each of those report suites.
* Rollup report suites can include a maximum of 40 child report suites.
* Rollup report suites can include a maximum of 100 events.
* Data contained in rollup report suites does not support breakdowns or segments.
* The Pages report is replaced with the Most Popular Sites report, which reports on metrics at the child-suite level.

## Comparison of Global Report Suite and Rollup Report  Features

**Secondary server calls**: Rollups do not incur any additional server calls beyond what a single report suite collects. If your organization uses multi-suite tagging, secondary server calls are made for each additional report suite included in an image request.

>[!TIP]
>
>If you use only a global report suite with [virtual report suites](/help/components/vrs/vrs-considerations.md), no secondary server calls are needed.

**Implementation changes**: Rollups do not require any implementation changes, while global report suites require you to include the global report suite ID in your implementation.

**Duplication**: Global report suites deduplicate unique visitors, while rollups do not. For example, if a user visits three of your domains in the same day, rollups would count three daily unique visitors. Global report suites would record one unique visitor.

**Time frame**: Rollups are only processed at midnight each night, while global report suites report data with standard latency.

**Breadth**: Rollups have no way to communicate between report suites. Global report suites can attribute credit to conversion variables between report suites and provide pathing across report suites.

**Historical data**: Rollups can aggregate historical data, while global report suites only report data from the point they were implemented.

**Reports**: Global report suites provide data on all dimensions; rollups provide aggregate data on only high-level reports.

**Supported products**: Rollups could only be used in Reports & Analytics. They are not supported in Analysis Workspace, or Data Warehouse. Global report suites can be used across all products.

**Number of aggregated report suites**: Rollups only support a maximum of 40 child report suites. Global report suites can be implemented on any number of domains or apps that you own.--->
