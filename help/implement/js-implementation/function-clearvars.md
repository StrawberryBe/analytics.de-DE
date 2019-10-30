---
description: Löscht die folgenden Werte aus dem Instanzobjekt. Diese Funktion entfernt die Elemente (legt sie als „undefiniert“ fest).
keywords: Analytics-Implementierung
seo-description: Löscht die folgenden Werte aus dem Instanzobjekt. Diese Funktion entfernt die Elemente (legt sie als „undefiniert“ fest).
seo-title: Die s.clearVars()-Funktion
solution: Analytics
title: Die s.clearVars()-Funktion
topic: Entwickler und Implementierung
uuid: 43c425bc-15ae-4892-a5a5-e1defcb25ff4
translation-type: tm+mt
source-git-commit: a2c38c2cf3a2c1451e2c60e003ebe1fa9bfd145d

---


# Die s.clearVars()-Funktion

Löscht die folgenden Werte aus dem Instanzobjekt. Diese Funktion entfernt die Elemente (legt sie als „undefiniert“ fest).

* `props`
* `eVars`
* `hier`
* `list`
* `events`
* `eventList`
* `products`
* `productsList`
* `channel`
* `purchaseID`
* `transactionID`
* `state`
* `zip`
* `campaign`

Beispiel:

```js
s.clearVars()
```

> [!NOTE] `clearVars()` ist enthalten in [AppMeasurement für JavaScript](../../implement/js-implementation/c-appmeasurement-js/appmeasure-mjs.md#concept_F3957D7093A94216BD79F35CFC1557E8), ist aber nicht in H-Code und früheren Versionen verfügbar.

