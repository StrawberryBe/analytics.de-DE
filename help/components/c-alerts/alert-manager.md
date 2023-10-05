---
description: Warnhinweise verwalten.
title: Warnhinweis-Manager - Übersicht
feature: Alerts
exl-id: 3408c79f-3d85-44b9-8fca-ce956853dfa4
source-git-commit: 9a6c2e7c2f83882f6df630f975b0c44e75a2ed7a
workflow-type: tm+mt
source-wordcount: '448'
ht-degree: 38%

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
   | Zuletzt verwendet | Zeigt das Datum der letzten Verwendung der Warnung an. <p>Mithilfe dieser Informationen können Sie feststellen, ob eine Komponente für Benutzerinnen und Benutzer in Ihrer Organisation nützlich ist, wo sie verwendet wird und ob sie gelöscht oder geändert werden muss.</p><p>Beachten Sie bei der Anzeige dieser Spalte Folgendes:</p><ul><li>Diese Informationen enthalten keine Verwendung von API, Report Builder oder Data Warehouse.</li><li>Bei einigen Komponenten enthält diese Spalte möglicherweise keine Daten, wenn die Komponente zuletzt vor September 2023 verwendet wurde.</li></ul> |

   {style="table-layout:auto"}
