---
title: Classification Set Manager
description: Verwalten Sie Classification-Sets in Adobe Analytics.
exl-id: b1a6721b-8e5d-4ee6-af6b-cda31c9f8b00
source-git-commit: 496b4891d447ed9dd091a6498a792146a2d5aceb
workflow-type: tm+mt
source-wordcount: '350'
ht-degree: 5%

---

# Classification Set Manager

Mit dem Classification Set Manager können Sie Classification-Sets erstellen, bearbeiten oder löschen.

**[!UICONTROL Komponenten]** > **[!UICONTROL Klassifizierungssätze]** > **[!UICONTROL Sets]**

Klassifizierungssätze bestehen aus **Abonnements** (Report Suite- und Dimensionskombinationen) und **Klassifizierungsnamen** (Dimensionen, die Classification-Daten enthalten). Abonnements werden unter [Einstellungen](settings.md), während Classification-Namen unter konfiguriert werden [Schema](schema.md).

## Filtern von Classification-Sets

Die linke Seite des Classification-Set-Managers bietet Filtereinstellungen, um den gewünschten Classification-Satz zu finden. Durch Klicken auf das Filtersymbol wird die Sichtbarkeit der Filtereinstellungen ein-/ausgeblendet. Sie können Classification-Sets nach **[!UICONTROL Tags]**, **[!UICONTROL Report Suite]** oder **[!UICONTROL Inhaber]**.

![Klassifizierungssatzfilter](../../assets/classification-set-filters.png)

## Spalten des Classification Set Manager

Die folgenden Spalten sind im Classification-Set-Manager verfügbar:

* **[!UICONTROL Klassifizierungssatz]**: Der Name des Classification-Sets. Klicken auf einen Classification-Set-Namen [bearbeitet seine Einstellungen](settings.md).
* **[!UICONTROL Abonnements]**: Die Anzahl der Abonnements, für die dieser Classification-Satz gilt.
* **[!UICONTROL Inhaber]**: Der Eigentümer des Classification-Sets.
* **[!UICONTROL Klassifizierungen]**: Die Anzahl der Classification-Dimensionen, die der Classification-Satz enthält.
* **[!UICONTROL Automatisiert]**: Bestimmt, ob der Classification-Satz so konfiguriert ist, dass Daten automatisch von einem Cloud-Speicherort importiert werden. Die Automatisierung kann im [schema](schema.md).
* **[!UICONTROL Zuletzt geändert]**: Datum und Uhrzeit der letzten Änderung des Classification-Sets.

## Erstellen oder Bearbeiten von Optionen

Die folgenden Schaltflächen sind im Classification Set Manager verfügbar:

* **[!UICONTROL Hinzufügen]**: [Erstellen](create.md) einen Classification-Satz.
* **[!UICONTROL Suche nach Titel]**: Suchen Sie nach Classification-Sets anhand des Namens.
* **[!UICONTROL Mehr laden]**: Der Classification Set Manager zeigt zunächst bis zu 1000 Classification-Sets an. Mit dieser Schaltfläche werden 1000 weitere Classification-Sets geladen.
* **Spalten ein-/ausblenden**: Sichtbarkeit für eine beliebige Spalte außer [!UICONTROL Klassifizierungssatz].

Wählen Sie einen oder mehrere Classification-Sets aus, indem Sie auf das Kontrollkästchen neben dem gewünschten Classification-Satz klicken. Bei der Auswahl eines Classification-Sets werden die folgenden Optionen angezeigt:

* **[!UICONTROL Tag]**: Fügen Sie den ausgewählten Classification-Sets ein oder mehrere Tags hinzu, um Classification-Sets zu organisieren oder zu gruppieren, damit sie in Zukunft leichter zu finden sind.
* **[!UICONTROL Löschen]**: Löscht den Classification-Satz. Auf diesem Classification-Satz basierende Classification-Dimensionen sind nicht mehr verfügbar. Geplante Projekte, die den gelöschten Classification-Satz verwenden, verwenden weiterhin abhängige Dimensionen, bis Sie das geplante Projekt erneut speichern.
* **[!UICONTROL Konsolidieren]**: Neu starten [Konsolidierung](../consolidations/process.md).
* **[!UICONTROL Umbenennen]**: Benennen Sie den ausgewählten Classification-Satz um.
