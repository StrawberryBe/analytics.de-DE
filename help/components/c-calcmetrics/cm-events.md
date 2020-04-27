---
title: Ableiten von Daten, die von Ereignissen betroffen sind
description: Verwenden Sie berechnete Metriken, um Trenddaten zu korrigieren, die von einem Ereignis betroffen sind.
translation-type: tm+mt
source-git-commit: 8d1a67f0c05afb66b6a961059101f5c889b52790

---


# Ableiten von Daten, die von Ereignissen betroffen sind

Wenn Daten von einem Ereignis [](/help/technotes/event-impacted.md)beeinflusst werden, können Sie berechnete Metriken verwenden, um Trendwerte für die Dauer des Ereignisses abzuleiten. Wenn Sie z. B. ein Ereignis hatten, das zu einem Datenverlust von 25 % führte, können Sie dies als Multiplikator in einer berechneten Metrik verwenden.

>[!NOTE] Diese Schritte funktionieren am besten, wenn Sie die Auswirkungen eines Ereignisses aus der Sicht der Segmentierung und des Datumsvergleichs verstehen. Vergewissern Sie sich, dass Sie die Daten [vergleichen, die von einem Ereignis betroffen sind, mit vorherigen Datumsbereichen](/help/analyze/analysis-workspace/components/calendar-date-ranges/compare-event.md) und bestimmte Daten in Analyse [](../c-segmentation/use-cases/exclude-date-range.md) ausschließen, bevor Sie dieser Seite folgen.

1. Erstellen Sie zwei Segmente für &quot;Betroffene Tage&quot;und &quot;Betroffene Tage ausschließen&quot;, wie unter Bestimmte Daten in der Analyse [ausschließen](../c-segmentation/use-cases/exclude-date-range.md)beschrieben.
2. Navigieren Sie zu **[!UICONTROL Components]** > **[!UICONTROL Calculated metrics]**.
3. Klicken Sie auf **[!UICONTROL Add]**.
4. Ziehen Sie beide oben genannten Segmente in die Arbeitsfläche der Definition. Ändern Sie den Operator zwischen ihnen in eine `+` Zusammenfassung.
5. Hinzufügen Sie die gewünschte Metrik in beiden Segmenten. Sie können beispielsweise die Metrik &quot;Besuche&quot;verwenden.

   ![Segmentaufbau](assets/event_segment_builder.png)

6. Klicken Sie **[!UICONTROL Add]** oben rechts im Container &quot;Betroffene Tage&quot;auf und klicken Sie dann auf **[!UICONTROL Static number]**. Stellen Sie die statische Zahl auf den Prozentwert ein, mit dem Sie Ihre Daten verrechnen möchten, wie unter Datum [vergleichen, das von einem Ereignis beeinflusst wurde, mit vorherigen Bereichen](/help/analyze/analysis-workspace/components/calendar-date-ranges/compare-event.md)beschrieben. In diesem Beispiel beträgt der Offset 25 % oder 1,25.

   ![Statische Zahl](assets/event_static_number.png)

7. Wenden Sie die &quot;korrigierte&quot;Metrik nebeneinander in einer Trendfreie Tabelle an. Alle Tage außerhalb des Ereignisses beziehen sich auf ihre normale Metrikanzahl, während alle betroffenen Tage den Multiplikator-Offset verwenden.

   ![Korrigierte Metrik](assets/event_corrected.png)

8. Ansicht der Daten in einer Linienvisualisierung, um die Auswirkungen Ihrer korrigierten Metrik zu sehen.

   ![Korrigierte Linie](assets/event_line.png)
