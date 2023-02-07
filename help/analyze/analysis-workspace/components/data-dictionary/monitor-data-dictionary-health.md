---
description: Administratoren sind für die Überwachung des Zustands von Datenwörterbüchern zuständig. Dazu gehört auch, ob Komponenten Daten sammeln, genehmigt werden, Beschreibungen enthalten und frei von Duplikaten sind.
title: Überwachen des Zustands von Datenwörterbüchern
feature: Components
role: Admin
hide: true
hidefromtoc: true
source-git-commit: b0a3ee6785bdc2f3e9a55e42591b4846984934b6
workflow-type: tm+mt
source-wordcount: '236'
ht-degree: 0%

---

# Überwachen des Zustands von Datenwörterbüchern

{{release-limited-testing}}

Analytics-Administratoren sind für die Pflege eines gesunden Datenwörterbuchs verantwortlich.

## Eigenschaften eines gesunden Datenwörterbuchs

Ein gesundes Datenwörterbuch ist eines, in dem alle Komponenten:

* werden verwendet und erfassen Daten

* Enthält hilfreiche Beschreibungen, damit Benutzer wissen, wie sie am besten verwendet werden können

* sind frei von unnötigen Duplikaten

* vom Administrator genehmigt werden

## Prüfen des Zustands Ihres Datenwörterbuchs

So identifizieren Sie Gesundheitsprobleme in Ihrem Datenwörterbuch:

1. Öffnen Sie ein Analysis Workspace-Projekt.

1. Wählen Sie auf der linken Seite von Analysis Workspace das Symbol Datenwörterbuch aus. (Alternative Möglichkeiten zum Zugriff auf das Datenwörterbuch werden unter &quot;Zugriff auf das Datenwörterbuch&quot;in [Datenwörterbuch - Übersicht](/help/analyze/analysis-workspace/components/data-dictionary/data-dictionary-overview.md).

   Das Fenster Datenwörterbuch wird angezeigt.

   ![Administratoransicht des Datenwörterbuchs](assets/data-dictionary-admin.png)

1. Stellen Sie sicher, dass im Dropdown-Menü die richtige Report Suite ausgewählt ist.

1. Im [!UICONTROL **Wörterbuchgesundheit**] Registerkarte, wählen Sie [!UICONTROL **Ansicht**] neben einer der folgenden Optionen:

   * [!UICONTROL **-Komponenten fehlen Beschreibungen**]

   * [!UICONTROL **Komponenten haben Duplikate**]

   * [!UICONTROL **Komponenten sind nicht mit Daten verbunden**]

   Je nachdem, was Sie auswählen, wird der entsprechende Filter auf das Datenwörterbuch angewendet und es werden nur die relevanten Komponenten angezeigt.

1. Bearbeiten Sie eine beliebige Komponente, um den Zustand des Datenwörterbuchs zu verbessern. Informationen zum Bearbeiten einer Komponente im Datenwörterbuch finden Sie unter [Bearbeiten von Komponenteneinträgen im Datenwörterbuch](/help/analyze/analysis-workspace/components/data-dictionary/edit-entries-data-dictionary.md).