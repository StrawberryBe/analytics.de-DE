---
title: linkURL
description: Überschreibt die automatisch generierte Link-URL, die AppMeasurement bei Linktracking-Aufrufen verwendet.
translation-type: tm+mt
source-git-commit: 468f97ee61f5d573d07475836df8d2c313b29fb3

---


# linkURL

Sobald ein Linktracking-Aufruf an Adobe gesendet wird, erkennen die Datenerfassungs-Server automatisch die URL. Verwenden Sie die `linkURL`-Variable, um die erkannte URL zu überschreiben.

## Link-URL in Adobe Experience Platform Launch

Es gibt kein spezielles Feld in Launch, um diese Variable zu verwenden. Verwenden Sie den Editor für benutzerdefinierten Code entsprechend der AppMeasurement-Syntax.

## s.linkURL in AppMeasurement und im benutzerdefinierten Code-Editor in Launch

Die `s.linkURL`-Variable ist eine Zeichenfolge, die die URL des Browsers enthält, wenn auf den Link geklickt wurde. Diese Variable füllt keine in Berichten verfügbaren Dimensionen.

```js
s.linkURL = "https://example.com";
```

Wenn die [`linkName`](linkname.md)-Variable nicht für einen Linktracking-Aufruf festgelegt ist, wird stattdessen die `linkURL`-Variable verwendet.
