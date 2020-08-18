---
description: Verwenden Sie die Linienvisualisierung zur Darstellung von (zeitbasierten) Trenddatensätzen
title: Linie
uuid: 0508ff29-43fe-4f3a-a5f7-051869271b55
translation-type: tm+mt
source-git-commit: 34db4e99589827fd41f642788e3409834b96d78a
workflow-type: tm+mt
source-wordcount: '446'
ht-degree: 16%

---


# Linie

Diese Visualisierung stellt Metriken anhand einer Linie dar, die den Wertverlauf über einen bestimmten Zeitraum hinweg zeigt. Ein Liniendiagramm kann nur verwendet werden, wenn die Zeit als Dimension verwendet wird.

## Visualisierungseinstellungen

>[!IMPORTANT]
>
> Einige Einstellungen für die Linienvisualisierung, wie &quot;Trendlinie anzeigen&quot;, werden derzeit nur eingeschränkt getestet. [Weitere Infos](https://docs.adobe.com/content/help/de-DE/analytics/landing/an-releases.html).

Klicken Sie auf das Zahnradsymbol oben rechts in der Linienvisualisierung, um auf die verfügbaren [**Visualisierungseinstellungen**](https://docs.adobe.com/content/help/en/analytics/analyze/analysis-workspace/visualizations/freeform-analysis-visualizations.html#section_D3BB5042A92245D8BF6BCF072C66624B) zuzugreifen. Einstellungen werden wie folgt kategorisiert:

* Allgemein - Einstellungen, die bei allen Visualisierungstypen üblich sind
* Achse - Einstellungen, die sich auf die X- oder Y-Achse der Linienvisualisierung auswirken
* Überlagerungen - Optionen zum Hinzufügen zusätzlicher Kontexte zu den Reihen, die in Ihrer Linienvisualisierung angezeigt werden.

### Granularität ändern

In den [Visualisierungseinstellungen](/help/analyze/analysis-workspace/visualizations/freeform-analysis-visualizations.md#section_D3BB5042A92245D8BF6BCF072C66624B) können Sie über ein Dropdown-Menü für die Granularität eine Trend-Visualisierung (z. B. Linie, Balken) von täglich zu wöchentlich zu monatlich usw. ändern. Die Granularität wird auch in der Datenquelle-Tabelle aktualisiert.

### Min. oder Max. anzeigen

Unter &quot; **Visualisierungseinstellungen&quot;> &quot;Überlagerungen&quot;> &quot;Min./max** anzeigen&quot;können Sie eine Mindest- und Höchstwertebeschriftung überlagern, um die Spitzen und Täler in einer Metrik schnell hervorzuheben.

### Trendzeilenüberlagerung anzeigen

Unter &quot; **Visualisierungseinstellungen&quot;> &quot;Überlagerungen&quot;> &quot;Trendlinie** anzeigen&quot;können Sie eine Regressions-Trendlinie zu Ihrer Zeilenserie hinzufügen. Trendlinien helfen, ein klareres Muster in den Daten darzustellen.

Alle Modelle passen mit den üblichen Minimalquadraten:

| Modell | Beschreibung |
|---|---|
| Linear | Erstellt eine am besten geeignete gerade Linie für einfache lineare Datensätze und ist nützlich, wenn die Daten mit einer konstanten Rate erhöht oder verringert werden. Gleichung: y = a + b * x |
| Logarithmisch | Erstellt eine am besten passende gekrümmte Linie und ist nützlich, wenn die Änderungsrate in den Daten schnell zunimmt oder abnimmt und dann ausgeglichen wird. Eine logarithmische Trendlinie kann negative und positive Werte verwenden. Gleichung: y = a + b * log(x) |
| Exponentiell | Erzeugt eine Kurven-Linie und ist nützlich, wenn die Daten in ständig steigenden Raten ansteigen oder fallen. Diese Option sollte nicht verwendet werden, wenn Ihre Daten null oder negative Werte enthalten. Gleichung: y = a +<sup>eb * x |
| Strom | Erstellt eine Kurvenlinie und ist nützlich für Datensätze, die Messungen vergleichen, die mit einer bestimmten Rate zunehmen. Diese Option sollte nicht verwendet werden, wenn Ihre Daten null oder negative Werte enthalten. Gleichung: y = a *<sup>xb |
| Quadratisch | Findet die beste Passform für einen Datensatz, der wie eine Parabola geformt ist (konkav nach oben oder unten). Gleichung: y = a + b * x + c * x<sup>2 |
| Polynomial | Nützlich, wenn Ihr Datensatz schwankt, z. B. die Analyse von Gewinnen und Verlusten über einen großen Datensatz. Gleichung: y = a + b * x + ... + k *<sup>xorder |
