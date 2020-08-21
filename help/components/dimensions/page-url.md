---
title: Seiten-URL
description: Die URL der Seite.
translation-type: tm+mt
source-git-commit: d3f92d72207f027d35f81a4ccf70d01569c3557f
workflow-type: tm+mt
source-wordcount: '154'
ht-degree: 92%

---


# Seiten-URL

Die Dimension „Seiten-URL“ listet die URLs auf Ihrer Site auf.

>[!IMPORTANT]
>
>Diese Dimension ist nur in Data Warehouse verfügbar. Wenn Sie eine URL-Dimension in anderen Analytics-Lösungen verwenden möchten, verwenden Sie eine [eVar](evar.md).

## Füllen dieser Dimension mit Daten

Diese Dimension ruft Daten aus der [`g` Abfragezeichenfolge](/help/implement/validate/query-parameters.md) in Bildanforderungen ab. AppMeasurement erfasst diese Daten mit der [`pageURL`](/help/implement/vars/page-vars/pageurl.md)-Variable.

## Füllen einer eVar mit der URL

Adobe empfiehlt, eine eVar für die verkettete Zeichenfolge `window.location.hostname + window.location.pathname` festzulegen. Diese Zeichenfolge funktioniert in der Regel besser als `window.location.href`, da sie Protokoll-, Abfragezeichenfolgen und Verankerungs-Tags auslässt.

Wenn Sie möchten, dass die eVar genau der Dimension „Seiten-URL“ in Data Warehouse entspricht, können Sie [dynamische Variablen](/help/implement/vars/page-vars/dynamic-variables.md) verwenden und die eVar bei jedem Treffer auf `D=g` setzen. Beachten Sie, dass diese Methode bei benutzerspezifischen Link-Treffern nicht funktioniert, da die Seiten-URL bei allen [`tl()`](/help/implement/vars/functions/tl-method.md)-Aufrufen entfernt wird.

## Dimensionen

Dimensionen beinhalten die URLs der Seiten auf Ihrer Site.
