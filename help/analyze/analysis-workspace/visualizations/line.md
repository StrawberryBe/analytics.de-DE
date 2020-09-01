---
description: Verwenden Sie die Linienvisualisierung zur Darstellung von (zeitbasierten) Trenddatensätzen
title: Linie
uuid: 0508ff29-43fe-4f3a-a5f7-051869271b55
translation-type: tm+mt
source-git-commit: 5bb2fc217cb7da3696a7c55ef8d193a93c18c2d8
workflow-type: tm+mt
source-wordcount: '400'
ht-degree: 12%

---


# Linie

Die Linienvisualisierung stellt Metriken mithilfe einer Zeile dar, um zu zeigen, wie sich Werte über einen bestimmten Zeitraum ändern. Ein Liniendiagramm kann nur verwendet werden, wenn die Zeit als Dimension verwendet wird.

![Linienvisualisierung](assets/line-viz.png)

>[!IMPORTANT]
>
>Einige Einstellungen für die Linienvisualisierung, wie z. B. Trendlinie [!UICONTROL anzeigen], werden derzeit nur eingeschränkt getestet. [Weitere Infos](/help/landing/an-releases.md)

Klicken Sie auf das Zahnradsymbol oben rechts in der Linienvisualisierung, um auf die verfügbaren [**Visualisierungseinstellungen**](freeform-analysis-visualizations.md) zuzugreifen. Einstellungen werden wie folgt kategorisiert:

* **Allgemein**: Einstellungen, die bei allen Visualisierungstypen üblich sind
* **Achse**: Einstellungen, die die X- oder Y-Achse der Linienvisualisierung beeinflussen
* **Überlagerungen**: Optionen zum Hinzufügen zusätzlicher Kontexte zu den Serien, die in Ihrer Linienvisualisierung angezeigt werden.

![Visualisierungseinstellungen](assets/viz-settings-modal.png)

## Granularität ändern

In den [Visualisierungseinstellungen](freeform-analysis-visualizations.md) können Sie über ein Dropdown-Menü für die Granularität eine Trend-Visualisierung (z. B. Linie, Balken) von täglich zu wöchentlich zu monatlich usw. ändern. Die Granularität wird auch in der Datenquelle-Tabelle aktualisiert.

## Min. oder Max. anzeigen

Unter &quot; **[!UICONTROL Visualisierungseinstellungen]** &quot;> &quot; **[!UICONTROL Überlagerungen]** &quot;> &quot;min/max **** anzeigen&quot;können Sie eine Mindest- und Höchstwertebeschriftung überlagern, um die Spitzen und Täler in einer Metrik schnell hervorzuheben. Hinweis: Die Min/Max-Werte werden aus den sichtbaren Datenpunkten in der Visualisierung abgeleitet, nicht aus dem vollständigen Satz von Werten innerhalb einer Dimension.

![Min./Max. anzeigen](assets/min-max-labels.png)

## Trendzeilenüberlagerung anzeigen

Unter &quot; **[!UICONTROL Visualisierungseinstellungen]** &quot;> &quot; **[!UICONTROL Überlagerungen]** &quot;> &quot;Trendlinie **[!UICONTROL anzeigen&quot;]** können Sie eine Regressions-Trendlinie zu Ihrer Zeilenserie hinzufügen. Trendlinien helfen, ein klareres Muster in den Daten darzustellen.

![Lineare Trendlinie](assets/show-linear-trendline.png)

Alle Modelle passen mit den üblichen Minimalquadraten:

| Modell | Beschreibung |
|---|---|
| Linear | Erstellt eine am besten geeignete gerade Linie für einfache lineare Datensätze und ist nützlich, wenn die Daten mit einer konstanten Rate erhöht oder verringert werden. Gleichung: `y = a + b * x` |
| Logarithmisch | Erstellt eine am besten passende gekrümmte Linie und ist nützlich, wenn die Änderungsrate in den Daten schnell zunimmt oder abnimmt und dann ausgeglichen wird. Eine logarithmische Trendlinie kann negative und positive Werte verwenden. Gleichung: `y = a + b * log(x)` |
| Exponentiell | Erzeugt eine Kurven-Linie und ist nützlich, wenn die Daten in ständig steigenden Raten ansteigen oder fallen. Diese Option sollte nicht verwendet werden, wenn Ihre Daten null oder negative Werte enthalten. Gleichung: `y = a + e^(b * x)` |
| Leistung | Erstellt eine Kurvenlinie und ist nützlich für Datensätze, die Messungen vergleichen, die mit einer bestimmten Rate zunehmen. Diese Option sollte nicht verwendet werden, wenn Ihre Daten null oder negative Werte enthalten. Gleichung: `y = a * x^b` |
| Quadratisch | Findet die beste Passform für einen Datensatz, der wie eine Parabola geformt ist (konkav nach oben oder unten). Gleichung: `y = a + b * x + c * x^2` |
