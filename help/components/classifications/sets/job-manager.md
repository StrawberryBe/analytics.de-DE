---
title: Auftrags-Manager für Klassifizierungssätze
description: Zeigen Sie aktuelle und abgeschlossene Classification-Aufträge an, die aus Classification-Sets generiert wurden.
exl-id: 0470e131-79c6-4906-85f0-530d360ac227
feature: Classifications
source-git-commit: 811e321ce96aaefaeff691ed5969981a048d2c31
workflow-type: tm+mt
source-wordcount: '415'
ht-degree: 49%

---

# Auftrags-Manager für Klassifizierungssätze

Mit dem Job Manager für Klassifizierungssätze können Sie aktuelle und abgeschlossene Klassifizierungsaufträge anzeigen, die aus Klassifizierungssätzen generiert wurden. Sie können diese Benutzeroberfläche auch verwenden, um Klassifizierungsdaten oder Vorlagen für einen bestimmten Auftrag herunterzuladen oder zusätzliche Daten in einen Auftrag hochzuladen.

**[!UICONTROL Komponenten]** > **[!UICONTROL Klassifizierungssätze]** > **[!UICONTROL Aufträge]**

Auf dieser Benutzeroberfläche können keine Aufträge erstellt werden. Erstellen Sie Aufträge, indem Sie Daten in einen Classification-Satz hochladen (entweder manuell oder über einen konfigurierten externen Speicherort), eine Download-Datei anfordern oder eine Vorlagendatei anfordern.

## Filtern von Classification-Sets

Die linke Seite des Auftrags-Managers für den Klassifizierungssatz enthält Filtereinstellungen, um den gewünschten Auftrag zu finden. Durch Klicken auf das Filtersymbol wird die Sichtbarkeit der Filtereinstellungen ein-/ausgeblendet. Sie können Classification-Sets nach **[!UICONTROL Klassifizierungssatz]**, **[!UICONTROL Abschlusszeit]**, **[!UICONTROL Status]**, **[!UICONTROL Auftragstyp]** oder **[!UICONTROL Quelle]**.

![Auftragsfilter für Classification-Sets](../assets/classification-set-job-filters.png)

Zusätzliche Filteroptionen sind über den Spalten für den Classification-Satz Job Manager verfügbar:

* **[!UICONTROL Suche nach Titel]**: Suche nach Aufträgen anhand des Dateinamens.
* **[!UICONTROL Mehr laden]**: Der Job Manager für Klassifizierungssätze zeigt zunächst bis zu 1000 Aufträge an. Wenn weitere Aufträge vorhanden sind, klicken Sie auf diese Schaltfläche, um 1000 weitere Aufträge zu laden.
* **Spalten ein-/ausblenden**: Ein-/Ausschalten der Sichtbarkeit für eine beliebige Spalte außer [!UICONTROL Dateiname] und [!UICONTROL Abschlusszeit].

## Spalten des Classification-Sets für Auftragsmanager

Die folgenden Spalten sind im Job Manager für Klassifizierungssätze verfügbar:

* **[!UICONTROL Dateiname]**: Der Name der Datei zum Hoch- oder Herunterladen.
* **[!UICONTROL Klassifizierungssatz]**: Der Name des Klassifizierungssatzes, für den die Datei gilt. Sie können auf den Namen des Klassifizierungssatzes klicken, um die [Einstellungen](manage/settings.md).
* **[!UICONTROL Größe]**: Die Größe der Datei.
* **[!UICONTROL Status]**: Der Status des Auftrags, der die Datei verarbeitet.
   * **[!UICONTROL Erstellt]**: Der Auftrag wurde eingereicht.
   * **[!UICONTROL In Warteschlange]**: Die Datei ist bereit zur Verarbeitung und wartet auf ihre Verarbeitung durch einen Klassifizierungs-Server.
   * **[!UICONTROL Validiert]**: Die Datei ist gültig und wartet auf die Verarbeitung.
   * **[!UICONTROL Fehlgeschlagene Validierung]**: Die Datei ist falsch formatiert oder anderweitig ungültig. Die Datei wird nicht verarbeitet.
   * **[!UICONTROL Verarbeitung]**: Die Datei wird aktiv von Adobe verarbeitet.
   * **[!UICONTROL Fehlgeschlagene Verarbeitung]**: Die Verarbeitung der Datei ist fehlgeschlagen.
   * **[!UICONTROL Fertig]**: Die Verarbeitung ist abgeschlossen. Klassifizierungsdaten sind in Berichten sichtbar.
   * **[!UICONTROL Fehlgeschlagen]**: Generischer Fehler, der nicht mit der Validierung oder Verarbeitung in Zusammenhang steht.
* **[!UICONTROL Auftragstyp]**: Die Art des Auftrags.
* **[!UICONTROL Quelle]**: Die Auftragsquelle.
* **[!UICONTROL Datei-Download]**: Gilt nur für Aufträge zum Herunterladen, wie das Herunterladen von Klassifizierungsdaten oder das Herunterladen von Vorlagen. Wenn ein Download bereit ist, enthält diese Spalte einen Link zum Herunterladen.
* **[!UICONTROL Geänderte Zeilen]**: Die Anzahl der geänderten Zeilen.
* **[!UICONTROL Abgeschlossene Zeilen]**: Die Anzahl der abgeschlossenen Zeilen.
* **[!UICONTROL Abschlusszeit]**: Datum und Uhrzeit des Abschlusses (oder Fehlschlagens) des Auftrags.
