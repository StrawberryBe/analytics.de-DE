---
description: AppMeasurement für JavaScript ist eine neue Bibliothek, die über die gleichen Kernfunktionen wie s_code.js verfügt, jedoch für den Einsatz auf Websites für Desktop- und Mobilgeräte gleichermaßen konzipiert und somit leichter und schneller ist.
keywords: appmeasurement;Analytics Implementation;javascript;appmeasurement for javascript;initialization;retrieve appmeasurement instance;clear vars;clearvars;appmeasurement utilities;appmeasurement instance;appmeasurement benefits
subtopic: JavaScript AppMeasurement
title: Info zu AppMeasurement für JavaScript
topic: Developer and implementation
uuid: dc71ad7a-92bd-40cd-8fab-707f6f8472e2
translation-type: tm+mt
source-git-commit: 99ee24efaa517e8da700c67818c111c4aa90dc02

---


# Info zu AppMeasurement für JavaScript

[!DNL AppMeasurement] für JavaScript ist eine neue Bibliothek, die über die gleichen Kernfunktionen wie s_code.js verfügt, jedoch für den Einsatz auf Websites für mobile und Desktopgeräte leichter und schneller ist.

## Was Sie vor dem Migrieren wissen sollten {#section_B8E7B39E8469468883BA0B41234F21C4}

In der folgenden Liste sind Änderungen aufgeführt, von denen Sie wissen sollten, bevor Sie auf diese neue [!DNL AppMeasurement]-Version umsteigen:

* Einige Plug-ins werden nicht mehr unterstützt. Siehe [AppMeasurement-Plug-in-Unterstützung](/help/implement/js-implementation/c-appmeasurement-js/plugins-support.md).
* Die Bibliothek unterstützt keine dynamische Kontoauswahl ([dynamicAccountList](/help/implement/js-implementation/c-variables/configuration-variables.md), [dynamicAccountMatch](/help/implement/js-implementation/c-variables/configuration-variables.md) und [dynamicAccountSelection](/help/implement/js-implementation/c-variables/configuration-variables.md)).

* Der Bibliotheks- und Seiten-Code kann innerhalb des `<head>`-Tags bereitgestellt werden.
* Das Media- und das Integrate-Modul werden mithilfe des aktualisierten Modulcodes unterstützt, der sich im JavaScript [!DNL AppMeasurement]-Downloadpaket befindet. Das Survey-Modul wird nicht unterstützt.
* Bereits vorhandener Seiten-Code ist mit der neuen Version kompatibel.
* Die Bibliothek enthält native Hilfsprogramme zum Abrufen von Abfrageparametern, zum Lesen und Schreiben von Cookies und zum Durchführen der erweiterten Linktracking.

## Häufig gestellte Fragen {#section_9BD41B08F7B54197B230937714B9357A}

Siehe [häufig gestellte Fragen](/help/implement/faq.md) zu Leistung, Videoverfolgung, Mobile und mehr.

## Initialisierungsprozess {#section_F6D5680F6D134B6AB1F01C6235860635}

Rufen Sie `s_gi()` auf und geben Sie so die Report Suite-ID weiter, um eine [!DNL AppMeasurement]-Instanz zu initialisieren:

```js
var s_account="INSERT-RSID-HERE"
var s=s_gi(s_account)
```

Wenn `s_gi` aufgerufen wird und keine [!DNL AppMeasurement]-Instanz für das angegebene `s_account` vorhanden ist, wird eine neue Instanz erstellt. Ansonsten wird die vorhandene Instanz zurückgegeben. So wird verhindert, dass mehrere Objekte für dasselbe Konto erstellt werden.

## Eine AppMeasurement-Instanz abrufen {#section_6F05C96DCAB24C8C9B4B91C5739630A6}

Rufen Sie im gesamten Code die globale Funktion [s_gi()](/help/implement/js-implementation/function-s-gi.md) auf, um eine vorhandene [!DNL AppMeasurement]-Instanz abzurufen.

## Hilfsprogramme {#section_0F47694DD0214645A24C94AB6A4142A0}

JavaScript [!DNL AppMeasurement] enthält die folgenden integrierten Hilfsprogramme:

* [Util.cookieRead](/help/implement/js-implementation/util-cookieread.md)
* [Util.cookieWrite](/help/implement/js-implementation/util-cookiewrite.md)
* [Util.getQueryParam](/help/implement/js-implementation/util-getqueryparam.md)

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

