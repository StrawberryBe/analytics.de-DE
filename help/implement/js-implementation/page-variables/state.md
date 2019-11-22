---
description: Seitenvariablen werden direkt in Berichten ausgefüllt, z. B. pageName, List Props, List Variables usw.
keywords: Analytics Implementation
solution: Analytics
subtopic: Variables
title: Seitenvariablen
topic: null
uuid: null
translation-type: tm+mt
source-git-commit: 47291fb3d55ab3eb5ef181770bf2078c7ea55bc4

---


# state

Die Variablen „“ und „“ sind Konversionsvariablen.


<!-- 

state.xml

 -->

Sie erfassen wie eVars Ereignisse, sind jedoch nicht persistent. Die Variablen *`zip`* und *`state`* sind mit eVars vergleichbar, die unverzüglich ablaufen.

| Maximale Größe | Debug-Parameter | Ausgefüllte Berichte | Standardwert |
|---|---|---|---|
| 50 Byte | state | Konversion &gt; Besucherprofil &gt; Bundesstaat des Besuchers | "" |

Weil die Variablen *`state`* und *`zip`* sofort ablaufen, sind die einzigen Ereignisse, die ihnen zugeordnet sind, Ereignisse, die auf derselben Seite ausgelöst werden, auf der sie eingetragen sind. Wenn Sie beispielsweise die Variable *`state`* verwenden, um Konversionsraten nach dem Bundesstaat zu vergleichen, sollte die Variable *`state`* auf jeder Seite des Checkout erscheinen. Bei Konversions-Websites empfiehlt Adobe, die PLZ aus der Rechnungsadresse zu entnehmen. Sie können jedoch auch die Versandadresse verwenden (vorausgesetzt, zu der Bestellung ist nur eine Versandadresse vorhanden). Auf einer Medien-Website können *`zip`* und *`state`* zur Registrierung oder zum Anzeigen-Clickthrough-Tracking verwendet werden.

**Syntax und mögliche Werte** {#section_EDD1F5F9EDBC457898E61695F08C1744}

```js
s.state="state"
```

Bei der Variablen *`state`* sind keine besonderen Einschränkungen hinsichtlich Wert oder Format zu beachten. *`state`* unterliegt keinen Beschränkungen, die über die Standardbeschränkungen von Variablen hinausgehen.

**Beispiele** {#section_D181B163F79A41D199CA4C70765E583F}

```js
s.state="california" 
```

```js
s.state="prince edward island"
```

**Konfigurationseinstellungen** {#section_DB0D6DC3F4764AC59C11B10D27D2806C}

Keine

**Probleme, Fragen und Tipps** {#section_02F1620D0BB14AA6A838966FDB9A234F}

* Füllen Sie *`state`* auf jeder Seite auf, auf der ein relevantes Ereignis ausgelöst wird (z. B. auf jeder Seite des Checkout-Prozesses).
* Die Variablen *`zip`* und *`state`* verhalten sich wie eVars, die nach der Seitenansicht ablaufen.
