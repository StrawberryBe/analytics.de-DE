---
description: Der Segment-Manager bietet verschiedene Möglichkeiten zum Kuratieren von Segmenten wie das Freigeben, Filtern, Taggen, Genehmigen, Kopieren, Löschen und Kennzeichnen als Favoriten.
title: Segmente verwalten (Segment-Manager)
feature: Segmentation
exl-id: be182a55-23cb-415f-a7d0-3c1efeead1a1
source-git-commit: 637f498c8abee0f3c83780bccd0447f2e3a804e3
workflow-type: tm+mt
source-wordcount: '710'
ht-degree: 39%

---

# Segment-Manager

Der Segment-Manager bietet verschiedene Möglichkeiten zum Kuratieren von Segmenten wie das Freigeben, Filtern, Taggen, Genehmigen, Kopieren, Löschen und Kennzeichnen als Favoriten.

Der Segment-Manager in Analytics zeigt Ihnen alle Segmente, die sich in Ihrem Besitz befinden und für Sie freigegeben wurden. Benutzer auf Administratorebene sehen alle Segmente der Organisation. Dieser Überblick präsentiert die Benutzeroberfläche und die Funktionen des Segment-Managers.

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
   | Verwendet in | **Hinweis:** Diese Funktion befindet sich in der eingeschränkten Testphase der Veröffentlichung und ist möglicherweise noch nicht in Ihrer Umgebung verfügbar. Diese Anmerkung wird entfernt, wenn die Funktion allgemein verfügbar ist. Informationen zum Customer Journey Analytics-Veröffentlichungsprozess finden Sie unter [Customer Journey Analytics-Funktionsveröffentlichungen](/help/release-notes/releases.md).<p>Zeigt an, in welchem der folgenden Komponententypen das Segment derzeit verwendet wird:</p> <ul><li>Warnhinweise</li><li>Berechnete Metriken </li><li>Projekte</li><li>Geplante Projekte</li><li>Segmente </li></ul> Wenn das Segment beispielsweise in 40 Projekten und in 2 Warnhinweisen verwendet wird, zeigt diese Spalte [!UICONTROL **Warnhinweise (2), Projekte (40)**]. <p>Anhand dieser Informationen können Sie feststellen, ob ein Segment für Benutzer in Ihrer Organisation nützlich ist oder ob es gelöscht werden soll.</p><p>Diese Informationen enthalten keine Verwendung von API, Report Builder oder Data Warehouse.</p><p>Sie können die [Datenwörterbuch](/help/analyze/analysis-workspace/components/data-dictionary/data-dictionary-overview.md) zusammen mit diesen Informationen, damit Sie die Verwendung von Komponenten in Ihrem Unternehmen verfolgen und besser verstehen können. |
   | Zuletzt verwendet | **Hinweis:** Diese Funktion befindet sich in der eingeschränkten Testphase der Veröffentlichung und ist möglicherweise noch nicht in Ihrer Umgebung verfügbar. Diese Anmerkung wird entfernt, wenn die Funktion allgemein verfügbar ist. Informationen zum Customer Journey Analytics-Veröffentlichungsprozess finden Sie unter [Customer Journey Analytics-Funktionsveröffentlichungen](/help/release-notes/releases.md).<p>Zeigt das Datum der letzten Verwendung des Segments in einem der folgenden Komponententypen an:</p> <ul><li>Warnhinweise</li><li>Berechnete Metriken </li><li>Projekte</li><li>Geplante Projekte</li><li>Segmente </li></ul> <p>Anhand dieser Informationen können Sie feststellen, ob eine Komponente für Benutzer in Ihrer Organisation nützlich ist oder ob sie gelöscht werden soll.</p><p>Diese Informationen enthalten keine Verwendung von API, Report Builder oder Data Warehouse.</p><p>Sie können die [Datenwörterbuch](/help/analyze/analysis-workspace/components/data-dictionary/data-dictionary-overview.md) zusammen mit diesen Informationen, damit Sie die Verwendung von Komponenten in Ihrem Unternehmen verfolgen und besser verstehen können. |

   {style="table-layout:auto"}

## Anleitungsvideo {#section_B3C5DA22DC5248DBA17C56E03DA2D4F2}

In diesem [Adobe Analytics-Video](https://experienceleague.adobe.com/docs/analytics-learn/tutorials/components/segmentation/segment-management-and-sharing.html?lang=de) erhalten Sie einen kurzen Überblick darüber, wie Sie Segment Manager einsetzen können.


