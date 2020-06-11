---
title: Browsertyp
description: Die Organisation, die den Browser erstellt hat.
translation-type: tm+mt
source-git-commit: 4a7b3a00bdbf557c219de530e3e692c2b2db4a84
workflow-type: tm+mt
source-wordcount: '133'
ht-degree: 3%

---


# Browsertyp

Die Dimension &quot;Browsertyp&quot;Liste Organisationen, die den vom Besucher verwendeten Browser erstellt haben. Diese Dimension ist nützlich, wenn Sie sehen möchten, welche übergreifenden Browser von Besuchern verwendet werden. Es bietet einen Wert über der Dimension &quot;Browser&quot;insofern, als es keine verschiedenen Versionen desselben Browsers als separate Dimensionswerte Liste.

## Diese Dimension mit Daten füllen

Diese Dimension verweist auf eine interne Nachschlagetabelle von Adobe. Der Nachschlagewert basiert auf dem `User-Agent` HTTP-Header in Bildanforderungen. Wenn Sie eine AppMeasurement-Bibliothek verwenden (z. B. über Adobe Experience Platform Launch), funktioniert diese Dimension standardmäßig.

## Dimensionswerte

Zu den Dimensionswerten gehören Organisationen, die Browser erstellen. Zu den gemeinsamen Dimensionswerten gehören `"Google"` (die Ersteller von [!DNL Chrome]), `"Apple"` (die Ersteller von [!DNL Safari]), `"Microsoft"` (die Ersteller von [!DNL Edge]) und `"Mozilla"` (die Ersteller von [!DNL Firefox]).
