---
title: linkURL
description: Überschreibt die automatisch generierte Link-URL, die AppMeasurement bei Linktracking-Aufrufen verwendet.
exl-id: 15d6e423-d9fc-4f84-ad39-0bd91399cde4
source-git-commit: 1a49c2a6d90fc670bd0646d6d40738a87b74b8eb
workflow-type: ht
source-wordcount: '118'
ht-degree: 100%

---

# linkURL

Sobald ein Linktracking-Aufruf an Adobe gesendet wird, erkennen die Datenerfassungs-Server automatisch die URL. Verwenden Sie die `linkURL`-Variable, um die erkannte URL zu überschreiben.

## Link-URL bei Verwendung von Tags in Adobe Experience Platform

In der Datenerfassungs-Benutzeroberfläche gibt es kein eigenes Feld, um diese Variable zu verwenden. Verwenden Sie den Editor für benutzerdefinierten Code entsprechend der AppMeasurement-Syntax.

## s.linkURL in AppMeasurement und im benutzerdefinierten Code-Editor

Die `s.linkURL`-Variable ist eine Zeichenfolge, die die URL des Browsers enthält, wenn auf den Link geklickt wurde. Diese Variable füllt keine in Berichten verfügbaren Dimensionen.

```js
s.linkURL = "https://example.com";
```

Wenn das dritte Argument der Methode [tl()](../functions/tl-method.md) nicht angegeben wird, wird stattdessen die Variable `linkURL` verwendet.
