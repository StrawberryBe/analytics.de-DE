---
title: Häufig gestellte Fragen zu Attribution
description: Erhalten Sie Antworten auf häufig gestellte Fragen zur Attribution.
translation-type: tm+mt
source-git-commit: c206095b8024db0e31586abdf9639fba3401ce3f
workflow-type: tm+mt
source-wordcount: '760'
ht-degree: 95%

---


# Häufig gestellte Fragen zu Attribution

**Was ist der Zeileneintrag „Keine“ bei Verwendung von Attribution?**

Das Zeilenelement „Keine“ ist ein Sammelobjekt, der alle Konversionen darstellt, die ohne Touchpoints im Lookback-Fenster stattgefunden haben. Um die Anzahl der Konversionen zu reduzieren, die dem Zeilenelement „Keine“ zugeordnet sind, verwenden Sie ein benutzerdefiniertes Lookback-Fenster mit einem längeren Lookback-Zeitraum.

**Warum sehe ich manchmal Daten außerhalb meines Berichtsfensters, wenn ich Attributionsmodelle verwende?**

Diese zusätzlichen Daten sind auf das Lookback-Fenster des Besucherberichts zurückzuführen. Weitere Informationen finden Sie unter [Daten, die außerhalb des Berichtsfensters angezeigt werden](https://helpx.adobe.com/de/analytics/kb/data-appearing-outside-reporting-window.html) in der Analytics-KB.

**Wann sollte ich ein Besuchs-, Besucher- oder benutzerdefiniertes Attribution-Lookback verwenden?**

Die Auswahl des Attributions-Lookbacks hängt von Ihrem Anwendungsfall ab. Wenn Konversionen in der Regel länger als einen Besuch dauern, wird ein Besucher oder benutzerdefinierte Lookback empfohlen. Für längere Konversionszyklen sind benutzerdefinierte Lookback-Fenster am besten geeignet, da sie der einzige Typ sind, der Daten aus einer Zeit vor dem Berichtsfenster abrufen kann.

**Worin unterscheiden sich Props und eVars bei der Verwendung von Attribution?**

Die Attribution wird zur Laufzeit des Berichts neu berechnet. Es gibt also keinen Unterschied zwischen einer Prop oder einer eVar (oder einer anderen Dimension) hinsichtlich des Attributionsmodells. Eigenschaften können mit jedem Lookback-Fenster oder Attributionsmodell bestehen bleiben und die eVar-Zuordnungs-/Ablaufeinstellungen werden ignoriert.

**Sind Attributionsmodelle in anderen Analytics-Funktionen wie Data Feeds oder Data Warehouse verfügbar?**

Nein. Attributionsmodelle verwenden die Verarbeitung der Berichtszeit, die nur in Analysis Workspace verfügbar ist. Weitere Informationen finden Sie unter [Berichtszeitverarbeitung](/help/components/vrs/vrs-report-time-processing.md).

**Stehen Attributionsmodelle nur dann zur Verfügung, wenn ich eine Virtual Report Suite mit aktivierter Berichtszeitverarbeitung verwende?**

Attributionsmodelle stehen außerhalb der Virtual Report Suites zur Verfügung. Attributionsmodelle verwenden die Berichtszeitverarbeitung im Backend und stehen sowohl für Standard-Report Suites als auch für Virtual Report Suites zur Verfügung.

**Welche Dimensionen und Metriken werden nicht unterstützt?**

Das Attributionsbedienfeld unterstützt alle Dimensionen. Nicht unterstützte Metriken:

* Alle berechneten Metriken
* Unique Visitors
* Besuche
* Vorfälle
* Seitenansichten
* A4T-Metriken
* Besuchszeitmetriken
* Absprünge
* Absprungrate
* Einstiege
* Ausstiege
* Seiten nicht gefunden
* Suchvorgänge
* Einzelseitenbesuche
* Einzelzugriff

**Funktioniert die Attribution mit Klassifizierungen?**

Ja, Klassifizierungen werden vollständig unterstützt.

**Funktioniert Attribution mit Datenquellen?**

Ja, die meisten Datenquellen werden unterstützt. Bei Datenquellen auf Zusammenfassungsebene ist eine Attribution nicht möglich, da sie nicht mit einer Analytics-Besucher-ID verknüpft sind. Als Datenquellen werden auch Transaktions-IDs unterstützt, es sei denn sie werden in einer Virtual Report Suite mit aktivierter Berichtszeitverarbeitung verwendet.

**Funktioniert Attribution mit der Advertising Analytics-Integration?**

Metadatendimensionen wie Übereinstimmungstyp und Keyword funktionieren mit Attribution. Metriken (wie Impressions, Kosten, Klicks, durchschnittliche Position und durchschnittliche Qualitätsbewertung) verwenden jedoch Datenquellen auf Zusammenfassungsebene und sind daher inkompatibel.

**Wie funktioniert die Attribution bei Marketing-Kanälen?**

Als Marketing-Kanäle eingeführt wurden, hatten sie nur die Dimensionen „Erstkontakt“ und „Letztkontakt“. Explizite Dimensionen „Erstkontakt“ und „Letztkontakt“ sind mit der aktuellen Attributionsversion nicht mehr erforderlich. Adobe stellt allgemeine Dimensionen für „Marketing-Kanal“ und „Marketing-Kanal-Detail“ bereit, damit Sie diese mit Ihrem gewünschten Attributionsmodell verwenden können. Diese allgemeinen Dimensionen verhalten sich identisch mit den Dimensionen des Letztkontakt-Kanals, sind jedoch anders gekennzeichnet, um Verwirrung bei der Verwendung von Marketing-Kanälen mit einem anderen Attributionsmodell zu vermeiden.

Da die Marketing-Kanal-Dimensionen von einer traditionellen Besuchsdefinition abhängen (wie in den Verarbeitungsregeln definiert), kann ihre Besuchsdefinition nicht mit Virtual Report Suites geändert werden.

**Wie funktioniert die Attribution mit Variablen mit mehreren Werten, wie z. B. Listenvariablen?**

Einige Dimensionen in Analytics können bei einem einzelnen Hit mehrere Werte enthalten. Häufige Beispiele sind Listenvariablen und die Produktvariable.

Wenn die Attribution auf Hits mit mehreren Werten angewendet wird, erhalten alle Werte im selben Hit dieselbe Gewichtung. Da viele Werte diese Gewichtung erhalten können, kann sich die Berichtssumme von der Summe der einzelnen Zeileneinträge unterscheiden. Die Berichtsgesamtsumme wird dedupliziert, während jedem einzelnen Dimensionselement die korrekte Gutschrift zugeschrieben wird.

**Wie funktioniert die Attribution bei der Segmentierung?**

Die Attribution wird immer vor der Segmentierung ausgeführt und die Segmentierung wird ausgeführt, bevor Berichtsfilter angewendet werden. Dieses Konzept gilt auch für Virtual Report Suites, die Segmente verwenden.

Wenn Sie z. B. eine VRS mit angewendetem Segment „Hits anzeigen“ erstellen, können Sie mithilfe einiger Attributionsmodelle andere Kanäle in einer Tabelle sehen.

![Schreibgeschützte Virtual Report Suite](assets/vrs-aiq-example.png)

>[!NOTE]
>
>Wenn ein Segment Treffer unterdrückt, die Ihre Metrik enthalten, werden diese Metrikinstanzen keiner Dimension zugeordnet. Bei einem ähnlichen Berichtsfilter werden jedoch nur einige Dimensionselemente ausgeblendet, ohne dass sich dies auf die pro Zuordnungsmodell verarbeiteten Metriken auswirkt. Daher kann ein Segment niedrigere Werte zurückgeben als ein Filter mit einer vergleichbaren Definition.
