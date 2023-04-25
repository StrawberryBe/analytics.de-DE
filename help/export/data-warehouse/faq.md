---
title: Häufig gestellte Fragen zu Data Warehouse
description: Häufig gestellte Fragen zu Data Warehouse.
feature: Data Warehouse
exl-id: 51c3ba17-a8b2-4030-9521-355ebbbfcd0d
source-git-commit: 78cfb1f3c4d45fc983982a8da11b66f2b2c9ecbc
workflow-type: tm+mt
source-wordcount: '132'
ht-degree: 84%

---

# Häufig gestellte Fragen zu Data Warehouse

Häufig gestellte Fragen zu Data Warehouse.

## Welches Format kann ich erwarten, wenn ich die Dropdown-Liste für die Granularität beim Erstellen einer Anforderung verwende?

Bei der Anwendung der Granularität in einer Anforderung in Data Warehouse wird der Bericht um die Spalte „Datum“ ergänzt. Je nach ausgewählter Granularität ändert sich das Datumsformat.

| Granularität | Format | Beispiel |
| --- | --- | --- |
| Stündlich | `mmmm d, yyyy` Stunde `H` | 1. Januar 20XX, Stunde 0 |
| Täglich | `mmmm d, yyyy` | 1. Januar 20XX |
| Wöchentlich | Woche `w, yyyy` | Woche 1, 20XX |
| Monatlich | `mmmm yyyy` | Januar 20XX |
| Quartalsweise | `q` Quartal `yyyy` | 1. Quartal 20XX |
| Jährlich | `yyyy` | 20XX |

## Wie funktionieren Segmente als Dimensionen in Data Warehouse?

Wenn Sie ein Segment als Dimension in Data Warehouse verwenden, gibt der Bericht eine Spalte zurück, die `"0"` oder `"1"` enthält:

* **`"0"`**: Das Dimensionselement entsprach nicht den Kriterien des Segments.
* **`"1"`**: Das Dimensionselement entsprach den Kriterien des Segments.
