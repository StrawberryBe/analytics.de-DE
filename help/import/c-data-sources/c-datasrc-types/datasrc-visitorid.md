---
description: Besucher-IDs können durch Auswahl der Kategorie „Generisch (Transaktions-ID)“ integriert werden.
subtopic: Data sources
title: Visitor ID
topic-fix: Developer and implementation
uuid: 4e9ce675-72c2-42a4-8f2e-25140df19539
exl-id: 940af1ba-0d12-4552-a21e-0ceb06427ab2
source-git-commit: a7a116ddc9eddc500a52111e9c002bdbee3e4a56
workflow-type: tm+mt
source-wordcount: '224'
ht-degree: 81%

---

# VisitorID

Besucher-IDs können durch Auswahl der [!UICONTROL Callcenter-Daten] Kategorie.

Weitere Informationen finden Sie im Thema über das [Integrieren von Offline-Daten](/help/import/c-data-sources/datasrc-integrating-offline-data.md).

## VisitorID-Dimensionen

| Spaltenname | Beschreibung |
|--- |--- |
| [!UICONTROL VisitorID] | (Erforderlich) Eindeutiger Wert, der einen Kunden in Online- und Offline-Systemen kennzeichnet. |
| [!UICONTROL Datum] | Verwenden Sie das folgende Datumsformat: `MM/DD/YYYY/hh/mm/ss` (z. B. 14.7.2017/06/00/00) |
| [!UICONTROL Trackingcode] | Name des Trackingcodes. |
| [!UICONTROL Kategorie] | Name der Kategorie. Wenn Sie eine Kategorie angeben, müssen Sie auch ein Produkt auswählen. |
| [!UICONTROL Kanal] | Kanalname. |
| [!UICONTROL eVar ]*n* | Name von eVar *n*. Gültige Werte für *n* sind Ganzzahlen zwischen 1 und 75. |
| [!UICONTROL Produkt] | Produktname. |
| [!UICONTROL Bundesland] | Name des Landes. |
| [!UICONTROL Zip] | Postleitzahl. |

## Besucher-ID-Metriken

| Spaltenname | Beschreibung |
| --- | --- |
| [!UICONTROL Clickthroughs] | Anzahl der Trackingcode-Ansichten. |
| [!UICONTROL Hinzufügen zum Einkaufswagen] | Anzahl der Zusätze zum Einkaufswagen. |
| [!UICONTROL Öffnung des Einkaufswagens] | Anzahl der Öffnungen des Einkaufswagens. |
| [!UICONTROL Entnahmen aus dem Einkaufswagen] | Anzahl der Entnahmen aus dem Einkaufswagen. |
| [!UICONTROL Warenkorbansicht] | Anzahl der Einkaufswagenansichten. |
| [!UICONTROL Checkouts] | Anzahl der Kassengänge. |
| *Ereignis n* | Anzahl der geraden *n* aufgetreten. Gültige Werte für n sind Ganzzahlen zwischen 1 und 100.  Wenn Sie eine [!UICONTROL Ansicht] -Ereignis verwenden, müssen Sie auch die entsprechende Datendimension (eVar) angeben. Wenn Sie beispielsweise eVar2-Ansichten einschließen, müssen Sie eVar2 mit einem Wert angeben. |
| [!UICONTROL eVar ]*n*-Ansichten | Häufigkeit, in der eVar *n* angezeigt wurde. Gültige Werte für *n* sind Ganzzahlen zwischen 1 und 75. |
| [!UICONTROL Preis] | Produktpreis. |
| [!UICONTROL Bestellungen] | Anzahl der aufgegebenen Bestellungen. |
| [!UICONTROL Produktansichten] | Anzahl der Produktansichten. |
| [!UICONTROL Menge] | Anzahl der verkauften Einheiten. |
