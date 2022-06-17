---
title: Auftrags-Manager für Klassifizierungssätze
description: Zeigen Sie aktuelle und abgeschlossene Classification-Aufträge an, die aus Classification-Sets generiert wurden.
exl-id: 0470e131-79c6-4906-85f0-530d360ac227
source-git-commit: a1f199525c567bc9d7bb614ee03980f582cbbc7a
workflow-type: tm+mt
source-wordcount: '387'
ht-degree: 0%

---

# Auftrags-Manager für Klassifizierungssätze

Mit dem Job Manager für Klassifizierungssätze können Sie aktuelle und abgeschlossene Klassifizierungsaufträge anzeigen, die aus Klassifizierungssets generiert wurden. Sie können diese Benutzeroberfläche auch verwenden, um Classification-Daten oder Vorlagen für einen bestimmten Auftrag herunterzuladen oder zusätzliche Daten in einen Auftrag hochzuladen.

**[!UICONTROL Komponenten]** > **[!UICONTROL Klassifizierungssätze]** > **[!UICONTROL Aufträge]**

Beachten Sie, dass Sie keine Aufträge über diese Benutzeroberfläche erstellen können. Stattdessen können Sie Aufträge erstellen, indem Sie Daten in einen Klassifizierungssatz hochladen, eine Download-Datei anfordern oder eine Vorlagendatei anfordern.

## Filtern von Classification-Sets

Auf der linken Seite des Classification Set Job Manager finden Sie Filtereinstellungen, um den gewünschten Auftrag zu finden. Durch Klicken auf das Filtersymbol wird die Sichtbarkeit der Filtereinstellungen ein-/ausgeblendet. Sie können Classification-Sets nach **[!UICONTROL Klassifizierungssatz]**, **[!UICONTROL Abschlusszeit]** oder **[!UICONTROL Status]**.

![Klassifizierungsset-Auftragsfilter](../assets/classification-set-job-filters.png)

Zusätzliche Filteroptionen sind über den Spalten für den Classification Set Job Manager verfügbar:

* **[!UICONTROL Suche nach Titel]**: Suchen Sie nach Aufträgen anhand des Dateinamens.
* **[!UICONTROL Mehr laden]**: Der Job Manager für Klassifizierungssets zeigt zunächst bis zu 1000 Aufträge an. Klicken Sie auf diese Schaltfläche, um 1000 weitere Aufträge zu laden.
* **Spalten ein-/ausblenden**: Sichtbarkeit für eine beliebige Spalte außer [!UICONTROL Dateiname] und [!UICONTROL Abschlusszeit].

## Spalten im Classification Set Job Manager

Die folgenden Spalten sind im Classification Set Job Manager verfügbar:

* **[!UICONTROL Dateiname]**: Der Name der Upload- oder Download-Datei.
* **[!UICONTROL Klassifizierungssatz]**: Der Name des Klassifizierungssatzes, für den die Datei gilt. Sie können auf den Namen des Klassifizierungssatzes klicken, um die [Einstellungen](settings.md).
* **[!UICONTROL Größe]**: Die Größe der Datei.
* **[!UICONTROL Status]**: Der Status des Auftrags, der die Datei verarbeitet.
   * **[!UICONTROL Erstellt]**: Der Auftrag wurde eingereicht.
   * **[!UICONTROL In Warteschlange]**: Die Datei ist bereit zur Verarbeitung und wartet auf die Verarbeitung der Datei durch einen Classification-Server.
   * **[!UICONTROL Validiert]**: Die Datei ist gültig und wartet auf die Verarbeitung.
   * **[!UICONTROL Fehlgeschlagene Validierung]**: Die Datei ist falsch oder anderweitig ungültig formatiert. Die Datei wird nicht verarbeitet.
   * **[!UICONTROL Verarbeitung]**: Die Datei wird aktiv von Adobe verarbeitet.
   * **[!UICONTROL Fehlerhafte Verarbeitung]**: Die Verarbeitung der Datei ist fehlgeschlagen.
   * **[!UICONTROL Fertig]**: Die Verarbeitung ist abgeschlossen. Klassifizierungsdaten sind in Berichten sichtbar.
   * **[!UICONTROL Fehlgeschlagen]**: Generischer Fehler, der nicht mit der Validierung oder Verarbeitung in Zusammenhang steht.
* **[!UICONTROL Typ]**: Die Art des Auftrags.
* **[!UICONTROL Dateidownload]**: Gilt nur für Download-Aufträge, wie das Herunterladen von Classification-Daten oder das Herunterladen von Vorlagen. Wenn ein Download bereit ist, enthält diese Spalte einen Download-Link.
* **[!UICONTROL Abschlusszeit]**: Datum und Uhrzeit des Abschlusses (oder Fehlschlagens) des Auftrags.
