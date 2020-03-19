---
title: linkURL
description: Überschreibt die automatisch generierte Link-URL, die AppMeasurement bei Linkverfolgungsaufrufen verwendet.
translation-type: tm+mt
source-git-commit: 468f97ee61f5d573d07475836df8d2c313b29fb3

---


# linkURL

Wenn ein Link-Verfolgungsaufruf an Adobe gesendet wird, erkennen die Datenerfassungsserver automatisch die URL. Verwenden Sie die `linkURL` Variable, um die erkannte URL zu überschreiben.

## Link-URL beim Starten der Adobe Experience Platform

Es gibt kein spezielles Feld in Launch, um diese Variable zu verwenden. Verwenden Sie den benutzerdefinierten Code-Editor entsprechend der AppMeasurement-Syntax.

## s.linkURL in AppMeasurement und benutzerdefinierter Code-Editor starten

Die `s.linkURL` Variable ist eine Zeichenfolge, die die URL des Browsers enthält, wenn auf den Link geklickt wurde. Diese Variable füllt keine in Berichte verfügbaren Dimensionen.

```js
s.linkURL = "https://example.com";
```

Wenn die [`linkName`](linkname.md) Variable nicht für einen Linkverfolgungsaufruf festgelegt ist, wird stattdessen die `linkURL` Variable verwendet.
