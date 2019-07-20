---
description: Adobe Analytics bietet eine flexible Berichtsoberfläche, mit der Sie eine Vielzahl an komplexen Berichten generieren können. Während die meisten Berichte sehr schnell generiert werden, kann es bei manchen Berichten auch zu Timeouts oder Fehlern bei der Generierung kommen. Um Fehler bei der Berichtgenerierung zu vermeiden, werden in diesem Abschnitt zahlreiche Faktoren erläutert, die sich auf die Geschwindigkeit bei der Berichtgenerierung auswirken. Anhand dieser Informationen können Sie Berichte so strukturieren, dass Sie eher erfolgreich generiert werden können.
keywords: Best Practices; Fehler; timeout; Fehlerbehebung; langsam
seo-description: Adobe Analytics bietet eine flexible Berichtsoberfläche, mit der Sie eine Vielzahl an komplexen Berichten generieren können. Während die meisten Berichte sehr schnell generiert werden, kann es bei manchen Berichten auch zu Timeouts oder Fehlern bei der Generierung kommen. Um Fehler bei der Berichtgenerierung zu vermeiden, werden in diesem Abschnitt zahlreiche Faktoren erläutert, die sich auf die Geschwindigkeit bei der Berichtgenerierung auswirken. Anhand dieser Informationen können Sie Berichte so strukturieren, dass Sie eher erfolgreich generiert werden können.
seo-title: Best Practices und Fehlerbehebung für Berichterstellung
solution: Analytics
title: Best Practices und Fehlerbehebung für Berichterstellung
topic: 'Berichte    '
uuid: d 4 eef 0 a 3-1 d 26-4460-8 a 2 b -962001 c 9 f 846
translation-type: tm+mt
source-git-commit: 0d4e5bfc0f45b7b3ed9b89df25bcef0730a011d9

---


# Best Practices und Fehlerbehebung für Berichterstellung

Adobe Analytics bietet eine flexible Berichtsoberfläche, mit der Sie eine Vielzahl an komplexen Berichten generieren können. Während die meisten Berichte sehr schnell generiert werden, kann es bei manchen Berichten auch zu Timeouts oder Fehlern bei der Generierung kommen. Um Fehler bei der Berichtgenerierung zu vermeiden, werden in diesem Abschnitt zahlreiche Faktoren erläutert, die sich auf die Geschwindigkeit bei der Berichtgenerierung auswirken. Anhand dieser Informationen können Sie Berichte so strukturieren, dass Sie eher erfolgreich generiert werden können.

