---
description: AppMeasurement für JavaScript ist eine neue Bibliothek, die über die gleichen Kernfunktionen wie s_code.js verfügt, jedoch für den Einsatz auf Websites für Desktop- und Mobilgeräte gleichermaßen konzipiert und somit leichter und schneller ist.
keywords: appmeasurement; Analytics-Implementierung; javascript; Appmeasurement for javascript; initialisierung; Appmeasurement-Instanz abrufen; clear vars; clearvars; Appmeasurement utilities; appmeasurement-Instanz; Vorteile von appmeasurement
seo-description: AppMeasurement für JavaScript ist eine neue Bibliothek, die über die gleichen Kernfunktionen wie s_code.js verfügt, jedoch für den Einsatz auf Websites für Desktop- und Mobilgeräte gleichermaßen konzipiert und somit leichter und schneller ist.
seo-title: Info zu AppMeasurement für JavaScript
solution: Analytics
subtopic: JavaScript AppMeasurement
title: Info zu AppMeasurement für JavaScript
topic: Entwickler und Implementierung
uuid: dc 71 ad 7 a -92 bd -40 cd -8 fab -707 f 6 f 8472 e 2
translation-type: tm+mt
source-git-commit: 76d0ce11d9b560e0df866be9e753804b6fa4bb3d

---


# Info zu AppMeasurement für JavaScript

[!DNL AppMeasurement] für JavaScript ist eine neue Bibliothek, die über die gleichen Kernfunktionen wie s_code.js verfügt, jedoch für den Einsatz auf Websites für mobile und Desktopgeräte leichter und schneller ist.

## Was Sie vor dem Migrieren wissen sollten {#section_B8E7B39E8469468883BA0B41234F21C4}

The following list contains changes you need to understand before switching to this new [!DNL AppMeasurement] version:

* Einige Plug-ins werden nicht mehr unterstützt. See [AppMeasurement Plug-in Support](../../../implement/js-implementation/c-appmeasurement-js/plugins-support.md#concept_E31A189BC8A547738666EB5E00D2252A).
* The library does not support dynamic account selection ([dynamicAccountList](/help/implement/js-implementation/c-variables/configuration-variables.md), [dynamicAccountMatch](/help/implement/js-implementation/c-variables/configuration-variables.md), and [dynamicAccountSelection](/help/implement/js-implementation/c-variables/configuration-variables.md)).

* The library and page code can be deployed inside the `<head>` tag.
* The Media and Integrate modules are supported using updated module code that is in the JavaScript [!DNL AppMeasurement] download package. Das Survey-Modul wird nicht unterstützt.
* Bereits vorhandener Seiten-Code ist mit der neuen Version kompatibel.
* Die Bibliothek enthält native Hilfsprogramme zum Abrufen von Abfrageparametern, zum Lesen und Schreiben von Cookies und zum Durchführen der erweiterten Linktracking.

## Häufig gestellte Fragen {#section_9BD41B08F7B54197B230937714B9357A}

See the [FAQ](../../../implement/faq.md#concept_9BBC230E01114318BE9C08724F2040D3) for information about performance, video tracking, mobile, and more.

## Initialisierungsprozess {#section_F6D5680F6D134B6AB1F01C6235860635}

Call `s_gi()`, passing the report suite ID to initialize an [!DNL AppMeasurement] instance:

```js
var s_account="INSERT-RSID-HERE"
var s=s_gi(s_account)
```

When `s_gi` is called, if an [!DNL AppMeasurement] instance does not exist for the specified `s_account`, a new instance is created. Ansonsten wird die vorhandene Instanz zurückgegeben. So wird verhindert, dass mehrere Objekte für dasselbe Konto erstellt werden.

## Eine AppMeasurement-Instanz abrufen {#section_6F05C96DCAB24C8C9B4B91C5739630A6}

Throughout your code, call the global [s_gi() function](../../../implement/js-implementation/function-s-gi.md#concept_50EE6629F61A478BB67781408FBA04BD) to retrieve an existing [!DNL AppMeasurement] instance.

## Hilfsprogramme {#section_0F47694DD0214645A24C94AB6A4142A0}

JavaScript [!DNL AppMeasurement] provides the following built-in utilities:

* [Util.cookieRead](../../../implement/js-implementation/util-cookieread.md#concept_33BD774A90504F2C8094DDC16D47440D)
* [Util.cookieWrite](../../../implement/js-implementation/util-cookiewrite.md#concept_9BE4F7D9CDAE4445B9AF3212BC7E61F2)
* [Util.getQueryParam](../../../implement/js-implementation/util-getqueryparam.md#concept_763AD2621BB44A3990204BE72D3C9FA5)

## ClearVars {#section_597C411E7EDB42BC9A6A0508C9D57147}

Es gibt eine neue `clearVars`-Methode zum Löschen der folgenden Werte in einem Instanzobjekt:

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

## Vorteile {#section_091E5A28E89E438E8A54A95F55165743}

* Ist 3- bis 7-mal schneller als H.25-Code
* Dekomprimiert nur 21.000 und komprimiert im GZIP-Format nur 8.000 (H.25-Code dekomprimiert 33.000 und komprimiert im GZIP-Format 13.000).
* Nativer Support für verschiedene allgemeine Plug-ins ().
* Handlich und schnell genug zur Verwendung bei Websites für Mobilgeräte, stabil genug für die Verwendung bei vollwertigem Web für Desktops, ermöglicht Ihnen die Nutzung einer einzigen Bibliothek für alle Webumgebungen.

