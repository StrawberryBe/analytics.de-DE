---
description: Adobe Analytics bietet eine flexible Benutzeroberfläche für Berichte, mit der Sie eine Vielzahl komplexer Berichte erstellen können. Während die meisten Berichte sehr schnell generiert werden, kann es vorkommen, dass ein Timeout auftritt oder die Erstellung fehlschlägt. Um Fehler bei der Berichtgenerierung zu vermeiden, werden in diesem Abschnitt viele Faktoren erläutert, die sich auf die Geschwindigkeit der Berichtgenerierung auswirken. Anhand dieser Informationen können Sie Berichte so strukturieren, dass eine erfolgreiche Erstellung wahrscheinlicher ist.
keywords: best practices;failure;timeout;troubleshooting;slow
title: Best Practices und Fehlerbehebung für Berichterstellung
topic: Reports
uuid: d4eef0a3-1d26-4460-8a2b-962001c9f846
translation-type: tm+mt
source-git-commit: dca5bac72a2cf5f5ded5072e1867676392a7850e

---


# Best Practices und Fehlerbehebung für Berichterstellung

Adobe Analytics bietet eine flexible Benutzeroberfläche für Berichte, mit der Sie eine Vielzahl komplexer Berichte erstellen können. Während die meisten Berichte sehr schnell generiert werden, kann es vorkommen, dass ein Timeout auftritt oder die Erstellung fehlschlägt. Um Fehler bei der Berichtgenerierung zu vermeiden, werden in diesem Abschnitt viele Faktoren erläutert, die sich auf die Geschwindigkeit der Berichtgenerierung auswirken. Anhand dieser Informationen können Sie Berichte so strukturieren, dass eine erfolgreiche Erstellung wahrscheinlicher ist.

>[!Note]
>Diese Empfehlungen gelten für Reports &amp; Analytics, Ad Hoc Analysis und Report Builder.
>Sie gelten nicht für Analysis Workspace, da es dafür eigene [Best Practices](/help/analyze/analysis-workspace/workspace-faqs/optimizing-performance.md) gibt. Sie gelten auch nicht für die [Best Practices](https://marketing.adobe.com/resources/help/en_US/reference/data_warehouse_bp.html) für Data Warehouse. Ein weiterer Satz
>[Best Practices](https://marketing.adobe.com/developer/en_US/get-started/best-practices/c-best-practices) ist für die Reporting-API von Adobe Analytics verfügbar.

## Bericht-Timeouts und Anforderungswarteschlange {#section_A42AD7E487C749B7B879BAFA814FFEF9}

**Timeouts**

Ein einzelner Bericht wird in mehrere Anforderungen unterteilt (eine pro Aufschlüsselung), und jede Anforderung unterliegt einem individuellen Timeout. Terminierte Berichte erhalten längere Timeout-Zeiträume und sind wahrscheinlicher als direkt in der Benutzeroberfläche erstellte Berichte.

**Report Suite-Warteschlange**

Jede Report Suite führt eine separate Anforderungswarteschlange. Wenn viele Berichte gleichzeitig angefordert werden, auch von separaten Benutzern, wird eine kleine Anzahl von Berichten gleichzeitig generiert. Nach Abschluss der Berichte werden die verbleibenden Berichte in der Reihenfolge generiert, in der sie empfangen wurden. Wenn sich daher bereits eine große Anzahl komplexer Berichte in der Report Suite-Warteschlange befinden, kann es vorkommen, dass ein Bericht, der in der Regel schnell generiert wird, einen Timeout aufweist.

## Faktoren, die sich auf die Berichtgeschwindigkeit auswirken  {#section_6BA937EB6CEC4CBCB71FAAD32F031DC2}

Die folgenden Faktoren tragen zu längeren Berichtgenerierungszeiten bei. Das Erhöhen eines dieser Faktoren führt möglicherweise nicht zu einem Timeout für diesen Bericht, kann jedoch zu Verzögerungen bei anderen Berichten in der Report Suite-Warteschlange führen und zu einem Timeout in einem nachfolgenden Bericht.

**Berichtszeitraum**

Der größte Faktor, der sich auf die Berichtgenerierungszeit auswirkt, ist die Anzahl der angeforderten Monate. Wenn Sie die Anzahl der Monate von drei auf eins reduzieren, verringert sich die Generierungszeit erheblich, aber eine Reduzierung des Zeitraums von einem Monat auf eine Woche hat keine großen Auswirkungen auf die Berichtgenerierungszeit.

**Anzahl der Metriken**

Mit zunehmender Anzahl der Metriken steigt die Berichtslaufzeit. Durch Entfernen von Metriken wird die Berichtgenerierungszeit oft verkürzt.

**Anzahl der Aufschlüsselungen**

Innerhalb eines Berichts stellt jede Aufschlüsselung eine separate Anforderung dar. Während einzelne Anforderungen schnell abgeschlossen werden können, kann die Ausführung von Tausenden von Aufschlüsselungen in einem einzelnen Bericht die Berichtgenerierungszeit erheblich verlangsamen und die Report Suite-Warteschlange beeinträchtigen.

**Segmentkomplexität**

Segmente, die viele Dimensionen berücksichtigen oder über viele (über 24) Regeln verfügen, erhöhen die Verarbeitungsauswirkungen und erhöhen die Berichtgenerierungszeit.

**Anzahl der eindeutigen Werte**

Berichte mit Hunderttausenden individueller Werte werden langsamer generiert als Berichte mit weniger eindeutigen Werten, selbst wenn das Segment oder der Filter die Anzahl der Werte reduziert, die letztendlich in einem Bericht erscheinen. Ein Bericht, der Suchbegriffe anzeigt, generiert in der Regel langsamer als andere Berichte, selbst wenn ein Filter angewendet wird, um nur Suchbegriffe anzuzeigen, die einen bestimmten Wert enthalten.

## Andere Berichtsoptionen  {#section_FEF85C7FC6E14755A6086AFFF36E0EB4}

Zusätzlich zur Reduzierung des Zeitraums, der Anzahl der Metriken und der Anzahl der Aufschlüsselungen in einem Bericht können auch die folgenden Richtlinien dabei helfen, die Zuverlässigkeit bei der Berichterstellung zu verbessern:

* Verwenden Sie Data Warehouse, um Berichte anzufordern, die viele Aufschlüsselungen oder Metriken enthalten. Data Warehouse wurde zur Erstellung dieser Berichtstypen entwickelt.
* Planen Sie Berichte, die nicht zu Spitzenzeiten ausgeführt werden. Dadurch erhöht sich die Wahrscheinlichkeit, dass ein Bericht zurückgegeben wird, da die Anforderungswarteschlange für eine Report Suite in diesen Zeiten mit größerer Wahrscheinlichkeit leer ist.
* ReportBuilder kann verwendet werden, um Berichte in kleinere Zeiträume und Anforderungen mit weniger Metriken zu unterteilen. Anschließend können Sie mithilfe der nativen Excel-Funktion Daten aus verschiedenen Anforderungen in einem einzelnen Bericht zusammenführen.

