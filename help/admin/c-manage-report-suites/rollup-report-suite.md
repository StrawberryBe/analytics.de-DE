---
description: Bei Datenaggregations-Report Suites werden Daten aus mehreren untergeordneten Report Suites in einem Datensatz zusammengefasst.
seo-description: Bei Datenaggregations-Report Suites werden Daten aus mehreren untergeordneten Report Suites in einem Datensatz zusammengefasst.
seo-title: Datenaggregations- und globale Report Suites
solution: Analytics
title: Datenaggregations- und globale Report Suites
topic: Admin Tools
uuid: c 90 b 8 e 38-2 c 95-4318-8165-a 362106 b 6142
translation-type: tm+mt
source-git-commit: 86fe1b3650100a05e52fb2102134fee515c871b1

---


# Datenaggregations- und globale Report Suites

Bei Datenaggregations-Report Suites werden Daten aus mehreren untergeordneten Report Suites in einem Datensatz zusammengefasst.

Diese Report Suites unterscheiden sich von globalen Report Suites und bieten eine praktische Möglichkeit, Gesamtsummen anzuzeigen, wie Seitenansichten, Umsatz oder Technologiemetriken. Datenaggregationen werden häufig verwendet, weil sie keine zusätzliche Implementierung erfordern.

## Definitionen der Report Suite-Typen {#section_E51E03E3917040278600A7E9638A91C7}

**Globale Report Suite**: Die Implementierung wird geändert, um Bildanforderungen nicht nur in einzelne Report Suites, sondern auch domänenübergreifend zu senden.

**Datenaggregations-Report Suite**: Wird in den Admin Tools erstellt. Am Ende jeden Tages wird die Summe jeder Metrik berechnet.

* Datenaggregationen sind kostenlos und werden nicht auf Server-Aufrufe angerechnet.
* Datenaggregationen liefern Daten zu Gesamtsummen und verzeichnen keine Einzelwerte in Berichten. Beispielsweise sind keine eVar1-Werte enthalten, aber ihre aggregierte Summe kann enthalten sein.
* Daten werden beim Zusammenfassen der Daten aus den Report Suites nicht dedupliziert. Ein einzelner Benutzer kann in drei unterschiedliche Report Suites an einem Tag eingehen und wird als drei Unique Visitors in der Datenaggregation verzeichnet.
* Die Datenaggregation wird nachts durchgeführt.
* Wenn Sie eine Report Suite einer vorhandenen Datenaggregation hinzufügen, werden historische Daten nicht einbezogen.
* Datenaggregations-Report Suites haben beschränkte Berichterstellungsfähigkeiten. Zahlen über Unique Visitor werden beispielsweise für alle Report Suites addiert. Wenn dieselbe Person zwei verschiedene Report Suites besucht, führt die Datenaggregation diese Person als zwei Besucher auf, während eine globale Standard-Report Suite nur einen Besucher zeigt.
* Alle untergeordneten Report Suites müssen Daten enthalten, damit eine Datenaggregation funktioniert. Wenn in eine Datenaggregation neue Report Suites einbezogen werden, müssen Sie mindestens eine Seitenansicht an diese Report Suites senden.
* Datenaggregations-Report Suites sind auf maximal 40 untergeordnete Report Suites beschränkt.
* Datenaggregations-Report Suites sind auf maximal 100 Ereignisse begrenzt.
* Daten, die in Datenaggregations-Report Suites enthalten sind, unterstützen keine Subrelationen, Segmente oder sonstigen Metriken, die in den Marketing-Berichten eingeführt wurden.
* Der Bericht „Seiten“ ist in Datenaggregations-Report Suites nicht verfügbar. Er wird durch den Bericht zu den beliebtesten Sites ersetzt, der Metriken auf der Ebene der untergeordneten Suite enthält.

## Aggregations-Report Suites im Vergleich zu globalen Report Suites {#section_7B3703DC7ABF4B9EA9DF02A54592CAD0}

