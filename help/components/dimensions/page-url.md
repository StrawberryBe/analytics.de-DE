---
title: Seiten-URL
description: Die URL der Seite.
translation-type: tm+mt
source-git-commit: ec6d8e6a3cef3a5fd38d91775c83ab95de47fd55
workflow-type: tm+mt
source-wordcount: '221'
ht-degree: 69%

---


# Seiten-URL

Die Dimension „Seiten-URL“ listet die URLs auf Ihrer Site auf.

>[!IMPORTANT]
>
>Diese Dimension ist nur in Data Warehouse verfügbar. Wenn Sie eine URL-Dimension in anderen Analytics-Lösungen verwenden möchten, kopieren Sie den Wert bei jedem Treffer in ein [eVar](evar.md).

## Füllen dieser Dimension mit Daten

Diese Dimension ruft Daten aus den Abfrage-Zeichenfolgen [`g` und `-g` unter [Seitenaufrufen (`t()`)](/help/implement/vars/functions/t-method.md) ab. ](/help/implement/validate/query-parameters.md) [Linktracking-Aufrufe (`tl()`)](/help/implement/vars/functions/tl-method.md) entfernen diese Dimension, auch wenn die  `g` Abfrage-Zeichenfolge vorhanden ist.

Manchmal sind URLs länger als 255 Byte. AppMeasurement verwendet den Abfragezeichenfolgenparameter `g` für die ersten 255 Byte der URL in Bildanforderungen. Wenn eine URL länger als 255 Byte ist, wird der Rest der URL im Abfragezeichenfolgenparameter `-g` gespeichert. Protokoll- und Abfragezeichenfolgen in der URL sind in dieser Variablen enthalten.

AppMeasurement erfasst diese Daten automatisch anhand der URL der Seite. Sie können den erfassten Wert mit der Variablen [`pageURL`](/help/implement/vars/page-vars/pageurl.md) überschreiben.

## Füllen einer eVar mit der URL

Adobe empfiehlt, eine eVar für die verkettete Zeichenfolge `window.location.hostname + window.location.pathname` festzulegen. Diese Zeichenfolge funktioniert in der Regel besser als `window.location.href`, da sie Protokoll-, Abfragezeichenfolgen und Verankerungs-Tags auslässt.

Wenn Sie möchten, dass die eVar genau der Dimension „Seiten-URL“ in Data Warehouse entspricht, können Sie [dynamische Variablen](/help/implement/vars/page-vars/dynamic-variables.md) verwenden und die eVar bei jedem Treffer auf `D=g` setzen.

## Dimensionselemente

Zu den Dimensionselementen gehören die URLs der Seiten auf Ihrer Site.
