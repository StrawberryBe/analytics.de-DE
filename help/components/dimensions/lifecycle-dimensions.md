---
title: Mobile Lebenszyklusdimensionen
description: Dimensionen basierend auf Daten, die mit dem Mobile SDK erfasst wurden.
feature: Dimensions
exl-id: b7ba45d7-7d30-48a3-a747-ea9fbb253abb
source-git-commit: d940428e1cbe1be6d8263e986e8b641ec18aace1
workflow-type: tm+mt
source-wordcount: '145'
ht-degree: 57%

---

# Mobile Lebenszyklusdimensionen

*Diese Seite referenziert Daten, die häufig über das Adobe Experience Platform Mobile SDK verfolgt werden. Informationen zu Mobilgeräten mit dem Benutzeragenten finden Sie unter [Mobile Suchdimensionen](mobile-dimensions.md). Informationen zu den mithilfe des Mobile SDK verfolgten Metriken finden Sie unter [Mobile Lebenszyklusmetriken](../metrics/lifecycle-metrics.md).*

| Name der Lebenszyklusdimension | Beschreibung | Kontextdatenvariable |
| --- | --- | --- |
| [!UICONTROL Erster Starttermin] | | TBD |
| [!UICONTROL Gerätename (SDK)] | | `a.DeviceName` |
| [!UICONTROL Betriebssystemversion (SDK)] | | `a.OSVersion` |
| [!UICONTROL Auflösung (SDK)] | | `a.Resolution` |
| [!UICONTROL Akquisequelle] | | `a.referrer.campaign.source` |
| [!UICONTROL App-ID] | | `a.AppID` |
| [!UICONTROL Akquisemedium] | | `a.referrer.campaign.medium` |
| [!UICONTROL Akquisebedingung] | | `a.referrer.campaign.term` |
| [!UICONTROL Akquiseinhalt] | | `a.refferer.campaign.content` |
| [!UICONTROL Akquisename] | | `a.referrer.campaign.name` |
| [!UICONTROL Standort (bis 10 km)] | | `a.loc.lat.a` + `a.loc.lon.a` |
| [!UICONTROL Standort (bis 100 m)] | | `a.loc.lat.b` + `a.loc.lon.b` |
| [!UICONTROL Standort (bis 1 m)] | | `a.loc.lat.c` + `a.loc.lon.c` |
| [!UICONTROL Zielpunkt-Bezeichnung] | | `a.loc.poi` |
| [!UICONTROL Entfernung zum Zentrum des Zielpunkts] | | `a.loc.dist` |
| [!UICONTROL Launch-Nummer] | | `a.Launches` |
| [!UICONTROL Tage seit der ersten Verwendung] | | `a.DaysSinceFirstUse` |
| [!UICONTROL Aktionsname] | | TBD |
| [!UICONTROL Lebenszeitwert (evar)] | | `a.ltv.amount` |
| [!UICONTROL Beacon-Major-Wert] | | TBD |
| [!UICONTROL Beacon-Minor-Wert] | | TBD |
| [!UICONTROL Beacon-UUID] | | TBD |
| [!UICONTROL Beacon-Nähe] | | TBD |
| [!UICONTROL Tage seit der letzten Verwendung] | | `a.DaysSinceFirstUse` |
| [!UICONTROL Stunde des Tages (SDK)] | | `a.HourOfDay` |
| [!UICONTROL Wochentag (SDK)] | | `a.DayOfWeek` |
| [!UICONTROL Zielpunkt-ID] | | TBD |

{style="table-layout:auto"}

<!-- Missing: Install Date -->
