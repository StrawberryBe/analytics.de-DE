---
description: Gibt den Wert eines angegebenen Abfragezeichenfolgen-Parameters zurück, wenn dieser in der aktuellen Seiten-URL oder in der angegebenen Zeichenfolge gefunden wird
keywords: Analytics Implementation
subtopic: JavaScript AppMeasurement
title: Util.getQueryParam
topic: Developer and implementation
uuid: 1fecd148-3e52-46f2-a73f-003563f7a62c
translation-type: tm+mt
source-git-commit: 99ee24efaa517e8da700c67818c111c4aa90dc02

---


# Util.getQueryParam

Gibt den Wert eines angegebenen Abfragezeichenfolgen-Parameters zurück, wenn dieser in der aktuellen Seiten-URL oder in der angegebenen Zeichenfolge gefunden wird

Da in der Abfragezeichenfolge einer Seite wichtige Daten enthalten sind (Kampagnen-Trackingcodes, interne Keywords usw.), können Sie mithilfe von „getQueryParam“ diese Daten in Analytics-Variablen erfassen.

Dieses Tool ersetzt das [getQueryParam](/help/implement/js-implementation/plugins/getqueryparam.md)-Plug-in.

**Syntax:**

```
s.Util.getQueryParam(key, [url], [delim])
```

> [!NOTE] Dieses Tool hat eine andere Syntax als das Plug-in.

**Parameter:**

| Parameter | Beschreibung |
|---|---|
| key | (erforderlich) Der Name des Abfragezeichenfolgen-Parameters, der abgerufen werden soll. Bei diesem Parameter wird die Groß-/Kleinschreibung beachtet. |
| url | (optional) Die Standard-URL lautet `s.pageURL` oder `window.location`. Wenn für diesen Parameter ein Wert angegeben ist, wird die URL, aus der der Abfrageparameter abgerufen wird, durch den angegebenen Wert ersetzt. |
| delim | (optional) Trennzeichen für Parameter in der URL. Das standardmäßige Trennzeichen lautet „&amp;“. Dieser Parameter ermöglicht Ihnen die Angabe eines alternativen Trennzeichens für Abfragezeichenfolgen (wie z. B. ein Semikolon). |

**Rückgabe:**

Die Funktion gibt die leere Zeichenfolge „“ aus, wenn kein Schlüssel angegeben wurde, keine URL-Optionen vorhanden sind oder wenn der Schlüssel nicht in der URL gefunden wurde. Wenn eine Fragment-Trennzeichen-Nr. in der URL gefunden wird, wird nicht alles berücksichtigt, was dem Fragment-Trennzeichen folgt. Wenn der Schlüssel vorhanden und einem Wert zugewiesen ist, wird der Wert URL decodiert und ausgegeben.

**Beispiel:**

```js
s.doPlugins = function(s) { 
  s.campaign = s.Util.getQueryParam("cid"); 
};
```

