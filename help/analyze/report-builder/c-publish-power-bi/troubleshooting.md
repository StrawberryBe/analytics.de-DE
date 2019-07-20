---
description: Im Folgenden werden häufige Fehler bei der Verwendung von ReportBuilder mit Power BI beschrieben.
seo-description: Im Folgenden werden häufige Fehler bei der Verwendung von ReportBuilder mit Power BI beschrieben.
seo-title: Fehlerbehebung für Power BI-Integration
title: Fehlerbehebung für Power BI-Integration
uuid: c 1 e 7 e 164-4 bc 6-4513-9332-92 c 53 be 021 cc
translation-type: tm+mt
source-git-commit: 86fe1b3650100a05e52fb2102134fee515c871b1

---


# Fehlerbehebung für Power BI-Integration

Im Folgenden werden häufige Fehler bei der Verwendung von ReportBuilder mit Power BI beschrieben.

## Schritt 1. Failure to publish to Power BI {#section_5B87DC1C302C4FD8AB9E4DD6B162DC9B}

Geplante Arbeitsmappen, die in Power BI veröffentlicht werden sollen, hängen davon ab, dass Power BI-Dienste ausgeführt werden. Zwei Hauptgründe für das Fehlschlagen einer Veröffentlichung sind:

* Power BI-Dienste werden nicht ausgeführt.
* Der Benutzer, der die Veröffentlichung der Arbeitsmappe geplant hat, besitzt keine gültigen Microsoft-Kontoanmeldedaten mehr.

Für jede geplante ReportBuilder-Aufgabe werden drei Versuche pro geplanter Ausführung durchgeführt:

* Nach dem ersten erfolglosen Versuch wird eine Fehlermeldung mit dem folgenden Wortlaut angezeigt: „Diese geplante Arbeitsmappe konnte nicht in Microsoft Power BI veröffentlicht werden. Ein neuer Versuch erfolgt in Kürze.“
* Nach dem zweiten erfolglosen Versuch wird keine Meldung angezeigt.
* Nach dem dritten erfolglosen Versuch wird eine Fehlermeldung mit dem folgenden Wortlaut angezeigt: „Diese geplante Arbeitsmappe konnte nicht in Power BI veröffentlicht werden.“

## Schritt 2: Broken visualizations in Power BI {#section_FFFE200D06F843B2AF093710FD678166}

Im Folgenden werden die wichtigsten Gründe für beschädigte Visualisierungen nach der Veröffentlichung von ReportBuilder-Anforderungen in Power BI aufgeführt:

* Sie haben eine Anforderung in ReportBuilder bearbeitet, z. B. durch Ändern der Metriken oder Dimensionen, und sie dann erneut in Power BI veröffentlicht. Durch Bearbeiten von Anforderungen können Ihre Visualisierungen beschädigt werden.
* Sie haben eine Anforderung gelöscht, die in einer Visualisierung verwendet wurde.

