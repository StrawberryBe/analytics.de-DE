---
description: 'Komponenten in Analysis Workspace bestehen aus Dimensionen, Metriken, Segmenten und Datumsbereichen, die Sie per Drag-and-Drop in einem Projekt platzieren können. '
title: Komponentenübersicht
feature: Components
role: User, Admin
exl-id: e2c98c77-64ee-4349-956a-3ab092e36017
source-git-commit: 10ae8213b8745439ab5968853f655a1176b8c38a
workflow-type: ht
source-wordcount: '714'
ht-degree: 100%

---

# Komponentenübersicht

Komponenten in Analysis Workspace bestehen aus Dimensionen, Metriken, Segmenten und Datumsbereichen, die Sie per Drag-and-Drop in einem Projekt platzieren können.

Klicken Sie auf der linken Leiste auf das Symbol **[!UICONTROL Komponenten]**, um auf das Menü „Komponenten“ zuzugreifen. Sie können über die Symbole in der linken Leiste oder über [Hotkeys](/help/analyze/analysis-workspace/build-workspace-project/fa-shortcut-keys.md) zwischen [Bedienfeldern](https://experienceleague.adobe.com/docs/analytics/analyze/analysis-workspace/panels/panels.html?lang=de), [Visualisierungen](https://experienceleague.adobe.com/docs/analytics/analyze/analysis-workspace/visualizations/freeform-analysis-visualizations.html?lang=de) und Komponenten wechseln.

![](assets/component-overview.png)

Sie können auch die [Ansichtsdichteeinstellungen](https://experienceleague.adobe.com/docs/analytics/analyze/analysis-workspace/build-workspace-project/view-density.html?lang=de) für das Projekt anpassen, sodass in der linken Leiste mehr Werte gleichzeitig angezeigt werden können. Gehen Sie hierzu auf **[!UICONTROL Projekt > Projektinformationen und -einstellungen > Ansichtsdichte]**.

## Dimensionen {#dimensions}

[**Dimensionen**](https://experienceleague.adobe.com/docs/analytics/components/dimensions/overview.html?lang=de) sind Textattribute, die das Verhalten Ihrer Besucher beschreiben und in Ihrer Analyse angezeigt, aufgeschlüsselt und verglichen werden können. Sie befinden sich in der Leiste „Komponente“ auf der linken Seite (orangefarbener Abschnitt) und werden in der Regel als Tabellenzeilen angewendet.

Beispiele für Dimensionen sind [!UICONTROL Seitenname], [!UICONTROL Marketing-Kanäle], [!UICONTROL Geräteklasse] und [!UICONTROL Produkte]. Dimensionen werden von Adobe bereitgestellt und über Ihre benutzerdefinierte Implementierung erfasst (beispielsweise eVar, Props, Klassifizierungen).

Jede Dimension enthält auch **Dimensionselemente**. Dimensionselemente finden Sie in der Leiste „Komponente“ auf der linken Seite, indem Sie auf den rechten Pfeil neben dem jeweiligen Dimensionsnamen klicken (Elemente sind gelb).

Beispiele für Dimensionselemente sind [!UICONTROL Startseite] (innerhalb der Dimension [!UICONTROL Seite]), [!UICONTROL Paid Search] (innerhalb der Dimension [!UICONTROL Marketing-Kanal]) und [!UICONTROL Tablet] (innerhalb der Dimension [!UICONTROL Mobilgerätetyp]).

![](assets/dimensions.png)

## Metriken {#metrics}

[**Metriken**](https://experienceleague.adobe.com/docs/analytics/components/metrics/overview.html?lang=de) sind quantitative Messungen zum Verhalten von Besuchern. Sie befinden sich in der Leiste „Komponente“ auf der linken Seite (grüner Abschnitt) und werden normalerweise als Tabellenspalten angewendet.

Zu den Metriken zählen beispielsweise [!UICONTROL Seitenansichten], [!UICONTROL Besuche], [!UICONTROL Bestellungen], [!UICONTROL Durchschnittliche Besuchszeit] und [!UICONTROL Umsatz/Bestellung]. Metriken werden von Adobe bereitgestellt, über Ihre benutzerdefinierte Implementierung ([!UICONTROL Erfolgsereignisse]) erfasst oder mit dem [Generator für berechnete Metriken](https://experienceleague.adobe.com/docs/analytics/components/calculated-metrics/calcmetric-workflow/cm-build-metrics.html?lang=de) erstellt.

![](assets/metrics.png)

## Segmente {#segments}

[**Segmente**](https://experienceleague.adobe.com/docs/analytics/analyze/analysis-workspace/components/segments/t-freeform-project-segment.html?lang=de) sind Zielgruppenfilter, die auf Ihre Analyse angewendet werden. Sie befinden sich in der Leiste „Komponente“ auf der linken Seite (blauer Abschnitt) und werden normalerweise oben in einem Bedienfeld oder über den Metrikspalten in einer Tabelle angewendet.

Beispiele für Segmente sind [!UICONTROL Besucher über Smartphone und Tablet], [!UICONTROL Besuche aus E-Mails] und [!UICONTROL Authentifizierte Treffer]. Segmente werden durch Adobe bereitgestellt oder in der [Dropzone des Bedienfelds](https://experienceleague.adobe.com/docs/analytics/analyze/analysis-workspace/panels/panels.html?lang=de) oder mit dem [Segment Builder](https://experienceleague.adobe.com/docs/analytics/components/segmentation/segmentation-workflow/seg-build.html?lang=de) erstellt.

![](assets/segments.png)

## Datumsbereiche {#date-ranges}

[**Datumsbereiche**](https://experienceleague.adobe.com/docs/analytics/analyze/analysis-workspace/components/calendar-date-ranges/calendar.html?lang=de) sind der Zeitraum, für den Sie Ihre Analyse durchführen. Sie befinden sich in der Leiste „Komponente“ auf der linken Seite (violetter Abschnitt) und werden normalerweise im Kalender der einzelnen Bedienfelder angewendet.

Beispiele für Datumsbereiche sind Juli 2019, [!UICONTROL Letzte 4 Wochen] und [!UICONTROL Diesen Monat]. Datumsbereiche werden von Adobe bereitgestellt, im [Kalender des Bedienfelds](https://experienceleague.adobe.com/docs/analytics/analyze/analysis-workspace/panels/panels.html?lang=de) angewendet oder mit der [Datumsbereicherstellung](https://experienceleague.adobe.com/docs/analytics/analyze/analysis-workspace/components/calendar-date-ranges/custom-date-ranges.html?lang=de) erstellt.

![](assets/date-ranges.png)

## Komponentenaktionen {#actions}

Sie können Komponenten (einzeln oder durch Auswahl mehrerer Komponenten) direkt in der linken Leiste verwalten. Klicken Sie mit der rechten Maustaste auf eine Komponente oder klicken Sie oben in der Komponentenliste auf den Punkt „Aktion“.

![](assets/component-actions.png)

| Komponentenaktion | Beschreibung |
|--- |--- |
| Tag | Organisieren oder verwalten Sie Komponenten, indem Sie Tags darauf anwenden. Sie können dann in der linken Leiste nach Tags suchen, indem Sie auf den Filter klicken oder „#“ eingeben. Tags fungieren auch als Filter in den Komponenten-Managern. |
| Favorit | Fügen Sie die Komponente Ihrer Favoritenliste hinzu. Genauso wie nach Tags können Sie in der linken Leiste auch nach Favoriten suchen und diese in den Komponenten-Managern als Filter verwenden. |
| Genehmigen | Markieren Sie Komponenten als „Genehmigt“, um Ihren Benutzern zu signalisieren, dass die Komponente vom Unternehmen genehmigt ist. Genauso wie nach Tags können Sie in der linken Leiste nach dem Status „Genehmigt“ suchen und diesen in den Komponenten-Managern als Filter verwenden. |
| Freigeben | Freigeben von Komponenten für Benutzer in Ihrer Organisation. Diese Option steht nur für benutzerdefinierte Komponenten zur Verfügung, beispielsweise für Segmente oder berechnete Metriken. |
| Löschen | Löschen Sie Komponenten, die Sie nicht mehr benötigen. Diese Option steht nur für benutzerdefinierte Komponenten zur Verfügung, beispielsweise für Segmente oder berechnete Metriken. |

Benutzerdefinierte Komponenten können auch über ihre jeweiligen Komponenten-Manager verwaltet werden. Ein Beispiel hierfür ist der [Segment-Manager](/help/components/segmentation/segmentation-workflow/seg-manage.md).
