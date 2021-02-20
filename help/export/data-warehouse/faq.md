---
title: Häufig gestellte Fragen zur Data Warehouse
description: Häufig gestellte Fragen zur Data Warehouse.
translation-type: tm+mt
source-git-commit: dbcdabdfd53b9d65d72e6269fcd25ac7118586e7
workflow-type: tm+mt
source-wordcount: '131'
ht-degree: 9%

---


# Häufig gestellte Fragen zur Data Warehouse

Häufig gestellte Fragen zur Data Warehouse.

## In welchem Format werden die Daten erwartet, wenn ich beim Erstellen einer Anforderung das Dropdownmenü für die Granularität verwende?

Bei der Anwendung der Granularität in einer Anforderung der Data Warehouse wird dem Bericht die Spalte &quot;Datum&quot;hinzugefügt. Je nach ausgewählter Granularität ändert sich das Datumsformat.

| Granularität | Format | Beispiel |
| --- | --- | --- |
| Stündlich | `mmmm d, yyyy` Stunde `H` | 1. Januar, 20XX, Stunde 0 |
| Täglich | `mmmm d, yyyy` | 1. Januar 2010 |
| Wöchentlich | Woche `w, yyyy` | Woche 1, 20XX |
| Monatlich | `mmmm yyyy` | 20XX. Januar |
| Quartalsweise | `q` Quartal `yyyy` | 1. Quartal 20XX |
| Jährlich | `yyyy` | 20 XX |

## Wie funktionieren Segmente als Dimensionen in der Data Warehouse?

Wenn Sie ein Segment als Dimension in der Data Warehouse verwenden, gibt der Bericht eine Spalte zurück, die `"0"` oder `"1"` enthält:

* **`"0"`**: Das Dimensionselement entsprach nicht den Kriterien des Segments.
* **`"1"`**: Das Dimensionselement entsprach den Kriterien des Segments.