**Server-Aufrufe:** In globalen Report Suites werden sekundäre Server-Aufrufe hochgezählt, in Aggregationen finden keinerlei Server-Aufrufe statt.

**Implementationsänderungen:** Aggregationen erfordern keine Implementationsänderungen, bei globalen Report Suites muss jedoch eine zusätzliche Report Suite-ID in die Datei „s_code.js“ eingetragen werden.

**Duplizierung:** In globalen Report Suites werden doppelte Unique Visitor entfernt, in Aggregationen dagegen nicht. Wenn ein Besucher beispielsweise drei Ihrer Domänen am gleichen Tag besucht, werden in den Aggregationen drei Unique Visitors pro Tag gezählt. In globalen Report Suites wird nur ein einziger Unique Visitor festgehalten.

**Zeitrahmen:** Aggregationen werden lediglich jeden Tag um Mitternacht verarbeitet, globale Report Suites melden Daten dagegen mit einer gewissen Standardlatenz.

**Breite:** Globale Report Suites können Gutschriften für Konversionsvariablen in anderen Report Suites vornehmen und auch Pfade zu anderen Report Suites bereitstellen. Bei Aggregationen gibt es keine Möglichkeit für eine Kommunikation zwischen den Report Suites.

**Historische Daten:** In Aggregationen können historische Daten gesammelt werden, globale Report Suites befassen sich nur mit den Daten, die ab dem Zeitpunkt der Implementierung dieser Suites anfallen.

**Berichte:** Globale Report Suites liefern Zusatzinformationen zu ALLEN implementierten Berichten; Aggregationen stellen die gesammelten Daten lediglich in Übersichtsberichten bereit.

**Unterstützte Produkte**: Aggregationen werden weder in Data Warehouse noch in Ad Hoc Analysis unterstützt. Marketing-Berichte können maximal 40 untergeordnete Report Suites haben. Globale Report Suites können in allen Produkten verwendet werden, und die Anzahl der untergeordneten Report Suites ist nicht begrenzt.

## Welcher Report Suite-Typ sollte implementiert werden? {#section_868066B9604B49BABBF84074BA5E9C71}

Bei der Wahl zwischen Aggregationen und globalen Report Suites sollten Sie Folgendes beachten:

* Ist die Anzahl der Server-Aufrufe für mein Unternehmen wichtig? Wenn die Anzahl der Server-Aufrufe beschränkt werden muss, sollten Sie sich für Aggregationen entscheiden. Globale Report Suites bewirken nahezu eine Verdoppelung der getätigten Server-Aufrufe.
* Sind Übersichtsberichte zum Traffic über alle Suites hinweg ausreichend? Wenn die Deduplizierung der Besucher wichtig ist, sollten Sie sich für eine globale Report Suite entscheiden.
* Sind Pfade und Konversions-/Erfolgsraten über Domänen hinweg wichig? Wenn Sie häufig mit siteübergreifenden Kampagnen arbeiten, sollten Sie sich für eine globale Report Suite entscheiden.
* Ist die zeitnahe Darstellung der Site-Gesamtdaten wichtig? Einzelne Report Suites werden immer noch nahezu in Echtzeit erstellt. Wenn die Anzeige der Report Suite-Gesamtzahlen auch noch am nächsten Tag ausreicht, werden Aggregationen empfohlen.
* Ist eine große Menge an relevanten historischen Daten verfügbar? Globale Report Suites sind nicht in der Lage, rückwirkend Berichte zu erstellen. Wenn historische Daten von Bedeutung sind, sollten Sie sich für Aggregationen entscheiden.
* Sind Data Warehouse und die Ad Hoc Analysis wesentliche Ergänzungen für die Berichterstellung? In diesem Fall wird eine globale Report Suite empfohlen.

Die Auswahl wirkt sich nicht auf einzelne Report Suites aus. Wägen Sie das Für und Wider sorgfältig ab, und entscheiden Sie sich dann für die Report Suites, die in Ihrem Unternehmen verwendet werden sollen.
