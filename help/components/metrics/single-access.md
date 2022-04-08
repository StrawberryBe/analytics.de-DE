---
title: Einzelzugriff
description: Die Häufigkeit, mit der sich ein Dimensionselement bei einem Besuch nicht geändert hat.
feature: Metrics
exl-id: 973ce835-9d6f-4ead-90c9-0b80aac82cc0
source-git-commit: 7d5383e1ee3bee189d3dd48bc6b899f4108f7ba8
workflow-type: ht
source-wordcount: '339'
ht-degree: 100%

---

# Einzelzugriff

Die Metrik „Einzelzugriff“ gibt die Anzahl der Besuche an, bei denen das Dimensionselement nur einen einzigen eindeutigen Wert für den gesamten Besuch enthielt. Diese Metrik ist hilfreich für alle Dimensionen, bei denen Sie sehen möchten, welche Dimensionselemente während eines Besuchs stagnieren.

## Berechnung dieser Metrik

Diese Metrik zählt Besuche, bei denen das Dimensionselement einen einzigen eindeutigen Wert enthielt. Sie können das Dimensionselement mehrmals festlegen oder beibehalten und dennoch als Einzelzugriff zählen. Sobald sich ein Dimensionselement in einen zweiten eindeutigen Wert ändert, gilt der Besuch nicht mehr als Einzelzugriff.

## Unterschied zwischen „Einzelzugriff“ und „Einzelseitenbesuch“

Im Kontext der Dimension [Seite](../dimensions/page.md) sind „Einzelzugriff“ und „Einzelseitenbesuche“ identisch. Die Unterschiede treten auf, wenn Sie andere Dimensionen verwenden.

* **Einzelzugriff**: Zeigt die Anzahl der Besuche an, bei denen sich das angegebene Dimensionselement während des gesamten Besuchs nicht geändert hat. Sie ist kontextabhängig von der Dimension, die Sie in Ihrem Projekt verwenden.
* **Einzelseitenbesuch**: Zeigt die Anzahl der Besuche an, bei denen sich die Dimension „Seite“ während des gesamten Besuchs nicht geändert hat. Auch wenn Sie in Ihrem Bericht eine andere Dimension verwenden, zählt diese Besuche, die ein einziges eindeutiges Dimensionselement „Seite“ enthalten.

Betrachten Sie beispielsweise die folgenden zwei Trefferbesuche. Die Dimension in Ihrem Bericht ist [Website-Bereich](../dimensions/site-section.md).

* Ein Besucher ruft zwei Seiten auf, die sich jedoch beide im gleichen Website-Bereich befinden. Da der Website-Bereich während des Besuchs gleich blieb, zählt dies als Einzelzugriff. Dies zählt nicht als Einzelseitenbesuch, da der Besuch mehr als ein eindeutiges Dimensionselement „Seite“ enthält.
* Ein Besucher ruft zwei Seiten in verschiedenen Website-Bereichen auf, aber beide Seiten haben zufällig den gleichen Namen. Der Besuch zählt nicht als Einzelzugriff, da es zwei eindeutige Website-Bereichswerte gab. Er zählt als Einzelseitenbesuch, da ein einzelnes eindeutiges Dimensionselement „Seite“ vorhanden war.
