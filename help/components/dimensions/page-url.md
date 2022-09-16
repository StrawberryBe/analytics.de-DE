---
title: Seiten-URL
description: Die URL der Seite.
feature: Dimensions
exl-id: 7c0ec494-d79b-4b65-9161-bdc48485af84
source-git-commit: 35413ac43eed5ab7218794f26e4753acf08f18ee
workflow-type: tm+mt
source-wordcount: '221'
ht-degree: 100%

---

# Seiten-URL

Die Dimension „Seiten-URL“ listet die URLs auf Ihrer Site auf.

>[!IMPORTANT]
>
>Diese Dimension ist nur in Data Warehouse verfügbar. Wenn Sie eine URL-Dimension in anderen Analytics-Lösungen verwenden möchten, kopieren Sie den Wert bei jedem Treffer in eine [eVar](evar.md).

## Füllen dieser Dimension mit Daten

Diese Dimension ruft Daten aus den Abfragezeichenfolgen](/help/implement/validate/query-parameters.md) [`g` und `-g` in [Seitenaufrufen (`t()`)](/help/implement/vars/functions/t-method.md) ab. [Linktracking-Aufrufe (`tl()`)](/help/implement/vars/functions/tl-method.md) entfernen diese Dimension immer, auch wenn die Abfragezeichenfolge `g` vorhanden ist.

Manchmal sind URLs länger als 255 Byte. AppMeasurement verwendet den Abfragezeichenfolgenparameter `g` für die ersten 255 Byte der URL in Bildanforderungen. Wenn eine URL länger als 255 Byte ist, wird der Rest der URL im Abfragezeichenfolgenparameter `-g` gespeichert. Protokoll- und Abfragezeichenfolgen in der URL sind in dieser Variablen enthalten.

AppMeasurement erfasst diese Daten automatisch anhand der URL der Seite. Sie können den erfassten Wert mithilfe der Variablen [`pageURL`](/help/implement/vars/page-vars/pageurl.md) überschreiben.

## Füllen einer eVar mit der URL

Adobe empfiehlt, eine eVar für die verkettete Zeichenfolge `window.location.hostname + window.location.pathname` festzulegen. Diese Zeichenfolge funktioniert in der Regel besser als `window.location.href`, da sie Protokoll-, Abfragezeichenfolgen und Verankerungs-Tags auslässt.

Wenn Sie möchten, dass die eVar genau der Dimension „Seiten-URL“ in Data Warehouse entspricht, können Sie [dynamische Variablen](/help/implement/vars/page-vars/dynamic-variables.md) verwenden und die eVar bei jedem Treffer auf `D=g` setzen.

## Dimensionselemente

Zu den Dimensionselementen gehören die URLs der Seiten auf Ihrer Site.
