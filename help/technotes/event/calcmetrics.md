---
title: Ableiten von Daten, die von Ereignissen betroffen sind
description: Verwenden Sie berechnete Metriken, um die von einem Ereignis betroffenen Trenddaten zu korrigieren.
exl-id: 0fe70c8b-fa07-47e4-b6b3-b55eebad1fef
source-git-commit: 549258b0168733c7b0e28cb8b9125e68dffd5df7
workflow-type: tm+mt
source-wordcount: '328'
ht-degree: 4%

---

# Ableiten von Daten, die von Ereignissen betroffen sind

Wenn Sie Daten haben [von einem Ereignis beeinflusst](overview.md)können Sie berechnete Metriken verwenden, um geschätzte Werte für die Dauer des Ereignisses abzuleiten. Wenn Sie beispielsweise über ein Ereignis verfügten, das zu einem Datenabfall von 25 % führte, können Sie dies als Multiplikator in einer berechneten Metrik verwenden.

Diese Schritte funktionieren am besten, wenn Sie die Auswirkungen eines Ereignisses sowohl aus der Sicht der Segmentierung als auch des Datumsvergleichs verstehen. Vergewissern Sie sich, dass Sie [Vergleichen der von einem Ereignis betroffenen Daten mit vorherigen Datumsbereichen](compare-dates.md) und [Ausschließen spezifischer Daten in der Analyse](segments.md) bevor Sie dieser Seite folgen.

>[!NOTE]
>
>Bei diesem Ansatz handelt es sich um eine Schätzung, die auf einem bestimmten Satz von Eingaben und Datumsbereichen basiert. Es wird keine umfassende Lösung für alle Anwendungsfälle oder Datenscheiben sein. Darüber hinaus erfordert dieser Ansatz, dass der betroffene Datumsbereich mindestens 1 Treffer enthält, aus dem berechnet werden soll.

So erstellen Sie eine geschätzte berechnete Metrik für den betroffenen Zeitraum:

1. Erstellen Sie zwei Segmente für &quot;Betroffene Tage&quot;und &quot;Betroffene Tage ausschließen&quot;, wie unter [Ausschließen spezifischer Daten in der Analyse](segments.md).
2. Navigieren Sie zu **[!UICONTROL Komponenten]** > **[!UICONTROL Berechnete Metriken]**.
3. Klicken Sie auf **[!UICONTROL Hinzufügen]**.
4. Ziehen Sie beide der oben genannten Segmente auf die Arbeitsfläche für die Definition. Ändern Sie den Operator zwischen ihnen in eine `+` um sie zu summieren.
5. Fügen Sie die gewünschte Metrik in beiden Segmenten hinzu. Sie können beispielsweise die Metrik &quot;Besuche&quot;verwenden.

   ![Segment Builder](assets/event_segment_builder.png)

6. Klicken **[!UICONTROL Hinzufügen]** Klicken Sie oben rechts im Container &quot;Betroffene Tage&quot;auf **[!UICONTROL Statische Zahl]**. Stellen Sie die statische Zahl auf den Prozentsatz ein, den Sie versetzen möchten, wie unter [Vergleichen der von einem Ereignis betroffenen Daten mit vorherigen Datumsbereichen](compare-dates.md). In diesem Beispiel beträgt der Offset 25 % oder 1,25.

   ![Statische Zahl](assets/event_static_number.png)

7. Wenden Sie die &quot;korrigierte&quot;Metrik in einer Trend-Freiformtabelle nebeneinander an. Alle Tage außerhalb des Ereignisses spiegeln die normale Metrikanzahl wider, während alle betroffenen Tage den Multiplikatorversatz verwenden.

   ![Korrigierte Metrik](assets/event_corrected.png)

8. Zeigen Sie die Daten in einer Linienvisualisierung an, um die Auswirkungen Ihrer korrigierten Metrik anzuzeigen.

   ![Korrigierte Linie](assets/event_line.png)
