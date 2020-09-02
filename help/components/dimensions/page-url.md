---
title: Seiten-URL
description: Die URL der Seite.
translation-type: tm+mt
source-git-commit: ec6d8e6a3cef3a5fd38d91775c83ab95de47fd55
workflow-type: tm+mt
source-wordcount: '221'
ht-degree: 64%

---


# Seiten-URL

Die Dimension „Seiten-URL“ listet die URLs auf Ihrer Site auf.

>[!IMPORTANT]
>
>Diese Dimension ist nur in Data Warehouse verfügbar. Wenn Sie eine URL-Dimension in anderen Analytics-Lösungen verwenden möchten, kopieren Sie den Wert bei jedem Treffer in eine [eVar](evar.md) .

## Füllen dieser Dimension mit Daten

This dimension retrieves data from the [`g` and `-g` query strings](/help/implement/validate/query-parameters.md) in [Page view calls (`t()`)](/help/implement/vars/functions/t-method.md). [Linktracking-Aufrufe (`tl()`)](/help/implement/vars/functions/tl-method.md) entfernen diese Dimension immer, auch wenn die `g` Abfrage-Zeichenfolge vorhanden ist.

Manchmal sind URLs länger als 255 Byte. AppMeasurement verwendet den Abfragezeichenfolgenparameter `g` für die ersten 255 Byte der URL in Bildanforderungen. Wenn eine URL länger als 255 Byte ist, wird der Rest der URL im Abfragezeichenfolgenparameter `-g` gespeichert. Protokoll- und Abfragezeichenfolgen in der URL sind in dieser Variablen enthalten.

AppMeasurement erfasst diese Daten automatisch anhand der URL der Seite. Sie können den erfassten Wert mit der [`pageURL`](/help/implement/vars/page-vars/pageurl.md) Variablen überschreiben.

## Füllen einer eVar mit der URL

Adobe empfiehlt, eine eVar für die verkettete Zeichenfolge `window.location.hostname + window.location.pathname` festzulegen. Diese Zeichenfolge funktioniert in der Regel besser als `window.location.href`, da sie Protokoll-, Abfragezeichenfolgen und Verankerungs-Tags auslässt.

Wenn Sie möchten, dass die eVar genau der Dimension „Seiten-URL“ in Data Warehouse entspricht, können Sie [dynamische Variablen](/help/implement/vars/page-vars/dynamic-variables.md) verwenden und die eVar bei jedem Treffer auf `D=g` setzen.

## Dimensionen

Dimensionen beinhalten die URLs der Seiten auf Ihrer Site.
