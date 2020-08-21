---
title: Einzelzugriff
description: Die Frequenz, mit der sich ein Dimensionselement bei einem Besuch nicht änderte.
translation-type: tm+mt
source-git-commit: d3f92d72207f027d35f81a4ccf70d01569c3557f
workflow-type: tm+mt
source-wordcount: '339'
ht-degree: 45%

---


# Einzelzugriff

Die Metrik &quot;Einzelzugriff&quot;zeigt die Anzahl der Besuche an, bei denen das Dimensionselement nur einen einzigen eindeutigen Wert für den gesamten Besuch enthielt. Diese Metrik ist hilfreich im Kontext jeder Dimension, in der Sie sehen möchten, welche Dimensionselemente während eines Besuchs stagnieren.

## Berechnung dieser Metrik

Diese Metrik zählt Besuche, bei denen das Dimensionselement einen einzigen eindeutigen Wert enthielt. Sie können das Dimensionselement mehrere Male festlegen oder es beibehalten und dennoch als Einzelzugriff zählen lassen. Sobald ein Dimensionselement in einen zweiten eindeutigen Wert umgewandelt wird, gilt der Besuch nicht mehr als Einzelzugriff.

## Unterschied zwischen „Einzelzugriff“ und „Einzelseitenbesuch“

Im Kontext der Dimension [Seite](../dimensions/page.md) sind „Einzelzugriff“ und „Einzelseitenbesuche“ identisch. Die Unterschiede treten auf, wenn Sie andere Dimensionen verwenden.

* **Einzelzugriff**: Zeigt die Anzahl der Besuche an, bei denen sich das angegebene Dimensionselement während des gesamten Besuchs nicht geändert hat. Sie ist kontextabhängig von der Dimension, die Sie in Ihrem Projekt verwenden.
* **Einzelseitenbesuch**: Zeigt die Anzahl der Besuche an, bei denen sich die Dimension „Seite“ während des gesamten Besuchs nicht geändert hat. Obwohl Sie eine andere Dimension in Ihrem Bericht verwenden, zählt dieser dennoch Besuche, die ein einziges eindeutiges Seitendimensionselement enthalten.

Betrachten Sie beispielsweise die folgenden zwei Trefferbesuche. Die Dimension in Ihrem Bericht ist [Website-Bereich](../dimensions/site-section.md).

* Ein Besucher ruft zwei Seiten auf, die sich jedoch beide im gleichen Website-Bereich befinden. Da der Website-Bereich während des Besuchs gleich blieb, zählt dies als Einzelzugriff. Er zählt nicht als Einzelseitenbesuch, da der Besuch mehr als ein eindeutiges Seitendimensionselement enthält.
* Ein Besucher ruft zwei Seiten in verschiedenen Website-Bereichen auf, aber beide Seiten haben zufällig den gleichen Namen. Der Besuch zählt nicht als Einzelzugriff, da es zwei einzigartige Website-Bereichswerte gab. Er zählt als Einzelseitenbesuch, da es ein einzelnes Element mit der Dimension &quot;Seite&quot;gab.
