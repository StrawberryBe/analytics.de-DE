---
title: Fehlerbehebung bei der Datenpräsenz
description: Erfahren Sie, welche Schritte Sie ausführen können, wenn keine Daten in Berichten angezeigt werden.
source-git-commit: f669af03a502d8a24cea3047b96ec7cba7c59e6f
workflow-type: ht
source-wordcount: '332'
ht-degree: 100%

---


# Fehlerbehebung bei der Datenpräsenz

In Analysis Workspace geben einige Projekteinstellungen null Zeilen zurück. In Reports &amp; Analytics wird bei der Anzeige bestimmter Berichte die folgende Meldung zurückgegeben:

**„Für die gewählten Kriterien liegen keine Daten vor.“**

Verwenden Sie die folgenden Schritte, um zu ermitteln, warum ein Bericht keine Daten anzeigt.

## Daten existieren, werden aber herausgefiltert

Ihre Report Suite enthält Daten, aber die im Bericht verwendeten spezifischen Komponenten filtern alle Daten heraus.

* **Segmente**: Durch Segmente können Sie ganz einfach verhindern, dass alle Daten in einem Bericht angezeigt werden. Überprüfen Sie alle Segmentdefinitionen und entfernen Sie alle Segmente, um festzustellen, ob Ihre Daten durch ein Segment nicht angezeigt werden.
* **Metriken**: Überprüfen Sie, ob die richtigen Metriken verwendet werden. Ändern Sie die Metrik in [Vorfälle](/help/components/metrics/occurrences.md), um sicherzustellen, dass die Metrik nicht der Beitragende zu einem Bericht ohne Daten ist.
* **Datumsbereiche**: Datumsbereiche, die zu weit in der Vergangenheit oder zu einem späteren Zeitpunkt liegen, geben keine Daten zurück. Die [Richtlinie zur Datenaufbewahrung](data-retention.md) Ihres Unternehmens bestimmt, wie weit zurückliegende Daten aufbewahrt werden.
* **Filter**: Entfernen Sie alle Suchfilter aus dem Bericht.

## Keine Daten vorhanden

Wenn keine Segmente vorhanden sind, die Metrik „Instanzen“ lautet, der Datumsbereich der aktuelle Monat ist und es keine Suchfilter gibt, überprüfen Sie Folgendes:

* **Überprüfen der Report Suite**: Stellen Sie sicher, dass Sie sich in einer Report Suite befinden, die Daten enthält. Viele Unternehmen verfügen über neue Test- oder Entwicklungs-Report Suites, die normalerweise nicht viele Daten enthalten.
* **Latenz**: Bei der Anzeige aktueller Daten können die Daten verzögert sein. Weitere Informationen finden Sie unter [Latenz](latency.md).
* **Validieren der Datenerfassung**: Navigieren Sie zur Web-Eigenschaft, die Ihre Report Suite verfolgen soll, und öffnen Sie den [Adobe-Debugger](https://experienceleague.adobe.com/docs/debugger/using/experience-cloud-debugger.html?lang=de). Stellen Sie sicher, dass beim Laden einer Seite eine Analytics-Bildanforderung vorhanden ist. Wenn eine Bildanforderung angezeigt wird, stellen Sie sicher, dass sie die richtige Report Suite-ID verwendet, einen gültigen [currencyCode](/help/implement/vars/config-vars/currencycode.md) enthält und dass die [Zeitstempelunterstützung](/help/implement/vars/page-vars/timestamp.md) zwischen der Bildanforderung und der Report Suite übereinstimmt.
