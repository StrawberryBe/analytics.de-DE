---
title: Suchmaschine
description: Die Suchmaschine, mit der der Besucher Ihre Site erreichte.
translation-type: tm+mt
source-git-commit: 1869d69566d26aa7d99c520efc2e835901439d48
workflow-type: tm+mt
source-wordcount: '224'
ht-degree: 1%

---


# Suchmaschine

Die Dimension &quot;Suchmaschine&quot;zeigt die Suchmaschinen an, die Besucher zum Erreichen Ihrer Site verwenden. Ein Werber muss die beiden folgenden Kriterien erfüllen, um als Suchmaschine klassifiziert zu werden:

* Die verweisende Domäne wird von Adobe als gültige Suchmaschine erkannt.
* In der verweisenden URL ist ein Abfragen-Zeichenfolgenparameter vorhanden. Der Parameter für die Zeichenfolge der Abfrage kann leer sein (wie bei mehreren Suchmaschinen aufgrund von Datenschutzpraktiken).

Wenn Sie zwischen gebührenpflichtiger und kostenloser Suche unterscheiden möchten, ist eine Erkennung [gebührenpflichtiger Suchen](/help/admin/admin/paid-search-detection/paid-search-detection.md) erforderlich. Für Suchmaschinen stehen mehrere Dimensionen zur Verfügung:

* **Suchmaschine**: Die Suchmaschine, die zum Erreichen Ihrer Site verwendet wurde, unabhängig davon, ob diese gebührenpflichtig oder kostenlos ist.
* **Suchmaschine - gebührenpflichtig**: Die Suchmaschine, die zum Erreichen Ihrer Site verwendet wurde und die mit der gebührenpflichtigen Sucherkennung übereinstimmte.
* **Suchmaschine - kostenlos**: Die Suchmaschine, die Ihre Site erreichte, was nicht mit der gebührenpflichtigen Sucherkennung übereinstimmte.

## Diese Dimension mit Daten füllen

Diese Dimension verweist auf mehrere Nachschlagetabellen innerhalb von Adobe. Jeder Wert basiert auf dem [Werber](referrer.md) des Treffers, der von [internen URL-Filtern](/help/admin/admin/internal-url-filter-admin.md)abhängig ist. Vergewissern Sie sich, dass die Dimension &quot;Werber&quot;und die internen URL-Filter korrekt konfiguriert sind.

## Dimensionswerte

Dimensionswerte umfassen Suchmaschinen, die zum Erreichen Ihrer Site verwendet werden. Zu den Beispielwerten gehören `"Google"`, `"Microsoft Bing"`und `"DuckDuckGo"`. Der `"Unspecified"` Dimensionswert ist ausschließlich Traffic ohne Suche.
