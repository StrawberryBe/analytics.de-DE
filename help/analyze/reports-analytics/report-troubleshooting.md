---
title: Best Practices und Fehlerbehebung für das Reporting
description: Best Practices und Tipps zur Fehlerbehebung beim Generieren von Berichten.
keywords: Best Practices, Fehler, Timeout, Fehlerbehebung, langsam
role: Geschäftspraktiker, Administrator
translation-type: tm+mt
source-git-commit: 894ee7a8f761f7aa2590e06708be82e7ecfa3f6d
workflow-type: tm+mt
source-wordcount: '576'
ht-degree: 97%

---


# Best Practices und Fehlerbehebung für das Reporting

*Diese Hilfeseite bezieht sich auf die Best Practices für Reports &amp; Analytics. Weitere Informationen zu Analysis Workspace finden Sie unter [Optimieren der Analysis Workspace-Leistung](../analysis-workspace/workspace-faq/optimizing-performance.md).  Weitere Informationen zu Data Warehouse finden Sie unter [Best Practices für Data Warehouse](/help/export/data-warehouse/data-warehouse-bp.md).*

Adobe Analytics bietet eine flexible Berichtsoberfläche, mit der Sie eine Vielzahl an komplexen Berichten generieren können. Während die meisten Berichte sehr schnell generiert werden, kann es bei manchen Berichten auch zu Timeouts oder Fehlern bei der Generierung kommen. Auf dieser Seite werden Faktoren erläutert, die sich auf die Geschwindigkeit der Berichtgenerierung auswirken. Anhand dieser Informationen können Sie Berichte so strukturieren, dass sie eher erfolgreich generiert werden können.

## Bericht-Timeouts und Anforderungswarteschlange

* **Timeouts**: Ein einzelner Bericht ist in mehrere Anforderungen unterteilt (eine pro Aufschlüsselung) und jede Anforderung unterliegt einem individuellen Timeout. Terminierte Berichte erhalten längere Timeout-Intervalle und haben eine größere Erfolgswahrscheinlichkeit als Berichte, die direkt in einer Benutzeroberfläche generiert werden.
* **Report Suite-Warteschlange**: Jede Report Suite pflegt eine eigene Anforderungswarteschlange. Wenn zahlreiche Berichte gleichzeitig angefordert werden (selbst von unterschiedlichen Benutzern), wird eine geringe Anzahl an Berichten gleichzeitig generiert. Nach dem Abschluss von Berichten werden verbleibende Berichte in der Reihenfolge generiert, in der sie eingegangen sind. Wenn also bereits zahlreiche komplexe Berichte in der Report Suite-Warteschlange enthalten sind, kann es bei einem Bericht, der normalerweise schnell generiert wird, zu einem Timeout kommen.

## Faktoren, die sich auf die Berichtgeschwindigkeit auswirken

Die folgenden Faktoren tragen zu längeren Berichtgenerierungszeiten bei. Eine Erhöhung eines dieser Faktoren hat in der Regel keine Auswirkungen auf die Leistung, kann jedoch andere Berichte in der Report Suite-Warteschlange verzögern und zu einem Timeout in einem nachfolgenden Bericht führen.

* **Berichtszeitraum**: Der Hauptfaktor, der sich auf die Berichtgenerierungszeit auswirkt, ist die Anzahl der angeforderten Monate. Wenn Sie die Anzahl der Monate von drei auf eins verringern, wird die Generierungszeit erheblich verkürzt. Wenn Sie den Zeitraum aber von einem Monat auf eine Woche reduzieren, hat dies keine großen Auswirkungen auf die Berichtgenerierungszeit.
* **Anzahl der Metriken**: Je höher die Anzahl der Metriken, desto länger die Berichtausführungszeit. Durch Entfernen von Metriken kann die Berichtgenerierungszeit häufig verbessert werden.
* **Anzahl der Aufschlüsselungen**: Innerhalb eines Berichts stellt jede Aufschlüsselung eine separate Anforderung dar. Während individuelle Anforderungen schnell abgeschlossen werden können, kann die Ausführung von Tausenden Aufschlüsselungen in einem einzelnen Bericht die Berichtgenerierungszeit erheblich verlangsamen und die Report Suite-Warteschlange beeinträchtigen.
* **Segmentkomplexität**: Segmente für zahlreiche Dimensionen oder mit vielen (mehr als 24) Regeln erhöhen die Verarbeitungsauswirkungen und verlängern die Berichtgenerierungszeit.
* **Anzahl eindeutiger Werte**: Berichte mit Hunderttausenden eindeutigen Werten werden langsamer generiert als Berichte mit weniger eindeutigen Werten, selbst wenn das Segment oder der Filter die Anzahl der Werte reduziert, die schließlich in einem Bericht angezeigt werden. Beispiel: Ein Bericht, der Suchbegriffe anzeigt, wird im Allgemeinen langsamer generiert als andere Berichte, selbst wenn ein Filter angewendet wurde, um nur Suchbegriffe anzuzeigen, die einen bestimmen Wert enthalten.

## Andere Berichterstellungsoptionen

Die folgenden Richtlinien helfen, die Zuverlässigkeit des Berichtversands zu erhöhen:

* Verwenden Sie Data Warehouse, um Berichte anzufordern, die zahlreiche Aufschlüsselungen oder Metriken enthalten. Data Warehouse wurde für die Generierung dieser Berichtstypen entwickelt.
* Planen Sie Berichte so, dass sie außerhalb der Spitzenzeiten ausgeführt werden. Dadurch wird die Wahrscheinlichkeit, dass ein Bericht zurückgegeben wird, erhöht, da die Anforderungswarteschlange für eine Report Suite in diesen Zeiten eher leer ist.
* Sie können Report Builder verwenden, um Berichte in kleinere Zeiträume und Anforderungen mit weniger Metriken einzuteilen. Dann können Sie mit der nativen Excel-Funktionalität Daten aus verschiedenen Anforderungen in einem Bericht zusammenführen.
