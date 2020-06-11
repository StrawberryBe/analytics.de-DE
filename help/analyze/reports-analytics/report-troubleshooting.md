---
title: Best Practices und Fehlerbehebung für Berichte
description: Best Practices und Tipps zur Fehlerbehebung beim Generieren von Berichten.
keywords: best practices;failure;timeout;troubleshooting;slow
translation-type: tm+mt
source-git-commit: 1968162d856b6a74bc61f22f2e5a6b1599d04c79
workflow-type: tm+mt
source-wordcount: '567'
ht-degree: 58%

---


# Best Practices und Fehlerbehebung für Berichte

*Diese Hilfeseite bezieht sich auf die Best Practices von Reports &amp; Analysen. Informationen zu Analyse Workspace finden Sie unter[Optimieren der Leistung](../analysis-workspace/workspace-faq/optimizing-performance.md)von Analyse Workspace. Informationen zu Data Warehouse finden Sie unter Best Practices für[Data Warehouse](/help/export/data-warehouse/data-warehouse-bp.md).*

Adobe Analytics bietet eine flexible Berichtsoberfläche, mit der Sie eine Vielzahl an komplexen Berichten generieren können. Während die meisten Berichte sehr schnell generiert werden, können Sie auf Berichte mit einem Timeout oder einem Fehler bei der Generierung stoßen. Auf dieser Seite werden Faktoren erläutert, die die Geschwindigkeit der Berichtgenerierung beeinflussen. Anhand dieser Informationen können Sie Berichte so strukturieren, dass sie mit größerer Wahrscheinlichkeit erfolgreich generiert werden.

## Zeitüberschreitungen und Anforderungswarteschlange

* **Timeouts**: Ein einzelner Bericht wird in mehrere Anforderungen unterteilt (eine pro Aufschlüsselung), und jede Anforderung unterliegt einem individuellen Timeout. Terminierte Berichte erhalten längere Timeout-Intervalle und haben eine größere Erfolgswahrscheinlichkeit als Berichte, die direkt in einer Benutzeroberfläche generiert werden.
* **Report Suite-Warteschlange**: Jede Report Suite pflegt eine eigene Anforderungswarteschlange. Wenn zahlreiche Berichte gleichzeitig angefordert werden (selbst von unterschiedlichen Benutzern), wird eine geringe Anzahl an Berichten gleichzeitig generiert. Nach dem Abschluss von Berichten werden verbleibende Berichte in der Reihenfolge generiert, in der sie eingegangen sind. Wenn also bereits zahlreiche komplexe Berichte in der Report Suite-Warteschlange enthalten sind, kann es bei einem Bericht, der normalerweise schnell generiert wird, zu einem Timeout kommen.

## Faktoren, die sich auf die Berichtsgeschwindigkeit auswirken

Die folgenden Faktoren tragen zu längeren Berichtgenerierungszeiten bei. Eine Erhöhung eines dieser Faktoren hat in der Regel keine Auswirkungen auf die Leistung, kann jedoch andere Berichte in der Report Suite-Warteschlange verzögern und zu einem Timeout in einem nachfolgenden Bericht führen.

* **Berichtszeitraum**: Der größte Faktor, der sich auf die Berichtgenerierungszeit auswirkt, ist die Anzahl der angeforderten Monate. Wenn Sie die Anzahl der Monate von drei auf eins verringern, wird die Generierungszeit erheblich verkürzt. Wenn Sie den Zeitraum aber von einem Monat auf eine Woche reduzieren, hat dies keine großen Auswirkungen auf die Berichtgenerierungszeit.
* **Anzahl der Metriken**: Je höher die Anzahl der Metriken, desto länger die Berichtausführungszeit. Durch Entfernen von Metriken kann die Berichtgenerierungszeit häufig verbessert werden.
* **Anzahl der Aufschlüsselungen**: Jede Aufschlüsselung steht für eine eigene Anforderung in einem Bericht. Während individuelle Anforderungen schnell abgeschlossen werden können, kann die Ausführung von Tausenden Aufschlüsselungen in einem einzelnen Bericht die Berichtgenerierungszeit erheblich verlangsamen und die Report Suite-Warteschlange beeinträchtigen.
* **Segmentkomplexität**: Segmente, die viele Dimensionen berücksichtigen oder über viele (über 24) Regeln verfügen, erhöhen die Verarbeitungsauswirkungen und erhöhen die Berichtgenerierungszeit.
* **Anzahl der eindeutigen Werte**: Berichte mit Hunderttausenden individueller Werte werden langsamer generiert als Berichte mit weniger eindeutigen Werten, selbst wenn das Segment oder der Filter die Anzahl der Werte reduziert, die letztendlich in einem Bericht erscheinen. Beispiel: Ein Bericht, der Suchbegriffe anzeigt, wird im Allgemeinen langsamer generiert als andere Berichte, selbst wenn ein Filter angewendet wurde, um nur Suchbegriffe anzuzeigen, die einen bestimmen Wert enthalten.

## Andere Optionen für Berichte

Die folgenden Richtlinien helfen, die Zuverlässigkeit des Versands von Berichten zu erhöhen:

* Verwenden Sie Data Warehouse, um Berichte anzufordern, die zahlreiche Aufschlüsselungen oder Metriken enthalten. Data Warehouse wurde für die Generierung dieser Berichtstypen entwickelt.
* Planen Sie Berichte so, dass sie außerhalb der Spitzenzeiten ausgeführt werden. Dadurch wird die Wahrscheinlichkeit, dass ein Bericht zurückgegeben wird, erhöht, da die Anforderungswarteschlange für eine Report Suite in diesen Zeiten eher leer ist.
* Sie können Report Builder verwenden, um Berichte in kleinere Zeiträume und Anforderungen mit weniger Metriken einzuteilen. Dann können Sie mit der nativen Excel-Funktionalität Daten aus verschiedenen Anforderungen in einem Bericht zusammenführen.
