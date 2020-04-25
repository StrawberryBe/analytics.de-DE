---
description: Ein Histogramm ist ein neuer Visualisierungstyp in Analysis Workspace.
title: Histogramm
uuid: 8a6bd2c4-da15-4f64-b889-ab9add685046
translation-type: tm+mt
source-git-commit: dabaf6247695bc4f3d9bfe668f3ccfca12a52269

---


# Histogramm

Ein Histogramm ähnelt einem Balkendiagramm, fasst jedoch Zahlen zu Bereichen („Pakete“) zusammen. Analytics automatisiert diese Zusammenfassung von Zahlen zu Bereichen, wobei Sie jedoch die Einstellungen unter [Erweiterte Einstellungen](#section_09D774C584864D4CA6B5672DC2927477) ändern können.

## Erstellen eines Histogramms {#section_74647707CC984A1CB6D3097F43A30B45}

So erstellen Sie ein Histogramm:

1. Click **[!UICONTROL Visualizations]** in the left rail.
1. Drag **[!UICONTROL Histogram]** to the panel.
1. Choose a Metric to drag to the Histogram visualization and click **[!UICONTROL Build]**.

![](assets/histogram.png)

>[!NOTE]Histogramme unterstützen nur normale Metriken, nicht jedoch berechnete Metriken.

Hier haben wir die Metrik „Seitenansichten pro Unique Visitors“ verwendet. Das erste Paket (links) bezieht sich auf 1 Seitenansicht pro Unique Visitor, das zweite auf 2 Seitenansichten usw.

![](assets/histogram2.png)

## Erweiterte Einstellungen {#section_09D774C584864D4CA6B5672DC2927477}

Wenn Sie die Einstellungen für Ihr Histogramm ändern möchten, klicken Sie auf das Einstellungssymbol (Zahnrad) in der Ecke oben rechts. Die folgenden Einstellungen können Sie ändern:

| Histogramm-Einstellungen | Dient dem folgenden Zweck |
|---|---|
| Startpaket | Bestimmt, mit welchem Paket das Histogramm beginnt. Die Standardeinstellung lautet 1. Sie können Startwerte von null bis unendlich festlegen, jedoch keine negativen Zahlen. |
| Metrische Behälter | Hiermit können Sie die Anzahl der Datumsbereiche (Behälter) erhöhen/verringern. Maximal 50 Behälter sind möglich. |
| Metrische Behältergröße | Hiermit können Sie die Größe der einzelnen Behälter festlegen. So könnten Sie zum Beispiel die Behältergröße von 1 Seitenansicht zu 2 Seitenansichten ändern. |
| Zählmethode | Sie können [Besucher](https://marketing.adobe.com/resources/help/de_DE/reference/visitors.html), [Besuch](https://marketing.adobe.com/resources/help/de_DE/reference/metrics_visit.html) oder [Hit](https://marketing.adobe.com/resources/help/de_DE/reference/hit.html) auswählen, z. B. Seitenansichten pro Besuch, Seitenansichten pro Besucher oder Seitenansichten pro Hit. Für Hits wird „Vorkommen“ in der Freiformtabelle als Metrik der Y-Achse verwendet. |

**Beispiele**:

* Startpaket: 1; Metrische Behälter: 5; Metrische Behältergröße: 2 – Diese Werte würden zu dem folgenden Histogramm führen: 1-2, 3-4, 5-6, 7-8, 9-10.
* Startpaket: 0; Metrische Behälter: 3; Metrische Behältergröße: 5 – Diese Werte würden zu dem folgenden Histogramm führen: 0-4, 5-9, 10-14.

## Anzeigen und Bearbeiten von Histogrammdaten {#section_B2CD7CDF0F6B432F928103AE7AAA3617}

To view or change the data source for the histogram chart, click the dot next to the Histogram header to go to **[!UICONTROL Data Source Settings]** > **[!UICONTROL Show Data Source]**.

![](assets/manage-data-source.png)

Vorab erstellte Segmente, die in der Tabelle angezeigt werden, sind interne Segmente und werden in der Segmentauswahl nicht angezeigt. Click the &quot;i&quot; icon next to the segment name, then click **[!UICONTROL Make public]** to make the segment public.

![](assets/prebuilt_segments.png)

Weitere Möglichkeiten zum Verwalten von Freiform-Datentabellen und anderen Visualisierungen (wie zum Beispiel Datenaufschlüsselungen) finden Sie [hier](https://marketing.adobe.com/resources/help/de_DE/analytics/analysis-workspace/freeform-analysis-visualizations.html).
