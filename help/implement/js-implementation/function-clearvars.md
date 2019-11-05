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
source-git-commit: 2fc1a01aced4cf2b165b46353418fbee9b83bee5

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

>[!NOTE]
>
>`clearVars()` ist enthalten in [AppMeasurement für JavaScript](/help/implement/js-implementation/c-appmeasurement-js/appmeasure-mjs.md), ist aber nicht in H-Code und früheren Versionen verfügbar.

