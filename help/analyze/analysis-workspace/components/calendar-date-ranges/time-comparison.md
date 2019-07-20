---
description: Mit dem Datumsvergleich im Analysis Workspace können Sie jede Spalte mit einem Datumsbereich ausführen und einen allgemeinen Datumsvergleich erstellen, z. B. Jahres-, Quartals-, Monatsvergleich usw.
seo-description: Mit dem Datumsvergleich im Analysis Workspace können Sie jede Spalte mit einem Datumsbereich ausführen und einen allgemeinen Datumsvergleich erstellen, z. B. Jahres-, Quartals-, Monatsvergleich usw.
seo-title: Datumsvergleich
title: Datumsvergleich
uuid: ef 18 f 9 d 9-b 6 ad -4859-b 7 c 9-9750 ca 0 df 519
translation-type: tm+mt
source-git-commit: 86fe1b3650100a05e52fb2102134fee515c871b1

---


# Datumsvergleich

Mit dem Datumsvergleich in Analysis Workspace können Sie mit einer Spalte, die einen Datumsbereich enthält, einen standardmäßigen Datumsvergleich erstellen, z. B. Jahres-, Quartals-, Monatsvergleich usw.

## Zeiträume vergleichen {#section_C4E36BFE0F5C4378A74E705747C9DEE4}

Für Analysen wird Kontext benötigt, der oft durch einen vorherigen Zeitraum bereitgestellt wird. „Wie viel besser/schlechter geht es uns als zu diesem Zeitpunkt letztes Jahr?“ ist beispielsweise eine Kernfrage, um Ihr Geschäft zu verstehen. Der Datumsvergleich enthält automatisch eine Spalte „Differenz“, die die prozentuale Veränderung im Vergleich zu einem bestimmten Zeitraum angibt.

1. Erstellen Sie eine Freiform-Tabelle mit beliebigen Dimensionen und Metriken, die Sie mit einem bestimmten Zeitraum vergleichen möchten.
1. Rechtsklicken Sie auf eine Tabellenzeile und wählen Sie **[!UICONTROL Zeiträume vergleichen aus]**.

   ![](assets/compare-time.png)

   >[!IMPORTANT]
   >
   >Diese Rechtsklick-Option ist für Metrikzeilen, Datumsbereichzeilen und Zeitdimensionszeilen deaktiviert.

1. Je nachdem, wie Sie den Datumsbereich der Tabelle festgelegt haben, stehen die folgenden Optionen zum Vergleich zur Verfügung:

   | Option | Beschreibung |
   |---|---|
   | **[!UICONTROL Vorhergehende/r/s Woche/Monat/Quartal/Jahr vor diesem Datumsbereich]** | Vergleich mit der Woche/dem Monat usw. unmittelbar vor diesem Datumsbereich. |
   | **[!UICONTROL Diese/r/s Woche/Monat/Quartal/Jahr letztes Jahr]** | Vergleich mit demselben Datumsbereich vor einem Jahr. |
   | **[!UICONTROL Bereich auswählen]** | Ermöglicht die Auswahl eines benutzerdefinierten Datumsbereichs. |

   >[!NOTE]
   >
   >When you select a custom number of days, for example October 7 - October 20 (a 14-day range), you will get only 2 options: **[!UICONTROL Prior 14 days before this date range]**, and **[!UICONTROL Select range]**.

1. Der resultierende Vergleich sieht wie folgt aus:

   ![](assets/compare-time-result.png)

   Zeilen in der Spalte „Prozentwertänderung“ sind rot bei negativen Werten und grün bei positiven Werten.

1. (Optional) Wie bei allen anderen Workspace-Projekten können Sie basierend auf diesen Zeitvergleichen Visualisierungen erstellen. Hier ist z. B. ein Balkendiagramm:

   ![](assets/compare-time-barchart.png)

   Beachten Sie, dass Sie die Einstellung [!UICONTROL Prozentsätze] in den [!UICONTROL Visualisierungseinstellungen] aktivieren müssen, damit die prozentuale Änderung im Balkendiagramm angezeigt wird.

## Add a time period column for comparison {#section_93CC2B4F48504125BEC104046A32EB93}

Sie können jetzt Zeiträume zu allen Spalten in einer Tabelle hinzufügen. So können Sie einen Zeitraum hinzufügen, der von dem abweicht, auf den Ihr Kalender eingestellt ist. Dies ist eine weitere Möglichkeit, um Daten zu vergleichen.

1. Rechtsklicken Sie auf eine Spalte in der Tabelle und wählen Sie **[!UICONTROL Spalte für Zeitraum hinzufügen aus]** ![](assets/add-time-period-column.png)

1. Je nachdem, wie Sie den Datumsbereich der Tabelle festgelegt haben, stehen die folgenden Optionen zum Vergleich zur Verfügung:

   | Option | Beschreibung |
   |---|---|
   | **[!UICONTROL Vorhergehende/r/s Woche/Monat/Quartal/Jahr vor diesem Datumsbereich]** | Fügt eine Spalte mit der Woche/dem Monat usw. unmittelbar vor diesem Datumsbereich hinzu. |
   | **[!UICONTROL Diese/r/s Woche/Monat/Quartal/Jahr letztes Jahr]** | Fügt denselben Datumsbereich des Vorjahres hinzu. |
   | **[!UICONTROL Bereich auswählen]** | Ermöglicht die Auswahl eines benutzerdefinierten Datumsbereichs. |

   >[!NOTE]
   >
   >When you select a custom number of days, for example October 7 - October 20 (a 14-day range), you will get only 2 options: **[!UICONTROL Prior 14 days before this date range]**, and **[!UICONTROL Select range]**.

1. Der Zeitraum wird am Anfang der ausgewählten Spalte eingefügt:

   ![](assets/add-time-period-column2.png)

1. Sie können so viele Zeitspalten hinzufügen, wie Sie möchten, sowie verschiedene Datumsbereiche kombinieren:

   ![](assets/add-time-period-column4.png)

1. Sie können außerdem nach jeder Spalte sortieren. Dadurch wird die Reihenfolge der Tage abhängig von der jeweiligen Spalte geändert.

## Align column dates to start on same row {#section_5085E200082048CB899C3F355062A733}

Mit einer neuen Einstellung für alle Tabellen können Sie **[!UICONTROL Datumswerte in jeder Spalte so ausrichten, dass sie in der gleichen Zeile beginnen (wird auf die gesamte Tabelle angewendet)]**. „Wird auf die gesamte Tabelle angewendet“ bedeutet, dass, wenn Sie z. B. eine Aufschlüsselung in der Tabelle durchführen und diese Einstellung für die Aufschlüsselung ändern, die Einstellung für die gesamte Tabelle geändert wird.

![](assets/date-comparison-setting.png)

>[!IMPORTANT]
>
>This setting is **disabled** (unchecked) for all existing projects and **enabled** (checked) for all new projects.

Beispiel: Wenn Sie die Daten in einem Monatsvergleich zwischen Oktober und September 2016 ausrichten, beginnt die linke Spalte mit dem 1. Oktober und die rechte Spalte mit dem 1. September:

![](assets/add-time-period-column3.png)

<!-- 

<p>See Jonny Moon's email from November 3. </p>

 -->

