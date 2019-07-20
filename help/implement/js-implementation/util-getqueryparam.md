---
description: Gibt den Wert eines angegebenen Abfragezeichenfolgen-Parameters zurück, wenn dieser in der aktuellen Seiten-URL oder in der angegebenen Zeichenfolge gefunden wird
keywords: Analytics-Implementierung
seo-description: Gibt den Wert eines angegebenen Abfragezeichenfolgen-Parameters zurück, wenn dieser in der aktuellen Seiten-URL oder in der angegebenen Zeichenfolge gefunden wird
seo-title: Util.getQueryParam
solution: Analytics
subtopic: JavaScript AppMeasurement
title: Util.getQueryParam
topic: Entwickler und Implementierung
uuid: 1 fecd 148-3 e 52-46 f 2-a 73 f -003563 f 7 a 62 c
translation-type: tm+mt
source-git-commit: ee0cb9b64a3915786f8f77d80b55004daa68cab6

---


# Util.getQueryParam

Gibt den Wert eines angegebenen Abfragezeichenfolgen-Parameters zurück, wenn dieser in der aktuellen Seiten-URL oder in der angegebenen Zeichenfolge gefunden wird

Da in der Abfragezeichenfolge einer Seite wichtige Daten enthalten sind (Kampagnen-Trackingcodes, interne Keywords usw.), können Sie mithilfe von   „getQueryParam“ diese Daten in Analytics-Variablen erfassen.

Dieses Tool ersetzt das [getQueryParam](../../implement/js-implementation/plugins/getqueryparam.md#concept_E3D0FEC81E1F4987B39CC467F19FFCFF)-Plug-in.

**Syntax:**

```
s.Util.getQueryParam(key, [url], [delim])
```

>[!NOTE]
>
>Die Syntax für das Dienstprogramm unterscheidet sich von der Syntax für das Plug-in.

**Parameter:**

| Parameter | Beschreibung |
|---|---|
| key | (erforderlich) Der Name des Abfragezeichenfolgen-Parameters, der abgerufen werden soll. Bei diesem Parameter wird die Groß-/Kleinschreibung beachtet. |
| url | (optional) Default url is `s.pageURL` or `window.location`. Wenn für diesen Parameter ein Wert angegeben ist, wird die URL, aus der der Abfrageparameter abgerufen wird, durch den angegebenen Wert ersetzt. |
| delim | (optional) Trennzeichen für Parameter in der URL. Das standardmäßige Trennzeichen lautet „&amp;“. Dieser Parameter ermöglicht Ihnen die Angabe eines alternativen Trennzeichens für Abfragezeichenfolgen (wie z. B. ein Semikolon). |

**Rückgabe:**

Die Funktion gibt eine leere Zeichenfolge zurück, wenn kein Schlüssel angegeben ist oder keine der URL-Optionen vorhanden ist oder wenn der Schlüssel nicht in der URL gefunden wird. Wenn ein Fragment-Trennzeichen in der URL gefunden wird, wird alles, was dem Fragmenttrennzeichen folgt, nicht berücksichtigt. Wenn der Schlüssel vorhanden ist und einem Wert zugewiesen wird, wird der Wert URL dekodiert und zurückgegeben.

**Beispiel:**

```js
s.doPlugins = function(s) { 
  s.campaign = s.Util.getQueryParam("cid"); 
};
```

