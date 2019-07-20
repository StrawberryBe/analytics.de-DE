---
description: Administrative Schritte zum Einrichten von Echtzeit-Berichten
seo-description: Administrative Schritte zum Einrichten von Echtzeit-Berichten
seo-title: Konfiguration von Echtzeitberichten
solution: Analytics
title: Konfiguration von Echtzeitberichten
topic: Admin Tools
uuid: f 48692 a 0-77 c 0-4 ee 4-b 3 ec-eaa 842 d 06 ac 8
translation-type: tm+mt
source-git-commit: 86fe1b3650100a05e52fb2102134fee515c871b1

---


# Konfiguration von Echtzeitberichten

Administrative Schritte zum Einrichten von Echtzeit-Berichten

Um Echtzeit-Berichte in Marketing Reports &amp; Analytics einzurichten, wählen Sie die Report Suite aus und konfigurieren Sie bis zu drei Berichte.

1. Wählen Sie die Report Suite aus, für die Sie Echtzeit-Berichte aktivieren möchten.

   Navigate to **[!UICONTROL Analytics]** &gt; **[!UICONTROL Reports]** &gt; **[!UICONTROL View All Reports &gt; Site Metrics]** &gt; **[!UICONTROL Real-Time]** and select the report suite from the drop-down at the top:

   ![](assets/report_suite_selector.png)

   Wenn Sie versuchen, Echtzeitberichte für eine Report Suite anzuzeigen, die nicht für Echtzeitberichte eingerichtet wurde, wird eine Meldung angezeigt, die Ihnen das Einrichten der Report Suite ermöglicht.

   ![](assets/rep_suite_not_set_up.png)

1. Click **[!UICONTROL Configure]** (gear icon) to run the [!UICONTROL Report Suite Manager].

   (Also available under **[!UICONTROL Analytics]** &gt; **[!UICONTROL Admin &gt; Report Suites]** &gt; **[!UICONTROL Edit Settings]** &gt; **[!UICONTROL Real-Time]**.)

1. Turn on the **[!UICONTROL Enable Real-Time]** setting.
1. Richten Sie die Echtzeit-Datenerfassung für bis zu drei Berichte ein, wobei pro Bericht eine Metrik und drei Dimensionen oder Classifications erstellt werden.

   ![](assets/real_time_admin.png)

   For information on supported real-time metrics and dimensions, see [Supported Metrics and Dimensions](../../../admin/admin/realtime/realtime-metrics.md#concept_B86D8DF89AD448839332AD84B1DF2AE7).

   Falls Sie Classifications erstellt haben, werden sie unter der Dimension angezeigt, für die sie definiert wurden:

   ![](assets/classifications.png)

   >[!NOTE]
   >
   >Für einen einzelnen Echtzeitbericht unterstützen wir derzeit nicht die Aktivierung doppelter Dimensionen, auch wenn für jede Dimension eine andere Classification ausgewählt wurde.

   For more information about classifications, see [About Classifications](/help/components/c-classifications2/c-classifications.md).

   >[!NOTE]
   >
   >Einige Dimensionen wie "Suchbegriff" oder" Produkt" bleiben in Echtzeit nicht wie anderswo in Adobe Analytics erhalten. Wenn Sie eine nicht persistente Metrik auswählen, erscheint folgende Warnmeldung:

   ![](assets/warning_dimensions.png)

1. Click **[!UICONTROL Save]** or **[!UICONTROL Save and View Report]**.

   Nach diesem ersten Bericht-Setup kann es bis zu 20 Minuten dauern, bis Daten gestreamt werden. Daraufhin sind die Daten sofort verfügbar. Informationen zum Anzeigen von Echtzeitberichten erhalten Sie unter [Einen Echtzeitbericht ausführen](https://marketing.adobe.com/resources/help/en_US/sc/user/reports_realtime.html).

1. Standardmäßig haben alle Benutzer Zugriff auf Echtzeitberichte.
