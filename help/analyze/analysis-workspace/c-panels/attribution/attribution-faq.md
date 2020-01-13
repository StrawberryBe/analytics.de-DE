---
title: Häufig gestellte Fragen zu Attribution
description: Erhalten Sie Antworten auf häufig gestellte Fragen zur Attribution.
translation-type: ht
source-git-commit: 16ba0b12e0f70112f4c10804d0a13c278388ecc2

---


# Häufig gestellte Fragen zu Attribution

**Was ist der Zeileneintrag „Keine“ bei Verwendung von Attribution?**

Das Zeilenelement „Keine“ ist ein Sammelpunkt, der alle Konversionen darstellt, die ohne Touchpoints im Lookback-Fenster stattgefunden haben. Versuchen Sie, einen längeren Zeitraum in Ihr Berichtsfenster aufzunehmen.

**Warum sehe ich manchmal Daten außerhalb meines Berichtsfensters, wenn ich Attributionsmodelle verwende?**

Diese zusätzlichen Daten sind auf das Lookback-Fenster des Besucherberichts zurückzuführen. Weitere Informationen finden Sie unter [Daten, die außerhalb des Berichtsfensters angezeigt werden](https://helpx.adobe.com/de/analytics/kb/data-appearing-outside-reporting-window.html) in der Analytics-KB. Adobe wird diese zusätzlichen Zeilen in einer künftigen Version herausfiltern.

**Kann ich ein benutzerdefiniertes Lookback-Fenster mit meinen Attributionsmodellen verwenden?**

Attributionsmodelle basieren derzeit entweder auf einem Besucher- oder einem Besuchs-Lookback-Fenster. Diese Lookback-Fenster lassen sich entweder durch Änderung des Berichtsdatumsbereichs (für die Besuchersuche) oder durch Verwendung einer benutzerdefinierten Besuchsdefinition als Teil von Virtual Report Suites anpassen. Weitere Informationen finden Sie unter [Berichtszeitverarbeitung](../../../../components/vrs/vrs-report-time-processing.md).

**Wann sollte ich eine Rückmeldung zur Besuchszuordnung oder zur Besucherattribution verwenden?**

Die Auswahl des Attributions-Lookbacks hängt von Ihrem Anwendungsfall ab. Wenn Konversionen in der Regel länger als einen Besuch dauern, wird ein Besucher-Lookback empfohlen. Die Erstellung einer Virtual Report Suite mit einer längeren Besuchsdefinition ist ebenfalls eine potenzielle Lösung.

**Worin unterscheiden sich Props und eVars bei der Verwendung von Attribution?**

Die Attribution wird zur Laufzeit des Berichts neu berechnet. Es gibt also keinen Unterschied zwischen einer Prop oder einer eVar (oder einer anderen Dimension) hinsichtlich des Attributionsmodells. Eigenschaften können mit jedem Lookback-Fenster oder Attributionsmodell bestehen bleiben und die eVar-Zuordnungs-/Ablaufeinstellungen werden ignoriert.

**Sind Attributionsmodelle in anderen Analytics-Funktionen wie Data Feeds oder Data Warehouse verfügbar?**

Nein. Attributionsmodelle verwenden die Verarbeitung der Berichtszeit, die nur in Analysis Workspace verfügbar ist. Weitere Informationen finden Sie unter [Berichtszeitverarbeitung](../../../../components/vrs/vrs-report-time-processing.md).

**Stehen Attributionsmodelle nur dann zur Verfügung, wenn ich eine Virtual Report Suite mit aktivierter Berichtszeitverarbeitung verwende?**

Attributionsmodelle stehen außerhalb der Virtual Report Suites zur Verfügung. Attributionsmodelle verwenden die Berichtszeitverarbeitung im Backend und stehen sowohl für Standard-Report Suites als auch für Virtual Report Suites zur Verfügung.

**Welche Dimensionen und Metriken werden nicht unterstützt?**

Das Attributionsbedienfeld unterstützt alle Dimensionen. Nicht unterstützte Metriken:

* Unique Visitors
* Besuche
* Vorfälle
* Seitenansichten
* A4T-Metriken
* Besuchszeitmetriken
* Absprünge
* Absprungrate
* Einträge
* Ausstiege
* Seiten nicht gefunden
* Suchvorgänge
* Einzelseitenbesuche
* Einzelzugriff

**Wie unterscheidet sich die Attribution in Analysis Workspace von der Attribution in Data Workbench?**

Data Workbench bietet stufenweise Folgendes:

* Die Fähigkeit, eine Attribution über weitere Datenquellen auf Besucherebene vorzunehmen, beispielsweise Anzeigen-Impressions und Point of Sale.
* Algorithmische Modellierung. Die Attribution in Analysis Workspace umfasst nur regelbasierte Modelle. Siehe [Best fit-Modellierung](https://marketing.adobe.com/resources/help/en_US/insight/client/c_attrib_algorithmic.html) im Data Workbench-Benutzerhandbuch.
* Zusätzliche Visualisierungen, beispielsweise Wartezeittabellen. Siehe [Latenztabellen](https://marketing.adobe.com/resources/help/en_US/insight/client/c_lat_tbls.html) im Data Workbench-Benutzerhandbuch.

**Funktioniert die Attribution mit Klassifizierungen?**

Ja, Klassifizierungen werden vollständig unterstützt.

**Funktioniert Attribution mit Datenquellen?**

Ja, die meisten Datenquellen werden unterstützt. Bei Datenquellen auf Zusammenfassungsebene ist eine Attribution nicht möglich, da sie nicht mit einer Analytics-Besucher-ID verknüpft sind. Als Datenquellen werden auch Transaktions-IDs unterstützt, es sei denn sie werden in einer Virtual Report Suite mit aktivierter Berichtszeitverarbeitung verwendet.

**Funktioniert Attribution mit der Advertising Analytics-Integration?**

Metadatendimensionen wie Übereinstimmungstyp und Suchbegriff funktionieren mit Attribution. Metriken (wie Impressions, Kosten, Klicks, durchschnittliche Position und durchschnittliche Qualitätsbewertung) verwenden jedoch Datenquellen auf Zusammenfassungsebene und sind daher inkompatibel.
