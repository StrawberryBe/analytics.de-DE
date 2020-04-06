---
description: 'null'
title: In Power BI veröffentlichen – Übersicht
uuid: ad688817-6e3c-45da-983d-48c123465309
translation-type: tm+mt
source-git-commit: dabaf6247695bc4f3d9bfe668f3ccfca12a52269

---


# In Power BI veröffentlichen – Übersicht

Microsoft Power BI ist eine Suite von Business Analytics-Dashboards, um Daten zu analysieren und Erkenntnisse zu teilen. Die Adobe Analytics-Integration mit Power BI ermöglicht Ihnen, Report Builder-Analysedaten in Microsoft Power BI zu visualisieren und in Ihrem Unternehmen bequem gemeinsam zu verwenden.

Als Analytiker mussten Sie zuvor eine Verteilung von Report Builder-Arbeitsmappen per E-Mail (oder ftp) planen. Sie können Ihren Geschäftspartnern nun (aus ihren Power BI-Konten) Zugriff auf genaue und aktuelle Daten in einer webbasierten Umgebung geben, die plattformübergreifend und geräteübergreifend verfügbar ist.

Durch Kombination der Berichterstellungsfunktion von Report Builder mit den Visualisierungsfunktionen von Power BI sind Informationen für alle Mitglieder Ihres Unternehmens leichter zugänglich. Mit Power BI können Sie Adobe Analytics auch mit anderen Datenquellen (z. B. Verkaufsorte, CRM) integrieren, um einzigartige Kundeneinblicke, Verbände und Chancen zu ermitteln.

![](assets/aaplusbi.png)

Die Integration mit Adobe Report Builder ermöglicht Ihnen Folgendes

