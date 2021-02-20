---
title: Fehlerbehebung beim Vorhandensein von Daten
description: Erfahren Sie, welche Schritte Sie unternehmen können, wenn keine Daten in Berichten angezeigt werden.
translation-type: tm+mt
source-git-commit: 47b14bde1bb1217bcb172c6d4f01d68f917d44db
workflow-type: tm+mt
source-wordcount: '334'
ht-degree: 4%

---


# Fehlerbehebung beim Vorhandensein von Daten

In Analysis Workspace geben einige Projektinstallationen null Zeilen zurück. In Reports &amp; Analysen gibt die Anzeige bestimmter Berichte die folgende Meldung zurück:

**&quot;Für die gewählten Kriterien liegen keine Daten vor.&quot;**

Gehen Sie wie folgt vor, um zu ermitteln, warum ein Bericht keine Daten anzeigt.

## Daten vorhanden, aber herausgefiltert

Ihre Report Suite enthält Daten, aber die spezifischen Komponenten, die in den Report Filtern verwendet werden, alle Daten werden gelöscht.

* **Segmente**: Mit Segmenten können Sie ganz einfach verhindern, dass alle Daten in einem Bericht angezeigt werden. Überprüfen Sie alle Segmentdefinitionen und entfernen Sie alle Segmente, um festzustellen, ob Ihre Daten aufgrund eines Segments nicht angezeigt werden.
* **Metriken**: Überprüfen Sie, ob die richtigen Metriken verwendet werden. Ändern Sie die Metrik in [Vorfälle](/help/components/metrics/occurrences.md), um sicherzustellen, dass die Metrik nicht der Mitarbeiter eines Berichts ohne Daten ist.
* **Datumsbereiche**: Datumsbereiche, die in der Vergangenheit zu weit zurückliegen oder in der Zukunft liegen, geben keine Daten zurück. Die [Datenaufbewahrungsrichtlinie](data-retention.md) Ihres Unternehmens legt fest, wie weit die Daten zurückgehalten werden.
* **Filter**: Entfernen Sie alle Filter aus dem Bericht.

## Daten nicht vorhanden

Wenn keine Segmente vorhanden sind, ist die Metrik Vorfälle, der Datumsbereich der aktuelle Filter und es gibt keine Suchvorgänge, prüfen Sie Folgendes:

* **Report Suite** überprüfen: Stellen Sie sicher, dass Sie sich in einer Report Suite befinden, die Daten enthält. Viele Unternehmen verfügen über neue Report Suites, Test- oder Entwicklungs-Report Suites, die in der Regel nicht viele Daten enthalten.
* **Latenz**: Wenn Sie sich die neuesten Daten ansehen, werden die Daten möglicherweise verzögert. Weitere Informationen finden Sie unter [Latenzzeit](latency.md).
* **Datenerfassung** überprüfen: Navigieren Sie zu der Webeigenschaft, die Ihre Report Suite verfolgen soll, und öffnen Sie den  [Adobe-Debugger](https://experienceleague.adobe.com/docs/debugger/using/experience-cloud-debugger.html?lang=de-DE). Stellen Sie sicher, dass beim Laden einer Seite eine Analytics-Bildanforderung vorhanden ist. Wenn eine Bildanforderung angezeigt wird, stellen Sie sicher, dass die richtige Report Suite-ID verwendet wird, dass eine gültige [currencyCode](/help/implement/vars/config-vars/currencycode.md) vorhanden ist und dass [Zeitstempelunterstützung](/help/implement/vars/page-vars/timestamp.md) mit der Bildanforderung und der Report Suite übereinstimmt.
