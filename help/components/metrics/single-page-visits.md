---
title: Einzelseitenbesuche
description: Die Häufigkeit, mit der sich der Dimensionswert "Seite"bei einem Besuch nicht geändert hat.
translation-type: tm+mt
source-git-commit: 54aeaa35fea8f725c87030936fa24f415064e333
workflow-type: tm+mt
source-wordcount: '166'
ht-degree: 0%

---


# Einzelseitenbesuche

*Auf dieser Hilfeseite wird beschrieben, wie &quot;Einzelseitenbesuche&quot;als Metrik funktioniert. Weitere Informationen finden Sie unter Dimension[Einzelseitenbesuche](../dimensions/single-page-visits.md).*

Die Metrik &quot;Einzelseitenbesuche&quot;zeigt die Anzahl der Besuche an, bei denen der Dimensionswert &quot; [Seite](../dimensions/page.md) &quot;nur einen einzigen eindeutigen Wert für den gesamten Besuch enthielt. Diese Metrik ist hilfreich im Zusammenhang mit Dimensionen, in denen Sie kurze Besuche sehen möchten, aber keine so strengen Regeln wie [Absprünge](bounces.md)haben.

## Berechnung dieser Metrik

Diese Metrik zählt die Anzahl der Besuche, bei denen der Dimensionswert &quot;Seite&quot;nur einen einzigen eindeutigen Wert für den gesamten Besuch enthielt. Wenn ein Besucher die Seite neu lädt oder Link-Verfolgungsaufrufe auslöst, zählt dies immer noch als Einzelseitenbesuch. Sobald die Dimension &quot;Seite&quot;in einen zweiten eindeutigen Wert geändert wird, qualifiziert sich der Besuch nicht mehr als Einzelseitenbesuch.

Siehe [Einzelzugriff](single-access.md) für einen Vergleich der Metriken.
