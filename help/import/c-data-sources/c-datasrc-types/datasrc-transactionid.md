---
description: Transaktions-IDs können durch Auswahl der Kategorie „Generisch (Transaktions-ID)“ integriert werden.
seo-description: Transaktions-IDs können durch Auswahl der Kategorie „Generisch (Transaktions-ID)“ integriert werden.
seo-title: Transaktions-ID
solution: Analytics
subtopic: Datenquellen
title: Transaktions-ID
topic: Entwickler und Implementierung
uuid: f 3370 bb 7-3 f 28-460 b-a 20 d-c 9 e 58 d 7301 d 4
translation-type: tm+mt
source-git-commit: 86fe1b3650100a05e52fb2102134fee515c871b1

---


# Transaktions-ID

Transaktions-IDs können durch Auswahl der Kategorie „Generisch (Transaktions-ID)“ integriert werden.

See [Integrating Offline Data](../../../import/c-data-sources/datasrc-integrating-offline-data.md#concept_B5C576220F1548B5A3A57112AA3960C6).

Data uploaded with *`transactionID`* automatically associates with the same marketing channel that processed the original server call that contained the *`transactionID`*.

**Transaktions-ID-Dimensionen**

| Spaltenname | Beschreibung |
|--- |--- |
| Transaktions-ID | (Erforderlich) Eindeutiger Wert, der eine Online-Transaktion kennzeichnet, die zu einer Offline-Aktivität geführt hat. |
| Datum | Verwenden Sie das folgende Datumsformat: MM/TT/JJJJ/HH/mm/SS (zum Beispiel 01/01/2015/06/00/00). |
| Trackingcode | Name des Trackingcodes. |
| Kategorie | Name der Kategorie.  Wenn Sie eine Kategorie angeben, müssen Sie auch ein Produkt auswählen. |
| Kanal | Kanalname. |
| Evarn | Name des evarn. Gültige Werte für n sind Ganzzahlen zwischen 1 und 250. |
| Produkt | Produktname. |
| Land | Name des Landes. |
| PLZ | Postleitzahl. |

<p class="head"> <b>Transaktions-ID-Metriken</b> </p>



| Spaltenname | Beschreibung |
|--- |--- |
| Clickthroughs | Anzahl der Trackingcode-Ansichten. |
| Hinzufügen zum Einkaufswagen | Anzahl der Zusätze zum Einkaufswagen. |
| Öffnung des Einkaufswagens | Anzahl der Öffnungen des Einkaufswagens. |
| Entnahmen aus dem Einkaufswagen | Anzahl der Entnahmen aus dem Einkaufswagen. |
| Einkaufswagenansicht | Anzahl der Einkaufswagenansichten. |
| Kassengänge | Anzahl der Kassengänge. |
| Ereignis n | Häufigkeit, in der Ereignis n eintritt. Gültige Werte für n sind Ganzzahlen zwischen 1 und 1000.  Wenn Sie ein Ansichtereignis festlegen, müssen Sie auch die entsprechende Datendimension (eVar) festlegen. Wenn Sie beispielsweise eVar2-Ansichten einschließen, müssen Sie eVar2 mit einem Wert angeben. |
| Evarn-Ansichten | Häufigkeit, in der eVarn angezeigt wurde. Gültige Werte für n sind Ganzzahlen zwischen 1 und 250. |
| Preis | Produktpreis. |
| Bestellungen | Anzahl der aufgegebenen Bestellungen. |
| Produktansichten | Anzahl der Produktansichten. |
| Quantität | Anzahl der verkauften Einheiten. |