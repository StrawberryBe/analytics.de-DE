---
description: Schlüsseln Sie Dimensionen und Dimensionselemente in Analysis Workspace auf.
keywords: Analysis Workspace
title: Dimensionen aufschlüsseln
uuid: 0b888e26-f201-4405-99f9-755b3ee6cd18
feature: Workspace Basics
role: User, Admin
exl-id: 0d26c920-d0d9-4650-9cf0-b67dbc4629e1
source-git-commit: 9f0f17936de2597611728498c5ed82d36fd01d1c
workflow-type: tm+mt
source-wordcount: '343'
ht-degree: 63%

---

# Dimensionen aufschlüsseln

Schlüsseln Sie Dimensionen und Dimensionselemente in Analysis Workspace auf.

Sie können Ihre Daten für Ihre spezifischen Anforderungen unbegrenzt aufschlüsseln. Erstellen Sie Abfragen mithilfe relevanter Metriken, Dimensionen, Segmente, Zeitachsen und anderer Aufschlüsselungswerte für die Analyse.

1. [Erstellen Sie ein Projekt](/help/analyze/analysis-workspace/home.md) mit einer Datentabelle.
1. Klicken Sie in der Datentabelle mit der rechten Maustaste auf einen Zeileneintrag und wählen Sie **[!UICONTROL Aufschlüsselung]** > *`<item>`* aus.

   ![Ergebnis des Schritts](assets/fa_data_table_actions.png)

   Sie können Metriken nach Dimensionselementen oder Zielgruppensegmenten über ausgewählte Zeiträume aufschlüsseln. Sie können auch noch granularer aufschlüsseln.

   >[!NOTE]
   >
   >Die Anzahl der in der Tabelle angezeigten Aufschlüsselungen ist auf 200 beschränkt. Für das Exportieren von Aufschlüsselungen ist diese Einschränkung höher.

## Attributionsmodelle auf Aufschlüsselungen anwenden

Auf jede Aufschlüsselung innerhalb einer Tabelle kann auch ein beliebiges Attributionsmodell angewandt werden. Dieses Attributionsmodell kann mit der übergeordneten Spalte identisch sein oder sich von ihr unterscheiden. Sie können beispielsweise lineare Bestellungen in Ihrer Dimension „Marketing-Kanäle“ analysieren, jedoch U-förmige Bestellungen auf spezifische Trackingcodes in einem Kanal anwenden. Bewegen Sie zum Bearbeiten des auf eine Aufschlüsselung angewendeten Attributionsmodells einfach den Mauszeiger auf das Aufschlüsselungsmodell und klicken Sie auf **[!UICONTROL Bearbeiten]**:

![Aufschlüsselungseinstellungen](assets/breakdown_settings.png)

Dies ist das erwartete Verhalten beim Anwenden von Attributionsmodellen auf Aufschlüsselungen oder deren Bearbeitung:

* Wenn Sie eine Attribution anwenden, wenn keine anderen Attribute vorhanden sind, gilt die Attribution für die gesamte Spaltenstruktur.

* Wenn Sie eine Aufschlüsselung hinzufügen, nachdem eine Attribution angewendet wurde, wird für die hinzugefügte Aufschlüsselung der Standardwert verwendet, sofern diese Dimension über einen Standardwert verfügt. Andernfalls wird die Aufschlüsselung aus der übergeordneten Spalte verwendet. Einige Dimensionen haben eine Standardzuordnung.  Beispiel: [!UICONTROL Zeit] Dimensionen und [!UICONTROL Referrer] use [!UICONTROL Selber Kontakt]. Die [!UICONTROL Produkt] Dimensionsverwendungen [!UICONTROL Letztkontakt]. Andere Dimensionen haben keine Standardeinstellung und verwenden die Zuordnung der übergeordneten Spalte.

* Wenn sich bereits Attribute in der Spaltenstruktur befinden, wirkt sich eine Änderung der Attribution nur auf die Zuordnung aus, die Sie bearbeiten.

## Videos

Hinzufügen von Dimensionen und Metriken zu Ihrem Projekt in Analysis Workspace:

>[!VIDEO](https://video.tv.adobe.com/v/30606/?quality=12)

Arbeiten mit Dimensionen in einer Freiformtabelle:

>[!VIDEO](https://video.tv.adobe.com/v/40179/?quality=12)

Im Folgenden finden Sie ein Video zu Dimensionsaufschlüsselungen nach Position:

>[!VIDEO](https://video.tv.adobe.com/v/24033/?quality=12)
