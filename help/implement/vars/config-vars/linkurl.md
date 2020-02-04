---
title: linkURL
description: Überschreibt die automatisch generierte Link-URL, die AppMeasurement bei Linkverfolgungsaufrufen verwendet.
translation-type: tm+mt
source-git-commit: 4a6cfa479559a644588613bd127c5b45ee8787e6

---


# linkURL

Sobald ein Link-Verfolgungsaufruf an Adobe gesendet wird, erkennen die Datenerfassungsserver automatisch die URL. Verwenden Sie die `linkURL` Variable, um die erkannte URL zu überschreiben.

## Link-URL beim Starten der Adobe Experience Platform

Es gibt kein spezielles Feld in Launch, um diese Variable zu verwenden. Verwenden Sie den benutzerdefinierten Code-Editor entsprechend der AppMeasurement-Syntax.

## s.linkURL in AppMeasurement und benutzerdefinierten Code-Editor starten

Die `s.linkURL` Variable ist eine Zeichenfolge, die die URL des Browsers enthält, wenn auf den Link geklickt wurde. Diese Variable füllt keine in Berichten verfügbaren Dimensionen.

```js
s.linkURL = "https://example.com";
```

Wenn die `linkName` Variable nicht für einen Linkverfolgungsaufruf festgelegt ist, wird stattdessen die `linkURL` Variable verwendet.
