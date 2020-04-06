---
keywords: Analysis Workspace
title: Analysis Workspace  Übersicht
topic: Reports and analytics
uuid: 4df6be48-2c88-4b9d-9536-ed64ffbb6ee4
translation-type: tm+mt
source-git-commit: dabaf6247695bc4f3d9bfe668f3ccfca12a52269

---


# Analysis Workspace – Übersicht

Analyse Workspace entfernt alle typischen Einschränkungen eines einzelnen Analytics-Berichts. Es bietet eine robuste, flexible Arbeitsfläche zum Erstellen benutzerdefinierter Analysen. Ziehen Sie per Drag-and-Drop eine beliebige Anzahl von Datentabellen, Visualisierungen und Komponenten (Dimensionen, Metriken, Segmente und Zeitgranularitäten) in ein Projekt. Erstellen Sie sofort Aufschlüsselungen und Segmente, erstellen Sie Kohorten für die Analyse, erstellen Sie Warnungen, vergleichen Sie Segmente, führen Sie Fluss- und Trichteranalysen-Analysen durch und kuratieren und planen Sie Berichte für die Freigabe an andere in Ihrem Unternehmen.

**[!UICONTROL Analytics]** > **[!UICONTROL Workspace]**

## Überblickvideo {#section_B99BF8A326D94ECB91BD69C9888AD10C}