>[!Note]
>Diese Empfehlungen gelten für Reports &amp; Analysen, Ad-hoc-Analysen und Reportbuilder.
>They do not apply to Analysis Workspace, which has its own set of [best practices](/help/analyze/analysis-workspace/optimizing-performance.md). They also do not &gt;apply to Data Warehouse [best practices](https://marketing.adobe.com/resources/help/en_US/reference/?f=data_warehouse_bp). Ein weiterer Satz an
>[Best Practices](https://marketing.adobe.com/developer/en_US/get-started/best-practices/c-best-practices) sind für die Adobe Analytics Reporting-API verfügbar.

## Bericht-Timeouts und Anforderungswarteschlange {#section_A42AD7E487C749B7B879BAFA814FFEF9}

**Timeouts**

Ein einzelner Bericht ist in mehrere Anforderungen unterteilt (eine pro Aufschlüsselung), und jede Anforderung unterliegt einem individuellen Timeout. Terminierte Berichte erhalten längere Timeout-Intervalle und haben eine größere Erfolgswahrscheinlichkeit als Berichte, die direkt in einer Benutzeroberfläche generiert werden.

**Report Suite-Warteschlange**

Jede Report Suite pflegt eine eigene Anforderungswarteschlange. Wenn zahlreiche Berichte gleichzeitig angefordert werden (selbst von unterschiedlichen Benutzern), wird eine geringe Anzahl an Berichten gleichzeitig generiert. Nach dem Abschluss von Berichten werden verbleibende Berichte in der Reihenfolge generiert, in der sie eingegangen sind. Wenn also bereits zahlreiche komplexe Berichte in der Report Suite-Warteschlange enthalten sind, kann es bei einem Bericht, der normalerweise schnell generiert wird, zu einem Timeout kommen.

## Faktoren, die sich auf die Berichtgeschwindigkeit auswirken {#section_6BA937EB6CEC4CBCB71FAAD32F031DC2}

Die folgenden Faktoren tragen zu längeren Berichtgenerierungszeiten bei. Wenn Sie einen dieser Faktoren erhöhen, kommt es möglicherweise nicht zu einem Timeout für diesen Bericht. Es können aber andere Berichte in der Report Suite-Warteschlange verzögert werden, wodurch bei einem nachfolgenden Bericht möglicherweise ein Timeout auftritt.

**Berichtszeitraum**

Der Hauptfaktor, der sich auf die Berichtgenerierungszeit auswirkt, ist die Anzahl der angeforderten Monate. Wenn Sie die Anzahl der Monate von drei auf eins verringern, wird die Generierungszeit erheblich verkürzt. Wenn Sie den Zeitraum aber von einem Monat auf eine Woche reduzieren, hat dies keine großen Auswirkungen auf die Berichtgenerierungszeit.

**Anzahl der Metriken**

Je höher die Anzahl der Metriken, desto länger die Berichtausführungszeit. Durch Entfernen von Metriken kann die Berichtgenerierungszeit häufig verbessert werden.

**Anzahl der Aufschlüsselungen**

Jede Aufschlüsselung steht für eine eigene Anforderung in einem Bericht. Während individuelle Anforderungen schnell abgeschlossen werden können, kann die Ausführung von Tausenden Aufschlüsselungen in einem einzelnen Bericht die Berichtgenerierungszeit erheblich verlangsamen und die Report Suite-Warteschlange beeinträchtigen.

**Segmentkomplexität**

Segmente für zahlreiche Dimensionen oder mit vielen (mehr als 24) Regeln erhöhen die Verarbeitungsauswirkungen und verlängern die Berichtgenerierungszeit.

**Anzahl der eindeutigen Werte**

Berichte mit Hunderttausenden eindeutigen Werten werden langsamer generiert als Berichte mit weniger eindeutigen Werten, selbst wenn das Segment oder der Filter die Anzahl der Werte reduziert, die schließlich in einem Bericht angezeigt werden. Beispiel: Ein Bericht, der Suchbegriffe anzeigt, wird im Allgemeinen langsamer generiert als andere Berichte, selbst wenn ein Filter angewendet wurde, um nur Suchbegriffe anzuzeigen, die einen bestimmen Wert enthalten.

## Andere Berichtsoptionen {#section_FEF85C7FC6E14755A6086AFFF36E0EB4}

Zusätzlich zur Reduzierung des Zeitraums, der Anzahl der Metriken und der Anzahl der Aufschlüsselungen in einem Bericht können auch die folgenden Richtlinien dabei helfen, die Zuverlässigkeit bei der Berichterstellung zu verbessern:

* Verwenden Sie Data Warehouse, um Berichte anzufordern, die zahlreiche Aufschlüsselungen oder Metriken enthalten. Data Warehouse wurde für die Generierung dieser Berichtstypen entwickelt.
* Planen Sie Berichte so, dass sie außerhalb der Spitzenzeiten ausgeführt werden. Dadurch wird die Wahrscheinlichkeit, dass ein Bericht zurückgegeben wird, erhöht, da die Anforderungswarteschlange für eine Report Suite in diesen Zeiten eher leer ist.
* Sie können Report Builder verwenden, um Berichte in kleinere Zeiträume und Anforderungen mit weniger Metriken einzuteilen. Dann können Sie mit der nativen Excel-Funktionalität Daten aus verschiedenen Anforderungen in einem Bericht zusammenführen.

