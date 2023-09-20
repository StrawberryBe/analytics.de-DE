---
description: Die Seite "Berechnete Metriken"bietet viele Möglichkeiten zum Kuratieren von Metriken, z. B. Freigeben, Filtern, Taggen, Genehmigen, Kopieren, Löschen und Kennzeichnen als Favoriten.
title: Manager für berechnete Metriken
feature: Calculated Metrics
exl-id: 32430e77-2450-4672-9c21-255e76802a4c
source-git-commit: 637f498c8abee0f3c83780bccd0447f2e3a804e3
workflow-type: tm+mt
source-wordcount: '659'
ht-degree: 12%

---

# Manager für berechnete Metriken

Die Seite &quot;Berechnete Metriken&quot;bietet viele Möglichkeiten zum Kuratieren von Metriken, z. B. Freigeben, Filtern, Taggen, Genehmigen, Kopieren, Löschen und Kennzeichnen als Favoriten.

Auf der Seite Berechnete Metriken werden alle Segmente angezeigt, deren Inhaber Sie sind und die für Sie freigegeben wurden. Benutzer auf Administratorebene sehen alle benutzerdefinierten Metriken der Organisation.

<!-- add screenshot -->

## Zugriff auf den Manager für berechnete Metriken

1. Wählen Sie in Adobe Analytics [!UICONTROL **Komponenten**] > [!UICONTROL **Berechnete Metriken**].

## Verfügbare Aktionen im Manager für berechnete Metriken

Im Manager für berechnete Metriken haben Sie folgende Möglichkeiten:

* [Berechnete Metriken filtern](/help/components/c-calcmetrics/c-workflow/cm-workflow/cm-filter.md)

* [Berechnete Metriken als Favoriten markieren](/help/components/c-calcmetrics/c-workflow/cm-workflow/cm-favorite.md)

* [Berechnete Metriken genehmigen](/help/components/c-calcmetrics/c-workflow/cm-workflow/cm-approving.md)

* [Berechnete Metriken taggen](/help/components/c-calcmetrics/c-workflow/cm-workflow/cm-tagging.md)

* [Berechnete Metriken freigeben](/help/components/c-calcmetrics/c-workflow/cm-workflow/cm-sharing.md)

* Exportieren Sie eine berechnete Metrik in eine CSV-Datei.

* [Berechnete Metriken kopieren](/help/components/c-calcmetrics/c-workflow/cm-workflow/cm-copy.md)

* Berechnete Metriken löschen

## Spalten konfigurieren

Sie können die für jede berechnete Metrik angezeigten Informationen im Manager für berechnete Metriken konfigurieren, indem Sie die angezeigten Spalten konfigurieren.

So konfigurieren Sie die sichtbaren Spalten im Manager für berechnete Metriken:

1. Wählen Sie in Adobe Analytics die **[!UICONTROL Komponenten]** Registerkarte und wählen Sie **[!UICONTROL Berechnete Metriken]**.

