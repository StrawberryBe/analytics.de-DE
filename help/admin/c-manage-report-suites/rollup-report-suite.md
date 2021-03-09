---
description: Bei Datenaggregations-Report Suites werden Daten aus mehreren untergeordneten Report Suites in einem Datensatz zusammengefasst.
title: Datenaggregations-Report Suites und globale Report Suites
translation-type: tm+mt
source-git-commit: 4d0d5ca99049e48fcf1f248f78ecef94534b6815
workflow-type: tm+mt
source-wordcount: '566'
ht-degree: 98%

---


# Datenaggregations-Report Suites und globale Report Suites

Bei Datenaggregations-Report Suites werden Daten aus mehreren untergeordneten Report Suites in einem Datensatz zusammengefasst. Sie bieten eine komfortable Möglichkeit, die Gesamtsummen wie Seitenansichten, Umsatz oder andere grundlegende Dimensionen anzuzeigen. Datenaggregationen werden häufig verwendet, weil sie keine zusätzliche Implementierung erfordern.

## Definitionen der Report Suite-Typen

**Globale Report Suite**: Die Implementierung wird geändert, um Bildanforderungen domänenübergreifend in eine globale Report Suite zu senden. Wenn Treffer auch an einzelne Report Suites gesendet werden, wird dies als Multi-Suite-Tagging bezeichnet.

**Datenaggregations-Report Suite**: Wird in den Admin Tools erstellt. Am Ende jeden Tages wird die Summe jeder Metrik berechnet.

* Datenaggregationen können kostenlos verwendet werden und erhöhen nicht die Nutzung der Server-Aufrufe.
* Datenaggregationen liefern Daten zu Gesamtsummen und verzeichnen keine Einzelwerte in Berichten. Beispielsweise sind keine eVar1-Werte enthalten, aber ihre aggregierte Summe kann enthalten sein.
* Daten werden beim Zusammenfassen der Daten aus den Report Suites nicht dedupliziert.
* Datenaggregationen werden jede Nacht ausgeführt.
* Wenn Sie eine Report Suite einer vorhandenen Datenaggregation hinzufügen, werden historische Daten nicht einbezogen.
* Alle untergeordneten Report Suites müssen Daten enthalten, damit eine Datenaggregation funktioniert. Wenn in eine Datenaggregation neue Report Suites einbezogen werden, müssen Sie mindestens eine Seitenansicht an diese Report Suites senden.
* Datenaggregations-Report Suites sind auf maximal 40 untergeordnete Report Suites beschränkt.
* Datenaggregations-Report Suites sind auf maximal 100 Ereignisse begrenzt.
* Daten in Datenaggregations-Report Suites unterstützen keine Aufschlüsselungen oder Segmente.
* Der Seitenbericht wird durch den Bericht zu den beliebtesten Sites ersetzt, der Metriken auf der Ebene der untergeordneten Suite enthält.

## Aggregations-Report Suites im Vergleich zu globalen Report Suites

**Sekundäre Server-Aufrufe**: Bei Datenaggregationen gibt es keine zusätzlichen Server-Aufrufe, die über das hinausgehen, was eine einzelne Report Suite erfasst. Wenn Ihre Organisation Multi-Suite-Tagging verwendet, werden für jede zusätzliche Report Suite, die in einer Bildanforderung enthalten ist, sekundäre Server-Aufrufe durchgeführt.

>[!TIP]
>
>Wenn Sie nur eine globale Report Suite mit [Virtual Report Suites](../../components/vrs/vrs-considerations.md) verwenden, sind keine sekundären Server-Aufrufe erforderlich.

**Implementierungsänderungen**: Bei Datenaggregationen sind keine Implementierungsänderungen erforderlich, bei globalen Report Suites müssen Sie jedoch die globale Report Suite-ID in Ihre Implementierung einbeziehen.

**Duplizierung:** In globalen Report Suites werden doppelte Unique Visitor entfernt, in Aggregationen dagegen nicht. Wenn ein Besucher beispielsweise drei Ihrer Domänen am gleichen Tag besucht, werden in den Aggregationen drei Unique Visitors pro Tag gezählt. In globalen Report Suites wird nur ein einziger Unique Visitor festgehalten.

**Zeitrahmen:** Aggregationen werden lediglich jeden Tag um Mitternacht verarbeitet, globale Report Suites melden Daten dagegen mit einer gewissen Standardlatenz.

**Breite**: Bei Aggregationen gibt es keine Möglichkeit für eine Kommunikation zwischen den Report Suites. Globale Report Suites können Gutschriften für Konversionsvariablen in anderen Report Suites vornehmen und auch Pfade zu anderen Report Suites bereitstellen.

**Historische Daten:** In Aggregationen können historische Daten gesammelt werden, globale Report Suites befassen sich nur mit den Daten, die ab dem Zeitpunkt der Implementierung dieser Suites anfallen.

**Berichte:** Globale Report Suites liefern Daten zu allen Dimensionen; Aggregationen stellen die gesammelten Daten lediglich in Übersichtsberichten bereit.

**Unterstützte Produkte:** Datenaggregationen können nur in Reports &amp; Analytics verwendet werden. Sie werden in Analysis Workspace oder Data Warehouse nicht unterstützt. Globale Report Suites können in allen Produkten verwendet werden.

**Anzahl der aggregierten Report Suites:** Datenaggregationen unterstützen nur maximal 40 untergeordnete Report Suites. Globale Report Suites können auf beliebig vielen Domänen oder Apps implementiert werden, deren Inhaber Sie sind.
