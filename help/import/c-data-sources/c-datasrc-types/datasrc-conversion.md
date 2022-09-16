---
description: Datenquellen unterstützen die folgenden Konversions-Datendimensionen und -Metriken für Datentypen, die als Konversion verarbeitet werden.
subtopic: Data sources
title: Konversion
topic-fix: Developer and implementation
feature: Data Sources
exl-id: 00450ad4-7148-4cf1-bdba-5d1732dd0fd3
source-git-commit: 79294cfc6f86e5a41a39504099cd730f53668725
workflow-type: tm+mt
source-wordcount: '271'
ht-degree: 100%

---

# Konversion

Datenquellen unterstützen die folgenden Konversions-Datendimensionen und -Metriken für Datentypen, die als Konversion verarbeitet werden.

## Konversion-Dimensionen und -Metriken  {#section_FA1731B232B246DABEDF5A5D84159084}

Wenn Sie ein Ansichtereignis festlegen, müssen Sie auch die entsprechende Datendimension (eVar) festlegen. Wenn Sie beispielsweise eVar2-Ansichten einschließen, müssen Sie eVar2 mit einem Wert angeben. Die Anzahl der von einer Bericht-Suite unterstützten benutzerspezifischen Ereignisse und eVar-Ansichten ist vom Vertrag abhängig und kann sich je nach Unternehmen unterscheiden.

<p class="head"> <b>Konversion-Dimensionen</b> </p>

| Spaltenname | Beschreibung |
|--- |--- |
| Trackingcode | Name des Trackingcodes. |
| Datum | Verwenden Sie das folgende Datumsformat: MM/TT/JJJJ/HH/mm/SS (zum Beispiel 01/01/2015/06/00/00). |
| Kategorie | Name der Kategorie.  Wenn Sie eine Kategorie angeben, müssen Sie auch ein Produkt auswählen. |
| Kanal | Kanalname. |
| eVarn | eVarn-Name. Gültige Werte für n sind Ganzzahlen zwischen 1 und 250. |
| Produkt | Produktname. |
| Bundesland | Name des Landes. |
| Zip | Postleitzahl. |

<p class="head"> <b>Konversionsmetriken</b> </p>

| Spaltenname | Beschreibung |
|--- |--- |
| Durchklickrate | Anzahl der Trackingcode-Ansichten. |
| Hinzufügungen zum Warenkorb | Anzahl der Hinzufügungen zum Warenkorb. |
| Öffnungen des Warenkorbs | Anzahl der Öffnungen des Warenkorbs. |
| Entfernungen aus dem Warenkorb | Anzahl der Entfernungen aus dem Warenkorb. |
| Warenkorbansichten | Anzahl der Ansichten des Warenkorbs. |
| Checkouts | Anzahl der Kassengänge. |
| Ereignis n | Häufigkeit, in der Ereignis n eintritt. Gültige Werte für n sind Ganzzahlen zwischen 1 und 100.  Wenn Sie ein Ansichtereignis festlegen, müssen Sie auch die entsprechende Datendimension (eVar) festlegen. Wenn Sie beispielsweise eVar2-Ansichten einschließen, müssen Sie eVar2 mit einem Wert angeben. |
| eVarn-Ansichten | Häufigkeit, in der eVar n angezeigt wurde. Gültige Werte für n sind Ganzzahlen zwischen 1 und 250. |
| Preis | Produktpreis. |
| Bestellungen | Anzahl der aufgegebenen Bestellungen. |
| Produktansichten | Anzahl der Produktansichten. |
| Menge | Anzahl der verkauften Einheiten. |
