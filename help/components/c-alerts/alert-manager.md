---
description: Warnhinweise verwalten.
title: Warnhinweis-Manager - Übersicht
feature: Alerts
exl-id: 3408c79f-3d85-44b9-8fca-ce956853dfa4
source-git-commit: 637f498c8abee0f3c83780bccd0447f2e3a804e3
workflow-type: tm+mt
source-wordcount: '462'
ht-degree: 33%

---

# Warnhinweis-Manager

Der Warnhinweis-Manager ähnelt sehr dem [Segment-Manager](https://experienceleague.adobe.com/docs/analytics/components/segmentation/segmentation-workflow/seg-manage.html?lang=de) und [Manager für berechnete Metriken](https://experienceleague.adobe.com/docs/analytics/components/calculated-metrics/calcmetric-workflow/cm-manager.html?lang=de).

![](assets/alert-manager.png)

## Zugriff auf den Warnhinweis-Manager

1. Wählen Sie in Adobe Analytics [!UICONTROL **Komponenten**] > [!UICONTROL **Warnhinweise**].

## Verfügbare Aktionen im Warnhinweis-Manager

Im Warnhinweis-Manager haben Sie folgende Möglichkeiten:

* Die Warnhinweiserstellung per Klick auf **[!UICONTROL + Hinzufügen]** öffnen.
* Warnhinweise mit einem Tag versehen: Dadurch können Sie sie zur einfachen Anwendung organisieren.
* Warnhinweise löschen.
* Warnhinweise umbenennen.
* Warnhinweise genehmigen.
* Warnhinweise kopieren.
* Warnhinweise aktivieren/deaktivieren.
* Ein Ablaufdatum für den Warnhinweis **verlängern**: Wenn ein oder mehrere Warnhinweise ausgewählt sind, können diese durch Klicken auf **[!UICONTROL Verlängern]** verlängert werden. Dadurch werden die Ablaufdaten ab dem Tag, an dem auf **[!UICONTROL Verlängern]** geklickt wurde, unabhängig vom ursprünglichen Ablaufdatum um 1 Jahr verlängert.
* Einen Warnhinweis als .CSV-Datei exportieren.
* Warnhinweise durch Doppelklicken auf den Titel bearbeiten.
* Nach Warnhinweisen suchen.
* Warnhinweise zu anderen Report Suites hinzufügen.
* Den Eigentümer eines Warnhinweises angeben oder ändern.
* Andere Filter hinzufügen.
* Ein **Ablaufdatum** für den Warnhinweis definieren.

## Spalten konfigurieren

Sie können die für jeden Warnhinweis im Warnhinweis-Manager angezeigten Informationen konfigurieren, indem Sie die angezeigten Spalten konfigurieren.

So konfigurieren Sie die sichtbaren Spalten im Warnhinweis-Manager:

1. Wählen Sie in Adobe Analytics die **[!UICONTROL Komponenten]** Registerkarte und wählen Sie **[!UICONTROL Warnhinweise]**.

1. Wählen Sie im Warnhinweis-Manager die **Spalten anpassen** icon ![Symbol &quot;Spalten anpassen&quot;](assets/customize-columns-icon.png)und wählen Sie dann die Spalten aus, die im Warnhinweis-Manager angezeigt werden sollen.

   Die folgenden Spalten sind verfügbar:

   | Spaltentitel | Beschreibung |
   |---|---|
   | Favoriten | Zeigt neben jedem Warnhinweis Sternensymbole an, mit denen Sie Warnhinweise als Favoriten markieren können. <!-- For more information, see [Mark calculated metrics as favorites](/help/components/c-calcmetrics/c-workflow/cm-workflow/cm-favorite.md). --> |
   | Titel und Beschreibung | Diese Werte werden in der Warnhinweiserstellung bereitgestellt. Um den Titel und die Beschreibung zu bearbeiten, wählen Sie den Titel-Link aus, um die Warnhinweiserstellung zu öffnen. |
   | Report Suite | Gibt an, in welcher Report Suite die Warnung zuletzt gespeichert wurde. |
   | Verantwortlicher | Gibt an, wem der Warnhinweis gehört. Als Benutzer ohne Administratorrechte können Sie nur Warnhinweise sehen, deren Inhaber Sie sind, sowie solche, die für Sie freigegeben wurden. |
   | Tags | Zeigt Tags an, die entweder von Ihnen oder von Personen, die den Warnhinweis für Sie freigegeben haben, auf den Warnhinweis angewendet wurden. |
   | Freigegeben für | Listet Personen oder Gruppen (nur Administrator) oder Alle (nur Administrator) auf, für die Sie die Warnung freigegeben haben. |
   | Änderungsdatum | Gibt das Datum der letzten Änderung des Warnhinweises an. |
   | Zuletzt verwendet | **Hinweis:** Diese Funktion befindet sich in der eingeschränkten Testphase der Veröffentlichung und ist möglicherweise noch nicht in Ihrer Umgebung verfügbar. Diese Anmerkung wird entfernt, wenn die Funktion allgemein verfügbar ist. Informationen zum Customer Journey Analytics-Veröffentlichungsprozess finden Sie unter [Customer Journey Analytics-Funktionsveröffentlichungen](/help/release-notes/releases.md).<p>Zeigt das Datum der letzten Verwendung der Warnung an.</p> <p>Diese Informationen können Ihnen dabei helfen festzustellen, ob ein Warnhinweis für Benutzer in Ihrer Organisation nützlich ist oder ob er gelöscht werden soll.</p><p>Diese Informationen enthalten keine Verwendung von API, Report Builder oder Data Warehouse.</p> |

   {style="table-layout:auto"}
