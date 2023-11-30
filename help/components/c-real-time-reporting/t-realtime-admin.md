---
description: Administrative Schritte zum Einrichten von Echtzeitberichten.
title: Echtzeitberichte konfigurieren
feature: Real-time
exl-id: 9e7fc67c-71d5-465a-9553-5bb7e02a9bfd
source-git-commit: ee55349a8c676023a5ce33b56592cad7642199b8
workflow-type: tm+mt
source-wordcount: '295'
ht-degree: 78%

---

# Echtzeitberichte konfigurieren

Die folgenden Informationen enthalten administrative Schritte zum Einrichten von Echtzeitberichten.

Hierzu müssen Sie die Report Suite auswählen und bis zu drei Berichte konfigurieren.

1. Wählen Sie die Report Suite aus, für die Sie Echtzeit-Berichte aktivieren möchten.

   1. Wählen Sie in Analysis Workspace die [!UICONTROL **Arbeitsbereich**] Registerkarte und wählen Sie [!UICONTROL **Berichte**] > [!UICONTROL **Interaktion**] > **[!UICONTROL Echtzeit]**.

   1. Wählen Sie die Report Suite aus der Dropdown-Liste oben aus:

      ![](/help/admin/admin/c-manage-report-suites/c-edit-report-suites/realtime/assets/report_suite_selector.png)

      Wenn Sie versuchen, Echtzeitberichte für eine Report Suite anzuzeigen, die nicht für Echtzeitberichte eingerichtet wurde, wird eine Meldung angezeigt, die Ihnen das Einrichten der Report Suite ermöglicht.

      ![](/help/admin/admin/c-manage-report-suites/c-edit-report-suites/realtime/assets/rep_suite_not_set_up.png)

1. Auswählen **[!UICONTROL Konfigurieren]** zum Ausführen der [!UICONTROL Report Suite Manager].

   (Auch verfügbar unter **[!UICONTROL Analytics]** > **[!UICONTROL Admin > Report Suites]** > **[!UICONTROL Einstellungen bearbeiten]** > **[!UICONTROL Echtzeit]**)

1. Aktivieren Sie die Einstellung **[!UICONTROL Echtzeit aktivieren]**.
1. Richten Sie die Echtzeit-Datenerfassung für bis zu drei Berichte ein, wobei pro Bericht eine Metrik und drei Dimensionen oder Classifications erstellt werden.

   ![](assets/real_time_admin.png)

   Informationen zu unterstützten Echtzeit-Metriken und -Dimensionen finden Sie unter [Unterstützte Metriken und Dimensionen](/help/admin/admin/c-manage-report-suites/c-edit-report-suites/realtime/realtime-metrics.md).

   Falls Sie Classifications erstellt haben, werden sie unter der Dimension angezeigt, für die sie definiert wurden:

   ![](assets/classifications.png)

   >[!NOTE]
   >
   >Für einzelne Echtzeitberichte wird die Aktivierung doppelter Dimensionen derzeit nicht unterstützt, auch wenn für jede Dimension eine andere Classification ausgewählt wird.

   Weitere Informationen zu Klassifizierungen finden Sie unter [Informationen über Klassifizierungen](/help/components/classifications/c-classifications.md).

   >[!NOTE]
   >
   >Manche Dimensionen wie „Keyword“ oder „Produkt“ sind im Gegensatz zu anderen Funktionsbereichen in Adobe Analytics in Echtzeit nicht persistent. Wenn Sie eine nicht persistente Metrik auswählen, erscheint folgende Warnmeldung:

   ![](/help/admin/admin/c-manage-report-suites/c-edit-report-suites/realtime/assets/warning_dimensions.png)

1. Auswählen **[!UICONTROL Speichern]** oder **[!UICONTROL Bericht speichern und anzeigen]**.

   Nach diesem ersten Bericht-Setup kann es bis zu 20 Minuten dauern, bis Daten gestreamt werden. Daraufhin sind die Daten sofort verfügbar. Informationen zum Anzeigen von Echtzeitberichten erhalten Sie unter [Einen Echtzeitbericht ausführen](https://experienceleague.adobe.com/docs/analytics/analyze/reports-analytics/t-running-report-types.html?lang=de).

1. Standardmäßig haben alle Benutzer Zugriff auf Echtzeitberichte.
