---
description: 'null '
seo-description: 'null '
seo-title: Veröffentlichen auf Power BI - Übersicht
title: Veröffentlichen auf Power BI - Übersicht
uuid: ad 888817-6 e 3 c -45 da -983 d -48 c 123465309
translation-type: tm+mt
source-git-commit: 86fe1b3650100a05e52fb2102134fee515c871b1

---


# Veröffentlichen auf Power BI - Übersicht

Bei Microsoft Power BI handelt es sich um eine Suite von Business Analytics-Dashboards, die zur Analyse von Daten und zur Weitergabe von Erkenntnissen genutzt werden können. Die Adobe Analytics-Integration mit Power BI ermöglicht Ihnen, ReportBuilder-Analysedaten in Microsoft Power BI zu visualisieren und in Ihrem Unternehmen bequem gemeinsam zu verwenden.

Als Analytiker mussten Sie zuvor eine Verteilung von ReportBuilder-Arbeitsmappen per E-Mail (oder ftp) planen. Jetzt können Sie den Entscheidungsträgern in Ihrem Unternehmen Zugriff (über ihre Power BI-Konten) gewähren, um Daten in einer webbasierten Umgebung zu korrigieren und zu aktualisieren, die unabhängig von der Plattform und vom Gerät zugänglich ist.

Durch Kombination der Berichterstellungsfunktion von ReportBuilder mit den Visualisierungsfunktionen von Power BI sind Informationen für alle Mitglieder Ihres Unternehmens leichter zugänglich. Mithilfe von Power BI können Sie Adobe Analytics auch mit anderen Datenquellen verbinden (z. B. Verkaufsstellendaten, CRM), um einzigartige Erkenntnisse über Kunden, Zusammenhänge und Opportunities abzuleiten.

![](assets/aaplusbi.png)

Die Integration mit Adobe ReportBuilder ermöglicht Ihnen Folgendes

