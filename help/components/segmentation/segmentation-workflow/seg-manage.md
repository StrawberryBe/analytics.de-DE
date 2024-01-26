---
description: Der Segment-Manager bietet verschiedene Möglichkeiten zum Kuratieren von Segmenten wie das Freigeben, Filtern, Taggen, Genehmigen, Kopieren, Löschen und Kennzeichnen als Favoriten.
title: Segmente verwalten (Segment-Manager)
feature: Segmentation
exl-id: be182a55-23cb-415f-a7d0-3c1efeead1a1
source-git-commit: df9c6d59ef5f5c43d0e1ef822bd23bc0e09ff20e
workflow-type: tm+mt
source-wordcount: '749'
ht-degree: 30%

---

# Segment-Manager

Der Segment-Manager bietet verschiedene Möglichkeiten zum Kuratieren von Segmenten wie das Freigeben, Filtern, Taggen, Genehmigen, Kopieren, Löschen und Kennzeichnen als Favoriten.

Der Segment-Manager in Analytics zeigt Ihnen alle Segmente, die sich in Ihrem Besitz befinden und für Sie freigegeben wurden. Benutzer auf Administratorebene sehen alle Segmente der Organisation. Diese Übersicht zeigt die Benutzeroberfläche und die Funktionen des Segment-Managers.

![Segment-Manager](assets/segments-manager.png)

## Zugriff auf den Segment-Manager