1. Wählen Sie im Manager für berechnete Metriken die **Spalten anpassen** icon ![Symbol &quot;Spalten anpassen&quot;](assets/customize-columns-icon.png)und wählen Sie dann die Spalten aus, die im Manager für berechnete Metriken angezeigt werden sollen.

   Die folgenden Spalten sind verfügbar:

   | Spaltentitel | Beschreibung |
   |---|---|
   | Favoriten | Zeigt neben jeder berechneten Metrik Sternensymbole an, mit denen Sie berechnete Metriken als Favoriten markieren können. Weitere Informationen finden Sie unter [Berechnete Metriken als Favoriten markieren](/help/components/c-calcmetrics/c-workflow/cm-workflow/cm-favorite.md). |
   | Titel und Beschreibung | Diese Werte werden im Generator für berechnete Metriken bereitgestellt. Um den Titel und die Beschreibung zu bearbeiten, wählen Sie den Titel-Link aus, um den Generator für berechnete Metriken zu öffnen. |
   | Report Suite | Gibt an, in welcher Report Suite die Metrik zuletzt gespeichert wurde. |
   | Inhaber | Gibt den Inhaber der benutzerdefinierten Metrik an. Als Benutzer ohne Administratorrechte können Sie nur Metriken sehen, deren Inhaber Sie sind, sowie Metriken, die für Sie freigegeben wurden. |
   | Tags | Zeigt Tags an, die entweder von Ihnen oder von Personen, die die berechnete Metrik für Sie freigegeben haben, auf die Metrik angewendet wurden. |
   | Freigegeben für | Listet Personen oder Gruppen (nur Administrator) oder Alle (nur Administrator) auf, für die Sie die berechnete Metrik freigegeben haben. <p>Wenn eine berechnete Metrik freigegeben wird, wird neben dem Namen der berechneten Metrik ein Freigabesymbol angezeigt.</p> |
   | Änderungsdatum | Gibt das Datum der letzten Änderung der benutzerdefinierten Metrik an. |
   | Verwendet in | **Hinweis:** Diese Funktion befindet sich in der eingeschränkten Testphase der Veröffentlichung und ist möglicherweise noch nicht in Ihrer Umgebung verfügbar. Diese Anmerkung wird entfernt, wenn die Funktion allgemein verfügbar ist. Informationen zum Customer Journey Analytics-Veröffentlichungsprozess finden Sie unter [Customer Journey Analytics-Funktionsveröffentlichungen](/help/release-notes/releases.md).<p>Zeigt an, in welchem der folgenden Komponententypen die berechnete Metrik derzeit verwendet wird:</p> <ul><li>Warnhinweise</li><li>Berechnete Metriken </li><li>Projekte</li><li>Geplante Projekte</li></ul> Wenn die Komponenten beispielsweise in 40 Projekten und in 2 Warnhinweisen verwendet werden, zeigt diese Spalte [!UICONTROL **Warnhinweise (2), Projekte (40)**]. <p>Anhand dieser Informationen können Sie feststellen, ob eine Komponente für Benutzer in Ihrer Organisation nützlich ist oder ob sie gelöscht werden soll.</p><p>Diese Informationen enthalten keine Verwendung von API, Report Builder oder Data Warehouse.</p><p>Sie können die [Datenwörterbuch](/help/analyze/analysis-workspace/components/data-dictionary/data-dictionary-overview.md) zusammen mit diesen Informationen, damit Sie die Verwendung von Komponenten in Ihrem Unternehmen verfolgen und besser verstehen können. |
   | Zuletzt verwendet | **Hinweis:** Diese Funktion befindet sich in der eingeschränkten Testphase der Veröffentlichung und ist möglicherweise noch nicht in Ihrer Umgebung verfügbar. Diese Anmerkung wird entfernt, wenn die Funktion allgemein verfügbar ist. Informationen zum Customer Journey Analytics-Veröffentlichungsprozess finden Sie unter [Customer Journey Analytics-Funktionsveröffentlichungen](/help/release-notes/releases.md).<p>Zeigt das Datum an, an dem die berechnete Metrik zuletzt in einem der folgenden Komponententypen verwendet wurde:</p> <ul><li>Warnhinweise</li><li>Berechnete Metriken </li><li>Projekte</li><li>Geplante Projekte</li></ul> <p>Anhand dieser Informationen können Sie feststellen, ob eine Komponente für Benutzer in Ihrer Organisation nützlich ist oder ob sie gelöscht werden soll.</p><p>Diese Informationen enthalten keine Verwendung von API, Report Builder oder Data Warehouse.</p><p>Sie können die [Datenwörterbuch](/help/analyze/analysis-workspace/components/data-dictionary/data-dictionary-overview.md) zusammen mit diesen Informationen, damit Sie die Verwendung von Komponenten in Ihrem Unternehmen verfolgen und besser verstehen können. |

   {style="table-layout:auto"}
