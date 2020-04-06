---
description: Bei Datenaggregations-Report Suites werden Daten aus mehreren untergeordneten Report Suites in einem Datensatz zusammengefasst.
title: Datenaggregations-Report Suites und globale Report Suites
topic: Admin tools
uuid: c90b8e38-2c95-4318-8165-a362106b6142
translation-type: tm+mt
source-git-commit: dabaf6247695bc4f3d9bfe668f3ccfca12a52269

---


# Datenaggregations-Report Suites und globale Report Suites

Bei Datenaggregations-Report Suites werden Daten aus mehreren untergeordneten Report Suites in einem Datensatz zusammengefasst. Sie bieten eine komfortable Möglichkeit, die Gesamtsummen wie Seitenansichten, Umsatz oder andere grundlegende Dimensionen anzuzeigen. Datenaggregationen werden häufig verwendet, weil sie keine zusätzliche Implementierung erfordern.

## Definitionen der Report Suite-Typen

**Globale Report Suite**: Die Implementierung wird geändert, um Bildanforderungen domänenübergreifend in eine globale Report Suite zu senden. Wenn Treffer auch an einzelne Report Suites gesendet werden, wird dies als Multi-Suite-Tagging bezeichnet.

**Datenaggregations-Report Suite**: Wird in den Admin Tools erstellt. Am Ende jeden Tages wird die Summe jeder Metrik berechnet.

* Datenaggregationen können kostenlos verwendet werden und erhöhen nicht die Nutzung der Server-Aufrufe.
* Datenaggregationen liefern Gesamtdaten, melden jedoch keine einzelnen Werte in Berichten. Beispielsweise werden eVar1-Werte nicht einbezogen, aber der Gesamtwert des Aggregats kann angegeben werden.
* Daten werden beim Zusammenfassen der Daten aus den Report Suites nicht dedupliziert.
* Datenaggregationen werden jede Nacht ausgeführt.
* Wenn Sie eine Report Suite einer vorhandenen Datenaggregation hinzufügen, werden historische Daten nicht einbezogen.
* Alle untergeordneten Report Suites müssen Daten enthalten, damit eine Datenaggregation funktioniert. Wenn neue Report Suites in einer Datenaggregation enthalten sind, stellen Sie sicher, dass Sie mindestens eine Ansicht an diese Report Suites senden.
* Datenaggregations-Report Suites sind auf maximal 40 untergeordnete Report Suites beschränkt.
* Datenaggregations-Report-Suites sind auf maximal 100 Ereignis beschränkt.
* Daten in Datenaggregations-Report Suites unterstützen keine Aufschlüsselungen oder Segmente.
* Der Seitenbericht wird durch den Bericht zu den beliebtesten Sites ersetzt, der Metriken auf der Ebene der untergeordneten Suite enthält.

## Aggregations-Report Suites im Vergleich zu globalen Report Suites

**Sekundäre Server-Aufrufe**: Bei Datenaggregationen gibt es keine zusätzlichen Server-Aufrufe, die über das hinausgehen, was eine einzelne Report Suite erfasst. Wenn Ihre Organisation Multi-Suite-Tagging verwendet, werden für jede zusätzliche Report Suite, die in einer Bildanforderung enthalten ist, sekundäre Server-Aufrufe durchgeführt.

>[!TIP] Wenn Sie nur eine globale Report Suite mit [Virtual Report Suites](../../components/vrs/vrs-considerations.md) verwenden, sind keine sekundären Server-Aufrufe erforderlich.

**Implementierungsänderungen**: Bei Datenaggregationen sind keine Implementierungsänderungen erforderlich, bei globalen Report Suites müssen Sie jedoch die globale Report Suite-ID in Ihre Implementierung einbeziehen.

**Duplizierung**: Globale Report Suites deduplizieren eindeutige Besucher, Datenaggregationen nicht. Wenn ein Benutzer z. B. drei Ihrer Domänen am selben Tag besucht, zählen Datenaggregationen drei individuelle Besucher pro Tag. Globale Report Suites würden einen eindeutigen Besucher aufzeichnen.

**Zeitraum**: Datenaggregationen werden nur jeden Abend um Mitternacht verarbeitet, während globale Report Suites Daten mit Standardlatenz melden.

**Breite**: Bei Aggregationen gibt es keine Möglichkeit für eine Kommunikation zwischen den Report Suites. Globale Report Suites können Gutschriften für Konversionsvariablen in anderen Report Suites vornehmen und auch Pfade zu anderen Report Suites bereitstellen.

**Historische Daten:** In Aggregationen können historische Daten gesammelt werden, globale Report Suites befassen sich nur mit den Daten, die ab dem Zeitpunkt der Implementierung dieser Suites anfallen.

**Berichte:** Globale Report Suites liefern Daten zu allen Dimensionen; Aggregationen stellen die gesammelten Daten lediglich in Übersichtsberichten bereit.

**Unterstützte Produkte:** Datenaggregationen können nur in Reports &amp; Analytics verwendet werden. Sie werden in Analysis Workspace, Data Warehouse oder Ad Hoc Analysis nicht unterstützt. Globale Report Suites können in allen Produkten verwendet werden.

**Anzahl der aggregierten Report Suites:** Datenaggregationen unterstützen nur maximal 40 untergeordnete Report Suites. Globale Report Suites können auf beliebig vielen Domänen oder Apps implementiert werden, deren Inhaber Sie sind.
