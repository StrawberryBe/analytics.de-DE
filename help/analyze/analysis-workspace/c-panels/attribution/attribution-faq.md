---
title: Häufig gestellte Fragen zu Attribution
description: Erhalten Sie Antworten auf häufig gestellte Fragen zur Attribution.
translation-type: tm+mt
source-git-commit: 06b9ac8ddbfb0398341a2ab5656237e3520a8612
workflow-type: tm+mt
source-wordcount: '487'
ht-degree: 88%

---


# Häufig gestellte Fragen zu Attribution

**Was ist der Zeileneintrag „Keine“ bei Verwendung von Attribution?**

Das Zeilenelement &quot;Keine&quot;ist ein Sammelelement, das alle Konvertierungen darstellt, die ohne Berührungspunkte im Lookback-Fenster stattgefunden haben. Versuchen Sie, einen längeren Zeitraum in Ihr Berichtsfenster aufzunehmen.

**Warum sehe ich manchmal Daten außerhalb meines Berichtsfensters, wenn ich Attributionsmodelle verwende?**

Diese zusätzlichen Daten sind auf das Lookback-Fenster des Besucherberichts zurückzuführen. Weitere Informationen finden Sie unter [Daten, die außerhalb des Berichtsfensters angezeigt werden](https://helpx.adobe.com/de/analytics/kb/data-appearing-outside-reporting-window.html) in der Analytics-KB. Adobe wird diese zusätzlichen Zeilen in einer künftigen Version herausfiltern.

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

**Kann ich ein benutzerdefiniertes Lookback-Fenster mit meinen Attributionsmodellen verwenden?**

Ja. Mithilfe der Option für das benutzerdefinierte Lookback-Fenster können Lookback-Fenster bis zu 90 Tage vor dem Fenster des Berichte für einen beliebigen Datumsbereich konfiguriert werden. Weitere Informationen finden Sie unter [Berichtszeitverarbeitung](https://docs.adobe.com/content/help/en/analytics/components/virtual-report-suites/vrs-report-time-processing.html).

**Funktioniert die Attribution mit Klassifizierungen?**

Ja, Klassifizierungen werden vollständig unterstützt.

**Funktioniert Attribution mit Datenquellen?**

Ja, die meisten Datenquellen werden unterstützt. Bei Datenquellen auf Zusammenfassungsebene ist eine Attribution nicht möglich, da sie nicht mit einer Analytics-Besucher-ID verknüpft sind. Als Datenquellen werden auch Transaktions-IDs unterstützt, es sei denn sie werden in einer Virtual Report Suite mit aktivierter Berichtszeitverarbeitung verwendet.

**Funktioniert Attribution mit der Advertising Analytics-Integration?**

Metadatendimensionen wie Übereinstimmungstyp und Suchbegriff funktionieren mit Attribution. Metriken (wie Impressions, Kosten, Klicks, durchschnittliche Position und durchschnittliche Qualitätsbewertung) verwenden jedoch Datenquellen auf Zusammenfassungsebene und sind daher inkompatibel.
