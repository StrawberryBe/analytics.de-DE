---
title: Häufig gestellte Fragen zur Zuordnung
seo-title: Häufig gestellte Fragen zur Zuordnung
description: Erhalten Sie Antworten auf häufig gestellte Fragen zur Zuordnung.
translation-type: tm+mt
source-git-commit: a2c38c2cf3a2c1451e2c60e003ebe1fa9bfd145d

---


# Häufig gestellte Fragen zur Zuordnung

**Was ist der Zeileneintrag "Keine"bei Verwendung der Zuordnung?**

Das Zeilenelement "Keine"ist ein Sammelpunkt, der alle Konvertierungen darstellt, die ohne Berührungspunkte im Lookback-Fenster stattgefunden haben. Versuchen Sie, einen längeren Zeitraum in Ihr Berichtsfenster aufzunehmen.

**Warum sehe ich manchmal Daten außerhalb meines Berichtsfensters, wenn ich Zuordnungsmodelle verwende?**

Diese zusätzlichen Daten sind auf das Lookback-Fenster des Besucherberichts zurückzuführen. Weitere Informationen finden Sie unter [Daten, die außerhalb des Berichtsfensters](https://helpx.adobe.com/analytics/kb/data-appearing-outside-reporting-window.html) in der Analytics-KB angezeigt werden. Adobe plant, diese zusätzlichen Zeilen in einer kommenden Version auszufiltern.

**Kann ich ein benutzerdefiniertes Lookback-Fenster mit meinen Zuordnungsmodellen verwenden?**

Zuordnungsmodelle basieren derzeit entweder auf einem Besucher- oder einem Besuchs-Lookback-Fenster. Diese Lookback-Fenster lassen sich entweder durch Änderung des Berichtsdatumsbereichs (für die Besuchersuche) oder durch Verwendung einer benutzerdefinierten Besuchsdefinition als Teil von Virtual Report Suites anpassen. Weitere Informationen finden Sie unter [Berichtszeitverarbeitung](../../../../components/vrs/vrs-report-time-processing.md) .

**Wann sollte ich eine Rückmeldung zur Besuchszuordnung oder zur Besucherzuordnung verwenden?**

Die Wahl der Zuordnungs-Lookback hängt von Ihrem Anwendungsfall ab. Wenn Konversionen in der Regel länger als ein einzelner Besuch dauern, wird eine Rückkopplung des Besuchers empfohlen. Die Erstellung einer Virtual Report Suite mit einer längeren Besuchsdefinition ist ebenfalls eine potenzielle Lösung.

**Wie vergleichen Props und eVars bei der Verwendung von Attributen?**

Die Zuordnung wird zur Laufzeit des Berichts neu berechnet. Es gibt also keinen Unterschied zwischen einer Prop oder einer eVar (oder einer anderen Dimension), um das Zuordnungsmodell zu erhalten. Eigenschaften können mit jedem Lookback-Fenster oder Zuordnungsmodell bestehen bleiben, und die eVar-Zuordnungs-/Ablaufeinstellungen werden ignoriert.

**Sind Zuordnungsmodelle in anderen Analytics-Funktionen wie Data Feeds oder Data Warehouse verfügbar?**

Nein. Zuordnungsmodelle verwenden die Verarbeitung der Berichtszeit, die nur in Analysis Workspace verfügbar ist. Weitere Informationen finden Sie unter [Berichtszeitverarbeitung](../../../../components/vrs/vrs-report-time-processing.md) .

**Sind Zuordnungsmodelle nur verfügbar, wenn ich eine Virtual Report Suite mit aktivierter Berichtszeitverarbeitung verwende?**

Zuordnungsmodelle stehen außerhalb der Virtual Report Suites zur Verfügung. Während sie die Berichtszeitverarbeitung im Backend verwenden, stehen Zuordnungsmodelle sowohl für Standard-Report Suites als auch für Virtual Report Suites zur Verfügung.

**Welche Dimensionen und Metriken werden nicht unterstützt?**

Das Zuordnungsbedienfeld unterstützt alle Dimensionen. Nicht unterstützte Metriken:

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

**Wie unterscheidet sich die Zuordnung im Analysis Workspace von der Zuordnung in Data Workbench?**

Data Workbench bietet inkrementelle Angebote:

* Die Fähigkeit, eine Attribution über weitere Datenquellen auf Besucherebene vorzunehmen, beispielsweise Anzeigenimpressionen und Point of Sale.
* Algorithmische Modellierung. Die Zuordnung im Analysis Workspace umfasst nur regelbasierte Modelle. Siehe [Best fit-Modellierung](https://marketing.adobe.com/resources/help/en_US/insight/client/c_attrib_algorithmic.html) im Data Workbench-Benutzerhandbuch.
* Zusätzliche Visualisierungen, beispielsweise Wartezeittabellen. Siehe [Latenztabellen](https://marketing.adobe.com/resources/help/en_US/insight/client/c_lat_tbls.html) im Data Workbench-Benutzerhandbuch.

**Funktioniert die Zuordnung mit Klassifizierungen?**

Ja, Classifications werden vollständig unterstützt.

**Funktioniert die Zuordnung mit Datenquellen?**

Ja, die meisten Datenquellen werden unterstützt. Bei Datenquellen auf Zusammenfassungsebene ist eine Zuordnung nicht möglich, da sie nicht mit einer Analytics-Besucher-ID verknüpft sind. Transaktions-ID-Datenquellen werden ebenfalls unterstützt, es sei denn, sie werden in einer Virtual Report Suite mit aktivierter Berichtszeitverarbeitung verwendet.

**Funktioniert die Zuordnung mit der Advertising Analytics-Integration?**

Metadatendimensionen wie Übereinstimmungstyp und Suchbegriff funktionieren mit der Zuordnung. Metriken (wie Impressionen, Kosten, Klicks, durchschnittliche Position und durchschnittliche Qualitätsbewertung) verwenden jedoch Datenquellen auf Zusammenfassungsebene und sind daher inkompatibel.
