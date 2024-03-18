---
title: linkURL
description: Überschreibt die automatisch generierte Link-URL, die AppMeasurement bei Linktracking-Aufrufen verwendet.
feature: Variables
exl-id: 15d6e423-d9fc-4f84-ad39-0bd91399cde4
role: Admin, Developer
source-git-commit: 12347957a7a51dc1f8dfb46d489b59a450c2745a
workflow-type: tm+mt
source-wordcount: '139'
ht-degree: 74%

---

# linkURL

Sobald ein Linktracking-Aufruf an Adobe gesendet wird, erkennen die Datenerfassungs-Server automatisch die URL. Verwenden Sie die `linkURL`-Variable, um die erkannte URL zu überschreiben.

## Link-URL mit dem Web SDK

Die Link-URL ist den folgenden Variablen zugeordnet:

* [XDM-Objekt](/help/implement/aep-edge/xdm-var-mapping.md): `web.webInteraction.URL`
* [Datenobjekt](/help/implement/aep-edge/data-var-mapping.md): `data.__adobe.analytics.linkURL` oder `data.__adobe.analytics.pev1`

## Link-URL mit der Adobe Analytics-Erweiterung

In der Adobe Analytics-Erweiterung gibt es kein eigenes Feld, um diese Variable zu verwenden. Verwenden Sie den Editor für benutzerdefinierten Code entsprechend der AppMeasurement-Syntax.

## s.linkURL in AppMeasurement und im benutzerdefinierten Code-Editor der Analytics-Erweiterung

Die `s.linkURL`-Variable ist eine Zeichenfolge, die die URL des Browsers enthält, wenn auf den Link geklickt wurde. Diese Variable füllt keine in Berichten verfügbaren Dimensionen.

```js
s.linkURL = "https://example.com";
```

Wenn das dritte Argument der Methode [tl()](../functions/tl-method.md) nicht angegeben wird, wird stattdessen die Variable `linkURL` verwendet.
