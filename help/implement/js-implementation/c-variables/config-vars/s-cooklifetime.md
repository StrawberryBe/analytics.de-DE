---
description: Mit dynamischen Variablen können Sie Werte von einer Variablen in eine andere kopieren, ohne die vollständigen Werte mehrfach in die Bildanforderung auf Ihrer Site eingeben zu müssen.
keywords: Analytics Implementation
solution: null
title: Dynamische Variablen
translation-type: ht
source-git-commit: 16ba0b12e0f70112f4c10804d0a13c278388ecc2

---


# s.cookieLifetime

Die Variable „“ wird sowohl von JavaScript als auch von Datenerfassungsservern verwendet, um die Lebensdauer eines Cookies zu bestimmen.

| Maximale Größe | Debug-Parameter | Ausgefüllte Berichte | Standardwert |
|---|---|---|---|
| nicht angegeben | cl | „Datenverkehr“ &gt; „Technologie“ &gt; „Cookies“ &gt; Alle Berichte, die mit Besuchern in Verbindung stehen | "" |

Wenn *`cookieLifetime`* festgelegt ist, überschreibt sie alle anderen Cookie-Ablauffristen sowohl für JavaScript als auch für Datenerfassungsserver (mit einer Ausnahme, die unten beschrieben ist). Die Variable *`cookieLifetime`* kann einen von drei Werten haben:

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

Keine

## Probleme, Fragen und Tipps

*`cookieLifetime`* betrifft [!DNL Analytics]-Tracking. Wenn zum Beispiel *`cookieLifetime`* eine Zeitdauer von zwei Tagen vorgibt, sind monatliche, vierteljährliche und jährliche Unique Visitor-Berichte fehlerhaft. Seien Sie daher vorsichtig, wenn Sie in *`cookieLifetime`*.
