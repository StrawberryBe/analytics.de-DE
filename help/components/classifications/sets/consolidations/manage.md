---
title: Konsolidierungs-Manager für Klassifizierungssatz
description: Konsolidieren Sie einen oder mehrere Classification-Sets in einem einzigen Classification-Satz.
source-git-commit: d0e3b28590b24d630a192ee857a7d84c115dc8c1
workflow-type: tm+mt
source-wordcount: '251'
ht-degree: 5%

---

# Konsolidierungs-Manager für Klassifizierungssätze

Wenn Sie mehrere Classification-Sets haben, die ähnliche Daten enthalten, können Sie sie zu einem einzigen Classification-Satz zusammenfassen. Wenn Sie zwei oder mehr Classification-Sets zusammenfassen, generiert Adobe einen neuen Classification-Satz, der alle Classification-Daten aus jedem Classification-Satz enthält. Konsolidierungen sind nützlich, wenn Sie Daten in viele Report Suites oder Dimensionen hochgeladen haben, die dieselben Classification-Daten enthalten und diese zu einem einzigen Workflow zusammenführen möchten.

**[!UICONTROL Komponenten]** > **[!UICONTROL Klassifizierungssätze]** > **[!UICONTROL Konsolidierung]**

Sobald eine Konsolidierung ausgeführt wird, werden die ursprünglichen Classification-Sets entfernt, wobei der konsolidierte Classification-Satz ihren Platz einnimmt. Klicken **[!UICONTROL Hinzufügen]** nach [Konsolidierung erstellen](process.md).

## Filtern von Classification-Sets

Die linke Seite des Konsolidierungs-Managers für den Klassifizierungssatz bietet Filtereinstellungen, um die gewünschte Konsolidierung zu finden. Durch Klicken auf das Filtersymbol wird die Sichtbarkeit der Filtereinstellungen ein-/ausgeblendet. Sie können Konsolidierungen nach **[!UICONTROL Status]**, **[!UICONTROL Abschlusszeit]** oder **[!UICONTROL Erstellungszeit]**.

![Konsolidierungsfilter für Klassifizierungssätze](../../assets/classification-set-consolidation-filters.png)

Zusätzliche Filteroptionen sind über den Spalten des Konsolidierungs-Managers für den Classification-Satz verfügbar:

* **[!UICONTROL Suche nach Titel]**: Suche nach Konsolidierungen anhand des Namens.
* **Spalten ein-/ausblenden**: Sichtbarkeit für eine beliebige Spalte außer [!UICONTROL Name].

## Konsolidierungs-Manager-Spalten für Klassifizierungssätze

Die folgenden Spalten sind im Konsolidierungs-Manager für Klassifizierungssätze verfügbar:

* **[!UICONTROL Name]**: Der Name der Konsolidierung.
* **[!UICONTROL Aktueller Auftrag]**: Der aktuelle Auftrag. <!-- todo: better description -->
* **[!UICONTROL Status]**: Der Status der Konsolidierung. <!-- todo: get list of possible statuses -->
* **[!UICONTROL Erstellungsdatum]**: Datum und Uhrzeit der Erstellung der Konsolidierung.
* **[!UICONTROL Abschlussdatum]**: Datum und Uhrzeit des Abschlusses (oder Fehlschlagens) der Konsolidierung.
