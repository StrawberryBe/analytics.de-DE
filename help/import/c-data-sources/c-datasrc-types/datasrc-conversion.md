---
description: Data Sources unterstützt die folgenden Konversion-Datendimensionen und -Metriken für Datentypen, die als Konversion verarbeitet werden.
subtopic: Data sources
title: Konversion
topic-fix: Developer and implementation
uuid: 5e7907b1-6c9c-4073-876b-410f3a29767d
exl-id: 00450ad4-7148-4cf1-bdba-5d1732dd0fd3
translation-type: tm+mt
source-git-commit: 78412c2588b07f47981ac0d953893db6b9e1d3c2
workflow-type: tm+mt
source-wordcount: '271'
ht-degree: 100%

---

# Konversion

Data Sources unterstützt die folgenden Konversion-Datendimensionen und -Metriken für Datentypen, die als Konversion verarbeitet werden.

## Konversion  Dimensionen und Metriken {#section_FA1731B232B246DABEDF5A5D84159084}

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
| Clickthroughs | Anzahl der Trackingcode-Ansichten. |
| Hinzufügen zum Einkaufswagen | Anzahl der Zusätze zum Einkaufswagen. |
| Öffnung des Einkaufswagens | Anzahl der Öffnungen des Einkaufswagens. |
| Entnahmen aus dem Einkaufswagen | Anzahl der Entnahmen aus dem Einkaufswagen. |
| Warenkorbansichten | Anzahl der Einkaufswagenansichten. |
| Checkouts | Anzahl der Kassengänge. |
| Ereignis n | Häufigkeit, in der Ereignis n eintritt. Gültige Werte für n sind Ganzzahlen zwischen 1 und 100.  Wenn Sie ein Ansichtereignis festlegen, müssen Sie auch die entsprechende Datendimension (eVar) festlegen. Wenn Sie beispielsweise eVar2-Ansichten einschließen, müssen Sie eVar2 mit einem Wert angeben. |
| eVarn-Ansichten | Häufigkeit, in der eVar n angezeigt wurde. Gültige Werte für n sind Ganzzahlen zwischen 1 und 250. |
| Preis | Produktpreis. |
| Bestellungen | Anzahl der aufgegebenen Bestellungen. |
| Produktansichten | Anzahl der Produktansichten. |
| Menge | Anzahl der verkauften Einheiten. |
