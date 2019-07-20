---
description: Löscht die folgenden Werte aus dem Instanzobjekt. Diese Funktion entfernt die Elemente (legt sie als „undefiniert“ fest).
keywords: Analytics-Implementierung
seo-description: Löscht die folgenden Werte aus dem Instanzobjekt. Diese Funktion entfernt die Elemente (legt sie als „undefiniert“ fest).
seo-title: Die s.clearVars()-Funktion
solution: Analytics
title: Die s.clearVars()-Funktion
topic: Entwickler und Implementierung
uuid: 43 c 425 bc -15 ae -4892-a 5 a 5-e 1 defcb 25 ff 4
translation-type: tm+mt
source-git-commit: 86fe1b3650100a05e52fb2102134fee515c871b1

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
>`clearVars()` in [appmeasurement for javascript enthalten](../../implement/js-implementation/c-appmeasurement-js/appmeasure-mjs.md#concept_F3957D7093A94216BD79F35CFC1557E8) ist, aber nicht im H-Code und in früheren Versionen verfügbar ist.

