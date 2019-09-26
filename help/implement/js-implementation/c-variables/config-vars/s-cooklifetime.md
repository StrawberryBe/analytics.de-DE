---
description: Mit dynamischen Variablen können Sie Werte von einer Variablen in eine andere kopieren, ohne die vollständigen Werte mehrfach in die Bildanforderung auf Ihrer Site eingeben zu müssen.
keywords: Analytics-Implementierung
seo-description: Mit dynamischen Variablen können Sie Werte von einer Variablen in eine andere kopieren, ohne die vollständigen Werte mehrfach in die Bildanforderung auf Ihrer Site eingeben zu müssen.
solution: null
title: Dynamische Variablen
translation-type: tm+mt
source-git-commit: 60dd1b300035e5149f53870239de85fb3174a77a

---


# s.cookieLifetime

Die Variable „“ wird sowohl von JavaScript als auch von Datenerfassungsservern verwendet, um die Lebensdauer eines Cookies zu bestimmen.

| Maximale Größe | Debug-Parameter | Ausgefüllte Berichte | Standardwert |
|---|---|---|---|
| Keine | cl | „Datenverkehr“ &gt; „Technologie“ &gt; „Cookies“ &gt; Alle Berichte, die mit Besuchern in Verbindung stehen | "" |

Wenn *`cookieLifetime`* festgelegt ist, überschreibt sie alle anderen Cookie-Ablauffristen sowohl für JavaScript als auch für Datenerfassungsserver (mit einer Ausnahme, die unten beschrieben wird). The *`cookieLifetime`* variable can have one of three values:

* [!DNL Analytics] Cookies
* Cookies
* JavaScript-Einstellungen und -Plug-ins

## Syntax und mögliche Werte

```js
s.cookieLifetime="value"
```

Die folgenden Werte sind möglich:

* ""
* „NONE“
* „SESSION“
* Eine Ganzzahl, die für die Anzahl der Sekunden bis zum Ablaufen steht

## Beispiele

```js
s.cookieLifetime="SESSION"
```

```js
s.cookieLifetime="86400" // one day in seconds
```

## Konfigurationseinstellungen

–

## Probleme, Fragen und Tipps

*`cookieLifetime`* betrifft die [!DNL Analytics] Verfolgung. If, for example, *`cookieLifetime`* is two days, then monthly, quarterly, and yearly unique visitor reports will be incorrect. Seien Sie daher vorsichtig, wenn Sie in *`cookieLifetime`*.
