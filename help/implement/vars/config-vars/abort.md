---
title: abort
description: Die Variable „abort“ ist ein boolescher Wert, der verhindert, dass ein Treffer an die Adobe-Datenerfassungs-Server gesendet wird.
exl-id: e4e25a89-272b-4444-b52b-c7fe2478ff30
source-git-commit: 3986084eaab81842b6ea0dbabc7bdb78e39f887a
workflow-type: tm+mt
source-wordcount: '193'
ht-degree: 79%

---

# abort

Die Variable `abort` ist ein boolescher Wert, der verhindern kann, dass der nächste Tracking-Aufruf an Adobe gesendet wird.

## Verwenden der abort-Variablen in der Datenerfassungs-Benutzeroberfläche in Adobe Experience Platform

In der Datenerfassungs-Benutzeroberfläche gibt es kein dediziertes Feld, um diese Variable zu verwenden. Verwenden Sie den Editor für benutzerdefinierten Code entsprechend der AppMeasurement-Syntax.

## AppMeasurement-Syntax und benutzerdefinierter Code-Editor in der Datenerfassungs-Benutzeroberfläche

Die `abort`-Variable ist ein boolescher Wert. Der Standardwert lautet `false`.

* Wenn auf `true` gesetzt, sendet der nächste Tracking-Aufruf ([`t()`](../functions/t-method.md) oder [`tl()`](../functions/tl-method.md)) keine Daten an Adobe.
* Wenn diese Variable auf `false` gesetzt oder nicht definiert ist, hat sie keine Auswirkung.

```js
s.abort = true;
```

>[!NOTE]
>
>Die `abort`-Variable wird nach jedem Tracking-Aufruf auf `false` zurückgesetzt. Wenn Sie nachfolgende Tracking-Aufrufe auf derselben Seite abbrechen müssen, setzen Sie `abort` erneut auf `true`.

## Beispiel

Die `abort`-Variable kann in der [`doPlugins()`](../functions/doplugins.md)-Funktion gesetzt werden. Dies ist die letzte Funktion, die ausgeführt wird, bevor eine Bildanforderung an Adobe gesendet wird.

```js
s.doPlugins = function(s) {
     s.campaign = s.Util.getQueryParam("cid");
     if ((!s.campaign) && (!s.events)) {
          s.abort = true;
     }
};
```

Damit können Sie die Logik zentralisieren, mit der Sie Aktivitäten ermitteln, die Sie nicht nachverfolgen möchten, z. B. einige benutzerspezifische Links oder externe Links in Display-Anzeigen.
