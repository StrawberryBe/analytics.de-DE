---
description: Komponenten in Analysis Workspace bestehen aus Dimensionen, Metriken, Segmenten und Datumsbereichen, die Sie per Drag-and-Drop in einem Projekt platzieren können.
title: Komponentenübersicht
feature: Components
role: User, Admin
exl-id: e2c98c77-64ee-4349-956a-3ab092e36017
source-git-commit: 6247f44aca1e6aba6cf02ed34a0e26ef5e182021
workflow-type: tm+mt
source-wordcount: '1120'
ht-degree: 71%

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

Sie können die Datumsbereichskomponenten relativ zum Bedienfeldkalender festlegen. Weitere Informationen finden Sie unter [Über relative Bereichsdatumsbereiche](/help/analyze/analysis-workspace/components/calendar-date-ranges/calendar.md#relative-panel-dates).

Beispiele für Datumsbereiche sind Juli 2019, [!UICONTROL Letzte 4 Wochen] und [!UICONTROL Diesen Monat]. Datumsbereiche werden von Adobe bereitgestellt, im [Kalender des Bedienfelds](https://experienceleague.adobe.com/docs/analytics/analyze/analysis-workspace/panels/panels.html?lang=de) angewendet oder mit der [Datumsbereicherstellung](https://experienceleague.adobe.com/docs/analytics/analyze/analysis-workspace/components/calendar-date-ranges/custom-date-ranges.html?lang=de) erstellt.

![](assets/date-ranges.png)


## Komponenten verwalten {#actions}

Sie können Komponenten direkt in der linken Leiste verwalten.

1. Klicken Sie mit der rechten Maustaste auf eine Komponente.

   Oder

   Wählen Sie eine Komponente aus und wählen Sie dann die **Aktion** (3-Punkt) oben in der Komponentenliste.

   >[!TIP]
   >
   >   Sie können mehrere Komponenten auswählen, indem Sie die Umschalttaste gedrückt halten oder die Befehlstaste (Mac) oder die Strg-Taste (Windows) gedrückt halten.


   ![](assets/component-actions.png)

   | Komponentenaktion | Beschreibung |
   |--- |--- |
   | [!UICONTROL **Tag**] | Organisieren oder verwalten Sie Komponenten, indem Sie Tags darauf anwenden. Sie können dann in der linken Leiste nach Tags suchen, indem Sie auf den Filter klicken oder „#“ eingeben. Tags fungieren auch als Filter in den Komponenten-Managern. |
   | [!UICONTROL **Favorit**] | Fügen Sie die Komponente Ihrer Favoritenliste hinzu. Genauso wie nach Tags können Sie in der linken Leiste auch nach Favoriten suchen und diese in den Komponenten-Managern als Filter verwenden. |
   | [!UICONTROL **Genehmigen**] | Markieren Sie Komponenten als „Genehmigt“, um Ihren Benutzern zu signalisieren, dass die Komponente vom Unternehmen genehmigt ist. Genauso wie nach Tags können Sie in der linken Leiste nach dem Status „Genehmigt“ suchen und diesen in den Komponenten-Managern als Filter verwenden. |
   | [!UICONTROL **Freigeben**] | Freigeben von Komponenten für Benutzer in Ihrer Organisation. Diese Option steht nur für benutzerdefinierte Komponenten zur Verfügung, beispielsweise für Segmente oder berechnete Metriken. |
   | [!UICONTROL **Löschen**] | Löschen Sie Komponenten, die Sie nicht mehr benötigen. Diese Option steht nur für benutzerdefinierte Komponenten zur Verfügung, beispielsweise für Segmente oder berechnete Metriken. |

Benutzerdefinierte Komponenten können auch über ihre jeweiligen Komponenten-Manager verwaltet werden. Ein Beispiel hierfür ist der [Segment-Manager](/help/components/segmentation/segmentation-workflow/seg-manage.md).

## Suchen, Filtern und Sortieren der Komponentenliste

Sie können die Komponentenliste in der linken Leiste von Analysis Workspace suchen, filtern und sortieren, um eine bestimmte Komponente schnell zu finden.

### Durchsuchen der Komponentenliste

1. Wählen Sie die **Komponenten** icon ![Symbol &quot;Komponenten&quot;](assets/components-icon.png) in der linken Leiste.

1. Geben Sie im Suchfeld den Namen der Komponente ein, die Sie in Ihrem Projekt verwenden möchten.

   Der Komponententyp kann sowohl durch Farbe als auch durch Symbol identifiziert werden. **Dimensionen** ![Symbol &quot;Dimension&quot;](assets/dimension-icon.png) orange sind, **Segmente** ![Segmentsymbol](assets/segment-icon.png) blau sind, **Datumsbereiche** ![Symbol für Datumsbereich](assets/date-range-icon.png) violett sind und **Metriken** ![Metriksymbol](assets/default-metric-icon.png) sind grün. Das Symbol Adobe ![Symbol &quot;Adobe&quot;](assets/default-calc-metric-icon.png) gibt entweder eine Vorlage für berechnete Metriken oder eine Segmentvorlage an und das Symbol für den Rechner ![Symbol &quot;Rechner&quot;](assets/calculated-metric-icon-created.png) eine berechnete Metrik angezeigt, die von einem Analytics-Administrator in Ihrer Organisation erstellt wurde.

1. Wählen Sie die Komponente aus, wenn sie in der Dropdown-Liste angezeigt wird.

### Filtern der Komponentenliste

1. Wählen Sie die **Komponenten** icon ![Symbol &quot;Komponenten&quot;](assets/components-icon.png) in der linken Leiste.

1. Wählen Sie die **Filter** icon ![Symbol &quot;Datenwörterbuchfilter&quot;](assets/components-filter-icon.png).

   Oder

   Geben Sie das Rautenzeichen (#) in das Suchfeld ein.

1. Wählen Sie eine der folgenden Filteroptionen aus, um die Liste der Komponenten zu filtern:

   | Option | Funktion |
   |---------|----------|
   | [!UICONTROL **Genehmigt**] | Nur Komponenten anzeigen, die von Admins als genehmigt markiert wurden. |
   | [!UICONTROL **Favoriten**] | Nur Komponenten anzeigen, die sich in Ihrer Favoritenliste befinden. Informationen zum Hinzufügen von Komponenten zur Favoritenliste finden Sie in der [Komponentenübersicht](/help/analyze/analysis-workspace/components/analysis-workspace-components.md). |
   | [!UICONTROL **Dimensionen**] | Nur Komponenten anzeigen, die Dimensionen sind. |
   | [!UICONTROL **Metriken**] | Nur Komponenten anzeigen, die Metriken sind. |
   | [!UICONTROL **Segmente**] | Nur Komponenten anzeigen, die Segmente sind. <!--this is Filters in CJA--> |
   | [!UICONTROL **Datumsbereiche**] | Zeigt nur Komponenten an, die Datumsbereiche sind. |
   | [!UICONTROL **Alle anzeigen**] | Alle Komponenten anzeigen. Diese Option steht nur Admins zur Verfügung. |
   | [!UICONTROL **Nicht genehmigt**] | Nur Komponenten anzeigen, die von Admins noch nicht als genehmigt markiert wurden. Für Admins beim Identifizieren von Komponenten hilfreich, die überprüft und genehmigt werden müssen. Diese Option steht nur Admins zur Verfügung. |

1. (Optional) Um die Liste weiter zu verfeinern, können Sie die Komponentenliste sortieren, wie hier beschrieben: [Sortieren der Komponentenliste](#sort-the-component-list).

### Sortieren der Komponentenliste

1. (Optional) Wenden Sie alle Filter auf die Komponentenliste an, wie unter [Filtern der Komponentenliste](#filter-the-component-list).

1. Wählen Sie die **Komponenten** icon ![Symbol &quot;Komponenten&quot;](assets/components-icon.png) in der linken Leiste.

1. Wählen Sie die **Sortieren** icon ![Symbol &quot;Komponenten sortieren&quot;](assets/component-sort-icon.png)und wählen Sie eine der folgenden Filteroptionen aus, um die Liste der Komponenten zu sortieren:

   {{components-sort-options}}
