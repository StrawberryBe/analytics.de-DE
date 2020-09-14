---
description: 'Komponenten in Analysis Workspace bestehen aus Dimensionen, Metriken, Segmenten und Datumsbereichen, die Sie per Drag & Drop in ein Projekt ziehen können. '
title: Komponentenübersicht
uuid: 1a4e1c35-eac9-4eb4-be2e-ecb2c6728150
translation-type: tm+mt
source-git-commit: 08d61f4e41bae8a9a0a4be6a950db4ef093c4b02
workflow-type: tm+mt
source-wordcount: '731'
ht-degree: 13%

---


# Komponentenübersicht

Komponenten in Analysis Workspace bestehen aus Dimensionen, Metriken, Segmenten und Datumsbereichen, die Sie per Drag &amp; Drop in ein Projekt ziehen können.

To access the Components menu, click the **Components** icon in the left rail. Sie können zwischen [Bedienfeldern](https://docs.adobe.com/content/help/en/analytics/analyze/analysis-workspace/panels/panels.html), [Visualisierungen](https://docs.adobe.com/content/help/de-DE/analytics/analyze/analysis-workspace/visualizations/freeform-analysis-visualizations.html)und Komponenten über die linken Leiste oder über [Hotkeys](/help/analyze/analysis-workspace/build-workspace-project/fa-shortcut-keys.md)wechseln.

Sie können auch die Einstellungen [für die Dichte der](https://docs.adobe.com/content/help/de-DE/analytics/analyze/analysis-workspace/build-workspace-project/view-density.html) Ansicht für das Projekt anpassen, um mehr Werte auf einmal in der linken Leiste anzuzeigen, indem Sie zu **&quot;Projekt&quot;> &quot;Projektinfo und Einstellungen&quot;> &quot;Ansicht-Dichte&quot;** navigieren.

## Dimensionen {#dimensions}

[**Dimensionen**](https://docs.adobe.com/content/help/en/analytics/components/dimensions/overview.html) sind Textattribute, die das Verhalten Ihres Besuchers beschreiben und in Ihrer Analyse angezeigt, aufgeschlüsselt und verglichen werden können. Sie befinden sich in der Leiste &quot;Komponente links&quot;(orangefarbener Abschnitt) und werden in der Regel als Tabellenzeilen angewendet.

Beispiele für Dimensionen sind Seitenname, Marketing-Kanal, Gerätetyp und Produkte. Dimensionen werden von der Adobe bereitgestellt und über Ihre benutzerdefinierte Implementierung erfasst (eVar, Props, Classifications usw.).

Jede Dimension enthält auch **Dimensionselemente** darin. Elemente der Dimension finden Sie in der linken Leiste Komponente, indem Sie auf den Chevron-Pfeil neben einem beliebigen Dimensionsnamen klicken (Elemente sind gelb).

Beispiele für Dimensionselemente sind Homepage (innerhalb der Seitendimension), gebührenpflichtige Suche (innerhalb der Dimension &quot;Marketing-Kanal&quot;), Tablet (innerhalb der Dimension &quot;Mobilgerätetyp&quot;) usw.

## Metriken {#metrics}

[**Metriken**](https://docs.adobe.com/content/help/en/analytics/components/metrics/overview.html) sind quantitative Messungen zum Verhalten von Besuchern. Sie befinden sich in der linken Leiste Komponente (grüner Abschnitt) und werden normalerweise als Tabellenspalten angewendet.

Beispiele für Metriken sind Ansichten auf der Seite, Besuche, Bestellungen, durchschnittliche Besuchszeit und Umsatz/Bestellungen. Metriken werden durch Adoben bereitgestellt, über Ihre benutzerdefinierte Implementierung (Erfolgsergebnisse) erfasst oder mit dem Generator für [berechnete Metriken](https://docs.adobe.com/content/help/de-DE/analytics/components/calculated-metrics/calcmetric-workflow/cm-build-metrics.html)erstellt.

## Segmente {#segments}

[**Segmente**](https://docs.adobe.com/content/help/de-DE/analytics/analyze/analysis-workspace/components/t-freeform-project-segment.html) sind Filter der Audience, die auf Ihre Analyse angewendet werden. Sie befinden sich in der Leiste &quot;Komponente links&quot;(blauer Abschnitt) und werden normalerweise oben in einem Bereich oder über den Metrikspalten in einer Tabelle angewendet.

Beispiele für Segmente sind Besucher von Mobilgeräten, Besuche von E-Mails und authentifizierte Treffer. Segmente werden durch Adoben bereitgestellt, im [Bedienfeld-Dropzone](https://docs.adobe.com/content/help/en/analytics/analyze/analysis-workspace/panels/panels.html)erstellt oder mit dem [Segmentaufbau](https://docs.adobe.com/content/help/de-DE/analytics/components/segmentation/segmentation-workflow/seg-build.html)erstellt.

## Datumsbereiche {#date-ranges}

[**Datumsbereiche**](https://docs.adobe.com/content/help/de-DE/analytics/analyze/analysis-workspace/components/calendar-date-ranges/calendar.html) sind der Datumsbereich, über den Sie Ihre Analyse durchführen. Sie befinden sich in der Leiste &quot;Komponente links&quot;(violetter Abschnitt) und werden normalerweise im Kalender der einzelnen Bereiche angewendet.

Beispiele für Datumsbereiche sind Juli 2019, Letzte 4 Wochen und Dieser Monat. Datumsbereiche werden nach Adobe bereitgestellt, im [Bereichskalender](https://docs.adobe.com/content/help/en/analytics/analyze/analysis-workspace/panels/panels.html)angewendet oder mit dem [Datumsbereich-Builder](https://docs.adobe.com/content/help/en/analytics/analyze/analysis-workspace/components/calendar-date-ranges/custom-date-ranges.html)erstellt.

## Komponentenaktionen {#actions}

Sie können Komponenten (einzeln oder durch Auswahl mehrerer Komponenten) direkt in der linken Leiste verwalten. Klicken Sie mit der rechten Maustaste auf eine Komponente oder klicken Sie auf das Aktionspunkt-Symbol oben in der Liste der Komponente.

| Komponentenaktion | Beschreibung |
|--- |--- |
| Tag | Organisieren oder verwalten Sie Komponenten, indem Sie Tags darauf anwenden. Sie können dann in der linken Leiste nach Tag suchen, indem Sie auf den Filter klicken oder # eingeben. Tags fungieren auch als Filter in den Komponentenmanagern. |
| Favorit | Fügen Sie die Komponente Ihrer Favoritenliste hinzu. Wie Tags können Sie in der linken Leiste nach Favoriten suchen und sie in den Komponentenmanagern filtern. |
| Genehmigen | Markieren Sie Komponenten als genehmigt, um Ihren Benutzern zu signalisieren, dass die Komponente vom Unternehmen genehmigt wurde. Wie Tags können Sie in der linken Leiste nach Genehmigt suchen und in den Komponentenmanagern filtern. |
| Freigeben | Freigeben von Komponenten für Benutzer in Ihrer Organisation. Diese Option steht nur für benutzerdefinierte Komponenten zur Verfügung, z. B. Segmente oder berechnete Metriken. |
| Löschen | Löschen Sie Komponenten, die Sie nicht mehr benötigen. Diese Option steht nur für benutzerdefinierte Komponenten zur Verfügung, z. B. Segmente oder berechnete Metriken. |

Benutzerdefinierte Komponenten können auch über ihre jeweiligen Komponentenmanager verwaltet werden.