* [Terminierte Report Builder-Arbeitsmappen in Power BI veröffentlichen](/help/analyze/report-builder/whats-new-arb.md#rb-5-5-section)
* [Alle formatierten Tabellen in der Arbeitsmappe als Power BI-Datensatztabellen veröffentlichen](/help/analyze/report-builder/whats-new-arb.md#rb-5-5-section)
* [Alle Report Builder-Anforderungen als Power BI-Datensatztabellen veröffentlichen](/help/analyze/report-builder/whats-new-arb.md#rb-5-5-section)

## Systemanforderungen {#section_0B71092D853446F38FA36447DAC0D32B}

* Adobe Report Builder 5.5 [installiert](/help/analyze/report-builder/setup/t-install-arb.md)
* Aktives Microsoft-Konto für die Anmeldung bei Power BI

## Arbeitsmappe in Power BI veröffentlichen {#section_21CA66229EC240D49594A9A7D3FBA687}

Geplante Arbeitsmappen sind Excel-Arbeitsblätter, die mit Daten aus Adobe Analytics gefüllt sind und regelmäßig nach einem festen Zeitplan gesendet werden.

**Arbeitsmappe in Report Builder veröffentlichen**

1. Generieren Sie eine Arbeitsmappe in Report Builder und speichern Sie sie.
1. On the Report Builder Toolbar, click **[!UICONTROL Schedule]** > **[!UICONTROL New]**.

1. Aktivieren Sie im einfachen Planungsassistenten das Kontrollkästchen neben **[!UICONTROL Publish Workbook to Microsoft Power BI]**.

   ![](assets/simple-schedule-wizard.png)

1. Geben Sie Ihre E-Mail an und senden Sie sie sofort oder geben Sie die Häufigkeit der Planung an (stündlich, täglich usw.).
1. Klicken Sie **[!UICONTROL OK]** zum Veröffentlichen auf .
1. Sie werden jetzt aufgefordert, sich bei Ihrem Microsoft-Konto anzumelden. Geben Sie Ihre Anmeldeinformationen ein.
1. Die Report Builder-Arbeitsmappe wird in die Planung aufgenommen und in Power BI veröffentlicht.

   Durch jede geplante Instanz und nachdem der Report Builder-Prozess die Arbeitsmappe mit den neuesten Analytics-Daten aktualisiert hat, wird die Arbeitsmappe in Microsoft Power BI veröffentlicht.

**Report Builder-Arbeitsmappendaten in Power BI anzeigen**

1. Klicken Sie in Power BI auf die Arbeitsmappe unter dem [!UICONTROL Workbooks] Menü.

   ![](assets/workbooks-power-bi.png)

1. Jetzt können Sie die Dashboard-Daten der Arbeitsmappe anzeigen.  ![](assets/view-data-pbi.png)

1. Sie können dann einen Bereich dieser Arbeitsmappe anheften, um sie in ein beliebiges Power BI-Dashboard einzuschließen.

## Alle formatierten Tabellen in der Arbeitsmappe als Power BI-Datensatztabellen veröffentlichen {#section_7C54A54E75184DD6BAEF4ACCE241239A}

>[!NOTE] Wenn die Arbeitsmappe ein Makro enthält, wird „Alle formatierten Tabellen in der Arbeitsmappe als Power BI-Datensatztabellen veröffentlichen“ deaktiviert.

Anstatt die gesamte Arbeitsmappe zu importieren, können Sie nur den Inhalt aller formatierten Tabellen in der Arbeitsmappe importieren.

**Verwendungsfall**: Sie besitzen eine Excel-Arbeitsmappe, die Daten aus mehreren Report Builder-Anforderungen abruft und eine Zusammenfassungstabelle mit zahlreichen Formeln erstellt. Sie können nur die Zusammenfassungstabelle in Power BI importieren und eine Visualisierung dafür erstellen.

**Formatierte Tabelle in Report Builder veröffentlichen**

1. Generieren Sie in Report Builder eine Datentabelle, die eine Kopfzeile gefolgt von einer Datenzeile enthält.
1. Wählen Sie die Tabelle und dann **[!UICONTROL Format as Table]** im [!UICONTROL Home] Menü aus. Die Tabelle erhält einen Standardnamen (Tabelle 1, Tabelle 2 usw.), den Sie jedoch im Menü [!UICONTROL Design] ändern können.

1. On the Report Builder Toolbar, click **[!UICONTROL Schedule]** > **[!UICONTROL New]**.

1. Klicken Sie im einfachen Planungsassistenten auf **[!UICONTROL Advanced Scheduling Options]**.
1. Markieren Sie [!UICONTROL Scheduling Wizard - Advanced]auf der **[!UICONTROL Publishing Options]** Registerkarte das Kontrollkästchen neben **[!UICONTROL Publish all Formatted Tables as Power BI dataset tables]**.

   ![](assets/advanced-schedule-wizard2.png)

1. (Optional) Sie können den Namen des veröffentlichten Assets in Power BI anpassen. Dies kann nützlich sein, wenn Sie die Versionsverwaltung als Teil des Arbeitsmappennamens verwenden (z. B. myappe_v1.1.xlsx) und die Versionsnummer nicht im Namen des veröffentlichten Power BI-Assets angezeigt werden soll. Es hat den zusätzlichen Vorteil, dass sich das veröffentlichte Asset nicht ändert, wenn sich die Versionsnummer ändert. ( [Spezifikationen](/help/analyze/report-builder/c-publish-power-bi/specifications-limits.md) zur Ansicht.)

**Tabellendaten in Power BI anzeigen**

1. Wechseln Sie in Power BI zum **[!UICONTROL Workspaces]** > **[!UICONTROL Datasets]** -Menü.

   ![](assets/datasets-menu.png)

1. Wählen Sie den veröffentlichten Datensatz aus und klicken Sie auf das [!UICONTROL Create report] Symbol daneben. Beachten Sie, dass die Tabellen als Felder angezeigt werden.

   ![](assets/formatted-tables.png)

1. Wählen Sie eine Tabelle und die zugehörigen Spalten aus.

   ![](assets/view-table-dataset.png)

1. Im [!UICONTROL Visualizations] Menü können Sie auswählen, wie eine Tabelle in Power BI visualisiert werden soll. Sie können Ihre Daten beispielsweise als Liniendiagramm präsentieren:

   ![](assets/bi-line-graph.png)

1. Von hier aus können Sie Visualisierungen aus dieser Datensatztabelle erstellen.

## Veröffentlichen Sie alle Report Builder-Anforderungen als Power BI-Datensatztabellen {#section_0C26057C7DBB4068A643FDD688F6E463}

Sie können alle Ihre Anforderungen in Datensatztabellen umwandeln und daraus Visualisierungen erstellen.

>[!IMPORTANT]
>
>Wenn die Arbeitsmappe mehr als 100 Anforderungen enthält, werden nur die ersten 100 Anforderungen in Power BI veröffentlicht. Darüber hinaus werden für jede an Power BI veröffentlichte Anforderung nur die ersten 10.000 Datenzeilen veröffentlicht. Während diese Anfragen erfolgreich über die Planung bereitgestellt werden, ist der Umfang der Veröffentlichung auf Power BI begrenzt.

1. Öffnen oder erstellen Sie in Report Builder eine Arbeitsmappe mit Report Builder-Anforderungen.
1. On the Report Builder Toolbar, click **[!UICONTROL Schedule]** > **[!UICONTROL New]**.

1. Klicken Sie im einfachen Planungsassistenten auf **[!UICONTROL Advanced Scheduling Options]**.
1. Aktivieren Sie auf der [!UICONTROL Scheduling Wizard - Advanced]Registerkarte **[!UICONTROL Publishing Options]** das Kontrollkästchen neben **[!UICONTROL Publish all Report Builder Requests as Power BI Dataset Tables]**![](assets/advanced-schedule-wizard2.png)

1. Klicken Sie auf **[!UICONTROL OK]**.

**Anforderungsdaten in Power BI anzeigen**

Jede terminierte Report Builder-Anforderung wird als Tabelle im Datensatz veröffentlicht. Jede Anforderungstabelle wird nach der primären Dimension in der Anforderung benannt und verfügt über eine [!UICONTROL Report Suite] und eine [!UICONTROL Segments] Spalte.

1. Wechseln Sie in Power BI zum **[!UICONTROL Workspaces]** > **[!UICONTROL Datasets]** -Menü.

1. Wählen Sie die von Ihnen veröffentlichte Anforderung aus und klicken Sie auf das [!UICONTROL Create report] Symbol daneben.

   Beachten Sie, dass die Anforderungen als Tabellen im [!UICONTROL Fields] Menü angezeigt werden.

   ![](assets/published-requests.png)

   >[!NOTE]
   >
   >Unabhängig davon, welches Layout Sie für Ihre Report Builder-Anforderung auf dem Arbeitsblatt konfiguriert haben (Pivot-Layout, benutzerdefiniertes Layout, Layout mit nicht sichtbaren Spalten), veröffentlicht Report Builder Ihre Anforderung immer in dem gleichen zweidimensionalen Format mit einer Kopfzeile: Datum, Dimensionen, Metriken, Report Suites, Segmente.

1. Beachten Sie auch, dass es eine zusätzliche Tabelle namens **[!UICONTROL Legend]**. Wenn Sie eine Anforderung aus dem Report Builder-Kontext herausnehmen, können Sie sich möglicherweise nicht mehr an die Bedeutung jeder einzelnen Anforderung erinnern. Die Legende-Tabelle zeigt beispielsweise den Namen der einzelnen Anforderungen unter der Tabelle-ID an. Sie können auch die anderen Legend-Spalten hinzufügen, um eine vollständige Ansicht der Anforderung zu erhalten.

   ![](assets/legend-table.png)

