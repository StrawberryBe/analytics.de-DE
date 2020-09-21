---
title: Browser-Typ
description: Die Organisation, die den Browser erstellt hat.
translation-type: ht
source-git-commit: d3f92d72207f027d35f81a4ccf70d01569c3557f
workflow-type: ht
source-wordcount: '133'
ht-degree: 100%

---


# Browser-Typ

In der Dimension „Browser-Typ“ werden Organisationen aufgelistet, die den vom Besucher verwendeten Browser erstellt haben. Diese Dimension ist nützlich, wenn Sie sehen möchten, welche übergeordneten Browser von Besuchern verwendet werden. Sie ist insofern nützlicher als die Dimension „Browser“, als sie verschiedene Versionen desselben Browsers nicht als separate Dimensionselemente auflistet.

## Füllen dieser Dimension mit Daten

Diese Dimension verweist auf eine interne Tabelle von Adobe. Der Wert basiert auf der HTTP-Kopfzeile `User-Agent` in den Bildanforderungen. Wenn Sie eine AppMeasurement-Bibliothek verwenden (z. B. über Adobe Experience Platform Launch), ist diese Dimension vorkonfiguriert.

## Dimensionselemente

Zu den Dimensionselementen gehören die Organisationen, die Browser erstellen. Zu den gängigen Dimensionselementen gehören `"Google"` (die Ersteller von [!DNL Chrome]), `"Apple"` (die Ersteller von [!DNL Safari]), `"Microsoft"` (die Ersteller von [!DNL Edge]) und `"Mozilla"` (die Ersteller von [!DNL Firefox]).
