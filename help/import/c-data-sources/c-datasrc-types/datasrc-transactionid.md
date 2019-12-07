---
description: Transaktions-IDs können durch Auswahl der Kategorie „Generisch (Transaktions-ID)“ integriert werden.
subtopic: Data sources
title: Transaktions-ID
topic: Developer and implementation
uuid: f3370bb7-3f28-460b-a20d-c9e58d7301d4
translation-type: tm+mt
source-git-commit: 99ee24efaa517e8da700c67818c111c4aa90dc02

---


# Transaktions-ID

Transaktions-IDs können durch Auswahl der Kategorie „Generisch (Transaktions-ID)“ integriert werden.

See [Integrating Offline Data](/help/import/c-data-sources/datasrc-integrating-offline-data.md).

Data uploaded with *`transactionID`* automatically associates with the same marketing channel that processed the original server call that contained the *`transactionID`*.

**Transaktions-ID-Dimensionen**

| Spaltenname | Beschreibung |
|--- |--- |
| Transaktions-ID | (Erforderlich) Eindeutiger Wert, der eine Online-Transaktion kennzeichnet, die zu einer Offline-Aktivität geführt hat. |
| Datum | Verwenden Sie das folgende Datumsformat: MM/TT/JJJJ/HH/mm/SS (zum Beispiel 01/01/2015/06/00/00). |
| Trackingcode | Name des Trackingcodes. |
| Kategorie | Name der Kategorie.  Wenn Sie eine Kategorie angeben, müssen Sie auch ein Produkt auswählen. |
| Kanal | Kanalname. |
| eVarN | eVarN-Name. Gültige Werte für N sind Ganzzahlen 1 - 250. |
| Produkt | Produktname. |
| Land | Name des Landes. |
| Zip | Postleitzahl. |

<p class="head"> <b>Transaktions-ID-Metriken</b> </p>



| Spaltenname | Beschreibung |
|--- |--- |
| Clickthroughs | Anzahl der Trackingcode-Ansichten. |
| Hinzufügen zum Einkaufswagen | Anzahl der Zusätze zum Einkaufswagen. |
| Öffnung des Einkaufswagens | Anzahl der Öffnungen des Einkaufswagens. |
| Entnahmen aus dem Einkaufswagen | Anzahl der Entnahmen aus dem Einkaufswagen. |
| Warenkorbansicht | Anzahl der Einkaufswagenansichten. |
| Checkouts | Anzahl der Kassengänge. |
| EventN | Häufigkeit, mit der eventN aufgetreten ist. Gültige Werte für N sind Ganzzahlen zwischen 1 und 1000.  Wenn Sie ein Ansichtereignis festlegen, müssen Sie auch die entsprechende Datendimension (eVar) festlegen. Wenn Sie beispielsweise eVar2-Ansichten einschließen, müssen Sie eVar2 mit einem Wert angeben. |
| eVarN-Ansichten | Anzahl der Wiedergaben von eVarN. Gültige Werte für N sind Ganzzahlen 1 - 250. |
| Preis | Produktpreis. |
| Bestellungen | Anzahl der aufgegebenen Bestellungen. |
| Produktansichten | Anzahl der Produktansichten. |
| Quantität | Anzahl der verkauften Einheiten. |