* [Terminierte ReportBuilder-Arbeitsmappen in Power BI veröffentlichen](../../../analyze/report-builder/whats-new-arb.md#section_21CA66229EC240D49594A9A7D3FBA687)
* [Alle formatierten Tabellen in der Arbeitsmappe als Power BI-Datensatztabellen veröffentlichen](../../../analyze/report-builder/whats-new-arb.md#section_7C54A54E75184DD6BAEF4ACCE241239A)
* [Alle ReportBuilder-Anforderungen als Power BI-Datensatztabellen veröffentlichen](../../../analyze/report-builder/whats-new-arb.md#section_0C26057C7DBB4068A643FDD688F6E463)

## Systemanforderungen {#section_0B71092D853446F38FA36447DAC0D32B}

* Adobe Report Builder 5.5 [installed](../../../analyze/report-builder/setup/t-install-arb.md#task_0CA66703882F469EB6DBD9298975D6C3)
* Aktives Microsoft-Konto für die Anmeldung bei Power BI

## Publish workbook to Power BI {#section_21CA66229EC240D49594A9A7D3FBA687}

Geplante Arbeitsmappen sind Excel-Arbeitsblätter, die mit Daten aus Adobe Analytics gefüllt sind und regelmäßig nach einem festen Zeitplan gesendet werden.

**Arbeitsmappe in Reportbuilder veröffentlichen**

1. Generieren Sie eine Arbeitsmappe in ReportBuilder und speichern Sie sie.
1. On the Report Builder Toolbar, click **[!UICONTROL Schedule]** &gt; **[!UICONTROL New]**.

1. Aktivieren Sie im Fenster „Planungs-Assistent – Grundlegend“ das Kontrollkästchen neben **[!UICONTROL Arbeitsmappe in Microsoft Power BI veröffentlichen]**.

   ![](assets/simple-schedule-wizard.png)

1. Geben Sie Ihre E-Mail-Adresse an, um die Arbeitsmappe sofort zu senden, oder geben Sie die Planungshäufigkeit (stündlich, täglich usw.) an.
1. Klicken Sie zum Veröffentlichen auf **[!UICONTROL OK].**
1. Jetzt werden Sie aufgefordert, sich bei Ihrem Microsoft-Konto anzumelden. Geben Sie Ihre Anmeldedaten an.
1. Die ReportBuilder-Arbeitsmappe wird in die Planung aufgenommen und in Power BI veröffentlicht.

   Durch jede geplante Instanz und nachdem der ReportBuilder-Prozess die Arbeitsmappe mit den neuesten Analytics-Daten aktualisiert hat, wird die Arbeitsmappe in Microsoft Power BI veröffentlicht.

**Report Builder-Arbeitsmappen-Daten in Power BI anzeigen**

1. Doppelklicken Sie in Power BI auf die Arbeitsmappe unter dem Menü [!UICONTROL Arbeitsmappen].

   ![](assets/workbooks-power-bi.png)

1. Jetzt können Sie die Dashboard-Daten der Arbeitsmappe anzeigen.  ![](assets/view-data-pbi.png)

1. Sie können dann einen Bereich dieser Arbeitsmappe anheften, um sie in ein beliebiges Power BI-Dashboard einzuschließen.

## Publish all formatted tables in the workbook as Power BI dataset tables {#section_7C54A54E75184DD6BAEF4ACCE241239A}

>[!NOTE]
>
>Wenn die Arbeitsmappe ein Makro enthält, wird die Option "Alle formatierten Tabellen in den Arbeitsmappen als Power BI Datenblatt veröffentlichen" deaktiviert.

Statt die gesamte Arbeitsmappe zu importieren, können Sie nur den Inhalt aller formatierten Tabellen innerhalb der Arbeitsmappe importieren.

**Verwendungsfall**: Sie besitzen eine Excel-Arbeitsmappe, die Daten aus mehreren ReportBuilder-Anforderungen abruft und eine Zusammenfassungstabelle mit zahlreichen Formeln erstellt. Sie können nur die Zusammenfassungstabelle in Power BI importieren und eine Visualisierung dafür erstellen.

**Veröffentlichen einer formatierten Tabelle in Reportbuilder**

1. Generieren Sie in ReportBuilder eine Datentabelle, die eine Kopfzeile gefolgt von einer Datenzeile enthält.
1. Wählen Sie die Tabelle aus und anschließend im Menü **[!UICONTROL Startseite]die Option**[!UICONTROL Als Tabelle formatieren]. Die Tabelle erhält einen Standardnamen (Tabelle 1, Tabelle 2 usw.), den Sie jedoch im Menü [!UICONTROL Design] ändern können.

1. On the Report Builder Toolbar, click **[!UICONTROL Schedule]** &gt; **[!UICONTROL New]**.

1. Klicken Sie im Fenster „Planungs-Assistent – Grundlegend“ auf **[!UICONTROL Erweiterte Planungsoptionen]**.
1. In the [!UICONTROL Scheduling Wizard - Advanced], on the **[!UICONTROL Publishing Options]**tab, check the box next to **[!UICONTROL Publish all Formatted Tables as Power BI dataset tables]**.

   ![](assets/advanced-schedule-wizard2.png)

1. (Optional) Sie können den Namen des veröffentlichten Assets in Power BI anpassen. Dies kann nützlich sein, wenn Sie eine Versionsnummer als Teil des Arbeitsmappennamens verwenden (z. B. meineArbeitsmappe_v1.1.xlsx) und nicht möchten, dass die Versionsnummer im Namen des veröffentlichten Power BI-Assets angezeigt wird. Dies hat den zusätzlichen Vorteil, dass sich das veröffentlichte Asset nicht ändert, wenn sich die Versionsnummer ändert. ([Angaben](../../../analyze/report-builder/c-publish-power-bi/specifications-limits.md#concept_1B6522B4D7A9482680198F125D94EEFD) dazu finden Sie hier.)

**Anzeigen der Tabellendaten in Power BI**

1. In Power BI, go to the **[!UICONTROL Workspaces]** &gt; **[!UICONTROL Datasets]** menu.

   ![](assets/datasets-menu.png)

1. Wählen Sie den Datensatz aus, den Sie veröffentlicht haben, und klicken Sie daneben auf das Symbol [!UICONTROL Bericht erstellen]. Beachten Sie, dass die Tabellen als Felder angezeigt werden.

   ![](assets/formatted-tables.png)

1. Wählen Sie eine Tabelle und die dazugehörigen Spalten aus.

   ![](assets/view-table-dataset.png)

1. Im Menü [!UICONTROL Visualisierungen] können Sie auswählen, wie eine Tabelle in Power BI visualisiert werden soll. Beispielsweise können Sie festlegen, dass Ihre Daten als Kantengraph dargestellt werden:

   ![](assets/bi-line-graph.png)

1. Hier können Sie Visualisierungen aus dieser Datensatztabelle erstellen.

## Publish all Report Builder requests as Power BI Dataset tables {#section_0C26057C7DBB4068A643FDD688F6E463}

Sie können alle Ihre Anforderungen in Datensatztabellen umwandeln und daraus Visualisierungen erstellen.

>[!IMPORTANT]
>
>Wenn die Arbeitsmappe mehr als 100 Anforderungen enthält, werden nur die ersten 100 Anforderungen auf Power BI veröffentlicht. Außerdem werden nur die ersten 10.000 Datenzeilen jeder an Power BI gesendeten Anforderung veröffentlicht. Während diese Anforderungen also erfolgreich von der Planungsfunktion bereitgestellt werden, ist der Umfang der Veröffentlichungen in Power BI eingeschränkt.

1. Öffnen oder erstellen Sie in ReportBuilder eine Arbeitsmappe mit ReportBuilder-Anforderungen.
1. On the Report Builder Toolbar, click **[!UICONTROL Schedule]** &gt; **[!UICONTROL New]**.

1. Klicken Sie im Fenster „Planungs-Assistent – Grundlegend“ auf **[!UICONTROL Erweiterte Planungsoptionen]**.
1. In the [!UICONTROL Scheduling Wizard - Advanced], on the **[!UICONTROL Publishing Options]**tab, check the box next to **[!UICONTROL Publish all Report Builder Requests as Power BI Dataset Tables]** ![](assets/advanced-schedule-wizard2.png)

1. Klicken Sie auf **[!UICONTROL OK]**.

**Anforderungsdaten in Power BI anzeigen**

Jede terminierte ReportBuilder-Anforderung wird als Tabelle im Datensatz veröffentlicht. Jede Anforderungstabelle wird nach der primären Dimension in der Anforderung benannt und verfügt über eine Spalte [!UICONTROL Report Suite] und [!UICONTROL Segmente].

1. In Power BI, go to the **[!UICONTROL Workspaces]** &gt; **[!UICONTROL Datasets]** menu.

1. Wählen Sie die Anforderung aus, die Sie veröffentlicht haben, und klicken Sie daneben auf das Symbol [!UICONTROL Bericht erstellen].

   Beachten Sie, dass die Anforderungen im Menü [!UICONTROL Felder] als Tabellen angezeigt werden.

   ![](assets/published-requests.png)

   >[!NOTE]
   >
   >Unabhängig davon, wie Sie Ihre Reportbuilder-Anforderung für das Layout im Arbeitsblatt konfiguriert haben (Pivot-Layout, benutzerdefiniertes Layout, unsichtbare Spalten), veröffentlicht Reportbuilder Ihre Anforderung immer im zweidimensionalen und einzelnen Header-Format: Datum, Dimensionen, Metriken, Report Suites, Segmente.

1. Beachten Sie außerdem, dass eine zusätzliche Tabelle mit dem Namen **[!UICONTROL Legende vorhanden ist]**. Wenn Sie eine Anforderung aus dem ReportBuilder-Kontext herausnehmen, können Sie sich möglicherweise nicht mehr an die Bedeutung jeder einzelnen Anforderung erinnern. Der Zweck der Tabelle „Legende“ besteht darin, beispielsweise den Namen der einzelnen Anforderungen unter „Tabellen-ID“ anzuzeigen. Sie können die anderen Legendenspalten hinzufügen, um eine vollständige Ansicht der Anforderung zu erhalten.

   ![](assets/legend-table.png)

