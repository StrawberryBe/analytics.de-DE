---
title: abbrechen
description: Die abort-Variable ist ein boolescher Wert, der verhindert, dass ein Treffer an Adobe-Datenerfassungsserver gesendet wird.
translation-type: tm+mt
source-git-commit: 468f97ee61f5d573d07475836df8d2c313b29fb3

---


# abbrechen

Die `abort` Variable ist ein boolescher Wert, der verhindern kann, dass der nächste Verfolgungsaufruf an Adobe gesendet wird.

## Verwenden der Variablen abort in Adobe Experience Platform Launch

Es gibt kein spezielles Feld in Launch, um diese Variable zu verwenden. Verwenden Sie den benutzerdefinierten Code-Editor entsprechend der AppMeasurement-Syntax.

## AppMeasurement-Syntax und benutzerdefinierter Code-Editor in Launch

Die `abort` Variable ist ein boolescher Wert. Its default value is `false`.

* Bei Festlegung auf `true`sendet der nächste Verfolgungsaufruf ([`t()`](../functions/t-method.md) oder [`tl()`](../functions/tl-method.md)) keine Daten an Adobe.
* Wenn diese Variable auf `false` oder nicht definiert ist, hat sie keine Auswirkung.

```js
s.abort = true;
```

> [!NOTE] Die `abort` Variable wird nach jedem Verfolgungsaufruf auf `false` zurückgesetzt. Wenn Sie nachfolgende Verfolgungsaufrufe auf derselben Seite abbrechen müssen, setzen Sie `abort` den Wert `true` erneut.

## Beispiel

Die `abort` Variable kann in der [`doPlugins()`](../functions/doplugins.md) Funktion eingestellt werden, die die letzte Funktion ist, die ausgeführt wird, bevor eine Bildanforderung an Adobe gesendet wird.

```js
s.doPlugins = function(s) {
     s.campaign = s.Util.getQueryParam("cid");
     if ((!s.campaign) && (!s.events)) {
          s.abort = true;
     }
};
```

Sie können die Logik zentralisieren, mit der Sie Aktivitäten identifizieren können, die Sie nicht verfolgen möchten, z. B. einige benutzerspezifische Links oder externe Links in Display-Anzeigen.
