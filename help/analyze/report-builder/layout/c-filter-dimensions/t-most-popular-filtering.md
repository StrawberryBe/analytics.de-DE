---
description: Rangordnung und bedingte Filter, die Sie mit UND/ODER-Suchausdrücken entsprechend Boolscher Logik konfigurieren.
title: Bevorzugte Filter
topic: Report builder
uuid: 558fa592-41be-4e66-8705-81262afe1fc7
translation-type: tm+mt
source-git-commit: 99ee24efaa517e8da700c67818c111c4aa90dc02

---


# Bevorzugte Filter

Rangordnung und bedingte Filter, die Sie mit UND/ODER-Suchausdrücken entsprechend Boolscher Logik konfigurieren.

Am meisten bevorzugte Filter sind Ausdruck-Filter, die Sie mit UND/ODER-Bedingungen konfigurieren, z. B. [!UICONTROL Page does not contain]*`<product name>`* mit Bedingungen oder Bedingungsgruppen wie [!UICONTROL Includes All], [!UICONTROL Includes Any]oder [!UICONTROL Excludes All]. Sie können die Ausdrücke [speichern](/help/analyze/report-builder/layout/c-filter-dimensions/saved-filters.md), um sie in anderen Anforderungen in der aktuellen oder anderen Arbeitsmappen zu verwenden.

**So erstellen Sie am meisten bevorzugte Filter**

1. Erstellen oder bearbeiten Sie eine Anforderung und gehen Sie zum [!UICONTROL Request Wizard: Step 2]Bericht.

   ![Schritt-Info](assets/dimension_filter.png)

1. On the [!UICONTROL Request Wizard: Step 2], click the link next to the dimension in the grid, then choose **[!UICONTROL Filter]**.
1. Aktivieren Sie im [!UICONTROL Choose Page] Formular die folgenden Optionen **[!UICONTROL Most Popular]** und konfigurieren Sie sie:

   **Startrang:** Der Startrang einer Dimension. Der Standardwert von 1 steht für das Element mit dem höchsten Wert in der Liste der berichteten Daten. For example, for the dimension [!UICONTROL Page], a starting mark of 1 indicates the single most requested page of your site. Sie können beispielsweise 10 oder einen anderen Wert als Startrangzelle angeben, wodurch ein Bericht erstellt wird, der mit 10 als höchstem Wert beginnt. Metriken werden in absteigender Reihenfolge angeordnet, d. h. die Zeileneinträge mit der höchsten Aktivität werden als erste in der Liste aufgeführt. Wenn Sie mehr als 50.000 Seitennamen in einer Anforderung benötigen, aber einen Bericht über tausende von Seiten ausführen, können Sie die Anforderung kopieren und den Startrang so ändern, dass die Daten in Blöcken von 50.000 abgerufen werden.

   **Anzahl der Einträge:** ( [!UICONTROL Pivot Layout] Nur) Definiert, wie viele Elemente für eine bestimmte Metrik über einen Datumsbereich gemeldet werden. Einige Metriken können hunderte von Einträge aufweisen, andere nur einige wenige. Beispielsweise zeigt eine Zahl von Einträgen von 25 für die Dimension [!UICONTROL Site Section] an, dass der Bericht die 25 am häufigsten besuchten Seiten aufführt.

   Mit Pfeilen können Sie den [!UICONTROL Starting Rank] und [!UICONTROL Number of Entries] den ersten Datenpunkt im Arbeitsblatt ändern. Standardmäßig [!UICONTROL Starting Rank] ist der Wert auf 1 und der Wert [!UICONTROL Number of Entries] auf 10 festgelegt. Diese Werte sind für bestimmte Metriken von mindestens 1 bis maximal 50.000 einstellbar. Jede Metrik hat eine eigene Obergrenze [!UICONTROL Number of Entries]. In diesen Feldern sind keine negativen oder Nullwerte erlaubt. If you choose a [!UICONTROL Starting Rank] as 15 and [!UICONTROL Number of Entries] as 10, data requests for the metric return the 10 most visited pages, where the first most visited page is number 15 in the list for the specific date range. Die 15. bis 25. der am meisten besuchten Seiten werden in absteigender Reihenfolge angezeigt.

   >[!NOTE]
   >
   >Wenn Sie Filter auf bestehende Anforderungen anwenden, ändern sich die angezeigten Daten. Nehmen wir an, Sie haben die zehn besten Karten den Zellen $A$1 bis $A$10 zugeordnet, mit 1 für [!UICONTROL Pages] und 10 für [!UICONTROL Starting Rank] [!UICONTROL Number of Entries]. If you change these values to show 1 for [!UICONTROL Starting Rank] and only 3 for [!UICONTROL Number of Entries], the data previously filling cells $A$4 through $A$10 will no longer appear.

1. To create a search expression, click **[!UICONTROL Add]**.

   ![Schritt-Info](assets/expressions_define_filter.png)

1. On the [!UICONTROL Define Filter] form, configure the conditions appropriate for your needs.

   ![select_cell_icon.png](assets/select_cell_icon.png): Hiermit können Sie eine Bedingung finden, die in einem Zellenwert definiert ist.

   **Bedingung hinzufügen:** Fügt eine Bedingung zum Ausdruck hinzu. Die Zahl der Bedingungen, die Sie hinzufügen können, ist nicht beschränkt.

1. Klicken Sie auf **[!UICONTROL OK]**.

   ![Schritt-Info](assets/choose_page_02.png)

1. Klicken Sie im [!UICONTROL Choose Page] Formular auf **[!UICONTROL Save]** , um den Ausdruck zu speichern.
1. Klicken Sie auf **[!UICONTROL OK]**.
