---
title: Rangansicht der Suchseite
description: Bestimmen Sie, welche Seite in einer Suchmaschine ein Besucher auf Ihre Site durchgeklickt hat.
translation-type: tm+mt
source-git-commit: d3f92d72207f027d35f81a4ccf70d01569c3557f
workflow-type: tm+mt
source-wordcount: '145'
ht-degree: 0%

---


# Rangansicht der Suchseite

Die Dimension &quot;Rangansicht aller Suchseiten&quot;bietet einen Einblick, auf welcher Seite der Suchergebnisse ein Besucher auf Ihre Site geklickt hat. Wenn Ihre Site beispielsweise auf der zweiten Seite der Suchergebnisse einer Suchmaschine erscheint, ist das Dimensionselement für diese Variable &quot;Suchseite 2&quot;.

## Diese Dimension mit Daten füllen

Damit diese Dimension nur funktioniert, müssen die [internen URL-Filter](/help/admin/admin/internal-url-filter-admin.md) in Ihrer Report Suite korrekt eingerichtet sein. AppMeasurement füllt diese Dimension automatisch, ohne dass Änderungen am Implementierungscode vorgenommen werden.

## Dimensionselemente

Wenn ein Besucher von einer Suchmaschine durch Ihre Site klickt, lautet der Wert dieser Dimension &quot;Suchseite&quot;, gefolgt von der Seitenzahl, auf die sie geklickt haben. Wenn ein Treffer nicht von einer Suchmaschine stammt, lautet der Wert dieser Dimension &quot;Nicht angegeben&quot;.
