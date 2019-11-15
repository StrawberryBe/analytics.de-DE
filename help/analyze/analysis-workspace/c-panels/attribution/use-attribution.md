---
description: 'null'
title: Attribution IQ in Analysis Workspace verwenden
uuid: 99fc91b6-eebe-4a60-bb82-64a7611a04c6
translation-type: tm+mt
source-git-commit: 16ba0b12e0f70112f4c10804d0a13c278388ecc2

---


# Attribution IQ in Analysis Workspace verwenden

Mit Attribution IQ in Analysis Workspace können Sie unterstützte Attributionsmodelle miteinander vergleichen, die wichtigsten zur Konversion führenden Marketing-Sequenzen mit erweiterten Fluss- und Fallout-Visualisierungen visualisieren, Trends für Marketing-Kanäle oder Kampagnen einfach offenlegen, um die Leistung über einen Zeitraum anzuzeigen, nach statistischen Abweichungen in der Kanal-/Kampagnenleistung suchen und gewarnt werden, wenn die Leistung verschlechtert oder verbessert wird.

## Use attribution in freeform tables {#section_F2F72AE840EB4EA781302A559726E6F4}

Analysis Workspace-Freiform-Tabellen unterstützen Attributionsmodelle, die für beinah jede Metrik verwendet werden können. Attributionsmodelle können für eine Freiform-Tabellenspaltenmetrik in „Spalteneinstellungen“ festgelegt werden:

1. Klicken Sie auf das Zahnradsymbol „Einstellungen“ in einer Freiform-Tabellenspalte.

   ![](assets/Column_Settings.png)

1. Aktivieren Sie unter **[!UICONTROL Dateneinstellungen]** die Option **[!UICONTROL Nicht standardmäßiges Attributionsmodell verwenden]**. For more information on the different attribution models, see [Attribution IQ Overview](attribution.md).

   ![](assets/Attribution_Model_Selection.png)

## Apply attribution models to breakdowns {#section_ED1E7532CF084B5AB0942BD80B4770C9}

Auf die Aufschlüsselungen in einer Freiformtabelle kann auch ein beliebiges Attributionsmodell angewendet werden. Dieses kann mit der übergeordneten Spalte übereinstimmen oder sich von dieser unterscheiden. Sie möchten vielleicht beispielsweise lineare Bestellungen in Ihrer Dimension „Marketingkanäle“ analysieren, wenden jedoch U-förmige Bestellungen auf spezifische Trackingcodes in einem Kanal an. Um das auf eine Aufschlüsselung angewendete Zuordnungsmodell zu bearbeiten, halten Sie den Mauszeiger über das Aufschlüsselungsmodell und klicken Sie auf "Bearbeiten":

![](assets/breakdown_settings.png)

## Compare one attribution model to another {#section_1D74C09549CC4EC8A952A7392C76D375}

If you'd like to quickly and easily compare one attribution model to another, right click a metric and select **[!UICONTROL Add comparative attribution model]**:

![](assets/Comparative_Attribution_Model.png)

Dadurch können Sie Attributionsmodelle schnell und einfach miteinander vergleichen, ohne eine Metrik hereinzuziehen und sie zweifach zu konfigurieren.

## Attribution panel and visualizations {#section_6B02F28182F14ECC9FC5020F224726E6}

Der Attributionsbereich bietet eine einfache Möglichkeit, eine Analyse zu erstellen, mit der verschiedene Attributionsmodelle verglichen werden. Klicken Sie für den Zugriff auf den Attributionsbereich

1. ganz links auf das Bereichssymbol.
1. Ziehen Sie den Attributionsbereich in Ihr Analysis Workspace-Projekt.

   ![](assets/Attribution_Panel_1.png)

1. Fügen Sie eine mit Attributen zu versehende Erfolgsmetrik und eine beliebige Kanaldimension hinzu, mit der die Attribution abgeglichen werden soll (beispielsweise Marketingkanäle oder interne Promotions).

   ![](assets/attribution_panel2.png)

1. Wählen Sie die zu vergleichenden [Attributionsmodelle](attribution.md) und das Lookback-Fenster aus.

   Der Attributionsbereich gibt eine Vielzahl an Daten und Visualisierungen zurück, mit denen Sie besser nachvollziehen können, wie Ihre Marketing-Kanäle (oder andere Dimensionen) interagieren:

   ![](assets/attr_panel_vizs.png)

   Im Folgenden werden die einzelnen Visualisierungen beschrieben:

| Visualization | Beschreibung |
|--- |--- |
| Metrik insgesamt | Die Gesamtanzahl der im Berichtszeitfenster aufgetretenen Konversionen. Hierbei handelt es sich um die Konversionen, die über die von Ihnen ausgewählte Dimension hinweg mit Attributen versehen werden. |
| Balkendiagramm für Metrikattributionsvergleich | Hiermit können Sie die mit Attributen versehenen Konversionen in Ihrer ausgewählten Dimension über die Dimensionselemente hinweg visuell vergleichen. Jede Balkenfarbe stellt ein unterschiedliches Attributionsmodell dar, das ausgewählt wurde. |
| Metrikattributions-Freiformtabelle | Zeigt dieselben Daten wie das Balkendiagramm an. Wenn Sie verschiedene Spalten oder Zeilen in dieser Tabelle auswählen, werden das Balkendiagramm sowie einige andere Visualisierungen im Bedienfeld gefiltert. Diese Tabelle funktioniert genauso wie jede andere Freiform-Tabelle in Workspace - Sie können Metriken, Segmente, Aufschlüsselungen usw. hinzufügen. |
| Dimensionsüberschneidungsdiagramm | Ein Mengendiagramm, das die obersten drei Dimensionen (z. B. Kanäle) und anzeigt, wie oft sie zusammen in einer Konversion partizipieren. So gibt beispielsweise die Größe der Blasendiagrammüberschneidung die Häufigkeit der Konversionen an, wenn bei einem Besucher beide Dimensionselemenente (z. B. Kanälen) angewandt wurden. Durch die Auswahl anderer Zeilen in der Freiformtabelle wird die Visualisierung zum Berücksichtigen Ihrer Auswahl entsprechend aktualisiert. |
| Marketingkontaktpunkte pro Journey | Ein Histogramm, das die Anzahl der Marketingkontaktpunkte (oder eine beliebige Dimension) eines Besuchers im Berichtsdatumsbereich angibt. Dies ist hilfreich, um nachzuvollziehen, wie wirkungsvoll die Mehrkontaktattribution für Ihren Datensatz ist. Wenn nahezu alle Besucher nur einen einzelnen Kontaktpunkt aufweisen, unterscheiden sich unterschiedliche Attributionsmodelle in den zugehörigen Ergebnissen nicht sonderlich voneinander. |
| Marketing-Kanalleistungsdetails | Hiermit können Sie bis zu drei Attributionsmodelle visuell mit einem Streudiagramm vergleichen. |
| Marketingkanalfluss | Ermöglicht Ihnen, zu sehen, mit welchen Kanälen am häufigsten und in welcher Reihenfolge während der gesamten Besucherreise interagiert wird. |
