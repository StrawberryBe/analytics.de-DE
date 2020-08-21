---
title: Suchbegriff
description: Der Suchbegriff, mit dem der Besucher Ihre Site erreichte.
translation-type: tm+mt
source-git-commit: d3f92d72207f027d35f81a4ccf70d01569c3557f
workflow-type: tm+mt
source-wordcount: '250'
ht-degree: 78%

---


# Suchbegriff

Die Dimension „Suchbegriff“ erfasst die Suchbegriffe, die Besucher zum Erreichen Ihrer Site verwenden.

>[!IMPORTANT]
>
>Die meisten Suchmaschinen übergeben den Suchbegriff nicht mehr, da die Datenschutzpraktiken zunehmen. Hits where Adobe recognizes a search engine but is missing a keyword groups under the dimension item `"Keyword unavailable"`.

Ein Referrer muss die beiden folgenden Kriterien erfüllen, um als Suchbegriff klassifiziert zu werden:

* Die Referrer-Domäne wird von Adobe als gültige [Suchmaschine](search-engine.md) erkannt.
* In der Referrer-URL ist ein Abfragezeichenfolgenparameter für Suchbegriffe vorhanden. If the keyword query string exists but does not contain a value, it groups under the dimension item `"Keyword unavailable"`.

Wenn Sie zwischen gebührenpflichtiger und kostenloser Suche unterscheiden möchten, ist eine [Gebührenpflichtige Sucherkennung](/help/admin/admin/paid-search-detection/paid-search-detection.md) erforderlich. Für Suchbegriffe stehen mehrere Dimensionen zur Verfügung:

* **Suchbegriff**: Der Suchbegriff, mit dem Sie Ihre Site erreichen, unabhängig davon, ob die Suche gebührenpflichtig oder kostenlos ist.
* **Suchbegriff - bezahlt**: Der Suchbegriff, mit dem Ihre Site erreicht wurde und der mit der gebührenpflichtigen Sucherkennung übereinstimmt.
* **Suchbegriff - kostenlos**: Der Suchbegriff, mit dem Ihre Site erreicht wurde und der nicht mit der gebührenpflichtigen Sucherkennung übereinstimmt.

## Füllen dieser Dimension mit Daten

Diese Dimension verweist auf mehrere interne Suchtabellen von Adobe. Jeder Wert basiert auf dem [Referrer](referrer.md) des Treffers, der von [internen URL-Filtern](/help/admin/admin/internal-url-filter-admin.md) abhängig ist. Vergewissern Sie sich, dass die Dimension „Referrer“ und die internen URL-Filter korrekt konfiguriert sind.

## Dimensionen

Zu den Dimensionen gehören Suchbegriffe, die zum Erreichen Ihrer Site verwendet werden. The `"Unspecified"` dimension item is all non-search traffic.
