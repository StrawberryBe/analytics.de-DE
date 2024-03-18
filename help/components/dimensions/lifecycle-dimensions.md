---
title: Lebenszyklusdimensionen für Mobile
description: Dimensionen basierend auf Daten, die mit dem Mobile SDK erfasst wurden.
feature: Dimensions
exl-id: b7ba45d7-7d30-48a3-a747-ea9fbb253abb
source-git-commit: 4c472d9a99f15ed253b68124aa31bdc88554d9a5
workflow-type: tm+mt
source-wordcount: '184'
ht-degree: 26%

---

# Lebenszyklusdimensionen für Mobile

*Diese Seite referenziert Daten, die häufig über das Adobe Experience Platform Mobile SDK verfolgt werden. Informationen zu Mobilgeräten mit dem Benutzeragenten finden Sie unter [Mobile Suchdimensionen](mobile-dimensions.md). Informationen zu den mithilfe des Mobile SDK verfolgten Metriken finden Sie unter [Mobile Lebenszyklusmetriken](../metrics/lifecycle-metrics.md).*

| Name der Lebenszyklusdimension | Beschreibung | Kontextdatenvariable |
| --- | --- | --- |
| [!UICONTROL Erstes Startdatum] | | TBD |
| [!UICONTROL Gerätename (SDK)] | | `a.DeviceName` |
| [!UICONTROL Betriebssystemversion (SDK)] | | `a.OSVersion` |
| [!UICONTROL Auflösung (SDK)] | | `a.Resolution` |
| [!UICONTROL Akquisequelle] | | `a.referrer.campaign.source` |
| [!UICONTROL App-ID] | | `a.AppID` |
| [!UICONTROL Akquise-Medium] | | `a.referrer.campaign.medium` |
| [!UICONTROL Akquise-Begriff] | | `a.referrer.campaign.term` |
| [!UICONTROL Akquise-Inhalt] | | `a.refferer.campaign.content` |
| [!UICONTROL Akquise-Name] | | `a.referrer.campaign.name` |
| [!UICONTROL Standort (bis 10 km)] | Der Längen- und Breitengrad des Besuchers, der auf die erste Dezimalstelle genau ist. Beispiel: `040.9` `-111.9`. | `a.loc.lat.a` + `a.loc.lon.a` |
| [!UICONTROL Standort (bis 100 m)] | Der Längen- und Breitengrad des Besuchers, der auf die dritte Dezimalstelle genau ist. Beispiel: `040.932` `-111.931`. | `a.loc.lat.a` + `a.loc.lat.b` + `a.loc.lon.a` + `a.loc.lon.b` |
| [!UICONTROL Standort (bis 1 m)] | Der Längen- und Breitengrad des Besuchers, der auf die fünfte Dezimalstelle genau ist. Beispiel: `040.93231` `-111.93152`. | `a.loc.lat.a` + `a.loc.lat.b` + `a.loc.lat.c` + `a.loc.lon.a` + `a.loc.lon.b` + `a.loc.lon.c` |
| [!UICONTROL Zielpunkt-Bezeichnung] | | `a.loc.poi` |
| [!UICONTROL Entfernung zum Zentrum des Zielpunkts] | | `a.loc.dist` |
| [!UICONTROL Startanzahl] | | `a.Launches` |
| [!UICONTROL Tage seit der ersten Verwendung] | | `a.DaysSinceFirstUse` |
| [!UICONTROL Aktionsname] | | TBD |
| [!UICONTROL Lebenszeitwert (evar)] | | `a.ltv.amount` |
| [!UICONTROL Beacon Major] | | TBD |
| [!UICONTROL Beacon Minor] | | TBD |
| [!UICONTROL Beacon-UUID] | | TBD |
| [!UICONTROL Beacon-Nähe] | | TBD |
| [!UICONTROL Tage seit der letzten Verwendung] | | `a.DaysSinceFirstUse` |
| [!UICONTROL Stunde des Tages (SDK)] | | `a.HourOfDay` |
| [!UICONTROL Wochentag (SDK)] | | `a.DayOfWeek` |
| [!UICONTROL Zielpunkt-ID] | | TBD |

{style="table-layout:auto"}

<!-- Missing: Install Date -->
