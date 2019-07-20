---
description: Data Sources unterstützt die folgenden Konversion-Datendimensionen und -Metriken für Datentypen, die als Konversion verarbeitet werden.
seo-description: Data Sources unterstützt die folgenden Konversion-Datendimensionen und -Metriken für Datentypen, die als Konversion verarbeitet werden.
seo-title: Konversion
solution: Analytics
subtopic: Datenquellen
title: Konversion
topic: Entwickler und Implementierung
uuid: 5 e 7907 b 1-6 c 9 c -4073-876 b -410 f 3 a 29767 d
translation-type: tm+mt
source-git-commit: 86fe1b3650100a05e52fb2102134fee515c871b1

---


# Konversion

Data Sources unterstützt die folgenden Konversion-Datendimensionen und -Metriken für Datentypen, die als Konversion verarbeitet werden.

## Konversion-Dimensionen und -Metriken {#section_FA1731B232B246DABEDF5A5D84159084}

Wenn Sie ein Ansichtereignis festlegen, müssen Sie auch die entsprechende Datendimension (eVar) festlegen. Wenn Sie beispielsweise eVar2-Ansichten einschließen, müssen Sie eVar2 mit einem Wert angeben. Die Anzahl der von einer Bericht-Suite unterstützten benutzerspezifischen Ereignisse und eVar-Ansichten ist vom Vertrag abhängig und kann sich je nach Unternehmen unterscheiden.

<p class="head"> <b>Konversion-Dimensionen</b> </p>

| Spaltenname | Beschreibung |
|--- |--- |
| Trackingcode | Name des Trackingcodes. |
| Datum | Verwenden Sie das folgende Datumsformat: MM/TT/JJJJ/HH/mm/SS (zum Beispiel 01/01/2015/06/00/00). |
| Kategorie | Name der Kategorie.  Wenn Sie eine Kategorie angeben, müssen Sie auch ein Produkt auswählen. |
| Kanal | Kanalname. |
| Evarn | Name des evarn. Gültige Werte für n sind Ganzzahlen zwischen 1 und 75. |
| Produkt | Produktname. |
| Land | Name des Landes. |
| PLZ | Postleitzahl. |

<p class="head"> <b>Konversionsmetriken</b> </p>

| Spaltenname | Beschreibung |
|--- |--- |
| Clickthroughs | Anzahl der Trackingcode-Ansichten. |
| Hinzufügen zum Einkaufswagen | Anzahl der Zusätze zum Einkaufswagen. |
| Öffnung des Einkaufswagens | Anzahl der Öffnungen des Einkaufswagens. |
| Entnahmen aus dem Einkaufswagen | Anzahl der Entnahmen aus dem Einkaufswagen. |
| Einkaufswagenansicht | Anzahl der Einkaufswagenansichten. |
| Kassengänge | Anzahl der Kassengänge. |
| Ereignis n | Häufigkeit, in der Ereignis n eintritt. Gültige Werte für n sind Ganzzahlen zwischen 1 und 100.  Wenn Sie ein Ansichtereignis festlegen, müssen Sie auch die entsprechende Datendimension (eVar) festlegen. Wenn Sie beispielsweise eVar2-Ansichten einschließen, müssen Sie eVar2 mit einem Wert angeben. |
| Evarn-Ansichten | Häufigkeit, in der eVarn angezeigt wurde. Gültige Werte für n sind Ganzzahlen zwischen 1 und 75. |
| Preis | Produktpreis. |
| Bestellungen | Anzahl der aufgegebenen Bestellungen. |
| Produktansichten | Anzahl der Produktansichten. |
| Quantität | Anzahl der verkauften Einheiten. |