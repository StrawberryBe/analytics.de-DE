---
title: „Seiten-URL“
description: Die URL der Seite.
translation-type: tm+mt
source-git-commit: c4833525816d81175a3446215eb92310ee4021dd
workflow-type: tm+mt
source-wordcount: '154'
ht-degree: 2%

---


# „Seiten-URL“

Die Dimension &quot;Seiten-URL&quot;Liste die URLs auf Ihrer Site.

>[!IMPORTANT]
>
>Diese Dimension ist nur in Data warehouse verfügbar. Wenn Sie eine URL-Dimension in anderen Analytics-Lösungen verwenden möchten, verwenden Sie eine [eVar](evar.md).

## Diese Dimension mit Daten füllen

Diese Dimension ruft Daten aus der [`g` Abfrage-Zeichenfolge](/help/implement/validate/query-parameters.md) in Bildanforderungen ab. AppMeasurement erfasst diese Daten mit der [`pageURL`](/help/implement/vars/page-vars/pageurl.md) Variablen.

## Eine eVar mit URL füllen

Adobe empfiehlt, eine eVar auf die verkettete Zeichenfolge festzulegen `window.location.hostname + window.location.pathname`. Diese Zeichenfolge funktioniert in der Regel besser als `window.location.href` , da Protokoll-, Abfragen- und Anker-Tags fehlen.

Wenn die eVar exakt mit der Dimension &quot;Seiten-URL&quot;in Data warehouse übereinstimmen soll, können Sie [dynamische Variablen](/help/implement/vars/page-vars/dynamic-variables.md) verwenden und die eVar bei jedem Treffer `D=g` auf setzen. Beachten Sie, dass diese Methode bei benutzerdefinierten Link-Treffern nicht funktioniert, da die Seiten-URL bei allen [`tl()`](/help/implement/vars/functions/tl-method.md) Aufrufen entfernt wird.

## Dimensionswerte

Dimensionswerte umfassen die URLs der Seiten auf Ihrer Site.