>[!VIDEO](https://www.youtube.com/watch?v=IHOy-QsvVcA)

Eine vollständige YouTube-Playlist ist [hier](https://www.youtube.com/playlist?list=PL2tCx83mn7GuNnQdYGOtlyCu0V5mEZ8sS) verfügbar.

>[!NOTE]
>
>[Neuerungen in Analysis Workspace](/help/analyze/analysis-workspace/new-features-in-analysis-workspace.md) enthält aktuelle Informationen zu Funktionen.

## Vollständige Kontrolle über Projektelemente und Komponenten {#section_B7E3EDA3EDEE407D833F4FDB69646EEC}

Analyse Workspace bietet Freiheit und Flexibilität:

* Drag-and-Drop von Komponenten (Dimensionen, Metriken, Segmente und Zeitgranularitäten)
* Drag-and-Drop von mehreren Visualisierungen in das Projekt
* Visualisierungen verschieben, skalieren und stapeln, wo immer Sie möchten

![](assets/fa_project_new.png)

Weitere Informationen finden Sie unter [Erstellen eines Projekts in Analysis Workspace](/help/analyze/analysis-workspace/build-workspace-project/t-freeform-project.md).

## Mehrere Visualisierungen in einem Projekt {#section_B7670740C2D44130B21DAF0873280DA5}

Erstellen Sie per Drag-and-Drop beliebig viele Visualisierungen in einem Projekt.

![](assets/visualizations-multiple.png)

Erstellen Sie ein Projekt, das den Prozentsatz der Veränderung anzeigt, mit mehreren Visualisierungen, die den Zellen in einer Freiform-Datentabelle entsprechen.

![](assets/visualizations-multiple02.png)

Weitere Informationen finden Sie unter [Erstellen eines Projekts in Analysis Workspace](/help/analyze/analysis-workspace/build-workspace-project/t-freeform-project.md).

## Intra-Linking zu Bereichen und Visualisierungen {#section_253EA04E067F4A29A8B54CE2B7631086}

Mithilfe der [Rich-Text-Bearbeitungsfunktionen](/help/analyze/analysis-workspace/visualizations/text.md) von Analysis Workspace können Sie innerhalb eines Projekts von einem Textfeld aus Verknüpfungen zu bestimmten Bereichen und Visualisierungen anlegen, beispielsweise um das Inhaltsverzeichnis eines Projekts zu erstellen. Sie können diese Verknüpfungen dann wie eine Projektverknüpfung freigeben, um eine Person an eine bestimmte Visualisierung oder einen Bereich innerhalb eines Projekts weiterzuleiten. Die neuen Rechtsklickoptionen „Bereichslink abrufen“ und „Visualisierungslink abrufen“ wurden hinzugefügt. So fügen Sie Ihrem Projekt Intra-Linking hinzu:

1. Ziehen Sie eine Textvisualisierung in ein Projekt, möglicherweise neben einer Visualisierung oder Tabelle, die einen bestimmten Kontext benötigt.
1. Füllen Sie das Textfeld beispielsweise mit einer Inhaltstabelle und markieren Sie dann ein Element, das Sie mit einem Bereich oder einer Visualisierung verknüpfen möchten, z. B. Erfolgsmetriken.

   ![](assets/intra-linking1.png)

1. Blättern Sie zu diesem Bedienfeld oder zu dieser Visualisierung und klicken Sie mit der rechten Maustaste auf die Kopfzeile des Bedienfelds.
1. Blättern Sie nach unten und wählen Sie **[!UICONTROL Get Panel Link]** oder **[!UICONTROL Get Visualization Link]**:

   ![](assets/intra-linking2.png)

1. Kopieren Sie diesen Link und fügen Sie ihn dem Hyperlink &quot;Erfolgsmetriken&quot;in der Textvisualisierung hinzu. Klicken Sie auf das Häkchen, um den Text zu speichern.

Wenn in Ihrem Projekt Bereiche oder Visualisierungen reduziert sind, wird durch Klicken auf einen Link das Bedienfeld/die Visualisierung erweitert, damit die Benutzer es sehen können.

>[!NOTE] Sie können diese Funktion auch mit der **[!UICONTROL Edit Description]** Rechtsklick-Option verwenden.

## Verknüpfung zu anderen Projekten {#section_AE886C367C3E4F189B65B1BD9BCDBD8C}

You can link users to other projects that may be of interest to them by going to  **[!UICONTROL Share]** > **[!UICONTROL Get Project Link]** and embedding this link in project descriptions, for example.

## Dynamische Visualisierung ausgewählter Zellen {#section_182CEC285E4547EBA4608D5F70C9D5D7}

Wählen Sie einzelne Zellen aus und sehen Sie, wie sich die Visualisierungen dynamisch ändern. [Synchronisieren und sperren](/help/analyze/analysis-workspace/analysis-workspace-features.md#section_9D66A001586F49CEB0C565581E44957C) Sie eine Visualisierung mit ausgewählten Zellen.

![](assets/visualize-selected-cells.png)

## Ausgewählte Elemente oder Positionen sperren {#section_9D66A001586F49CEB0C565581E44957C}

Durch das Sperren von Visualisierungen können Sie steuern, welche Freiform-Datentabellenquellen den Visualisierungen entsprechen.

![](assets/manage-data-source.png)

[Data Sources verwalten](/help/analyze/analysis-workspace/visualizations/t-sync-visualization.md).

## Trend-Visualisierungen aus ausgewählten Zellen {#section_34930C967C104C2B9092BA8DCF2BF81A}

Erstellen Sie eine Visualisierung aus ausgewählten Zellen. (Rechtsklick > **[!UICONTROL Trend Selection]**.)

![](assets/trend-selection.png)

Trendauswahlen werden jetzt mit der Tabelle darunter **verknüpft**. Wenn Sie daher in der Tabelle eine andere Zeile auswählen, bezieht sich das Trend-Diagramm auf diese Zeile.

![](assets/trend-selection2.png)

## Aufschlüsselungen von Dimensionen und Dimensionselementen {#section_1380C1F9E51E4BFB8C5D35E7A53BC70D}

Als Einzelhändler können Sie tiefer als je zuvor in Ihre Kampagnen eintauchen, um zu verstehen, wie Sie Ihre Kunden besser binden können. Daten auf unbegrenzte Weise für Ihre spezifischen Anforderungen aufschlüsseln; Erstellen Sie Abfragen mithilfe relevanter Metriken, Dimensionen, Segmente, Zeitlinien und anderer Aufschlüsselungswerte für Analysen.

![Schritt Ergebnis](assets/fa_data_table_actions.png)

[Schlüsseln Sie Dimensionen auf](/help/analyze/analysis-workspace/components/dimensions/t-breakdown-fa.md).

## Segmente aus Tabellenauswahlen {#section_73BC3688089B426D969B3D5B606DA970}

Wählen Sie Zellen in der Freiformtabelle aus und erstellen Sie aus der Auswahl ein Segment.

Vergleichen Sie mehrere Segmente und erstellen und wenden Sie Segmente sofort an. Sie können mehrere Segmente anwenden, um sich basierend auf Verhalten und Interaktion auf bestimmte Kunden zu konzentrieren und dann vergleichen und kontrastreichen zu können.

![](assets/segment_inline.png)

Ziehen Sie ein Segment auf der Projektebene in den Freiformbereich, und das Segment wird auf das gesamte Projekt angewendet.

![](assets/segment-panel.png)

Siehe [Segmente](/help/analyze/analysis-workspace/components/t-freeform-project-segment.md).

## Projekt- und Komponenten-Tagging {#section_F54D688132A541F2982326D5E022B90D}

In Analysis Workspace können Sie Tags auf Projekte und Komponenten anwenden:

* Anwenden oder Erstellen von Tags auf Projektebene im Informationsbereich ![](assets/information_icon.png)

* Klicken Sie mit der rechten Maustaste auf Komponenten, um Tags im Komponentenbedienfeld zu taggen (oder zu erstellen).
* Verwenden Sie # im Suchfeld, um Tags zu suchen.

## Komponentenaktionen {#section_CBF4D0A5F63E4B0883077B8D852B800B}

Aktionen auf Komponentenebene führen Sie über das Menü „Aktionen“ durch, das sich oben in der linken Leiste von „Komponenten“ befindet. Select a component and click **[!UICONTROL Actions]** to view the actions.

| Komponentenaktion | Beschreibung |
|--- |--- |
| Tag | Organisieren oder verwalten Sie Komponenten, indem Sie Tags darauf anwenden. Dies wird dann bei der jeweiligen Komponentenverwaltung angezeigt, beispielsweise „Analysen“ > „Komponenten“ > „Segmente“ oder „Analysen“ > „Komponenten“ > „Projekte“. |
| Favorit | Fügen Sie die Komponente Ihrer Favoritenliste hinzu. Dies wird dann bei der jeweiligen Komponentenverwaltung angezeigt, beispielsweise „Analysen“ > „Komponenten“ > „Segmente“ oder „Analysen“ > „Komponenten“ > „Projekte“. |
| Genehmigen | Genehmigen Sie die Komponente, um sie zu autorisieren. Dies wird dann bei der jeweiligen Komponentenverwaltung angezeigt, beispielsweise „Analysen“ > „Komponenten“ > „Segmente“ oder „Analysen“ > „Komponenten“ > „Projekte“. |
| Freigabe | Gilt nur für Segmente. |
| Löschen | Gilt nur für Segmente. |

Weitere Informationen finden Sie unter [Visualisierungen](/help/analyze/analysis-workspace/visualizations/freeform-analysis-visualizations.md) .

## Beschreibung weiterer Funktionen {#section_5F06AE43C0194CFDBCA7EE0EA3C30B05}

**Was Sie ziehen und stapeln können**

Komponenten

* Dimensionen
* Segmente
* Metriken
* Datumsbereiche
* Zeitgranularitäten (Stunde, Tag, Woche usw.).

**Mehrere Freiformtabellen und mehrere Visualisierungen**

Es gibt keine technische Einschränkung für die Anzahl der Freiformtabellen und Visualisierungen, die Sie zum Bereich hinzufügen können. Sie können auch eine neue Visualisierung (oder einen Export in eine CSV-Datei) der einzelnen Freiformtabellen oder ausgewählten Zeilen einer Tabelle ausführen.

**Anordnen, Sortieren und Kopieren von Spalten**

* Sortieren von Datumsbereichsvorgaben (ohne benutzerdefinierte Datumsbereiche)
* STRG (oder Command) + Klick + Ziehen einer Spalte kopiert die Spalte und beim Ziehen der Kopie wird sie an der neuen Position in der Tabelle eingefügt.

Für weitere Informationen siehe [Tastaturbefehle in Analysis Workspace](/help/analyze/analysis-workspace/build-workspace-project/fa-shortcut-keys.md).

**Auswahlen und Aktionen**

Sie können Zeilen und Spalten ähnlich wie in Excel auswählen. Anschließend können Sie Aktionen für diese Auswahlen ausführen. Beispiel:

* Erstellen von Visualisierungen aus Auswahlen
* In die Zwischenablage kopieren (STRG oder Command + C)
* Aufschlüsseln von Zeilen mit mehreren ausgewählten Zeilen. Wählen Sie die Zeilen aus und ziehen Sie dann eine Dimension auf die Auswahl. Oder klicken Sie mit der rechten Maustaste auf die Auswahl und verwenden Sie das Unterteilungsmenü.

**Automatisches Speichern und nicht gespeicherte Änderungen**

Sie werden aufgefordert, Ihre Änderungen zu speichern, wenn Sie versuchen, den Browser zu schließen (oder die Schaltfläche &quot;Zurück&quot;zu verwenden) und das Projekt nicht gespeichert wurde. Wenn Ihr System abstürzt, erhalten Sie beim Laden des Projekts eine Warnung, um den vorherigen Projektstatus wiederherzustellen.

Bereits vorhandene (nicht neue) Projekte werden nur dann automatisch gespeichert, wenn der Browser abstürzt, oder unter anderen Umständen, wenn Sie nicht die Möglichkeit hatten, sie zu speichern.

**Alle Besuche**

Ein spezifisches Standardsegment von Analysis Workspace. *`All Visits`* zeigt die Summen für die Komponenten, die Sie zur Tabelle hinzufügen, an.

**Berechnete Metriken**

Verwenden Sie Berechnungen auf dieselbe Weise wie Standardmetriken.

Siehe [Berechnete Metriken](https://marketing.adobe.com/resources/help/de_DE/analytics/calcmetrics/).
