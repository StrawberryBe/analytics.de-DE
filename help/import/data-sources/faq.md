---
title: Häufig gestellte Fragen zu Datenquellen
description: Häufig gestellte Fragen zu Datenquellen.
exl-id: a948dfe9-289f-43e2-a9e7-7990cf609f5c
feature: Data Sources
source-git-commit: 811e321ce96aaefaeff691ed5969981a048d2c31
workflow-type: tm+mt
source-wordcount: '414'
ht-degree: 7%

---

# Häufig gestellte Fragen zu Datenquellen

Häufig gestellte Fragen zu Datenquellen.

+++ Wie hoch sind die Kosten für die Verwendung von Datenquellen?
Für Datenquellen fallen keine Gebühren an und sie werden auch nicht für die Nutzung von Server-Aufrufen berücksichtigt. [Datenquellen mit vollständiger Verarbeitung](full-processing-eol.md) auf Server-Aufrufe vor deren Pensionierung angerechnet werden.
+++

+++ Wie wirken sich Datenquellen auf die Attribution und Gültigkeit von eVars aus?
Wenn eine transactionID zwischen einer Datenquelle und einem Online-Treffer übereinstimmt, gehen die zugehörigen eVar von der gleichen Attribution und Gültigkeit aus wie beim Online-Treffer.

Alle anderen Daten, die über Datenquellen hochgeladen werden, haben keine Attribution oder Gültigkeit.
+++

++ Wie wirken sich Datenquellen auf Standardmetriken wie Seitenansichten, Besuche oder Unique Visitors aus?
Daten, die über Datenquellen hochgeladen werden, wirken sich nicht aus [Seitenansichten](/help/components/metrics/page-views.md), [Besuche](/help/components/metrics/visits.md)oder [Unique Visitors](/help/components/metrics/unique-visitors.md) in irgendeiner Weise. Die einzige Standardmetrik, auf die sie sich auswirken, umfasst [Vorfälle](/help/components/metrics/occurrences.md).
+++

+++ Kann ich Daten löschen, die mithilfe von Datenquellen importiert wurden?

**Nein.** Daten, die mithilfe von Datenquellen in Berichte hochgeladen wurden, werden **dauerhaft**. Sie kann nicht entfernt werden, nicht einmal durch Adobe, nachdem sie importiert wurde. Adobe empfiehlt dringend, Datenquellen-Daten in eine Test-Report Suite hochzuladen, bevor sie in eine Produktions-Report Suite hochgeladen werden.
+++

+++Wie viele Daten kann ich gleichzeitig importieren?

Die Verarbeitung wird angehalten, wenn die Datenmenge 50 MB übersteigt, und wird erst fortgesetzt, wenn die Gesamtmenge unter 50 MB liegt. Stellen Sie sicher, dass die Gesamtgröße aller Dateien auf der FTP-Site weniger als 50 MB beträgt.
+++

++ Was passiert, wenn ich über Datenquellen negative Werte in Berichte einfüge?

Der Wert wird entsprechend verringert. Einige Unternehmen verwenden negative Datenquellenwerte, um zu versuchen, Daten zu korrigieren. Negative Datenquellenwerte können sich auf Berichte auf möglicherweise unerwünschte oder unerwartete Weise auswirken. Adobe empfiehlt, negative Datenquellen nur als letzten Ausweg zu verwenden.
+++

+++Wird bei Dateierweiterungen zwischen Groß- und Kleinschreibung unterschieden?
Ja. Dateien mit der Erweiterung `.TXT` oder `.FIN` nicht verarbeitet werden. Stellen Sie sicher, dass Dateierweiterungen nur in Kleinbuchstaben erfolgen.
+++

++ Wie viele Spalten kann ich zu einer Datenquellendatei hinzufügen?
Sie können beliebig viele Spalten in eine Datenquellendatei aufnehmen, wenn es sich um gültige Spalten handelt. Siehe [Dateiformat](file-format.md) für eine Liste gültiger Variablen-/Spaltennamen.
+++

+++ Kann ich Datenquellen verwenden, ohne den von der Adobe bereitgestellten FTP-Speicherort zu verwenden?
Sie können die [Data Sources-API](https://developer.adobe.com/analytics-apis/docs/1.4/guides/data-sources/), mit dem Sie API-Aufrufe direkt an Adobe senden können. Zu diesen API-Aufrufen gehören `UploadData` -Methode, mit der Sie Daten von einer JSON-Objekt-Payload senden können.
+++