1. Wählen Sie in Adobe Analytics die **[!UICONTROL Komponenten]** Registerkarte und wählen Sie **[!UICONTROL Segmente]**.

   Oder

   Wählen Sie in einem vorhandenen Bericht das Segmentsymbol aus ![](https://spectrum.adobe.com/static/icons/workflow_18/Smock_Segmentation_18_N.svg) Wählen Sie im linken Navigationsbereich die Option **[!UICONTROL Verwalten]**.

## Verfügbare Aktionen im Segment-Manager

Im Segment-Manager haben Sie folgende Möglichkeiten:

* [Filtern von Segmenten](/help/components/segmentation/segmentation-workflow/t-seg-filter.md)

* [Segmente als Favoriten markieren](/help/components/segmentation/segmentation-workflow/t-seg-favorite.md)

* [Segmente genehmigen](/help/components/segmentation/segmentation-workflow/seg-approve.md)

* [Segmente taggen](/help/components/segmentation/segmentation-workflow/seg-tag.md)

* [Segmente freigeben](/help/components/segmentation/segmentation-workflow/t-seg-share.md)

* Exportieren Sie ein Segment in eine CSV-Datei.

* [Segmente kopieren](/help/components/segmentation/segmentation-workflow/seg-copy.md)

* [Segmente löschen](/help/components/segmentation/segmentation-workflow/seg-delete.md)

## Spalten konfigurieren

Sie können die für jedes Segment im Segment-Manager angezeigten Informationen konfigurieren, indem Sie die angezeigten Spalten konfigurieren.

So konfigurieren Sie die sichtbaren Spalten im Segment-Manager:

1. Wählen Sie in Adobe Analytics die **[!UICONTROL Komponenten]** Registerkarte und wählen Sie **[!UICONTROL Segmente]**.

1. Wählen Sie im Segment-Manager die **Spalten anpassen** icon ![Symbol &quot;Spalten anpassen&quot;](assets/customize-columns-icon.png)und wählen Sie dann die Spalten aus, die im Segment-Manager angezeigt werden sollen.

   Die folgenden Spalten sind verfügbar:

   | Spaltentitel | Beschreibung |
   |---|---|
   | Titel und Beschreibung | Diese Werte werden im Segment Builder bereitgestellt. Um den Titel und die Beschreibung zu bearbeiten, wählen Sie den Titel-Link aus, um den Segment Builder zu öffnen. |
   | Favoriten | Zeigt neben jedem Segment Sternensymbole an, mit denen Sie Segmente als Favoriten markieren können. Weitere Informationen finden Sie unter [Segmente als Favoriten markieren](/help/components/segmentation/segmentation-workflow/t-seg-favorite.md). |
   | Report Suites | Diese Spalte zeigt an, in welcher Report Suite das Segment zuletzt gespeichert wurde. |
   | Inhaber | Zeigt an, wer Inhaber des Segments ist. Wenn Sie kein Administrator sind, können Sie nur Segmente sehen, deren Inhaber Sie sind, sowie Segmente, die für Sie freigegeben wurden. |
   | Tags (in der Spaltenauswahl nicht aktiviert, weshalb die Spalte nicht angezeigt wird) | Tags, die entweder durch Sie oder durch Personen, die ein Segment für Sie freigegeben haben, auf das Segment angewendet wurden. |
   | Freigegeben für | Zeigt Personen oder Gruppen (nur Administrator) oder „Alle“ (nur Administrator) an, für die Sie das Segment freigegeben haben. <p>Wenn ein Segment von Ihnen oder für Sie freigegeben wird, wird neben dem Segmentnamen ein Freigabesymbol angezeigt.</p> |
   | Änderungsdatum | Zeigt das Datum der letzten Änderung des Segments an. |
   | Verwendet in | Zeigt an, in wie vielen Komponenten das Segment derzeit verwendet wird. <p>Wenn das Segment beispielsweise in 40 Projekten und 2 Warnhinweisen verwendet wird, zeigt der Wert dieser Spalte als [!UICONTROL **42 Komponenten**].</p> <p>Wählen Sie den Wert in dieser Spalte aus, um die Aufschlüsselung der verwendeten Segmente anzuzeigen (z. B. [!UICONTROL **Projekte (40)**], [!UICONTROL **Warnhinweise (2)**]).</p><p>Segmente können in einem der folgenden Komponententypen verwendet werden:</p> <ul><li>Warnhinweise</li><li>Projekte</li><li>Geplante Projekte</li><li>Berechnete Metriken </li></ul><p>Diese Informationen können Ihnen dabei helfen festzustellen, ob eine Komponente für Benutzer in Ihrer Organisation nützlich ist, wo sie verwendet wird und ob sie gelöscht oder geändert werden muss.</p><p>Beachten Sie bei der Anzeige dieser Spalte Folgendes:</p><ul><li>Diese Informationen enthalten keine Verwendung von API, Report Builder oder Data Warehouse.</li><li>Die [!UICONTROL **Verwendet in**] -Spalte wird nicht standardmäßig angezeigt. [Spalten konfigurieren](#configure-columns) , um es anzuzeigen.</li><li>Wenn in dieser Spalte keine Daten für eine bestimmte Komponente vorhanden sind, aber eine [!UICONTROL **Zuletzt verwendet**] Datum, wurde die Komponente möglicherweise in einer Analyse verwendet, ohne gespeichert zu werden.</li><li>Diese Informationen sind nur für Systemadministratoren verfügbar.</li></ul><p>Sie können die [Datenwörterbuch](/help/analyze/analysis-workspace/components/data-dictionary/data-dictionary-overview.md) zusammen mit diesen Informationen, damit Sie die Verwendung von Komponenten in Ihrem Unternehmen verfolgen und besser verstehen können.</p> |
   | Zuletzt verwendet | Zeigt das Datum der letzten Verwendung des Segments in einem der folgenden Komponententypen an: <ul><li>Warnhinweise</li><li>Berechnete Metriken </li><li>Projekte</li><li>Geplante Projekte</li><li>Segmente </li></ul> <p>Diese Informationen können Ihnen dabei helfen festzustellen, ob eine Komponente für Benutzer in Ihrer Organisation nützlich ist, wo sie verwendet wird und ob sie gelöscht oder geändert werden muss.</p><p>Beachten Sie bei der Anzeige dieser Spalte Folgendes:</p><ul><li>Diese Informationen enthalten keine Verwendung von API, Report Builder oder Data Warehouse.</li><li>Bei einigen Komponenten enthält diese Spalte möglicherweise keine Daten, wenn die Komponente zuletzt vor September 2023 verwendet wurde.</li><li>Diese Informationen sind nur für Systemadministratoren verfügbar.</li></ul><p>Sie können die [Datenwörterbuch](/help/analyze/analysis-workspace/components/data-dictionary/data-dictionary-overview.md) zusammen mit diesen Informationen, damit Sie die Verwendung von Komponenten in Ihrem Unternehmen verfolgen und besser verstehen können. |

   {style="table-layout:auto"}

## Anleitungsvideo {#section_B3C5DA22DC5248DBA17C56E03DA2D4F2}

In diesem [Adobe Analytics-Video](https://experienceleague.adobe.com/docs/analytics-learn/tutorials/components/segmentation/segment-management-and-sharing.html?lang=de) erhalten Sie einen kurzen Überblick darüber, wie Sie Segment Manager einsetzen können.


