---
description: In diesen Schritten wird beschrieben, wie Sie eine Data Warehouse-Anforderung erstellen.
title: Berichtsoptionen für eine Data Warehouse-Anforderung konfigurieren
feature: Data Warehouse
source-git-commit: 6e6a406c7f3ab6ad83dcf60dbd78a5f6953f1fbb
workflow-type: tm+mt
source-wordcount: '532'
ht-degree: 18%

---

# Berichtsoptionen für eine Data Warehouse-Anforderung konfigurieren

>[!AVAILABILITY]
>
>Einige der in diesem Artikel beschriebenen Data Warehouse-Funktionen (und andere Data Warehouse-Artikel in diesem Abschnitt) sind nur in der Phase der eingeschränkten Testphase der Veröffentlichung verfügbar und sind möglicherweise noch nicht in Ihrer Umgebung verfügbar.
>
>Informationen darüber, welche Funktionen noch nicht für alle Kunden verfügbar sind, sowie Informationen über die Veröffentlichungszeitleiste dieser Funktionen finden Sie in der [Versionshinweise](/help/release-notes/latest.md).
>
>Diese Anmerkung wird entfernt, wenn die Funktion allgemein verfügbar ist. Informationen zum Analytics-Veröffentlichungsprozess finden Sie unter [Adobe Analytics-Funktionsversionen](/help/release-notes/releases.md).

Beim Erstellen einer Data Warehouse-Anfrage stehen verschiedene Konfigurationsoptionen zur Verfügung. Im Folgenden wird beschrieben, wie Sie Berichtsoptionen für die Anforderung konfigurieren.

Informationen zum Erstellen einer Anforderung sowie Links zu anderen wichtigen Konfigurationsoptionen finden Sie unter [Erstellen einer Data Warehouse-Anfrage](/help/export/data-warehouse/create-request/t-dw-create-request.md).

So konfigurieren Sie Berichtsoptionen für eine Data Warehouse-Anforderung:

1. Erstellen einer Anforderung in Adobe Analytics durch Auswahl von **[!UICONTROL Instrumente]** > **[!UICONTROL Data Warehouse]** > [!UICONTROL **Hinzufügen**].

   Weitere Informationen finden Sie unter [Erstellen einer Data Warehouse-Anfrage](/help/export/data-warehouse/create-request/t-dw-create-request.md).

1. Wählen Sie auf der Seite Neue Data Warehouse-Anforderung die [!UICONTROL **Berichtsoptionen**] Registerkarte.

   ![Berichtsziel-Tab](assets/dw-report-options.png) <!-- update screenshot to include Sort by metrics -->

1. Füllen Sie die folgenden Felder aus:

   | Option | Funktion |
   |---------|----------|
   | [!UICONTROL **Dateiname**] | Gibt den Bericht an. <p>Wenn im Dateinamen eines der folgenden Sonderzeichen verwendet wird, kann die Anforderung nicht gespeichert werden: <code>! &quot; # $ &amp; &#39; ( ) * + , / : ; > = &lt; ? @ [ ] \ ^ ` {  } \| ~</code> </p><p>Das Zeichen % kann nur verwendet werden, wenn es wie folgt durch &quot;R&quot;, &quot;rsid&quot;oder &quot;id&quot;gefolgt wird: <code>%R</code>, <code>%rsid</code>, und <code>%id</code>.</p> |
   | [!UICONTROL **Datumsbereich des Berichts an Dateinamen anhängen**] | Fügt den Datumsbereich zum Namen der Berichtsdatei hinzu. <p>Wenn Sie beispielsweise Daten vom 1. Mai 2024 bis zum 7. Mai 2024 anfordern, enthält der Dateiname den Datumsbereich 20240501 - 20240507.</p> |
   | [!UICONTROL **CSV**] | Stellt Berichte im CSV-Dateiformat zur Anzeige von Daten in einer Tabelle bereit. |
   | [!UICONTROL **Tableau (TDE)**] | Ermöglicht die Berichterstellung im Tableau-Datenextraktion-Dateiformat (TDE), mit dem Daten visualisiert und zusätzliche Daten in Tableau erfasst werden können. |
   | [!UICONTROL **Bericht als komprimierte Datei senden (ZIP)**] | Stellt Berichte im komprimierten ZIP-Dateiformat bereit. Wir empfehlen, diese Option zu aktivieren, wenn E-Mails als [Berichtsziel](/help/export/data-warehouse/create-request/dw-request-report-destinations.md). |
   | [!UICONTROL **Alle Zeilen zurückgeben**] | Wenn diese Option aktiviert ist, werden alle Zeilen in den Bericht aufgenommen. Deaktivieren Sie diese Option, um die Anzahl der einzuschließenden Zeilen anzugeben. |
   | [!UICONTROL **Kommentare zum Beginn des Berichts**] | Fügen Sie alle Kommentare hinzu, die Sie in den Bericht aufnehmen möchten. Kommentare werden zu Beginn des Berichts angezeigt. |
   | [!UICONTROL **Nach Metriken sortieren**] | Bietet nach Rang geordnet Detailberichte in Data Warehouse, die nach absteigendem Metrikwert sortiert sind. Die Sortierung nach Metrik erleichtert die Interpretation von Data Warehouse-Berichten und den Vergleich mit anderen Ansichten von Analytics-Aufschlüsselungsberichten.<p>Weitere Informationen finden Sie unter [Nach Metrik sortieren](/help/export/data-warehouse/sorting-by-metric.md).</p> |
   | [!UICONTROL **Manifestdatei senden**] | Enthält Metadaten zu den im Bericht enthaltenen Dateien.<!-- What kind of metadata is included in the manifest file? --> |
   | [!UICONTROL **Digitale Signaturdatei senden**] | Ermöglicht Empfängern des Berichts zu überprüfen, ob die Datei von Adobe stammt und nicht verändert wurde. |
   | [!UICONTROL **Leere Datei senden, wenn keine Daten im Bericht vorhanden sind**] | Sendet einen Bericht auch dann, wenn der Bericht keine Daten enthält. |

   {style="table-layout:auto"}

1. Fahren Sie mit der Konfiguration Ihrer Data Warehouse-Anfrage auf der [!UICONTROL **Planungsoptionen**] Registerkarte. Weitere Informationen finden Sie unter [Planungsoptionen für Data Warehouse-Anfragen konfigurieren](/help/export/data-warehouse/create-request/dw-request-scheduling.md).
