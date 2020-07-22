---
title: Browsertyp
description: Die Organisation, die den Browser erstellt hat.
translation-type: tm+mt
source-git-commit: d3f92d72207f027d35f81a4ccf70d01569c3557f
workflow-type: tm+mt
source-wordcount: '133'
ht-degree: 3%

---


# Browsertyp

Die Dimension &quot;Browsertyp&quot;Liste Organisationen, die den vom Besucher verwendeten Browser erstellt haben. Diese Dimension ist nützlich, wenn Sie sehen möchten, welche übergreifenden Browser von Besuchern verwendet werden. Es bietet einen Wert gegenüber der Dimension &quot;Browser&quot;insofern, als es keine verschiedenen Versionen desselben Browsers als separate Dimensionselemente Liste.

## Diese Dimension mit Daten füllen

Diese Dimension verweist auf eine interne Nachschlagetabelle von Adobe. Der Nachschlagewert basiert auf dem `User-Agent` HTTP-Header in Bildanforderungen. Wenn Sie eine AppMeasurement-Bibliothek verwenden (z. B. beim Starten der Adobe Experience Platform), funktioniert diese Dimension standardmäßig.

## Dimensionselemente

Dimensionselemente umfassen Organisationen, die Browser erstellen. Zu den gemeinsamen Dimensionselementen gehören `"Google"` (die Ersteller von [!DNL Chrome]), `"Apple"` (die Ersteller von [!DNL Safari]), `"Microsoft"` (die Ersteller von [!DNL Edge]) und `"Mozilla"` (die Ersteller von [!DNL Firefox]).
