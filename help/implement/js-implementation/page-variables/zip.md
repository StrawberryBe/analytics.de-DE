---
description: Seitenvariablen werden direkt in Berichten ausgefüllt, z. B. pageName, List Props, List Variables usw.
keywords: Analytics Implementation
subtopic: Variables
title: Seitenvariablen
topic: null
uuid: null
translation-type: tm+mt
source-git-commit: 99ee24efaa517e8da700c67818c111c4aa90dc02

---


# zip

Die Variablen „“ und „“ sind Konversionsvariablen.


<!-- 

zip.xml

 -->

Sie erfassen wie eVars Ereignisse, sind jedoch nicht persistent. Die Variablen *`zip`* und *`state`* sind mit eVars vergleichbar, die unverzüglich ablaufen.

| Maximale Größe | Debug-Parameter | Ausgefüllte Berichte | Standardwert |
|---|---|---|---|
| 50 Byte | zip | Konversion &gt; Besucherprofil &gt; PLZ/Postleitzahlen | "" |

Since the *`state`* and *`zip`* variables expire immediately, the only events associated with them are events fired on the same page that are populated. Wenn Sie beispielsweise die Variable *`zip`* verwenden, um Konversionsraten nach der Postleitzahl zu vergleichen, sollte die Variable *`zip`* auf jeder Seite des Checkout erscheinen. Adobe empfiehlt, als Quelle für die Postleitzahlen die Rechnungsadresse zu verwenden. Sie könnten stattdessen auch die Versandadresse verwenden (vorausgesetzt, für die Bestellung ist nur eine einzige Versandadresse vorhanden). Auf einer Medien-Website können *`zip`* und *`state`* zur Registrierung oder zum Anzeigen-Clickthrough-Tracking verwendet werden.

**Syntax und mögliche Werte** {#section_5EDCFCAC8FC241D1B4CC777996858CD7}

```js
s.zip="zip_code"
```

Die Variable *`zip`* legt keine Wert- oder Formatbeschränkungen fest. *`zip`* unterliegt keinen Beschränkungen, die über die Standardbeschränkungen von Variablen hinausgehen.

**Beispiele** {#section_F25C0D0CC3C04B81892A662CD605C593}

```js
s.zip="92806"
```

```js
s.zip="92806-4115"
```

**Konfigurationseinstellungen** {#section_7987084EECC34DD38B643B94F82385CA}

Keine

**Probleme, Fragen und Tipps** {#section_E86774D5CE8B40EFA36353CDEE3A84D0}

* Füllen Sie [!UICONTROL zip] auf jeder Seite mit Werten, auf der ein relevantes Ereignis ausgelöst wird (z. B. auf jeder Seite des Checkout-Prozess).
* Die Variablen *`zip`* und *`state`* verhalten sich wie eVars, die nach der Seitenansicht ablaufen.

