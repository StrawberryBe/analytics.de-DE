---
description: Lernen Sie die Grundlagen zum Erstellen eines Projekts in Analysis Workspace kennen
title: Projekte erstellen
feature: Workspace Basics
role: User, Admin
exl-id: 6130b1d8-078c-46d8-9fce-eb39739a9570
source-git-commit: fabe043264e4567d54dc497897fff0aaad77eaaf
workflow-type: tm+mt
source-wordcount: '705'
ht-degree: 14%

---

# Erstellen von Projekten in Analysis Workspace

[Projekte](/help/analyze/analysis-workspace/build-workspace-project/freeform-overview.md) in Analysis Workspace können Sie geschäftskritische Analysen anzeigen, die für Interessengruppen innerhalb oder außerhalb Ihres Unternehmens freigegeben werden können.

Allgemeine Informationen zu den ersten Schritten mit Analysis Workspace finden Sie unter [Übersicht über Analysis Workspace](/help/analyze/analysis-workspace/home.md).

In den folgenden Abschnitten wird beschrieben, wie Sie ein Projekt erstellen und die wichtigsten Bausteine für ein Analysis Workspace-Projekt hinzufügen: Bedienfelder, Visualisierungen und Komponenten.

## Erstellen eines Projekts aus einem leeren Projekt oder Bericht

1. Wählen Sie in Adobe Analytics [!UICONTROL **Arbeitsbereich**].

1. Wählen Sie aus, ob ein leeres Projekt oder ein Projekt aus einem Bericht erstellt werden soll:

   +++Leeres Projekt erstellen

   1. Im [!UICONTROL **Arbeitsbereich**] auswählen, wählen Sie die [!UICONTROL **Projekte**] auf der linken Seite der Seite ein und wählen Sie [!UICONTROL **Projekt erstellen**].

   1. Legen Sie fest, ob ein leeres Projekt oder eine leere mobile Scorecard erstellt werden soll.

      * **Leeres Projekt** , wenn Sie Ihre Analyse über den Browser freigeben möchten
      * [**Leere mobile Scorecard**](/help/analyze/mobile-app/curator.md) , wenn Sie Ihre Analyse über die mobile Adobe Analytics-Dashboards-App freigeben möchten.

   1. Wählen Sie [!UICONTROL **Erstellen**].

+++

   +++Projekt aus einem Bericht erstellen

   1. Im [!UICONTROL **Arbeitsbereich**] auswählen, wählen Sie die [!UICONTROL **Berichte**] auf der linken Seite der Seite.

   1. Suchen Sie nach dem Bericht, den Sie verwenden möchten, oder navigieren Sie zu ihm und wählen Sie ihn aus, wenn er angezeigt wird.

      Eine Reihe von Standardberichten ist standardmäßig verfügbar. Darüber hinaus hat Ihr Unternehmen möglicherweise benutzerdefinierte Berichte erstellt, aus denen Sie auswählen können.

   1. Auswählen [!UICONTROL **Projekt**] > [!UICONTROL **Speichern**] , um den Bericht als neues Projekt zu speichern.

      Weitere Informationen zu Berichten finden Sie unter &quot;Navigieren in der Registerkarte Berichte&quot;in [Adobe Analytics-Landingpage](/help/analyze/landing.md).

+++

