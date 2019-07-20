---
description: Besucher-IDs können durch Auswahl der Kategorie „Generisch (Transaktions-ID)“ integriert werden.
seo-description: Besucher-IDs können durch Auswahl der Kategorie „Generisch (Transaktions-ID)“ integriert werden.
seo-title: Besucher-ID
solution: Analytics
subtopic: Datenquellen
title: Visitor ID
topic: Entwickler und Implementierung
uuid: 4 e 9 ce 675-72 c 2-42 a 4-8 f 2 e -25140 df 19539
translation-type: tm+mt
source-git-commit: 86fe1b3650100a05e52fb2102134fee515c871b1

---


# Besucher-ID

Besucher-IDs können durch Auswahl der Kategorie „Generisch (Transaktions-ID)“ integriert werden.

See [Integrate Offline Data](../../../import/c-data-sources/datasrc-integrating-offline-data.md#concept_B5C576220F1548B5A3A57112AA3960C6).

<p class="head"> <b>Besucher-ID-Dimensionen</b> </p>

| Spaltenname | Beschreibung |
|--- |--- |
| Besucher-ID | (Erforderlich) Eindeutiger Wert, der einen Kunden in Online- und Offline-Systemen kennzeichnet. |
| Datum | Verwenden Sie das folgende Datumsformat: MM/TT/JJJJ/HH/mm/SS (zum Beispiel 07/14/2017/06/00/00) |
| Trackingcode | Name des Trackingcodes. |
| Kategorie | Name der Kategorie.  Wenn Sie eine Kategorie angeben, müssen Sie auch ein Produkt auswählen. |
| Kanal | Kanalname. |
| Evarn | Name des evarn. Gültige Werte für n sind Ganzzahlen zwischen 1 und 75. |
| Produkt | Produktname. |
| Land | Name des Landes. |
| PLZ | Postleitzahl. |

**Besucher-ID-Metriken**

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