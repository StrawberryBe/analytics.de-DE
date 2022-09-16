---
title: Vergleichen der von einem Ereignis betroffenen Daten mit vorherigen Datumsbereichen
description: Erfahren Sie mehr über die Auswirkungen eines Ereignisses, z. B. ein Implementierungsproblem oder ein Ausfall, indem Sie es mit früheren Trends vergleichen.
exl-id: 5e4ac1db-2740-4ec1-9d6a-5aa2005fadfd
source-git-commit: 549258b0168733c7b0e28cb8b9125e68dffd5df7
workflow-type: tm+mt
source-wordcount: '604'
ht-degree: 0%

---

# Vergleichen der von einem Ereignis betroffenen Daten mit vorherigen Datumsbereichen

Wenn Sie Daten haben [von einem Ereignis beeinflusst](overview.md)können Sie sich historische Trends ansehen, um ihre Auswirkungen abzuschätzen. Dieser Vergleich ist nützlich, um zu verstehen, wie stark sich ein Ereignis auf Ihre Daten auswirkt. So können Sie entscheiden, ob Sie die Daten ausschließen, Berichte mit Anmerkungen versehen oder ignorieren möchten.

## Erstellen eines Datumsbereichs, der das Ereignis enthält

Erstellen Sie einen Datumsbereich, der das Ereignis umfasst, um die Auswirkungen dieses Ereignisses zu untersuchen.

1. Navigieren Sie zu **[!UICONTROL Komponenten]** > **[!UICONTROL Datumsbereiche]**.
2. Klicken Sie auf **[!UICONTROL Hinzufügen]**.
3. Wählen Sie den Datumsbereich aus, in dem das Ereignis aufgetreten ist. Klicken Sie auf **[!UICONTROL Speichern]**.

   ![Generator für Datumsbereiche](assets/date_range_builder.png)

## Anzeigen von Ereignisdaten und ähnlichen vorherigen Bereichen nebeneinander

Sie können jede Metrik im Datumsbereich des Ereignisses mit ähnlichen vorherigen Datumsbereichen mithilfe einer Freiformtabellenvisualisierung vergleichen.

1. Öffnen Sie ein Workspace-Projekt und fügen Sie der Freiformtabelle die Dimension &quot;Tag&quot;hinzu. Wenden Sie den kürzlich erstellten Datumsbereich auf eine Metrik an, z. B. &quot;Vorfälle&quot;.

   ![Datumsbereichsmetrik](assets/date_range_metric.png)

2. Klicken Sie mit der rechten Maustaste auf den Datumsbereich und klicken Sie dann auf **[!UICONTROL Spalte &quot;Zeitraum hinzufügen&quot;]** > **[!UICONTROL Benutzerdefinierter Datumsbereich bis zu diesem Datumsbereich]**.
   * Wählen Sie für einen wöchentlichen Vergleich den Bereich des Ereignisses minus 7 Tage aus. Stellen Sie sicher, dass die Wochentage zwischen dem Ereignis und diesem Datumsbereich aufeinander abgestimmt sind.
   * Wählen Sie für einen Monatsvergleich den Bereich des Ereignisses im letzten Monat aus. Sie können auch den Bereich des Ereignisses minus 28 Tage auswählen, wenn Sie die Wochentage ausrichten möchten.
   * Wählen Sie für einen Jahresvergleich den Bereich des Ereignisses im letzten Jahr aus.
3. Wenn Sie den gewünschten Datumsbereich auswählen, werden diese der Freiformtabelle hinzugefügt. Sie können mit der rechten Maustaste klicken und so viele Datumsbereiche hinzufügen, wie Sie vergleichen möchten.

   ![Datumsorientierte Trends](assets/date_aligned_trends.png)

## Prozentunterschiede zwischen dem Ereignis und ähnlichen vorherigen Bereichen berechnen

Vergleichen Sie Dimensionselemente zwischen dem Datumsbereich eines Ereignisses und ähnlichen vorherigen Datumsbereichen mithilfe einer Freiformtabellenvisualisierung. Diese Schritte veranschaulichen ein Wochenzeitungsbeispiel, dem Sie folgen können.

1. Öffnen Sie ein Workspace-Projekt und fügen Sie eine **Nicht-Zeitdimension** in die Freiformtabelle ein. Sie können beispielsweise die Dimension &quot;Mobilgerätetyp&quot;verwenden. Wenden Sie den kürzlich erstellten Datumsbereich auf eine Metrik an, z. B. &quot;Vorfälle&quot;:

   ![Mobilgerätetyp nach betroffenem Datumsbereich](assets/mobile_device_type.png)

2. Klicken Sie mit der rechten Maustaste auf den Datumsbereich und klicken Sie dann auf **[!UICONTROL Zeiträume vergleichen]** > **[!UICONTROL Benutzerdefinierter Datumsbereich bis zu diesem Datumsbereich]**. Wählen Sie den Bereich des Ereignisses minus 7 Tage aus. Stellen Sie sicher, dass die Wochentage zwischen dem Ereignis und diesem Datumsbereich aufeinander abgestimmt sind.

   ![Menü &quot;Zeitraum vergleichen&quot;](assets/compare_time_custom.png)

3. Benennen Sie die resultierende Metrik &quot;Prozentänderung&quot;in eine spezifischere Metrik um, z. B. &quot;WoW-Betroffener Bereich&quot;. Klicken Sie auf das Infosymbol und dann auf das Stiftsymbol zum Bearbeiten, um den Metriknamen zu bearbeiten.

   ![Woche über Woche](assets/wow_affected_range.png)

4. Wiederholen Sie die Schritte 3 und 4 für Monatsvergleiche und Jahresvergleiche. Sie können diese Aktion in derselben Tabelle oder in separaten Tabellen ausführen.

## Vergleichs-Datumsbereiche nebeneinander als Zeilen analysieren

Wenn Sie die oben genannten prozentualen Änderungen weiter analysieren möchten, können Sie sie in Zeilen konvertieren.

1. Fügen Sie eine Freiformtabellenvisualisierung hinzu und aktivieren Sie den Tabellen-Builder. Mit dieser Aktion können Sie die Metriken zur prozentualen Änderung in die gewünschte Reihenfolge platzieren.
2. Halten `Ctrl` (Windows) oder `Cmd` (Mac) und ziehen Sie die 3-Prozent-Änderungsmetriken nacheinander in die Tabellenzeilen.

   ![Tabellenaufbau](assets/table_builder.png)

3. Fügen Sie das Segment &quot;Alle Besuche&quot;zur Spalte der Tabelle und andere gewünschte Segmente hinzu.

   ![Tabellenaufbau - Segmente](assets/table_builder_segments.png)

4. Klicken Sie auf **[!UICONTROL Erstellen]**. Aus der resultierenden Tabelle können Sie die betroffenen Bereiche über alle gewünschten Segmente hinweg im Vergleich zur Vorwoche, zum Monat und zum Jahr anzeigen.

   ![Abgeschlossene Tabelle](assets/table_builder_finished.png)