1. Als Nächstes müssen Sie Ihrem Projekt Bedienfelder, Visualisierungen und Komponenten hinzufügen. Fügen Sie zunächst Bedienfelder zu Ihrem Projekt in Analysis Workspace hinzu, wie unter [Hinzufügen von Bedienfeldern zum Projekt](#add-panels-to-the-project). Sie können dann allen Bedienfeldern Visualisierungen hinzufügen. Schließlich können Sie allen Bedienfeldern oder Visualisierungen Komponenten hinzufügen.

## Hinzufügen von Bedienfeldern zum Projekt {#panels}

[Bedienfelder](https://experienceleague.adobe.com/docs/analytics/analyze/analysis-workspace/panels/panels.html?lang=de) sind die Grundlage für jedes Projekt in Analysis Workspace. Bedienfelder dienen zum Organisieren der Inhalte (Visualisierungen und Komponenten) eines Projekts.

Viele der in Analysis Workspace bereitgestellten Bedienfelder generieren einen vollständigen Satz von Analysen auf der Grundlage einiger Benutzereingaben.

So fügen Sie einen Bereich hinzu:

1. Wählen Sie die [!UICONTROL **Bedienfelder**] in der linken Leiste.

   ![](assets/build-panels.png)

1. Suchen Sie nach dem Bereich, den Sie hinzufügen möchten. Wenn es in der linken Leiste angezeigt wird, ziehen Sie es in Ihr Projekt.

1. Fügen Sie Ihrem Bedienfeld Visualisierungen hinzu, wie unter [Hinzufügen von Visualisierungen zum Projekt](#add-visualizations-to-the-project).

   Alternativ können Sie Komponenten direkt zu einem Bedienfeld hinzufügen, wie unter [Komponenten zum Projekt hinzufügen](#add-components-to-the-project).

## Hinzufügen von Visualisierungen zum Projekt

[Visualisierung](https://experienceleague.adobe.com/docs/analytics/analyze/analysis-workspace/visualizations/freeform-analysis-visualizations.html?lang=de) (z. B. eine Freiformtabelle, ein Balkendiagramm oder ein Liniendiagramm) verwendet werden, um Daten visuell darzustellen.

>[!TIP]
>
>Freiformtabellen sind der am häufigsten verwendete Visualisierungstyp und bilden die Grundlage für die interaktive Datenanalyse. Weitere Informationen zum Arbeiten mit Freiformtabellen in Analysis Workspace finden Sie unter [Freiformtabelle](/help/analyze/analysis-workspace/visualizations/freeform-table/freeform-table.md).

So fügen Sie eine Visualisierung hinzu:

1. Wählen Sie die **[!UICONTROL Visualisierung]** in der linken Leiste.

   ![](assets/build-visualizations.png)

1. Suchen Sie nach der Visualisierung, die Sie hinzufügen möchten. Wenn es in der linken Leiste angezeigt wird, ziehen Sie es in ein Bedienfeld innerhalb Ihres Projekts.

1. Fügen Sie der Visualisierung Komponenten hinzu, wie unter [Komponenten zum Projekt hinzufügen](#add-components-to-the-project).

## Komponenten zum Projekt hinzufügen

[Komponenten](/help/analyze/analysis-workspace/components/analysis-workspace-components.md) die tatsächlichen Daten eines Projekts erstellen. Sie können Komponenten zu Visualisierungen oder Bedienfeldern hinzufügen.

>[!TIP]
>
>Informationen zu den einzelnen Komponenten erhalten Sie, wenn Sie in der linken Leiste auf das Infosymbol neben dem Namen einer Komponente klicken oder in der [Komponentenleitfaden für Analytics](/help/components/home.md).

So fügen Sie eine Komponente hinzu:

1. Wählen Sie die **[!UICONTROL Komponenten]** in der linken Leiste.

   ![](assets/build-components.png)

1. Suchen Sie nach der Komponente, die Sie hinzufügen möchten. Wenn es in der linken Leiste angezeigt wird, ziehen Sie es in ein Bedienfeld oder eine Visualisierung innerhalb Ihres Projekts.

1. (Optional) Geben Sie das Projekt wie unter [Projekt speichern und freigeben](#save-and-share-the-project).

## Projekt speichern und freigeben

Bei der Erstellung einer Analyse in Analysis Workspace wird Ihre Arbeit [automatisch gespeichert](/help/analyze/analysis-workspace/build-workspace-project/save-projects.md).

Wenn Sie das Projekt fertiggestellt haben und es praktische Einblicke liefert, kann das Projekt auch von anderen genutzt werden. Sie können das Projekt für Benutzende sowie Gruppen in Ihrer Organisation oder auch für Personen außerhalb Ihrer Organisation freigeben. Informationen zum Freigeben eines Projekts finden Sie unter [Freigeben von Projekten](/help/analyze/analysis-workspace/curate-share/share-projects.md).
