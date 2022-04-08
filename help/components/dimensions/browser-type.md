---
title: Browser-Typ
description: Die Organisation, die den Browser erstellt hat.
feature: Dimensions
exl-id: 2a88ebc6-879e-4e5b-a8e5-40a32d54ac1b
source-git-commit: 35413ac43eed5ab7218794f26e4753acf08f18ee
workflow-type: ht
source-wordcount: '134'
ht-degree: 100%

---

# Browser-Typ

In der Dimension „Browser-Typ“ werden Organisationen aufgelistet, die den vom Besucher verwendeten Browser erstellt haben. Diese Dimension ist nützlich, wenn Sie sehen möchten, welche übergeordneten Browser von Besuchern verwendet werden. Sie ist insofern nützlicher als die Dimension „Browser“, als sie verschiedene Versionen desselben Browsers nicht als separate Dimensionselemente auflistet.

## Füllen dieser Dimension mit Daten

Diese Dimension verweist auf eine interne Tabelle von Adobe. Der Wert basiert auf der HTTP-Kopfzeile `User-Agent` in den Bildanforderungen. Wenn Sie eine AppMeasurement-Bibliothek verwenden (z. B. über Tags in Adobe Experience Platform), ist diese Dimension vorkonfiguriert.

## Dimensionselemente

Zu den Dimensionselementen gehören die Organisationen, die Browser erstellen. Zu den gängigen Dimensionselementen gehören `"Google"` (die Ersteller von [!DNL Chrome]), `"Apple"` (die Ersteller von [!DNL Safari]), `"Microsoft"` (die Ersteller von [!DNL Edge]) und `"Mozilla"` (die Ersteller von [!DNL Firefox]).
