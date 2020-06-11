---
title: Einzelzugriff
description: Die Häufigkeit, mit der sich ein Dimensionswert bei einem Besuch nicht änderte.
translation-type: tm+mt
source-git-commit: 52e00470df0f0c6bff84b26c1548e64ff5114fb8
workflow-type: tm+mt
source-wordcount: '339'
ht-degree: 0%

---


# Einzelzugriff

Die Metrik &quot;Einzelzugriff&quot;zeigt die Anzahl der Besuche an, bei denen der Dimensionswert nur einen einzigen eindeutigen Wert für den gesamten Besuch enthielt. Diese Metrik ist hilfreich im Kontext jeder Dimension, in der Sie sehen möchten, welche Dimensionswerte während eines Besuchs stagnieren.

## Berechnung dieser Metrik

Diese Metrik zählt Besuche, bei denen der Dimensionswert einen einzigen eindeutigen Wert enthielt. Sie können den Dimensionswert mehrmals festlegen oder beibehalten und dennoch als Einzelzugriff zählen. Sobald sich ein Dimensionswert in einen zweiten eindeutigen Wert ändert, gilt der Besuch nicht mehr als Einzelzugriff.

## Unterschied zwischen &quot;Einzelzugriff&quot;und &quot;Einzelseitenbesuch&quot;

Im Kontext der [Seitendimension](../dimensions/page.md) sind &quot;Einzelzugriff&quot;und &quot;Einzelseitenbesuche&quot;exakt identisch. Ihre Unterschiede treten auf, wenn Sie andere Dimensionen verwenden.

* **Einzelzugriff**: Zeigt die Anzahl der Besuche an, bei denen sich der angegebene Dimensionswert während des gesamten Besuchs nicht geändert hat. Es ist kontextuell mit der Dimension, die Sie in Ihrem Projekt verwenden.
* **Einzelseitenbesuch**: Zeigt die Anzahl der Besuche an, bei denen sich die Dimension &quot;Seite&quot;während des gesamten Besuchs nicht geändert hat. Obwohl Sie eine andere Dimension in Ihrem Bericht verwenden, zählt dieser dennoch Besuche, die einen einzigen eindeutigen Seitendimensionswert enthalten.

Betrachten Sie zum Beispiel das folgende Beispiel zwei Trefferbesuche. Die Dimension in Ihrem Bericht ist der [Site-Abschnitt](../dimensions/site-section.md).

* Ein Besucher ruft zwei Seiten auf, die sich jedoch beide im gleichen Sitebereich befinden. Da der Site-Abschnitt während des Besuchs gleich blieb, zählt er als Einzelzugriff. Er zählt nicht als Einzelseitenbesuch, da der Besuch mehr als einen eindeutigen Seitendimensionswert enthält.
* Ein Besucher ruft zwei Seiten in verschiedenen Site-Abschnitten auf, aber beide Seiten werden zufällig denselben Namen erhalten. Der Besuch zählt nicht als Einzelzugriff, da es zwei einzigartige Site-Abschnittswerte gab. Er zählt als Einzelseitenbesuch, da ein einzelner eindeutiger Seitendimensionswert vorhanden war.
