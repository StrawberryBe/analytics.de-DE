---
title: Suchbegriff
description: Der Suchbegriff, mit dem der Besucher Ihre Site erreichte.
translation-type: tm+mt
source-git-commit: c4833525816d81175a3446215eb92310ee4021dd
workflow-type: tm+mt
source-wordcount: '250'
ht-degree: 0%

---


# Suchbegriff

Die Dimension &quot;Suchbegriff&quot;erfasst die Suchbegriffe, die Besucher zum Erreichen Ihrer Site verwenden.

>[!IMPORTANT]
>
>Die meisten Suchmaschinen übergeben den Suchbegriff nicht mehr, da die Datenschutzpraktiken zunehmen. Treffer, bei denen Adobe eine Suchmaschine erkennt, unter dem Dimensionswert jedoch eine Suchbegriffgruppe fehlt `"Keyword unavailable"`.

Ein Werber muss die beiden folgenden Kriterien erfüllen, um als Suchbegriff klassifiziert zu werden:

* Die verweisende Domäne wird von Adobe als gültige [Suchmaschine](search-engine.md)erkannt.
* In der verweisenden URL ist ein Abfragen-Zeichenfolgenparameter vorhanden. Wenn die Suchbegriff-Abfrage vorhanden ist, jedoch keinen Wert enthält, gruppiert sie sich unter dem Dimensionswert `"Keyword unavailable"`.

Wenn Sie zwischen gebührenpflichtiger und kostenloser Suche unterscheiden möchten, ist eine Erkennung [gebührenpflichtiger Suchen](/help/admin/admin/paid-search-detection/paid-search-detection.md) erforderlich. Für Suchbegriffe stehen mehrere Dimensionen zur Verfügung:

* **Suchbegriff**: Der Suchbegriff, mit dem Sie Ihre Site erreichen, unabhängig davon, ob sie gebührenpflichtig oder kostenlos ist.
* **Suchbegriff - gebührenpflichtig**: Der Suchbegriff, mit dem Ihre Site erreicht wurde und der mit der gebührenpflichtigen Sucherkennung übereinstimmt.
* **Suchbegriff - kostenlos**: Der Suchbegriff, mit dem Ihre Site erreicht wurde und der nicht mit der Erkennung gebührenpflichtiger Suchen übereinstimmte.

## Diese Dimension mit Daten füllen

Diese Dimension verweist auf mehrere Nachschlagetabellen innerhalb von Adobe. Jeder Wert basiert auf dem [Werber](referrer.md) des Treffers, der von [internen URL-Filtern](/help/admin/admin/internal-url-filter-admin.md)abhängig ist. Vergewissern Sie sich, dass die Dimension &quot;Werber&quot;und die internen URL-Filter korrekt konfiguriert sind.

## Dimensionswerte

Dimensionswerte umfassen Suchbegriffe, die zum Erreichen Ihrer Site verwendet werden. Der `"Unspecified"` Dimensionswert ist ausschließlich Traffic ohne Suche.
